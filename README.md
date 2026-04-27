<div align="center">

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 320" width="900" height="320">
  <defs>
    <!-- Backgrounds -->
    <linearGradient id="bg" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#020408"/>
      <stop offset="50%" stop-color="#060a14"/>
      <stop offset="100%" stop-color="#030610"/>
    </linearGradient>

    <!-- Name gradient -->
    <linearGradient id="nameG" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#38bdf8"/>
      <stop offset="40%" stop-color="#818cf8"/>
      <stop offset="100%" stop-color="#34d399"/>
    </linearGradient>

    <!-- Glow filters -->
    <filter id="gNameBig" x="-20%" y="-40%" width="140%" height="200%">
      <feGaussianBlur stdDeviation="10" result="b1"/>
      <feGaussianBlur stdDeviation="4"  result="b2"/>
      <feMerge><feMergeNode in="b1"/><feMergeNode in="b2"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <filter id="gSoft" x="-30%" y="-30%" width="160%" height="160%">
      <feGaussianBlur stdDeviation="5" result="b"/>
      <feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <filter id="gTiny" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="2.5"/>
    </filter>
    <filter id="gMed" x="-40%" y="-40%" width="180%" height="180%">
      <feGaussianBlur stdDeviation="7" result="b"/>
      <feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>

    <!-- Sphere gradients -->
    <radialGradient id="sBlue" cx="32%" cy="28%" r="65%" fx="32%" fy="28%">
      <stop offset="0%"   stop-color="#93c5fd"/>
      <stop offset="35%"  stop-color="#3b82f6"/>
      <stop offset="75%"  stop-color="#1d4ed8"/>
      <stop offset="100%" stop-color="#060e2a"/>
    </radialGradient>
    <radialGradient id="sPurple" cx="32%" cy="28%" r="65%" fx="32%" fy="28%">
      <stop offset="0%"   stop-color="#c4b5fd"/>
      <stop offset="35%"  stop-color="#8b5cf6"/>
      <stop offset="75%"  stop-color="#6d28d9"/>
      <stop offset="100%" stop-color="#130720"/>
    </radialGradient>
    <radialGradient id="sTeal" cx="32%" cy="28%" r="65%" fx="32%" fy="28%">
      <stop offset="0%"   stop-color="#6ee7b7"/>
      <stop offset="35%"  stop-color="#10b981"/>
      <stop offset="75%"  stop-color="#065f46"/>
      <stop offset="100%" stop-color="#020f0a"/>
    </radialGradient>
    <radialGradient id="sPink" cx="32%" cy="28%" r="65%" fx="32%" fy="28%">
      <stop offset="0%"   stop-color="#fbcfe8"/>
      <stop offset="35%"  stop-color="#ec4899"/>
      <stop offset="75%"  stop-color="#9d174d"/>
      <stop offset="100%" stop-color="#1a0210"/>
    </radialGradient>

    <!-- Cube face gradients -->
    <linearGradient id="cTop" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#1e3a5f"/>
      <stop offset="100%" stop-color="#0c1f35"/>
    </linearGradient>
    <linearGradient id="cLeft" x1="100%" y1="0%" x2="0%" y2="0%">
      <stop offset="0%" stop-color="#0d1f38"/>
      <stop offset="100%" stop-color="#060e1c"/>
    </linearGradient>
    <linearGradient id="cRight" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#142d50"/>
      <stop offset="100%" stop-color="#0a1a30"/>
    </linearGradient>
    <linearGradient id="cTopP" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#2e1b5e"/>
      <stop offset="100%" stop-color="#160c30"/>
    </linearGradient>
    <linearGradient id="cLeftP" x1="100%" y1="0%" x2="0%" y2="0%">
      <stop offset="0%" stop-color="#1a0d3a"/>
      <stop offset="100%" stop-color="#0a0620"/>
    </linearGradient>
    <linearGradient id="cRightP" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#241444"/>
      <stop offset="100%" stop-color="#100828"/>
    </linearGradient>

    <!-- Horizontal line glow -->
    <linearGradient id="hLine" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#38bdf8" stop-opacity="0"/>
      <stop offset="30%"  stop-color="#38bdf8" stop-opacity="0.8"/>
      <stop offset="50%"  stop-color="#818cf8" stop-opacity="1"/>
      <stop offset="70%"  stop-color="#34d399" stop-opacity="0.8"/>
      <stop offset="100%" stop-color="#34d399" stop-opacity="0"/>
    </linearGradient>

    <!-- Ambient halo behind name -->
    <radialGradient id="halo" cx="50%" cy="50%" r="50%">
      <stop offset="0%"   stop-color="#818cf8" stop-opacity="0.12"/>
      <stop offset="100%" stop-color="#818cf8" stop-opacity="0"/>
    </radialGradient>
  </defs>

  <!-- ── BACKGROUND ── -->
  <rect width="900" height="320" fill="url(#bg)" rx="18"/>

  <!-- Subtle dot grid -->
  <g fill="#38bdf8" opacity="0.07">
    <circle cx="60"  cy="40"  r="1.2"/> <circle cx="150" cy="40"  r="1.2"/> <circle cx="240" cy="40"  r="1.2"/>
    <circle cx="60"  cy="100" r="1.2"/> <circle cx="150" cy="100" r="1.2"/> <circle cx="240" cy="100" r="1.2"/>
    <circle cx="60"  cy="160" r="1.2"/> <circle cx="150" cy="160" r="1.2"/> <circle cx="240" cy="160" r="1.2"/>
    <circle cx="60"  cy="220" r="1.2"/> <circle cx="150" cy="220" r="1.2"/> <circle cx="240" cy="220" r="1.2"/>
    <circle cx="60"  cy="280" r="1.2"/> <circle cx="150" cy="280" r="1.2"/> <circle cx="240" cy="280" r="1.2"/>
    <circle cx="660" cy="40"  r="1.2"/> <circle cx="750" cy="40"  r="1.2"/> <circle cx="840" cy="40"  r="1.2"/>
    <circle cx="660" cy="100" r="1.2"/> <circle cx="750" cy="100" r="1.2"/> <circle cx="840" cy="100" r="1.2"/>
    <circle cx="660" cy="160" r="1.2"/> <circle cx="750" cy="160" r="1.2"/> <circle cx="840" cy="160" r="1.2"/>
    <circle cx="660" cy="220" r="1.2"/> <circle cx="750" cy="220" r="1.2"/> <circle cx="840" cy="220" r="1.2"/>
    <circle cx="660" cy="280" r="1.2"/> <circle cx="750" cy="280" r="1.2"/> <circle cx="840" cy="280" r="1.2"/>
  </g>

  <!-- Corner brackets -->
  <path d="M18,42 L18,18 L42,18"  fill="none" stroke="#38bdf8" stroke-width="2" stroke-linecap="round" opacity="0.5"/>
  <path d="M882,42 L882,18 L858,18" fill="none" stroke="#38bdf8" stroke-width="2" stroke-linecap="round" opacity="0.5"/>
  <path d="M18,278 L18,302 L42,302" fill="none" stroke="#818cf8" stroke-width="2" stroke-linecap="round" opacity="0.5"/>
  <path d="M882,278 L882,302 L858,302" fill="none" stroke="#818cf8" stroke-width="2" stroke-linecap="round" opacity="0.5"/>

  <!-- ── LEFT SIDE 3D OBJECTS ── -->

  <!-- Big blue sphere -->
  <g transform="translate(60, 95)">
    <circle cx="52" cy="52" r="52" fill="#0a1830" opacity="0.6" filter="url(#gTiny)" transform="translate(6,10)"/>
    <circle cx="52" cy="52" r="52" fill="url(#sBlue)"/>
    <ellipse cx="36" cy="30" rx="14" ry="8" fill="white" opacity="0.22" transform="rotate(-20,36,30)"/>
    <circle  cx="30" cy="24" r="5"  fill="white" opacity="0.28"/>
    <ellipse cx="52" cy="52" rx="52" ry="14" fill="none" stroke="#60a5fa" stroke-width="1.5" opacity="0.35" transform="rotate(-15,52,52)"/>
    <ellipse cx="52" cy="52" rx="52" ry="14" fill="none" stroke="#60a5fa" stroke-width="0.8" opacity="0.2"  transform="rotate(30,52,52)"/>
  </g>

  <!-- Blue isometric cube above sphere -->
  <g transform="translate(50, 28)" filter="url(#gSoft)">
    <polygon points="42,0 78,20 78,58 42,38" fill="url(#cRight)" stroke="#38bdf8" stroke-width="0.9" opacity="0.95"/>
    <polygon points="6,20 42,0 42,38 6,58"   fill="url(#cLeft)"  stroke="#38bdf8" stroke-width="0.9" opacity="0.95"/>
    <polygon points="6,20 42,0 78,20 42,40"   fill="url(#cTop)"   stroke="#38bdf8" stroke-width="0.9" opacity="0.95"/>
    <line x1="42" y1="0" x2="42" y2="38" stroke="#38bdf8" stroke-width="1.2" opacity="0.7"/>
    <circle cx="42" cy="0" r="3.5" fill="#38bdf8" filter="url(#gSoft)" opacity="0.95"/>
    <circle cx="6"  cy="20" r="2"  fill="#38bdf8" opacity="0.5"/>
    <circle cx="78" cy="20" r="2"  fill="#38bdf8" opacity="0.5"/>
    <circle cx="42" cy="40" r="2"  fill="#38bdf8" opacity="0.4"/>
  </g>

  <!-- Small teal sphere bottom-left -->
  <g transform="translate(24, 210)">
    <circle cx="28" cy="28" r="28" fill="#061812" opacity="0.5" filter="url(#gTiny)" transform="translate(4,6)"/>
    <circle cx="28" cy="28" r="28" fill="url(#sTeal)"/>
    <ellipse cx="19" cy="16" rx="8" ry="4.5" fill="white" opacity="0.2" transform="rotate(-20,19,16)"/>
    <circle  cx="16" cy="13" r="3"  fill="white" opacity="0.25"/>
  </g>

  <!-- Tiny floating diamond left -->
  <g transform="translate(158, 52)" opacity="0.8">
    <polygon points="14,0 26,14 14,28 2,14" fill="#0d1a35" stroke="#38bdf8" stroke-width="0.9"/>
    <polygon points="14,0 26,14 14,14"      fill="#1a2f55" opacity="0.7"/>
    <circle cx="14" cy="0" r="2" fill="#38bdf8" filter="url(#gSoft)"/>
  </g>

  <!-- Tiny pink sphere left -->
  <g transform="translate(162, 218)" opacity="0.85">
    <circle cx="18" cy="18" r="18" fill="url(#sPink)"/>
    <ellipse cx="12" cy="10" rx="5" ry="3" fill="white" opacity="0.22"/>
    <circle  cx="11" cy="9" r="2"  fill="white" opacity="0.28"/>
  </g>

  <!-- ── RIGHT SIDE 3D OBJECTS ── -->

  <!-- Big purple sphere -->
  <g transform="translate(788, 95)">
    <circle cx="52" cy="52" r="52" fill="#100520" opacity="0.6" filter="url(#gTiny)" transform="translate(6,10)"/>
    <circle cx="52" cy="52" r="52" fill="url(#sPurple)"/>
    <ellipse cx="36" cy="30" rx="14" ry="8" fill="white" opacity="0.2"  transform="rotate(-20,36,30)"/>
    <circle  cx="30" cy="24" r="5"  fill="white" opacity="0.26"/>
    <ellipse cx="52" cy="52" rx="52" ry="14" fill="none" stroke="#a78bfa" stroke-width="1.5" opacity="0.35" transform="rotate(15,52,52)"/>
    <ellipse cx="52" cy="52" rx="52" ry="14" fill="none" stroke="#a78bfa" stroke-width="0.8" opacity="0.2"  transform="rotate(-30,52,52)"/>
  </g>

  <!-- Purple isometric cube above sphere -->
  <g transform="translate(774, 28)" filter="url(#gSoft)">
    <polygon points="42,0 78,20 78,58 42,38" fill="url(#cRightP)" stroke="#818cf8" stroke-width="0.9" opacity="0.95"/>
    <polygon points="6,20 42,0 42,38 6,58"   fill="url(#cLeftP)"  stroke="#818cf8" stroke-width="0.9" opacity="0.95"/>
    <polygon points="6,20 42,0 78,20 42,40"   fill="url(#cTopP)"   stroke="#818cf8" stroke-width="0.9" opacity="0.95"/>
    <line x1="42" y1="0" x2="42" y2="38" stroke="#818cf8" stroke-width="1.2" opacity="0.7"/>
    <circle cx="42" cy="0" r="3.5" fill="#818cf8" filter="url(#gSoft)" opacity="0.95"/>
    <circle cx="6"  cy="20" r="2"  fill="#818cf8" opacity="0.5"/>
    <circle cx="78" cy="20" r="2"  fill="#818cf8" opacity="0.5"/>
    <circle cx="42" cy="40" r="2"  fill="#818cf8" opacity="0.4"/>
  </g>

  <!-- Small teal sphere bottom-right -->
  <g transform="translate(848, 210)">
    <circle cx="28" cy="28" r="28" fill="#020f08" opacity="0.5" filter="url(#gTiny)" transform="translate(4,6)"/>
    <circle cx="28" cy="28" r="28" fill="url(#sTeal)"/>
    <ellipse cx="19" cy="16" rx="8" ry="4.5" fill="white" opacity="0.2" transform="rotate(-20,19,16)"/>
    <circle  cx="16" cy="13" r="3"  fill="white" opacity="0.25"/>
  </g>

  <!-- Tiny diamond right -->
  <g transform="translate(718, 52)" opacity="0.8">
    <polygon points="14,0 26,14 14,28 2,14" fill="#1a0d35" stroke="#818cf8" stroke-width="0.9"/>
    <polygon points="14,0 26,14 14,14"      fill="#2e1660" opacity="0.7"/>
    <circle cx="14" cy="0" r="2" fill="#818cf8" filter="url(#gSoft)"/>
  </g>

  <!-- Tiny pink sphere right -->
  <g transform="translate(716, 218)" opacity="0.85">
    <circle cx="18" cy="18" r="18" fill="url(#sPink)"/>
    <ellipse cx="12" cy="10" rx="5" ry="3" fill="white" opacity="0.22"/>
    <circle  cx="11" cy="9"  r="2"  fill="white" opacity="0.28"/>
  </g>

  <!-- ── FLOATING PARTICLES ── -->
  <circle cx="210" cy="75"  r="1.8" fill="#38bdf8" opacity="0.7" filter="url(#gSoft)"/>
  <circle cx="195" cy="180" r="1.2" fill="#34d399" opacity="0.6"/>
  <circle cx="230" cy="250" r="1.5" fill="#818cf8" opacity="0.5" filter="url(#gSoft)"/>
  <circle cx="170" cy="290" r="1"   fill="#38bdf8" opacity="0.4"/>
  <circle cx="690" cy="75"  r="1.8" fill="#818cf8" opacity="0.7" filter="url(#gSoft)"/>
  <circle cx="710" cy="180" r="1.2" fill="#34d399" opacity="0.6"/>
  <circle cx="675" cy="250" r="1.5" fill="#38bdf8" opacity="0.5" filter="url(#gSoft)"/>
  <circle cx="730" cy="290" r="1"   fill="#818cf8" opacity="0.4"/>
  <circle cx="320" cy="40"  r="1.2" fill="#818cf8" opacity="0.35"/>
  <circle cx="580" cy="40"  r="1.2" fill="#38bdf8" opacity="0.35"/>
  <circle cx="360" cy="290" r="1.2" fill="#34d399" opacity="0.35"/>
  <circle cx="540" cy="290" r="1.2" fill="#818cf8" opacity="0.35"/>

  <!-- ── CENTER TEXT ── -->

  <!-- Halo glow blob behind name -->
  <ellipse cx="450" cy="165" rx="240" ry="90" fill="url(#halo)"/>

  <!-- Top separator line -->
  <rect x="280" y="72" width="340" height="1" fill="url(#hLine)" opacity="0.7"/>

  <!-- Tag -->
  <text x="450" y="98"
        font-family="'Courier New',monospace"
        font-size="11" font-weight="400"
        fill="#38bdf8" text-anchor="middle"
        letter-spacing="5" opacity="0.9">// ML ENGINEER · BACKEND · WEB</text>

  <!-- 3D layered name shadows -->
  <text x="456" y="172"
        font-family="Georgia,'Times New Roman',serif"
        font-size="88" font-weight="900"
        fill="#0c1a30" text-anchor="middle"
        letter-spacing="-3" opacity="0.85">DEEPAK R</text>

  <text x="453" y="169"
        font-family="Georgia,'Times New Roman',serif"
        font-size="88" font-weight="900"
        fill="#162b4a" text-anchor="middle"
        letter-spacing="-3" opacity="0.9">DEEPAK R</text>

  <!-- Main name with gradient + glow -->
  <text x="450" y="166"
        font-family="Georgia,'Times New Roman',serif"
        font-size="88" font-weight="900"
        fill="url(#nameG)" text-anchor="middle"
        letter-spacing="-3"
        filter="url(#gNameBig)">DEEPAK R</text>

  <!-- Subtitle -->
  <text x="450" y="202"
        font-family="'Courier New',monospace"
        font-size="13" font-weight="400"
        fill="#94a3b8" text-anchor="middle"
        letter-spacing="3">Machine Learning · Backend · Web Development</text>

  <!-- Bottom separator line -->
  <rect x="280" y="220" width="340" height="1" fill="url(#hLine)" opacity="0.7"/>

  <!-- Status pill -->
  <rect x="358" y="236" width="184" height="28" rx="14" fill="#0d1f38" stroke="#38bdf8" stroke-width="0.8" opacity="0.85"/>
  <circle cx="376" cy="250" r="4" fill="#34d399" opacity="0.9" filter="url(#gSoft)"/>
  <text x="450" y="255"
        font-family="'Courier New',monospace"
        font-size="11"
        fill="#94a3b8" text-anchor="middle"
        letter-spacing="1.5">Open to Collaborations</text>

  <!-- Bottom label -->
  <text x="450" y="300"
        font-family="'Courier New',monospace"
        font-size="10"
        fill="#334155" text-anchor="middle"
        letter-spacing="4">CRAFTING AI · POWERED EXPERIENCES</text>
</svg>

<br/>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=17&pause=1000&color=38BDF8&center=true&vCenter=true&width=600&height=40&lines=Building+AI-powered+web+experiences+%F0%9F%9A%80;Machine+Learning+%7C+Backend+%7C+Full-Stack+%F0%9F%A7%A0;Turning+ideas+into+impactful+products+%E2%9C%A8;Open+to+collaborations+%F0%9F%A4%9D)](https://github.com/deepak-5656)

<br/>

[![GitHub followers](https://img.shields.io/github/followers/deepak-5656?label=Followers&style=for-the-badge&color=38bdf8&labelColor=0b0d14&logo=github&logoColor=38bdf8)](https://github.com/deepak-5656)
[![Profile Views](https://komarev.com/ghpvc/?username=deepak-5656&label=Profile+Views&color=818cf8&style=for-the-badge&labelColor=0b0d14)](https://github.com/deepak-5656)
[![Stars](https://img.shields.io/github/stars/deepak-5656?label=Total+Stars&style=for-the-badge&color=34d399&labelColor=0b0d14&logo=github&logoColor=34d399)](https://github.com/deepak-5656)

</div>

---

## `{ about_me }`

```python
class Deepak:
    name        = "Deepak R"
    location    = "India 🇮🇳"
    roles       = ["ML Engineer", "Backend Developer", "Web Craftsman"]
    passion     = "AI-powered web experiences 🚀"

    stack = {
        "ml"       : ["Python", "TensorFlow", "PyTorch", "scikit-learn", "Pandas", "NumPy"],
        "backend"  : ["Node.js", "Express", "MongoDB", "MySQL", "PostgreSQL", "REST APIs"],
        "frontend" : ["JavaScript", "TypeScript", "React", "HTML5", "CSS3"],
        "tools"    : ["Git", "GitHub", "VS Code", "Postman", "Docker"],
    }

    currently   = "Exploring LLMs · MLOps · System Design"
    open_to     = "Collaborations on ML & Full-Stack projects 🤝"
    fun_fact    = "I debug code and ideas equally well ☕"

    def say_hi(self):
        print("Let's build something amazing together! 🔥")
```

---

## `{ tech_universe }`

### 🧠 Machine Learning & AI

<div align="center">

<table>
<tr>
<td align="center" width="110">
<img src="https://skillicons.dev/icons?i=python" width="48" height="48" alt="Python"/><br/><sub><b>Python</b></sub>
</td>
<td align="center" width="110">
<img src="https://skillicons.dev/icons?i=tensorflow" width="48" height="48" alt="TensorFlow"/><br/><sub><b>TensorFlow</b></sub>
</td>
<td align="center" width="110">
<img src="https://skillicons.dev/icons?i=pytorch" width="48" height="48" alt="PyTorch"/><br/><sub><b>PyTorch</b></sub>
</td>
<td align="center" width="110">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pandas/pandas-original.svg" width="48" height="48" alt="Pandas"/><br/><sub><b>Pandas</b></sub>
</td>
<td align="center" width="110">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/numpy/numpy-original.svg" width="48" height="48" alt="NumPy"/><br/><sub><b>NumPy</b></sub>
</td>
<td align="center" width="110">
<img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" width="48" height="48" alt="scikit-learn"/><br/><sub><b>scikit-learn</b></sub>
</td>
<td align="center" width="110">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jupyter/jupyter-original.svg" width="48" height="48" alt="Jupyter"/><br/><sub><b>Jupyter</b></sub>
</td>
</tr>
</table>

</div>

### ⚙️ Backend Development

<div align="center">

<table>
<tr>
<td align="center" width="110">
<img src="https://skillicons.dev/icons?i=nodejs" width="48" height="48" alt="Node.js"/><br/><sub><b>Node.js</b></sub>
</td>
<td align="center" width="110">
<img src="https://skillicons.dev/icons?i=express" width="48" height="48" alt="Express"/><br/><sub><b>Express</b></sub>
</td>
<td align="center" width="110">
<img src="https://skillicons.dev/icons?i=mongodb" width="48" height="48" alt="MongoDB"/><br/><sub><b>MongoDB</b></sub>
</td>
<td align="center" width="110">
<img src="https://skillicons.dev/icons?i=mysql" width="48" height="48" alt="MySQL"/><br/><sub><b>MySQL</b></sub>
</td>
<td align="center" width="110">
<img src="https://skillicons.dev/icons?i=postgresql" width="48" height="48" alt="PostgreSQL"/><br/><sub><b>PostgreSQL</b></sub>
</td>
<td align="center" width="110">
<img src="https://skillicons.dev/icons?i=firebase" width="48" height="48" alt="Firebase"/><br/><sub><b>Firebase</b></sub>
</td>
</tr>
</table>

</div>

### 🌐 Frontend & Web

<div align="center">

<table>
<tr>
<td align="center" width="110">
<img src="https://skillicons.dev/icons?i=js" width="48" height="48" alt="JavaScript"/><br/><sub><b>JavaScript</b></sub>
</td>
<td align="center" width="110">
<img src="https://skillicons.dev/icons?i=ts" width="48" height="48" alt="TypeScript"/><br/><sub><b>TypeScript</b></sub>
</td>
<td align="center" width="110">
<img src="https://skillicons.dev/icons?i=react" width="48" height="48" alt="React"/><br/><sub><b>React</b></sub>
</td>
<td align="center" width="110">
<img src="https://skillicons.dev/icons?i=html" width="48" height="48" alt="HTML5"/><br/><sub><b>HTML5</b></sub>
</td>
<td align="center" width="110">
<img src="https://skillicons.dev/icons?i=css" width="48" height="48" alt="CSS3"/><br/><sub><b>CSS3</b></sub>
</td>
<td align="center" width="110">
<img src="https://skillicons.dev/icons?i=tailwind" width="48" height="48" alt="Tailwind"/><br/><sub><b>Tailwind</b></sub>
</td>
</tr>
</table>

</div>

### 🧰 Tools & DevOps

<div align="center">

<table>
<tr>
<td align="center" width="110">
<img src="https://skillicons.dev/icons?i=git" width="48" height="48" alt="Git"/><br/><sub><b>Git</b></sub>
</td>
<td align="center" width="110">
<img src="https://skillicons.dev/icons?i=github" width="48" height="48" alt="GitHub"/><br/><sub><b>GitHub</b></sub>
</td>
<td align="center" width="110">
<img src="https://skillicons.dev/icons?i=vscode" width="48" height="48" alt="VS Code"/><br/><sub><b>VS Code</b></sub>
</td>
<td align="center" width="110">
<img src="https://skillicons.dev/icons?i=postman" width="48" height="48" alt="Postman"/><br/><sub><b>Postman</b></sub>
</td>
<td align="center" width="110">
<img src="https://skillicons.dev/icons?i=docker" width="48" height="48" alt="Docker"/><br/><sub><b>Docker</b></sub>
</td>
<td align="center" width="110">
<img src="https://skillicons.dev/icons?i=linux" width="48" height="48" alt="Linux"/><br/><sub><b>Linux</b></sub>
</td>
</tr>
</table>

</div>

---

## `{ featured_projects }`

<div align="center">

<a href="https://github.com/deepak-5656/wanderease">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=deepak-5656&repo=wanderease&theme=tokyonight&hide_border=true&bg_color=060a14&title_color=38bdf8&icon_color=34d399&text_color=94a3b8&border_radius=12"/>
</a>
&nbsp;
<a href="https://github.com/deepak-5656/Ecommercechatbot">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=deepak-5656&repo=Ecommercechatbot&theme=tokyonight&hide_border=true&bg_color=060a14&title_color=818cf8&icon_color=34d399&text_color=94a3b8&border_radius=12"/>
</a>

</div>

<br/>

> 🗺️ **WanderEase** — AI-powered travel platform with smart itinerary planning and seamless booking UX
> `JavaScript` &nbsp; `AI Features` &nbsp; `Web APIs`

> 🤖 **E-commerce Chatbot** — Conversational AI shopping assistant with NLP for smarter product discovery
> `TypeScript` &nbsp; `NLP` &nbsp; `Machine Learning`

---

## `{ github_stats }`

<div align="center">

<img height="175em" src="https://github-readme-stats.vercel.app/api?username=deepak-5656&show_icons=true&theme=tokyonight&hide_border=true&bg_color=060a14&title_color=38bdf8&icon_color=34d399&text_color=94a3b8&ring_color=818cf8&border_radius=12&include_all_commits=true&count_private=true"/>
<img height="175em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=deepak-5656&layout=compact&theme=tokyonight&hide_border=true&bg_color=060a14&title_color=38bdf8&text_color=94a3b8&border_radius=12&langs_count=8"/>

</div>

<div align="center">

[![GitHub Streak](https://streak-stats.demolab.com?user=deepak-5656&theme=tokyonight&hide_border=true&background=060a14&ring=38bdf8&fire=818cf8&currStreakLabel=34d399&border_radius=12)](https://github.com/deepak-5656)

</div>

<div align="center">

[![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=deepak-5656&bg_color=060a14&color=38bdf8&line=818cf8&point=34d399&hide_border=true&radius=8)](https://github.com/deepak-5656)

</div>

---

## `{ achievements }`

<div align="center">

[![Trophies](https://github-profile-trophy.vercel.app/?username=deepak-5656&theme=tokyonight&no-frame=true&no-bg=true&margin-w=8&column=6)](https://github.com/deepak-5656)

</div>

---

## `{ currently }`

```bash
🔭  Building AI-powered features for smarter user experiences
🌱  Deepening expertise in Deep Learning & Large Language Models
🛠️  Designing scalable backend systems & clean REST APIs
📚  Exploring MLOps — model deployment, monitoring & pipelines
🤝  Open to collabs on impactful ML & full-stack web projects
```

---

## `{ lets_connect }`

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-deepak--5656-060a14?style=for-the-badge&logo=github&logoColor=38bdf8&color=060a14&labelColor=060a14)](https://github.com/deepak-5656)

<br/><br/>

*"Crafting impactful web projects and experimenting with AI-powered features*
*for smarter, more human digital experiences."*

<br/>

**⭐ If you like my work, drop a star — it means the world! ⭐**

<br/>

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 60" width="900" height="60">
  <defs>
    <linearGradient id="fBg" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#020408"/>
      <stop offset="50%"  stop-color="#060a14"/>
      <stop offset="100%" stop-color="#020408"/>
    </linearGradient>
    <linearGradient id="fLine" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#38bdf8" stop-opacity="0"/>
      <stop offset="25%"  stop-color="#38bdf8" stop-opacity="0.9"/>
      <stop offset="50%"  stop-color="#818cf8" stop-opacity="1"/>
      <stop offset="75%"  stop-color="#34d399" stop-opacity="0.9"/>
      <stop offset="100%" stop-color="#34d399" stop-opacity="0"/>
    </linearGradient>
  </defs>
  <rect width="900" height="60" fill="url(#fBg)" rx="10"/>
  <rect x="0" y="0" width="900" height="1" fill="url(#fLine)" opacity="0.8"/>
  <text x="450" y="36" font-family="'Courier New',monospace" font-size="11" fill="#475569" text-anchor="middle" letter-spacing="4">DEEPAK R · 2024 · BUILT WITH ☕ AND PYTHON</text>
  <circle cx="200" cy="30" r="1.5" fill="#38bdf8" opacity="0.5"/>
  <circle cx="700" cy="30" r="1.5" fill="#818cf8" opacity="0.5"/>
</svg>

</div>
