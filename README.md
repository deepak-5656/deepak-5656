<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Deepak R — Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Mono:ital,wght@0,300;0,400;0,500;1,300&display=swap" rel="stylesheet"/>
<style>
:root {
  --bg: #04050a;
  --surface: #0b0d14;
  --card: #0f1118;
  --border: rgba(255,255,255,0.06);
  --border-glow: rgba(99,179,237,0.25);
  --text: #eef2ff;
  --muted: #6b7a99;
  --accent: #63b3ed;
  --accent2: #76e3c4;
  --accent3: #f6ad55;
  --accent-ml: #a78bfa;
  --accent-be: #34d399;
  --accent-fe: #fbbf24;
  --accent-tool: #f87171;
}

*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

html { scroll-behavior: smooth; }

body {
  background: var(--bg);
  color: var(--text);
  font-family: 'DM Mono', monospace;
  min-height: 100vh;
  overflow-x: hidden;
}

/* ─── CANVAS BG ─── */
#bg-canvas {
  position: fixed;
  inset: 0;
  z-index: 0;
  pointer-events: none;
  opacity: 0.35;
}

.wrapper {
  position: relative;
  z-index: 1;
  max-width: 900px;
  margin: 0 auto;
  padding: 0 24px 80px;
}

/* ─── HERO ─── */
.hero {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 60px 0 40px;
}

.hero-tag {
  font-size: 11px;
  letter-spacing: 3px;
  color: var(--accent);
  text-transform: uppercase;
  margin-bottom: 20px;
  opacity: 0;
  animation: fadeUp 0.7s 0.2s forwards;
}

.hero-name {
  font-family: 'Syne', sans-serif;
  font-size: clamp(52px, 10vw, 96px);
  font-weight: 800;
  line-height: 0.95;
  letter-spacing: -3px;
  color: var(--text);
  margin-bottom: 6px;
  opacity: 0;
  animation: fadeUp 0.7s 0.35s forwards;
}

.hero-name span {
  display: block;
  background: linear-gradient(135deg, var(--accent) 0%, var(--accent2) 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.hero-role {
  font-family: 'Syne', sans-serif;
  font-size: clamp(18px, 3vw, 26px);
  font-weight: 600;
  color: var(--muted);
  margin-bottom: 28px;
  opacity: 0;
  animation: fadeUp 0.7s 0.5s forwards;
}

.hero-desc {
  font-size: 14px;
  line-height: 1.9;
  color: #8892a4;
  max-width: 520px;
  margin-bottom: 40px;
  opacity: 0;
  animation: fadeUp 0.7s 0.65s forwards;
}

.hero-cta {
  display: flex;
  gap: 14px;
  flex-wrap: wrap;
  opacity: 0;
  animation: fadeUp 0.7s 0.8s forwards;
}

.btn {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 12px 24px;
  border-radius: 8px;
  font-family: 'Syne', sans-serif;
  font-size: 13px;
  font-weight: 600;
  text-decoration: none;
  transition: all 0.2s;
  cursor: pointer;
  border: none;
}

.btn-primary {
  background: var(--accent);
  color: #020408;
}
.btn-primary:hover { transform: translateY(-2px); box-shadow: 0 8px 30px rgba(99,179,237,0.35); }

.btn-outline {
  background: transparent;
  color: var(--text);
  border: 1px solid var(--border-glow);
}
.btn-outline:hover { background: rgba(99,179,237,0.07); transform: translateY(-2px); }

.hero-stats {
  display: flex;
  gap: 40px;
  margin-top: 56px;
  padding-top: 40px;
  border-top: 1px solid var(--border);
  opacity: 0;
  animation: fadeUp 0.7s 1s forwards;
}

.stat-item { text-align: left; }
.stat-num {
  font-family: 'Syne', sans-serif;
  font-size: 32px;
  font-weight: 800;
  color: var(--accent);
  line-height: 1;
}
.stat-lbl { font-size: 11px; color: var(--muted); margin-top: 4px; letter-spacing: 1px; }

/* ─── SECTIONS ─── */
.section { padding: 80px 0; }

.section-label {
  font-size: 10px;
  letter-spacing: 4px;
  color: var(--accent2);
  text-transform: uppercase;
  margin-bottom: 12px;
  display: flex;
  align-items: center;
  gap: 10px;
}
.section-label::after {
  content: '';
  flex: 1;
  height: 1px;
  background: var(--border);
}

.section-title {
  font-family: 'Syne', sans-serif;
  font-size: clamp(28px, 5vw, 42px);
  font-weight: 800;
  letter-spacing: -1px;
  margin-bottom: 48px;
  line-height: 1.1;
}

/* ─── ABOUT ─── */
.about-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 24px;
}

.code-card {
  background: var(--card);
  border: 1px solid var(--border);
  border-radius: 16px;
  overflow: hidden;
}

.code-bar {
  display: flex;
  align-items: center;
  gap: 8px;
  padding: 12px 16px;
  background: #080a10;
  border-bottom: 1px solid var(--border);
}

.dot { width: 10px; height: 10px; border-radius: 50%; }
.dot-r { background: #ff5f56; }
.dot-y { background: #ffbd2e; }
.dot-g { background: #27c93f; }

.code-filename { font-size: 11px; color: var(--muted); margin-left: 8px; }

.code-body {
  padding: 20px;
  font-size: 12px;
  line-height: 2;
  font-family: 'DM Mono', monospace;
}

.c-kw { color: #c792ea; }
.c-fn { color: #82aaff; }
.c-str { color: #c3e88d; }
.c-val { color: #f78c6c; }
.c-cm { color: #546e7a; font-style: italic; }
.c-num { color: var(--accent3); }

.info-card {
  background: var(--card);
  border: 1px solid var(--border);
  border-radius: 16px;
  padding: 28px;
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.info-row {
  display: flex;
  flex-direction: column;
  gap: 4px;
  padding-bottom: 16px;
  border-bottom: 1px solid var(--border);
}
.info-row:last-child { border-bottom: none; padding-bottom: 0; }
.info-key { font-size: 10px; letter-spacing: 2px; color: var(--muted); text-transform: uppercase; }
.info-val { font-size: 13px; color: var(--text); }
.info-val.accent { color: var(--accent); }

/* ─── SKILLS — 3D HOVER ─── */
.skills-categories { display: flex; flex-direction: column; gap: 44px; }

.skill-category-title {
  font-size: 11px;
  letter-spacing: 3px;
  color: var(--muted);
  text-transform: uppercase;
  margin-bottom: 16px;
  display: flex;
  align-items: center;
  gap: 10px;
}
.skill-category-title .dot-cat {
  width: 6px; height: 6px; border-radius: 50%;
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(90px, 1fr));
  gap: 14px;
}

.skill-card {
  perspective: 600px;
  cursor: default;
}

.skill-card-inner {
  background: var(--card);
  border: 1px solid var(--border);
  border-radius: 14px;
  padding: 18px 10px 14px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
  transition: transform 0.15s ease, box-shadow 0.15s ease, border-color 0.15s ease;
  transform-style: preserve-3d;
  will-change: transform;
  position: relative;
  overflow: hidden;
}

.skill-card-inner::before {
  content: '';
  position: absolute;
  inset: 0;
  border-radius: 14px;
  opacity: 0;
  transition: opacity 0.2s;
  pointer-events: none;
}

.skill-card:hover .skill-card-inner {
  box-shadow: 0 20px 50px rgba(0,0,0,0.5), 0 0 0 1px var(--glow-color, rgba(99,179,237,0.3));
  border-color: var(--glow-color, rgba(99,179,237,0.4));
}
.skill-card:hover .skill-card-inner::before { opacity: 1; }

.skill-logo {
  width: 40px;
  height: 40px;
  object-fit: contain;
  filter: drop-shadow(0 2px 6px rgba(0,0,0,0.4));
  transition: transform 0.15s ease, filter 0.15s ease;
  transform-style: preserve-3d;
}

.skill-card:hover .skill-logo {
  filter: drop-shadow(0 6px 16px var(--glow-color, rgba(99,179,237,0.5)));
  transform: translateZ(20px) scale(1.15);
}

.skill-name {
  font-size: 10px;
  color: var(--muted);
  text-align: center;
  letter-spacing: 0.5px;
  transition: color 0.15s;
  line-height: 1.3;
}
.skill-card:hover .skill-name { color: var(--text); }

/* ─── PROJECTS ─── */
.projects-grid { display: flex; flex-direction: column; gap: 20px; }

.project-card {
  background: var(--card);
  border: 1px solid var(--border);
  border-radius: 16px;
  padding: 28px 32px;
  display: grid;
  grid-template-columns: 1fr auto;
  gap: 16px;
  align-items: start;
  transition: border-color 0.2s, transform 0.2s, box-shadow 0.2s;
  cursor: pointer;
  text-decoration: none;
  color: inherit;
}

.project-card:hover {
  border-color: rgba(99,179,237,0.3);
  transform: translateY(-3px);
  box-shadow: 0 16px 50px rgba(0,0,0,0.4);
}

.project-num {
  font-family: 'Syne', sans-serif;
  font-size: 11px;
  color: var(--accent);
  letter-spacing: 2px;
  margin-bottom: 10px;
}

.project-name {
  font-family: 'Syne', sans-serif;
  font-size: 20px;
  font-weight: 700;
  margin-bottom: 8px;
}

.project-desc {
  font-size: 13px;
  color: var(--muted);
  line-height: 1.8;
  margin-bottom: 16px;
}

.project-tags { display: flex; gap: 8px; flex-wrap: wrap; }

.tag {
  font-size: 10px;
  padding: 4px 10px;
  border-radius: 20px;
  letter-spacing: 0.5px;
}

.tag-js { background: rgba(251,191,36,0.1); color: #fbbf24; border: 1px solid rgba(251,191,36,0.2); }
.tag-ts { background: rgba(96,165,250,0.1); color: #60a5fa; border: 1px solid rgba(96,165,250,0.2); }
.tag-ai { background: rgba(167,139,250,0.1); color: #a78bfa; border: 1px solid rgba(167,139,250,0.2); }
.tag-ml { background: rgba(52,211,153,0.1); color: #34d399; border: 1px solid rgba(52,211,153,0.2); }

.project-arrow {
  font-size: 22px;
  color: var(--muted);
  transition: transform 0.2s, color 0.2s;
  margin-top: 4px;
}
.project-card:hover .project-arrow { transform: translate(4px,-4px); color: var(--accent); }

/* ─── CURRENTLY ─── */
.current-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 14px;
}

.current-item {
  background: var(--card);
  border: 1px solid var(--border);
  border-radius: 12px;
  padding: 20px;
  display: flex;
  gap: 14px;
  align-items: flex-start;
  transition: border-color 0.2s;
}
.current-item:hover { border-color: var(--border-glow); }

.current-icon {
  font-size: 20px;
  flex-shrink: 0;
  width: 36px;
  height: 36px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: rgba(255,255,255,0.04);
  border-radius: 8px;
}

.current-text { font-size: 12px; color: #8892a4; line-height: 1.7; }

/* ─── CONTACT ─── */
.contact-box {
  background: var(--card);
  border: 1px solid var(--border);
  border-radius: 20px;
  padding: 48px;
  text-align: center;
  position: relative;
  overflow: hidden;
}

.contact-box::before {
  content: '';
  position: absolute;
  top: -80px; left: 50%; transform: translateX(-50%);
  width: 300px; height: 300px;
  background: radial-gradient(circle, rgba(99,179,237,0.08) 0%, transparent 70%);
  pointer-events: none;
}

.contact-title {
  font-family: 'Syne', sans-serif;
  font-size: 36px;
  font-weight: 800;
  margin-bottom: 12px;
}

.contact-sub { font-size: 13px; color: var(--muted); margin-bottom: 32px; line-height: 1.8; }

/* ─── FOOTER ─── */
footer {
  padding: 40px 0 20px;
  text-align: center;
  border-top: 1px solid var(--border);
  margin-top: 40px;
}
footer p { font-size: 12px; color: var(--muted); }

/* ─── ANIMATIONS ─── */
@keyframes fadeUp {
  from { opacity: 0; transform: translateY(20px); }
  to   { opacity: 1; transform: translateY(0); }
}

.reveal {
  opacity: 0;
  transform: translateY(24px);
  transition: opacity 0.6s ease, transform 0.6s ease;
}
.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}

/* ─── SCROLLBAR ─── */
::-webkit-scrollbar { width: 4px; }
::-webkit-scrollbar-track { background: var(--bg); }
::-webkit-scrollbar-thumb { background: #1e2235; border-radius: 4px; }

@media (max-width: 640px) {
  .about-grid, .current-grid { grid-template-columns: 1fr; }
  .hero-stats { gap: 24px; }
  .contact-box { padding: 32px 20px; }
}
</style>
</head>
<body>

<canvas id="bg-canvas"></canvas>

<div class="wrapper">

  <!-- ─── HERO ─── -->
  <section class="hero">
    <p class="hero-tag">// hello world — welcome to my space</p>
    <h1 class="hero-name">
      Deepak R
      <span>builds things.</span>
    </h1>
    <p class="hero-role">ML Engineer · Backend Developer · Web Craftsman</p>
    <p class="hero-desc">
      Crafting impactful web projects and experimenting with AI-powered features for smarter, more human digital experiences. I live at the intersection of machine intelligence and elegant backend systems.
    </p>
    <div class="hero-cta">
      <a href="https://github.com/deepak-5656" class="btn btn-primary">
        <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0 0 24 12c0-6.63-5.37-12-12-12z"/></svg>
        GitHub Profile
      </a>
      <a href="#projects" class="btn btn-outline">View Projects →</a>
    </div>
    <div class="hero-stats">
      <div class="stat-item">
        <div class="stat-num">18</div>
        <div class="stat-lbl">Repositories</div>
      </div>
      <div class="stat-item">
        <div class="stat-num">6+</div>
        <div class="stat-lbl">Stars Earned</div>
      </div>
      <div class="stat-item">
        <div class="stat-num">3+</div>
        <div class="stat-lbl">Domains</div>
      </div>
      <div class="stat-item">
        <div class="stat-num">∞</div>
        <div class="stat-lbl">Curiosity</div>
      </div>
    </div>
  </section>

  <!-- ─── ABOUT ─── -->
  <section class="section reveal" id="about">
    <p class="section-label">01 — About</p>
    <h2 class="section-title">A little about me.</h2>
    <div class="about-grid">
      <div class="code-card">
        <div class="code-bar">
          <span class="dot dot-r"></span>
          <span class="dot dot-y"></span>
          <span class="dot dot-g"></span>
          <span class="code-filename">deepak.py</span>
        </div>
        <div class="code-body">
          <span class="c-kw">class</span> <span class="c-fn">Deepak</span>:<br>
          &nbsp;&nbsp;<span class="c-cm"># who I am</span><br>
          &nbsp;&nbsp;<span class="c-val">name</span> = <span class="c-str">"Deepak R"</span><br>
          &nbsp;&nbsp;<span class="c-val">from</span> = <span class="c-str">"India 🇮🇳"</span><br><br>
          &nbsp;&nbsp;<span class="c-cm"># what I do</span><br>
          &nbsp;&nbsp;<span class="c-val">roles</span> = [<br>
          &nbsp;&nbsp;&nbsp;&nbsp;<span class="c-str">"ML Engineer"</span>,<br>
          &nbsp;&nbsp;&nbsp;&nbsp;<span class="c-str">"Backend Developer"</span>,<br>
          &nbsp;&nbsp;&nbsp;&nbsp;<span class="c-str">"Web Craftsman"</span><br>
          &nbsp;&nbsp;]<br><br>
          &nbsp;&nbsp;<span class="c-kw">def</span> <span class="c-fn">passion</span>(<span class="c-val">self</span>):<br>
          &nbsp;&nbsp;&nbsp;&nbsp;<span class="c-kw">return</span> <span class="c-str">"AI × Web 🚀"</span>
        </div>
      </div>
      <div class="info-card">
        <div class="info-row">
          <span class="info-key">Status</span>
          <span class="info-val accent">● Open to collaborations</span>
        </div>
        <div class="info-row">
          <span class="info-key">Focus</span>
          <span class="info-val">ML · Backend · Full-Stack</span>
        </div>
        <div class="info-row">
          <span class="info-key">Achievements</span>
          <span class="info-val">🦈 Pull Shark · 🎯 YOLO</span>
        </div>
        <div class="info-row">
          <span class="info-key">Currently learning</span>
          <span class="info-val">LLMs · MLOps · System Design</span>
        </div>
        <div class="info-row">
          <span class="info-key">Fun fact</span>
          <span class="info-val">I debug code and ideas equally well ☕</span>
        </div>
      </div>
    </div>
  </section>

  <!-- ─── SKILLS ─── -->
  <section class="section reveal" id="skills">
    <p class="section-label">02 — Skills</p>
    <h2 class="section-title">My tech universe.</h2>

    <div class="skills-categories">

      <!-- ML & AI -->
      <div>
        <p class="skill-category-title">
          <span class="dot-cat" style="background:var(--accent-ml)"></span>
          Machine Learning &amp; AI
        </p>
        <div class="skills-grid">
          <div class="skill-card" style="--glow-color:rgba(167,139,250,0.4)">
            <div class="skill-card-inner" style="--before-bg:rgba(167,139,250,0.04)">
              <img class="skill-logo" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" alt="Python"/>
              <span class="skill-name">Python</span>
            </div>
          </div>
          <div class="skill-card" style="--glow-color:rgba(255,111,0,0.4)">
            <div class="skill-card-inner">
              <img class="skill-logo" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tensorflow/tensorflow-original.svg" alt="TensorFlow"/>
              <span class="skill-name">TensorFlow</span>
            </div>
          </div>
          <div class="skill-card" style="--glow-color:rgba(242,141,0,0.4)">
            <div class="skill-card-inner">
              <img class="skill-logo" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pandas/pandas-original.svg" alt="Pandas"/>
              <span class="skill-name">Pandas</span>
            </div>
          </div>
          <div class="skill-card" style="--glow-color:rgba(77,166,255,0.4)">
            <div class="skill-card-inner">
              <img class="skill-logo" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/numpy/numpy-original.svg" alt="NumPy"/>
              <span class="skill-name">NumPy</span>
            </div>
          </div>
          <div class="skill-card" style="--glow-color:rgba(255,140,60,0.4)">
            <div class="skill-card-inner">
              <img class="skill-logo" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jupyter/jupyter-original.svg" alt="Jupyter"/>
              <span class="skill-name">Jupyter</span>
            </div>
          </div>
          <div class="skill-card" style="--glow-color:rgba(167,139,250,0.4)">
            <div class="skill-card-inner">
              <img class="skill-logo" src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" alt="scikit-learn"/>
              <span class="skill-name">scikit-learn</span>
            </div>
          </div>
        </div>
      </div>

      <!-- Backend -->
      <div>
        <p class="skill-category-title">
          <span class="dot-cat" style="background:var(--accent-be)"></span>
          Backend Development
        </p>
        <div class="skills-grid">
          <div class="skill-card" style="--glow-color:rgba(52,211,153,0.4)">
            <div class="skill-card-inner">
              <img class="skill-logo" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg" alt="Node.js"/>
              <span class="skill-name">Node.js</span>
            </div>
          </div>
          <div class="skill-card" style="--glow-color:rgba(255,255,255,0.15)">
            <div class="skill-card-inner">
              <img class="skill-logo" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/express/express-original.svg" alt="Express" style="filter:invert(1) drop-shadow(0 2px 6px rgba(0,0,0,0.4))"/>
              <span class="skill-name">Express</span>
            </div>
          </div>
          <div class="skill-card" style="--glow-color:rgba(71,162,72,0.4)">
            <div class="skill-card-inner">
              <img class="skill-logo" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg" alt="MongoDB"/>
              <span class="skill-name">MongoDB</span>
            </div>
          </div>
          <div class="skill-card" style="--glow-color:rgba(0,116,186,0.4)">
            <div class="skill-card-inner">
              <img class="skill-logo" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" alt="MySQL"/>
              <span class="skill-name">MySQL</span>
            </div>
          </div>
          <div class="skill-card" style="--glow-color:rgba(99,179,237,0.4)">
            <div class="skill-card-inner">
              <img class="skill-logo" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg" alt="PostgreSQL"/>
              <span class="skill-name">PostgreSQL</span>
            </div>
          </div>
        </div>
      </div>

      <!-- Frontend -->
      <div>
        <p class="skill-category-title">
          <span class="dot-cat" style="background:var(--accent-fe)"></span>
          Frontend &amp; Web
        </p>
        <div class="skills-grid">
          <div class="skill-card" style="--glow-color:rgba(247,223,30,0.4)">
            <div class="skill-card-inner">
              <img class="skill-logo" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" alt="JavaScript"/>
              <span class="skill-name">JavaScript</span>
            </div>
          </div>
          <div class="skill-card" style="--glow-color:rgba(49,120,198,0.4)">
            <div class="skill-card-inner">
              <img class="skill-logo" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" alt="TypeScript"/>
              <span class="skill-name">TypeScript</span>
            </div>
          </div>
          <div class="skill-card" style="--glow-color:rgba(97,218,251,0.4)">
            <div class="skill-card-inner">
              <img class="skill-logo" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" alt="React"/>
              <span class="skill-name">React</span>
            </div>
          </div>
          <div class="skill-card" style="--glow-color:rgba(227,76,38,0.4)">
            <div class="skill-card-inner">
              <img class="skill-logo" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" alt="HTML5"/>
              <span class="skill-name">HTML5</span>
            </div>
          </div>
          <div class="skill-card" style="--glow-color:rgba(21,114,182,0.4)">
            <div class="skill-card-inner">
              <img class="skill-logo" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" alt="CSS3"/>
              <span class="skill-name">CSS3</span>
            </div>
          </div>
        </div>
      </div>

      <!-- Tools -->
      <div>
        <p class="skill-category-title">
          <span class="dot-cat" style="background:var(--accent-tool)"></span>
          Tools &amp; Platforms
        </p>
        <div class="skills-grid">
          <div class="skill-card" style="--glow-color:rgba(240,80,50,0.4)">
            <div class="skill-card-inner">
              <img class="skill-logo" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" alt="Git"/>
              <span class="skill-name">Git</span>
            </div>
          </div>
          <div class="skill-card" style="--glow-color:rgba(255,255,255,0.2)">
            <div class="skill-card-inner">
              <img class="skill-logo" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" alt="GitHub" style="filter:invert(1) drop-shadow(0 2px 6px rgba(0,0,0,0.4))"/>
              <span class="skill-name">GitHub</span>
            </div>
          </div>
          <div class="skill-card" style="--glow-color:rgba(0,122,204,0.4)">
            <div class="skill-card-inner">
              <img class="skill-logo" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" alt="VS Code"/>
              <span class="skill-name">VS Code</span>
            </div>
          </div>
          <div class="skill-card" style="--glow-color:rgba(255,108,55,0.4)">
            <div class="skill-card-inner">
              <img class="skill-logo" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postman/postman-original.svg" alt="Postman"/>
              <span class="skill-name">Postman</span>
            </div>
          </div>
          <div class="skill-card" style="--glow-color:rgba(13,183,96,0.4)">
            <div class="skill-card-inner">
              <img class="skill-logo" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" alt="Docker"/>
              <span class="skill-name">Docker</span>
            </div>
          </div>
        </div>
      </div>

    </div>
  </section>

  <!-- ─── PROJECTS ─── -->
  <section class="section reveal" id="projects">
    <p class="section-label">03 — Projects</p>
    <h2 class="section-title">Things I've built.</h2>
    <div class="projects-grid">
      <a href="https://github.com/deepak-5656/wanderease" class="project-card" target="_blank">
        <div>
          <p class="project-num">01 / Featured</p>
          <h3 class="project-name">WanderEase 🗺️</h3>
          <p class="project-desc">
            An AI-powered travel experience platform that helps users plan and discover journeys. Built with smart recommendations and an intuitive, seamless web interface.
          </p>
          <div class="project-tags">
            <span class="tag tag-js">JavaScript</span>
            <span class="tag tag-ai">Web APIs</span>
            <span class="tag tag-ai">AI Features</span>
          </div>
        </div>
        <div class="project-arrow">↗</div>
      </a>

      <a href="https://github.com/deepak-5656/Ecommercechatbot" class="project-card" target="_blank">
        <div>
          <p class="project-num">02 / Featured</p>
          <h3 class="project-name">E-commerce Chatbot 🤖</h3>
          <p class="project-desc">
            An intelligent shopping assistant powered by NLP, designed to enhance user experience in e-commerce platforms with conversational AI and smart product discovery.
          </p>
          <div class="project-tags">
            <span class="tag tag-ts">TypeScript</span>
            <span class="tag tag-ml">NLP</span>
            <span class="tag tag-ai">AI / ML</span>
          </div>
        </div>
        <div class="project-arrow">↗</div>
      </a>
    </div>
  </section>

  <!-- ─── CURRENTLY ─── -->
  <section class="section reveal">
    <p class="section-label">04 — Now</p>
    <h2 class="section-title">What I'm working on.</h2>
    <div class="current-grid">
      <div class="current-item">
        <div class="current-icon">🧠</div>
        <p class="current-text">Deepening expertise in <strong style="color:var(--text)">Deep Learning</strong> architectures and Large Language Models</p>
      </div>
      <div class="current-item">
        <div class="current-icon">⚙️</div>
        <p class="current-text">Building <strong style="color:var(--text)">scalable backend systems</strong> with clean REST APIs and microservice patterns</p>
      </div>
      <div class="current-item">
        <div class="current-icon">🚀</div>
        <p class="current-text">Exploring <strong style="color:var(--text)">MLOps</strong> — model deployment, monitoring, and production pipelines</p>
      </div>
      <div class="current-item">
        <div class="current-icon">🤝</div>
        <p class="current-text">Open to <strong style="color:var(--text)">collaborations</strong> on impactful ML and full-stack web projects</p>
      </div>
    </div>
  </section>

  <!-- ─── CONTACT ─── -->
  <section class="section reveal">
    <div class="contact-box">
      <h2 class="contact-title">Let's build together.</h2>
      <p class="contact-sub">
        Whether it's a wild ML experiment, a backend challenge,<br/>
        or a full-stack product — I'm always up for a good project.
      </p>
      <div style="display:flex;gap:14px;justify-content:center;flex-wrap:wrap;">
        <a href="https://github.com/deepak-5656" class="btn btn-primary" target="_blank">
          <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0 0 24 12c0-6.63-5.37-12-12-12z"/></svg>
          Visit GitHub
        </a>
        <a href="mailto:deepak@example.com" class="btn btn-outline">Send a Message ✉️</a>
      </div>
    </div>
  </section>

  <footer>
    <p>Designed & built by <strong>Deepak R</strong> · 2024 · Made with ☕ &amp; Python</p>
  </footer>

</div>

<script>
/* ── Particle Canvas BG ── */
const canvas = document.getElementById('bg-canvas');
const ctx = canvas.getContext('2d');
let W, H, particles = [];

function resize() {
  W = canvas.width = window.innerWidth;
  H = canvas.height = window.innerHeight;
}
resize();
window.addEventListener('resize', resize);

class Particle {
  constructor() { this.reset(); }
  reset() {
    this.x = Math.random() * W;
    this.y = Math.random() * H;
    this.r = Math.random() * 1.2 + 0.3;
    this.vx = (Math.random() - 0.5) * 0.3;
    this.vy = (Math.random() - 0.5) * 0.3;
    this.alpha = Math.random() * 0.5 + 0.1;
  }
  update() {
    this.x += this.vx; this.y += this.vy;
    if (this.x < 0 || this.x > W || this.y < 0 || this.y > H) this.reset();
  }
  draw() {
    ctx.beginPath();
    ctx.arc(this.x, this.y, this.r, 0, Math.PI * 2);
    ctx.fillStyle = `rgba(99,179,237,${this.alpha})`;
    ctx.fill();
  }
}

for (let i = 0; i < 120; i++) particles.push(new Particle());

function drawLines() {
  for (let i = 0; i < particles.length; i++) {
    for (let j = i + 1; j < particles.length; j++) {
      const dx = particles[i].x - particles[j].x;
      const dy = particles[i].y - particles[j].y;
      const d = Math.sqrt(dx*dx + dy*dy);
      if (d < 100) {
        ctx.beginPath();
        ctx.moveTo(particles[i].x, particles[i].y);
        ctx.lineTo(particles[j].x, particles[j].y);
        ctx.strokeStyle = `rgba(99,179,237,${0.06 * (1 - d/100)})`;
        ctx.lineWidth = 0.5;
        ctx.stroke();
      }
    }
  }
}

function animate() {
  ctx.clearRect(0, 0, W, H);
  particles.forEach(p => { p.update(); p.draw(); });
  drawLines();
  requestAnimationFrame(animate);
}
animate();

/* ── 3D Tilt on Skill Cards ── */
document.querySelectorAll('.skill-card').forEach(card => {
  const inner = card.querySelector('.skill-card-inner');
  card.addEventListener('mousemove', e => {
    const rect = card.getBoundingClientRect();
    const cx = rect.left + rect.width / 2;
    const cy = rect.top + rect.height / 2;
    const dx = e.clientX - cx;
    const dy = e.clientY - cy;
    const rotX = -(dy / (rect.height / 2)) * 18;
    const rotY =  (dx / (rect.width  / 2)) * 18;
    inner.style.transform = `perspective(600px) rotateX(${rotX}deg) rotateY(${rotY}deg) scale(1.06)`;
  });
  card.addEventListener('mouseleave', () => {
    inner.style.transform = 'perspective(600px) rotateX(0) rotateY(0) scale(1)';
  });
});

/* ── Scroll Reveal ── */
const observer = new IntersectionObserver(entries => {
  entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
}, { threshold: 0.1 });
document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
</script>
</body>
</html>
