<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>✨ Công Vinh (Kenzy) ✨</title>
<link href="https://fonts.googleapis.com/css2?family=Cinzel+Decorative:wght@400;700;900&family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300&family=Rajdhani:wght@300;400;600;700&display=swap" rel="stylesheet">
<style>
  :root {
    --gold: #FFD700;
    --gold-light: #FFF0A0;
    --gold-dark: #B8860B;
    --copper: #FF8C42;
    --deep-navy: #020817;
    --navy: #050f2c;
    --navy-mid: #091435;
    --blue-glow: #1E90FF;
    --blue-soft: #4BA3FF;
    --white: #F8F4E8;
    --white-dim: rgba(248,244,232,0.6);
  }

  *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--deep-navy);
    color: var(--white);
    font-family: 'Cormorant Garamond', serif;
    overflow-x: hidden;
    min-height: 100vh;
  }

  /* ===== STARFIELD ===== */
  #canvas-stars {
    position: fixed;
    top: 0; left: 0;
    width: 100%; height: 100%;
    z-index: 0;
    pointer-events: none;
  }

  /* ===== FLOATING PARTICLES ===== */
  .particles {
    position: fixed;
    top: 0; left: 0;
    width: 100%; height: 100%;
    pointer-events: none;
    z-index: 1;
  }
  .particle {
    position: absolute;
    border-radius: 50%;
    animation: floatParticle linear infinite;
    opacity: 0;
  }

  @keyframes floatParticle {
    0%   { transform: translateY(100vh) scale(0); opacity: 0; }
    10%  { opacity: 1; }
    90%  { opacity: 1; }
    100% { transform: translateY(-10vh) scale(1); opacity: 0; }
  }

  /* ===== WRAPPER ===== */
  .wrapper {
    position: relative;
    z-index: 2;
    max-width: 900px;
    margin: 0 auto;
    padding: 40px 20px 80px;
  }

  /* ===== HERO SECTION ===== */
  .hero {
    text-align: center;
    padding: 60px 0 40px;
    position: relative;
  }

  .hero-orb {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 400px;
    height: 400px;
    border-radius: 50%;
    background: radial-gradient(circle at 35% 35%,
      rgba(255,215,0,0.15) 0%,
      rgba(30,144,255,0.08) 40%,
      transparent 70%
    );
    filter: blur(40px);
    animation: orbPulse 6s ease-in-out infinite;
    pointer-events: none;
  }

  @keyframes orbPulse {
    0%, 100% { transform: translate(-50%, -50%) scale(1); opacity: 0.6; }
    50%       { transform: translate(-50%, -50%) scale(1.2); opacity: 1; }
  }

  .title-crown {
    font-size: 0.9rem;
    font-family: 'Rajdhani', sans-serif;
    letter-spacing: 0.4em;
    color: var(--gold);
    text-transform: uppercase;
    margin-bottom: 12px;
    animation: fadeSlideDown 1s ease both;
    animation-delay: 0.2s;
    opacity: 0;
  }

  .title-main {
    font-family: 'Cinzel Decorative', cursive;
    font-size: clamp(2.2rem, 6vw, 3.8rem);
    font-weight: 900;
    line-height: 1.1;
    background: linear-gradient(135deg,
      var(--gold-light) 0%,
      var(--gold) 30%,
      var(--copper) 60%,
      var(--gold) 80%,
      var(--gold-light) 100%
    );
    background-size: 200% auto;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    animation: fadeSlideDown 1s ease both, shimmerText 4s linear infinite;
    animation-delay: 0.4s, 1s;
    opacity: 0;
    text-shadow: none;
    position: relative;
    z-index: 2;
  }

  @keyframes shimmerText {
    0%   { background-position: 0% center; }
    100% { background-position: 200% center; }
  }

  .title-sub {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(1.1rem, 3vw, 1.5rem);
    font-style: italic;
    font-weight: 300;
    color: var(--blue-soft);
    margin-top: 10px;
    animation: fadeSlideDown 1s ease both;
    animation-delay: 0.6s;
    opacity: 0;
    letter-spacing: 0.05em;
  }

  /* ===== AVATAR CONTAINER ===== */
  .avatar-ring {
    margin: 30px auto;
    width: 140px;
    height: 140px;
    position: relative;
    animation: fadeSlideDown 1s ease both;
    animation-delay: 0.8s;
    opacity: 0;
  }

  .avatar-ring::before {
    content: '';
    position: absolute;
    inset: -4px;
    border-radius: 50%;
    background: conic-gradient(
      var(--gold) 0deg,
      var(--blue-glow) 90deg,
      var(--gold) 180deg,
      var(--copper) 270deg,
      var(--gold) 360deg
    );
    animation: spinRing 6s linear infinite;
  }

  @keyframes spinRing {
    from { transform: rotate(0deg); }
    to   { transform: rotate(360deg); }
  }

  .avatar-ring::after {
    content: '';
    position: absolute;
    inset: -12px;
    border-radius: 50%;
    border: 1px solid rgba(255,215,0,0.2);
    animation: spinRing 10s linear infinite reverse;
  }

  .avatar-inner {
    position: absolute;
    inset: 3px;
    border-radius: 50%;
    background: var(--navy-mid);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 3.5rem;
    overflow: hidden;
  }

  /* Corgi GIF inside avatar */
  .avatar-inner img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 50%;
  }

  /* ===== FOLLOW BADGE ===== */
  .follow-badge {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    margin: 10px auto 0;
    padding: 10px 24px;
    border: 1px solid rgba(255,215,0,0.3);
    border-radius: 60px;
    font-family: 'Rajdhani', sans-serif;
    font-size: 0.85rem;
    letter-spacing: 0.25em;
    color: var(--gold);
    text-transform: uppercase;
    background: rgba(255,215,0,0.05);
    animation: fadeSlideDown 1s ease both, pulseBorder 3s ease-in-out infinite;
    animation-delay: 1s, 2s;
    opacity: 0;
  }

  @keyframes pulseBorder {
    0%, 100% { border-color: rgba(255,215,0,0.3); box-shadow: 0 0 0 0 rgba(255,215,0,0); }
    50%       { border-color: rgba(255,215,0,0.7); box-shadow: 0 0 20px rgba(255,215,0,0.15); }
  }

  .follow-dot {
    width: 6px; height: 6px;
    border-radius: 50%;
    background: var(--gold);
    animation: blinkDot 1.5s ease-in-out infinite;
  }

  @keyframes blinkDot {
    0%, 100% { opacity: 1; }
    50%       { opacity: 0.2; }
  }

  /* ===== DIVIDER ===== */
  .gold-divider {
    display: flex;
    align-items: center;
    gap: 16px;
    margin: 40px 0;
    animation: fadeIn 1s ease both;
    animation-delay: 1.2s;
    opacity: 0;
  }

  .gold-divider::before, .gold-divider::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--gold-dark), var(--gold), var(--gold-dark), transparent);
  }

  .divider-gem {
    width: 10px; height: 10px;
    background: var(--gold);
    transform: rotate(45deg);
    box-shadow: 0 0 12px var(--gold), 0 0 24px rgba(255,215,0,0.4);
    flex-shrink: 0;
  }

  /* ===== SECTION CARDS ===== */
  .card {
    background: linear-gradient(135deg,
      rgba(9,20,53,0.9) 0%,
      rgba(5,15,44,0.95) 100%
    );
    border: 1px solid rgba(255,215,0,0.15);
    border-radius: 2px;
    padding: 36px 40px;
    margin-bottom: 28px;
    position: relative;
    overflow: hidden;
    transform: perspective(1000px) rotateX(0deg);
    transition: transform 0.4s ease, box-shadow 0.4s ease, border-color 0.4s ease;
    animation: fadeSlideUp 0.8s ease both;
    opacity: 0;
  }

  .card:hover {
    transform: perspective(1000px) translateY(-4px);
    box-shadow:
      0 20px 60px rgba(0,0,0,0.5),
      0 0 40px rgba(255,215,0,0.08),
      inset 0 1px 0 rgba(255,215,0,0.2);
    border-color: rgba(255,215,0,0.3);
  }

  /* Corner decorations */
  .card::before {
    content: '';
    position: absolute;
    top: 0; left: 0;
    width: 40px; height: 40px;
    border-top: 2px solid var(--gold);
    border-left: 2px solid var(--gold);
  }

  .card::after {
    content: '';
    position: absolute;
    bottom: 0; right: 0;
    width: 40px; height: 40px;
    border-bottom: 2px solid var(--gold);
    border-right: 2px solid var(--gold);
  }

  /* Card inner top-right corner */
  .card-corner-tr {
    position: absolute;
    top: 0; right: 0;
    width: 40px; height: 40px;
    border-top: 2px solid var(--gold-dark);
    border-right: 2px solid var(--gold-dark);
  }

  .card-corner-bl {
    position: absolute;
    bottom: 0; left: 0;
    width: 40px; height: 40px;
    border-bottom: 2px solid var(--gold-dark);
    border-left: 2px solid var(--gold-dark);
  }

  /* Glow line on top */
  .card-glow {
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, transparent 0%, var(--gold) 50%, transparent 100%);
    opacity: 0;
    transition: opacity 0.4s;
  }
  .card:hover .card-glow { opacity: 1; }

  .card-title {
    font-family: 'Rajdhani', sans-serif;
    font-size: 0.75rem;
    font-weight: 700;
    letter-spacing: 0.4em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .card-title::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, rgba(255,215,0,0.4), transparent);
  }

  /* ===== CONTACT ===== */
  .contact-link {
    display: inline-flex;
    align-items: center;
    gap: 12px;
    padding: 14px 28px;
    border: 1px solid rgba(30,144,255,0.4);
    border-radius: 2px;
    color: var(--blue-soft);
    text-decoration: none;
    font-family: 'Rajdhani', sans-serif;
    font-size: 1rem;
    font-weight: 600;
    letter-spacing: 0.1em;
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;
  }

  .contact-link::before {
    content: '';
    position: absolute;
    inset: 0;
    background: linear-gradient(135deg, rgba(30,144,255,0.1), transparent);
    transform: translateX(-100%);
    transition: transform 0.4s ease;
  }

  .contact-link:hover::before { transform: translateX(0); }
  .contact-link:hover {
    color: var(--white);
    border-color: var(--blue-glow);
    box-shadow: 0 0 20px rgba(30,144,255,0.2);
  }

  .fb-icon {
    font-size: 1.2rem;
  }

  /* ===== TECH STACK ===== */
  .tech-category {
    margin-bottom: 24px;
  }

  .tech-label {
    font-family: 'Rajdhani', sans-serif;
    font-size: 0.65rem;
    letter-spacing: 0.35em;
    text-transform: uppercase;
    color: rgba(255,215,0,0.5);
    margin-bottom: 10px;
  }

  .tech-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  .tech-chip {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 6px 14px;
    background: rgba(255,255,255,0.03);
    border: 1px solid rgba(255,255,255,0.08);
    border-radius: 2px;
    font-family: 'Rajdhani', sans-serif;
    font-size: 0.8rem;
    font-weight: 600;
    letter-spacing: 0.05em;
    color: var(--white-dim);
    transition: all 0.25s ease;
    cursor: default;
    position: relative;
    overflow: hidden;
  }

  .tech-chip::before {
    content: '';
    position: absolute;
    inset: 0;
    background: linear-gradient(135deg, rgba(255,215,0,0.06), transparent);
    opacity: 0;
    transition: opacity 0.25s;
  }

  .tech-chip:hover {
    color: var(--gold-light);
    border-color: rgba(255,215,0,0.4);
    transform: translateY(-2px);
    box-shadow: 0 4px 16px rgba(255,215,0,0.1);
  }

  .tech-chip:hover::before { opacity: 1; }

  .chip-dot {
    width: 4px; height: 4px;
    border-radius: 50%;
    background: var(--gold);
    opacity: 0.6;
    flex-shrink: 0;
  }

  /* ===== EXPERIENCE ===== */
  .exp-header {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    flex-wrap: wrap;
    gap: 10px;
    margin-bottom: 16px;
  }

  .exp-title {
    font-family: 'Cinzel Decorative', cursive;
    font-size: 1rem;
    font-weight: 700;
    color: var(--gold);
  }

  .exp-date {
    font-family: 'Rajdhani', sans-serif;
    font-size: 0.75rem;
    letter-spacing: 0.2em;
    color: var(--blue-soft);
    padding: 4px 12px;
    border: 1px solid rgba(30,144,255,0.3);
    border-radius: 30px;
  }

  .exp-role {
    font-family: 'Rajdhani', sans-serif;
    font-size: 0.85rem;
    letter-spacing: 0.2em;
    color: rgba(255,215,0,0.6);
    text-transform: uppercase;
    margin-bottom: 12px;
  }

  .exp-list {
    list-style: none;
  }

  .exp-list li {
    display: flex;
    align-items: flex-start;
    gap: 10px;
    font-size: 1rem;
    line-height: 1.6;
    color: var(--white-dim);
    margin-bottom: 8px;
    font-style: italic;
  }

  .exp-list li::before {
    content: '◆';
    color: var(--gold-dark);
    font-size: 0.5rem;
    margin-top: 0.45em;
    flex-shrink: 0;
  }

  /* ===== GITHUB STATS 3D DISPLAY ===== */
  .stats-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 16px;
    margin-top: 8px;
  }

  .stat-box {
    background: rgba(255,255,255,0.02);
    border: 1px solid rgba(255,215,0,0.1);
    border-radius: 2px;
    padding: 20px 16px;
    text-align: center;
    position: relative;
    transition: all 0.3s;
    transform-style: preserve-3d;
    cursor: default;
  }

  .stat-box:hover {
    border-color: rgba(255,215,0,0.4);
    background: rgba(255,215,0,0.04);
    transform: perspective(300px) translateZ(8px);
    box-shadow: 0 8px 30px rgba(0,0,0,0.4), 0 0 20px rgba(255,215,0,0.08);
  }

  .stat-number {
    font-family: 'Cinzel Decorative', cursive;
    font-size: 1.8rem;
    font-weight: 700;
    color: var(--gold);
    display: block;
    line-height: 1;
    margin-bottom: 6px;
  }

  .stat-label {
    font-family: 'Rajdhani', sans-serif;
    font-size: 0.65rem;
    letter-spacing: 0.25em;
    text-transform: uppercase;
    color: rgba(255,255,255,0.35);
  }

  /* ===== 3D CUBE DECORATION ===== */
  .cube-scene {
    position: absolute;
    right: 30px;
    top: 50%;
    transform: translateY(-50%);
    width: 50px;
    height: 50px;
    perspective: 200px;
    pointer-events: none;
  }

  .cube {
    width: 30px;
    height: 30px;
    position: relative;
    transform-style: preserve-3d;
    animation: rotateCube 8s linear infinite;
    margin: 10px auto;
  }

  @keyframes rotateCube {
    from { transform: rotateX(30deg) rotateY(0deg); }
    to   { transform: rotateX(30deg) rotateY(360deg); }
  }

  .cube-face {
    position: absolute;
    width: 30px;
    height: 30px;
    border: 1px solid rgba(255,215,0,0.4);
    background: rgba(255,215,0,0.04);
  }

  .cube-face.front  { transform: translateZ(15px); }
  .cube-face.back   { transform: rotateY(180deg) translateZ(15px); }
  .cube-face.left   { transform: rotateY(-90deg) translateZ(15px); }
  .cube-face.right  { transform: rotateY(90deg) translateZ(15px); }
  .cube-face.top    { transform: rotateX(90deg) translateZ(15px); }
  .cube-face.bottom { transform: rotateX(-90deg) translateZ(15px); }

  /* ===== FOOTER ===== */
  .footer {
    text-align: center;
    padding: 40px 0 20px;
    animation: fadeIn 1s ease both;
    animation-delay: 2s;
    opacity: 0;
  }

  .footer-text {
    font-family: 'Cormorant Garamond', serif;
    font-style: italic;
    font-size: 1.1rem;
    color: rgba(255,215,0,0.5);
  }

  .footer-text span {
    color: var(--gold);
  }

  /* ===== ANIMATIONS ===== */
  @keyframes fadeSlideDown {
    from { opacity: 0; transform: translateY(-20px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  @keyframes fadeSlideUp {
    from { opacity: 0; transform: translateY(30px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  @keyframes fadeIn {
    from { opacity: 0; }
    to   { opacity: 1; }
  }

  /* Staggered card animations */
  .card:nth-child(1) { animation-delay: 1.0s; }
  .card:nth-child(2) { animation-delay: 1.2s; }
  .card:nth-child(3) { animation-delay: 1.4s; }
  .card:nth-child(4) { animation-delay: 1.6s; }
  .card:nth-child(5) { animation-delay: 1.8s; }

  /* ===== 3D TILT ON MOUSE ===== */
  .tilt-card {
    transform-style: preserve-3d;
    will-change: transform;
  }

  /* ===== RESPONSIVE ===== */
  @media (max-width: 600px) {
    .card { padding: 24px 20px; }
    .stats-container { grid-template-columns: repeat(3, 1fr); gap: 8px; }
    .stat-number { font-size: 1.3rem; }
    .cube-scene { display: none; }
  }
</style>
</head>
<body>

<!-- Starfield Canvas -->
<canvas id="canvas-stars"></canvas>

<!-- Floating Particles -->
<div class="particles" id="particles"></div>

<div class="wrapper">

  <!-- ===== HERO ===== -->
  <div class="hero">
    <div class="hero-orb"></div>
    <div class="title-crown">✦ Portfolio — Hồ sơ cá nhân ✦</div>
    <h1 class="title-main">Công Vinh</h1>
    <div class="title-sub">— Kenzy —</div>

    <div class="avatar-ring">
      <div class="avatar-inner">
        <img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExMWEyMGc0Ymx2eTFzYnNwd2did2ZsZGp4czVvbHdmOWJtdGE3NGozMSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/bi6RQ5x3tqoSI/giphy.webp" alt="Corgi waving" />
      </div>
    </div>

    <div class="follow-badge">
      <span class="follow-dot"></span>
      👋 Theo dõi tớ ở bên dưới nhé
      <span class="follow-dot"></span>
    </div>
  </div>

  <!-- Divider -->
  <div class="gold-divider">
    <div class="divider-gem"></div>
    <div class="divider-gem"></div>
    <div class="divider-gem"></div>
  </div>

  <!-- ===== CONTACT ===== -->
  <div class="card tilt-card" id="c1">
    <div class="card-glow"></div>
    <div class="card-corner-tr"></div>
    <div class="card-corner-bl"></div>
    <div class="card-title">📬 Liên hệ</div>
    <a class="contact-link" href="https://www.facebook.com/Vinhne2k4" target="_blank">
      <span class="fb-icon">𝕗</span>
      Facebook — Vinhne2k4
    </a>
  </div>

  <!-- ===== TECH STACK ===== -->
  <div class="card tilt-card" id="c2">
    <div class="card-glow"></div>
    <div class="card-corner-tr"></div>
    <div class="card-corner-bl"></div>

    <div class="cube-scene">
      <div class="cube">
        <div class="cube-face front"></div>
        <div class="cube-face back"></div>
        <div class="cube-face left"></div>
        <div class="cube-face right"></div>
        <div class="cube-face top"></div>
        <div class="cube-face bottom"></div>
      </div>
    </div>

    <div class="card-title">🛠 Tech Stack</div>

    <div class="tech-category">
      <div class="tech-label">Ngôn ngữ lập trình</div>
      <div class="tech-grid">
        <span class="tech-chip"><span class="chip-dot"></span>Python</span>
        <span class="tech-chip"><span class="chip-dot"></span>C</span>
        <span class="tech-chip"><span class="chip-dot"></span>HTML5</span>
        <span class="tech-chip"><span class="chip-dot"></span>CSS3</span>
        <span class="tech-chip"><span class="chip-dot"></span>SQL</span>
        <span class="tech-chip"><span class="chip-dot"></span>Java</span>
        <span class="tech-chip"><span class="chip-dot"></span>JavaScript</span>
        <span class="tech-chip"><span class="chip-dot"></span>Swift</span>
        <span class="tech-chip"><span class="chip-dot"></span>Lua</span>
        <span class="tech-chip"><span class="chip-dot"></span>Flutter</span>
      </div>
    </div>

    <div class="tech-category">
      <div class="tech-label">Cơ sở dữ liệu</div>
      <div class="tech-grid">
        <span class="tech-chip"><span class="chip-dot"></span>MySQL</span>
        <span class="tech-chip"><span class="chip-dot"></span>SQLite</span>
        <span class="tech-chip"><span class="chip-dot"></span>PostgreSQL</span>
        <span class="tech-chip"><span class="chip-dot"></span>MongoDB</span>
      </div>
    </div>

    <div class="tech-category">
      <div class="tech-label">Frameworks & Libraries</div>
      <div class="tech-grid">
        <span class="tech-chip"><span class="chip-dot"></span>Django</span>
        <span class="tech-chip"><span class="chip-dot"></span>Flask</span>
        <span class="tech-chip"><span class="chip-dot"></span>Spark</span>
        <span class="tech-chip"><span class="chip-dot"></span>Selenium</span>
        <span class="tech-chip"><span class="chip-dot"></span>Scrapy</span>
        <span class="tech-chip"><span class="chip-dot"></span>Pandas</span>
        <span class="tech-chip"><span class="chip-dot"></span>NumPy</span>
        <span class="tech-chip"><span class="chip-dot"></span>Matplotlib</span>
        <span class="tech-chip"><span class="chip-dot"></span>Seaborn</span>
      </div>
    </div>

    <div class="tech-category">
      <div class="tech-label">Công cụ phát triển</div>
      <div class="tech-grid">
        <span class="tech-chip"><span class="chip-dot"></span>Git</span>
        <span class="tech-chip"><span class="chip-dot"></span>GitHub</span>
        <span class="tech-chip"><span class="chip-dot"></span>Docker</span>
        <span class="tech-chip"><span class="chip-dot"></span>Anaconda</span>
        <span class="tech-chip"><span class="chip-dot"></span>Jupyter</span>
        <span class="tech-chip"><span class="chip-dot"></span>Google Colab</span>
        <span class="tech-chip"><span class="chip-dot"></span>PyCharm</span>
        <span class="tech-chip"><span class="chip-dot"></span>Spyder</span>
      </div>
    </div>

    <div class="tech-category" style="margin-bottom:0">
      <div class="tech-label">Công cụ văn phòng & OS</div>
      <div class="tech-grid">
        <span class="tech-chip"><span class="chip-dot"></span>MS Word</span>
        <span class="tech-chip"><span class="chip-dot"></span>MS Excel</span>
        <span class="tech-chip"><span class="chip-dot"></span>Canva</span>
        <span class="tech-chip"><span class="chip-dot"></span>Figma</span>
        <span class="tech-chip"><span class="chip-dot"></span>macOS</span>
        <span class="tech-chip"><span class="chip-dot"></span>Linux</span>
        <span class="tech-chip"><span class="chip-dot"></span>Windows</span>
      </div>
    </div>
  </div>

  <!-- ===== EXPERIENCE ===== -->
  <div class="card tilt-card" id="c3">
    <div class="card-glow"></div>
    <div class="card-corner-tr"></div>
    <div class="card-corner-bl"></div>
    <div class="card-title">💼 Kinh nghiệm</div>

    <div class="exp-header">
      <div class="exp-title">Software Developer</div>
      <div class="exp-date">May 2024 — Present</div>
    </div>
    <div class="exp-role">Freelancer</div>
    <ul class="exp-list">
      <li>Làm việc tự do về xử lý và phân tích phần mềm.</li>
      <li>Viết code về các phần mềm cho Android và Desktop.</li>
    </ul>
  </div>

  <!-- ===== STATS ===== -->
  <div class="card tilt-card" id="c4">
    <div class="card-glow"></div>
    <div class="card-corner-tr"></div>
    <div class="card-corner-bl"></div>
    <div class="card-title">📊 GitHub Stats</div>
    <div class="stats-container">
      <div class="stat-box">
        <span class="stat-number" id="s1">10+</span>
        <span class="stat-label">Ngôn ngữ</span>
      </div>
      <div class="stat-box">
        <span class="stat-number" id="s2">9+</span>
        <span class="stat-label">Frameworks</span>
      </div>
      <div class="stat-box">
        <span class="stat-number" id="s3">2024</span>
        <span class="stat-label">Freelance từ</span>
      </div>
    </div>
  </div>

  <!-- Footer -->
  <div class="footer">
    <div class="gold-divider"><div class="divider-gem"></div></div>
    <p class="footer-text">Cảm ơn bạn đã ghé thăm trang của <span>Vinh</span> ✨</p>
  </div>

</div>

<script>
/* ===== STARFIELD ===== */
(function() {
  const canvas = document.getElementById('canvas-stars');
  const ctx = canvas.getContext('2d');
  let W, H, stars = [];

  function resize() {
    W = canvas.width  = window.innerWidth;
    H = canvas.height = window.innerHeight;
  }

  function initStars() {
    stars = [];
    for (let i = 0; i < 180; i++) {
      stars.push({
        x: Math.random() * W,
        y: Math.random() * H,
        r: Math.random() * 1.2 + 0.2,
        a: Math.random(),
        speed: Math.random() * 0.005 + 0.002,
        phase: Math.random() * Math.PI * 2
      });
    }
  }

  function drawStars(t) {
    ctx.clearRect(0, 0, W, H);
    stars.forEach(s => {
      const alpha = 0.2 + 0.8 * (0.5 + 0.5 * Math.sin(t * s.speed + s.phase));
      ctx.beginPath();
      ctx.arc(s.x, s.y, s.r, 0, Math.PI * 2);
      ctx.fillStyle = `rgba(255,235,180,${alpha})`;
      ctx.fill();
    });
    requestAnimationFrame(drawStars);
  }

  resize();
  initStars();
  window.addEventListener('resize', () => { resize(); initStars(); });
  requestAnimationFrame(drawStars);
})();

/* ===== PARTICLES ===== */
(function() {
  const container = document.getElementById('particles');
  const colors = ['rgba(255,215,0,0.6)', 'rgba(30,144,255,0.5)', 'rgba(255,140,66,0.5)'];

  function spawn() {
    const p = document.createElement('div');
    p.className = 'particle';
    const size = Math.random() * 3 + 1;
    p.style.cssText = `
      left: ${Math.random() * 100}%;
      width: ${size}px;
      height: ${size}px;
      background: ${colors[Math.floor(Math.random() * colors.length)]};
      animation-duration: ${Math.random() * 12 + 8}s;
      animation-delay: ${Math.random() * 5}s;
    `;
    container.appendChild(p);
    setTimeout(() => p.remove(), 20000);
  }

  for (let i = 0; i < 20; i++) spawn();
  setInterval(spawn, 800);
})();

/* ===== 3D TILT ON HOVER ===== */
document.querySelectorAll('.tilt-card').forEach(card => {
  card.addEventListener('mousemove', e => {
    const r = card.getBoundingClientRect();
    const cx = r.left + r.width / 2;
    const cy = r.top + r.height / 2;
    const dx = (e.clientX - cx) / (r.width / 2);
    const dy = (e.clientY - cy) / (r.height / 2);
    const rotX = -dy * 4;
    const rotY =  dx * 4;
    card.style.transform = `perspective(900px) rotateX(${rotX}deg) rotateY(${rotY}deg) translateY(-4px)`;
  });

  card.addEventListener('mouseleave', () => {
    card.style.transform = 'perspective(900px) rotateX(0deg) rotateY(0deg) translateY(0px)';
    card.style.transition = 'transform 0.6s ease';
  });

  card.addEventListener('mouseenter', () => {
    card.style.transition = 'transform 0.1s ease';
  });
});
</script>
</body>
</html>
