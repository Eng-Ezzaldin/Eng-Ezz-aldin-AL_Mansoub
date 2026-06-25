<svg width="1920" height="720" viewBox="0 0 1920 720" fill="none" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="bg" x1="0" y1="0" x2="1920" y2="720">
      <stop offset="0" stop-color="#030712"/>
      <stop offset="0.45" stop-color="#071024"/>
      <stop offset="0.72" stop-color="#120A2E"/>
      <stop offset="1" stop-color="#031827"/>
    </linearGradient>

    <linearGradient id="neon" x1="0" y1="0" x2="1920" y2="720">
      <stop offset="0" stop-color="#00E5FF"/>
      <stop offset="0.5" stop-color="#6D5DF6"/>
      <stop offset="1" stop-color="#A855F7"/>
    </linearGradient>

    <linearGradient id="glass" x1="260" y1="140" x2="1660" y2="610">
      <stop offset="0" stop-color="#FFFFFF" stop-opacity="0.12"/>
      <stop offset="1" stop-color="#FFFFFF" stop-opacity="0.03"/>
    </linearGradient>

    <filter id="glow">
      <feGaussianBlur stdDeviation="8" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <filter id="softShadow" x="-20%" y="-20%" width="140%" height="140%">
      <feDropShadow dx="0" dy="20" stdDeviation="24" flood-color="#000000" flood-opacity="0.55"/>
    </filter>

    <pattern id="grid" width="48" height="48" patternUnits="userSpaceOnUse">
      <path d="M 48 0 L 0 0 0 48" fill="none" stroke="#00E5FF" stroke-opacity="0.08" stroke-width="1"/>
    </pattern>

    <style>
      .mono { font-family: "JetBrains Mono", "Fira Code", Consolas, monospace; }
      .sans { font-family: Inter, Segoe UI, Arial, sans-serif; }
      @keyframes pulse {
        0%, 100% { opacity: .35; }
        50% { opacity: 1; }
      }
      @keyframes float {
        0%, 100% { transform: translateY(0px); }
        50% { transform: translateY(-12px); }
      }
      @keyframes scan {
        0% { transform: translateX(-500px); opacity: 0; }
        30% { opacity: .65; }
        100% { transform: translateX(1900px); opacity: 0; }
      }
      .pulse { animation: pulse 2.4s infinite ease-in-out; }
      .float { animation: float 5s infinite ease-in-out; }
      .scan { animation: scan 6s infinite linear; }
    </style>
  </defs>

  <rect width="1920" height="720" fill="url(#bg)"/>
  <rect width="1920" height="720" fill="url(#grid)"/>

  <!-- cosmic particles -->
  <g opacity="0.75">
    <circle cx="160" cy="120" r="2" fill="#00E5FF"/>
    <circle cx="310" cy="520" r="1.8" fill="#A855F7"/>
    <circle cx="540" cy="90" r="2.2" fill="#FFFFFF"/>
    <circle cx="720" cy="640" r="1.7" fill="#00E5FF"/>
    <circle cx="1020" cy="105" r="2" fill="#A855F7"/>
    <circle cx="1280" cy="610" r="1.8" fill="#FFFFFF"/>
    <circle cx="1550" cy="155" r="2.2" fill="#00E5FF"/>
    <circle cx="1770" cy="470" r="1.7" fill="#A855F7"/>
  </g>

  <!-- scan beam -->
  <rect class="scan" x="0" y="0" width="260" height="720" fill="url(#neon)" opacity="0.08"/>

  <!-- main glass panel -->
  <rect x="150" y="90" width="1620" height="540" rx="38" fill="url(#glass)" stroke="url(#neon)" stroke-opacity="0.65" stroke-width="2" filter="url(#softShadow)"/>

  <!-- corner HUD lines -->
  <path d="M210 170V130H310" stroke="#00E5FF" stroke-width="4" stroke-linecap="round" filter="url(#glow)"/>
  <path d="M1710 170V130H1610" stroke="#A855F7" stroke-width="4" stroke-linecap="round" filter="url(#glow)"/>
  <path d="M210 550V590H310" stroke="#A855F7" stroke-width="4" stroke-linecap="round" filter="url(#glow)"/>
  <path d="M1710 550V590H1610" stroke="#00E5FF" stroke-width="4" stroke-linecap="round" filter="url(#glow)"/>

  <!-- left system label -->
  <g class="mono">
    <text x="230" y="160" fill="#00E5FF" font-size="28" font-weight="700">ACCESS GRANTED</text>
    <text x="230" y="196" fill="#94A3B8" font-size="18">EZZ OS • DEVELOPER PROFILE SYSTEM</text>
  </g>

  <!-- identity -->
  <g>
    <text x="230" y="315" class="sans" fill="#F8FAFC" font-size="92" font-weight="900" letter-spacing="2">EZZ ALDIN</text>
    <text x="234" y="365" class="mono" fill="#00E5FF" font-size="30" font-weight="700">Software Engineering Student</text>
    <text x="234" y="404" class="mono" fill="#CBD5E1" font-size="24">Flutter Developer  •  Laravel Backend Developer  •  Cybersecurity Learner</text>
  </g>

  <!-- status chips -->
  <g class="mono" font-size="18" font-weight="700">
    <rect x="230" y="450" width="170" height="48" rx="14" fill="#061826" stroke="#22C55E" stroke-opacity="0.8"/>
    <circle class="pulse" cx="258" cy="474" r="8" fill="#22C55E"/>
    <text x="278" y="481" fill="#D1FAE5">ONLINE</text>

    <rect x="420" y="450" width="260" height="48" rx="14" fill="#100F2E" stroke="#6D5DF6" stroke-opacity="0.8"/>
    <text x="448" y="481" fill="#DDD6FE">BUILDING REAL PROJECTS</text>

    <rect x="700" y="450" width="230" height="48" rx="14" fill="#071A24" stroke="#00E5FF" stroke-opacity="0.8"/>
    <text x="728" y="481" fill="#CFFAFE">CODE • BUILD • SECURE</text>
  </g>

  <!-- contact -->
  <g class="mono" font-size="18">
    <text x="234" y="550" fill="#94A3B8">COMMUNICATION GATEWAY</text>
    <text x="234" y="584" fill="#F8FAFC">ezzman1234567890@gmail.com</text>
    <text x="234" y="615" fill="#00E5FF">github.com/Eng-Ezzaldin</text>
  </g>

  <!-- right hologram orb -->
  <g class="float" transform="translate(1180 165)">
    <circle cx="240" cy="215" r="190" fill="#00E5FF" opacity="0.05"/>
    <circle cx="240" cy="215" r="160" stroke="#00E5FF" stroke-opacity="0.8" stroke-width="3" filter="url(#glow)"/>
    <circle cx="240" cy="215" r="120" stroke="#6D5DF6" stroke-opacity="0.65" stroke-width="2" stroke-dasharray="16 12"/>
    <circle cx="240" cy="215" r="82" stroke="#A855F7" stroke-opacity="0.65" stroke-width="2" stroke-dasharray="8 10"/>
    <circle cx="240" cy="215" r="36" fill="url(#neon)" filter="url(#glow)"/>

    <path d="M240 25V78" stroke="#00E5FF" stroke-width="3" stroke-linecap="round"/>
    <path d="M240 352V405" stroke="#A855F7" stroke-width="3" stroke-linecap="round"/>
    <path d="M50 215H104" stroke="#A855F7" stroke-width="3" stroke-linecap="round"/>
    <path d="M376 215H430" stroke="#00E5FF" stroke-width="3" stroke-linecap="round"/>

    <text x="95" y="480" class="mono" fill="#F8FAFC" font-size="26" font-weight="800">DIGITAL DIMENSION</text>
    <text x="110" y="515" class="mono" fill="#94A3B8" font-size="18">Flutter • Laravel • Cybersecurity • AI</text>
  </g>

  <!-- bottom progress cards -->
  <g class="mono">
    <rect x="1060" y="510" width="170" height="70" rx="18" fill="#07111F" stroke="#00E5FF" stroke-opacity="0.35"/>
    <text x="1084" y="540" fill="#94A3B8" font-size="16">FLUTTER</text>
    <rect x="1084" y="555" width="115" height="8" rx="4" fill="#1E293B"/>
    <rect x="1084" y="555" width="98" height="8" rx="4" fill="#00E5FF"/>

    <rect x="1250" y="510" width="170" height="70" rx="18" fill="#07111F" stroke="#6D5DF6" stroke-opacity="0.35"/>
    <text x="1274" y="540" fill="#94A3B8" font-size="16">LARAVEL</text>
    <rect x="1274" y="555" width="115" height="8" rx="4" fill="#1E293B"/>
    <rect x="1274" y="555" width="92" height="8" rx="4" fill="#6D5DF6"/>

    <rect x="1440" y="510" width="210" height="70" rx="18" fill="#07111F" stroke="#A855F7" stroke-opacity="0.35"/>
    <text x="1464" y="540" fill="#94A3B8" font-size="16">CYBERSECURITY</text>
    <rect x="1464" y="555" width="145" height="8" rx="4" fill="#1E293B"/>
    <rect x="1464" y="555" width="93" height="8" rx="4" fill="#A855F7"/>
  </g>
</svg>
