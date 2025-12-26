<?xml version="1.0" encoding="utf-8"?>
<!-- Neon/Neo animated header for GitHub README
     Save as neon-header.svg and optionally convert to neon-header.gif for guaranteed animation.
-->
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 160" width="1200" height="160" role="img" aria-label="Neon header for Udhayaprakash J">
  <defs>
    <!-- animated gradient -->
    <linearGradient id="grad" x1="0" x2="1">
      <stop offset="0" stop-color="#00ff99">
        <animate attributeName="stop-color" values="#00ff99;#00d4ff;#7a00ff;#00ff99" dur="5s" repeatCount="indefinite"/>
      </stop>
      <stop offset="1" stop-color="#00d4ff">
        <animate attributeName="stop-color" values="#00d4ff;#7a00ff;#00ff99;#00d4ff" dur="5s" repeatCount="indefinite"/>
      </stop>
    </linearGradient>

    <!-- glow filter -->
    <filter id="glow" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="6" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <!-- subtle scanline overlay -->
    <pattern id="scan" width="4" height="4" patternUnits="userSpaceOnUse">
      <rect width="4" height="2" fill="rgba(255,255,255,0.02)"/>
    </pattern>

    <style type="text/css"><![CDATA[
      .bg { fill:#04060a; }
      .title { font-family: 'Poppins', 'Inter', sans-serif; font-weight:800; font-size:56px; fill:url(#grad); }
      .subtitle { font-family: 'Inter', Arial, sans-serif; font-size:16px; fill:#8ef0ff; opacity:0.92; letter-spacing:1px; }
      .outline { fill:none; stroke:rgba(255,255,255,0.06); stroke-width:1.2; }
      .flicker { animation: flicker 3s infinite; }
      @keyframes flicker {
        0% { opacity:1; filter:brightness(1); }
        5% { opacity:0.85; filter:brightness(1.3); }
        10% { opacity:0.98; }
        30% { opacity:1; }
        60% { opacity:0.9; filter:brightness(0.9); }
        100% { opacity:1; }
      }
    ]]></style>
  </defs>

  <!-- background rounded card with scan pattern -->
  <rect x="0" y="0" width="1200" height="160" rx="12" class="bg"/>
  <rect x="8" y="8" width="1184" height="144" rx="10" fill="url(#scan)" opacity="0.06"/>

  <!-- neon title group -->
  <g transform="translate(44,46)">
    <!-- layered glow text for stronger neon -->
    <text class="title" x="0" y="50" filter="url(#glow)">
      Udhayaprakash J
    </text>

    <!-- thin stroke for sharp neon edge -->
    <text x="0" y="50" class="title" fill="none" stroke="rgba(255,255,255,0.06)" stroke-width="1">
      Udhayaprakash J
    </text>

    <!-- animated neon stroke that sweeps across -->
    <rect x="-12" y="60" width="520" height="6" rx="4" fill="url(#grad)" opacity="0.95">
      <animate attributeName="x" from="-520" to="520" dur="2.5s" repeatCount="indefinite" />
      <animate attributeName="opacity" values="0.0;0.95;0.0" dur="2.5s" repeatCount="indefinite"/>
    </rect>

    <!-- subtitle with typing-like fade in -->
    <text x="0" y="86" class="subtitle" opacity="0">
      <tspan>DevOps &amp; Cloud Engineer</tspan>
      <tspan dx="12"> • AWS • CI/CD • Docker • Kubernetes • Terraform</tspan>
      <animate attributeName="opacity" from="0" to="1" begin="0.5s" dur="1.1s" fill="freeze" />
    </text>

    <!-- tiny holographic badge -->
    <g transform="translate(520,-6)" class="flicker">
      <rect x="0" y="0" width="180" height="56" rx="8" fill="#02080b" stroke="rgba(255,255,255,0.04)"/>
      <text x="14" y="22" font-size="12" fill="#9ef6d1" font-family="Inter, Arial">M.Tech (Software Eng.)</text>
      <text x="14" y="40" font-size="11" fill="#9ef6d1" opacity="0.85" font-family="Inter, Arial">VIT Chennai • 7.69 CGPA</text>
    </g>
  </g>

  <!-- subtle bottom-right neon spark -->
  <g transform="translate(980,108)">
    <circle cx="0" cy="0" r="6" fill="#00ff99" opacity="0.95">
      <animate attributeName="r" values="4;8;4" dur="2.2s" repeatCount="indefinite" />
      <animate attributeName="opacity" values="0.6;1;0.6" dur="2.2s" repeatCount="indefinite" />
    </circle>
  </g>
</svg>
