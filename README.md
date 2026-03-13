<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=gradient&height=220&section=header&text=Công%20Vinh%20(Kenzy)&fontSize=70&fontColor=ffffff&animation=twinkling&fontAlignY=45&desc=Full-Stack%20Developer%20%E2%80%A2%20Freelancer&descAlign=62&descAlignY=70&descSize=26" alt="header" />
</div>

<br><br>

<!-- Cosmic background particles -->
<div style="position: relative; overflow: hidden; margin: 40px 0;">
  <div class="stars" style="
    position: absolute;
    inset: 0;
    background: radial-gradient(circle at 20% 30%, #0f0c29 0%, #000 100%);
    pointer-events: none;
  "></div>

  <!-- Main 3D Card -->
  <div id="card" class="card-3d" style="
    background: linear-gradient(135deg, #0d001a, #1a0033, #2a004d);
    border: 1px solid rgba(120, 100, 255, 0.3);
    border-radius: 28px;
    padding: 50px 60px;
    max-width: 920px;
    margin: 0 auto;
    box-shadow: 0 40px 120px rgba(0,0,0,0.9),
                inset 0 0 60px rgba(120,100,255,0.12);
    transform-style: preserve-3d;
    transition: transform 0.4s ease-out, box-shadow 0.4s;
    position: relative;
    overflow: hidden;
  ">

    <!-- Glow spotlight follow mouse -->
    <div class="glow" style="
      position: absolute;
      inset: -100%;
      background: radial-gradient(circle at var(--mx, 50%) var(--my, 50%), rgba(180,140,255,0.22) 0%, transparent 60%);
      pointer-events: none;
      transition: all 0.25s;
      opacity: 0.8;
    "></div>

    <h1 style="
      font-size: 4.2rem;
      margin: 0;
      background: linear-gradient(90deg, #c084fc, #8b5cf6, #ec4899, #c084fc);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      font-weight: 900;
      letter-spacing: -1px;
      text-shadow: 0 0 50px rgba(168,85,247,0.7);
      animation: neon 4s ease-in-out infinite alternate;
    ">✨ Công Vinh (Kenzy) ✨</h1>

    <h2 style="
      font-size: 2.4rem;
      color: #a5b4fc;
      margin: 20px 0 40px;
      font-weight: 500;
    ">Tớ là Vinh đây! 🚀</h2>

    <img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExMWEyMGc0Ymx2eTFzYnNwd2did2ZsZGp4czVvbHdmOWJtdGE3NGozMSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/bi6RQ5x3tqoSI/giphy.webp" 
         width="160" alt="Corgi" 
         style="border-radius: 50%; box-shadow: 0 0 60px rgba(168,85,247,0.5); margin: 25px 0;" />

    <p style="font-size: 1.35rem; color: #c7d2fe; max-width: 720px; line-height: 1.8; margin: 30px auto;">
      Đam mê code đẹp • Xây dựng sản phẩm mạnh mẽ • Python • Mobile • Web • Automation • Data Pipeline
    </p>

    <p>
      <img src="https://img.shields.io/github/followers/Daocongvinh?label=Follow&style=social&logo=github&color=8b5cf6" alt="followers" />
    </p>

  </div>
</div>

<!-- JavaScript cho tilt 3D + glow follow -->
<script>
document.addEventListener('DOMContentLoaded', () => {
  const card = document.getElementById('card');
  if (!card) return;

  card.addEventListener('mousemove', (e) => {
    const rect = card.getBoundingClientRect();
    const x = e.clientX - rect.left;
    const y = e.clientY - rect.top;
    
    const centerX = rect.width / 2;
    const centerY = rect.height / 2;
    
    const rotateX = (y - centerY) / 18;
    const rotateY = (centerX - x) / 18;
    
    card.style.transform = `perspective(1400px) rotateX(${rotateX}deg) rotateY(${rotateY}deg) scale(1.02)`;
    card.querySelector('.glow').style.setProperty('--mx', `${x}px`);
    card.querySelector('.glow').style.setProperty('--my', `${y}px`);
  });

  card.addEventListener('mouseleave', () => {
    card.style.transform = 'perspective(1400px) rotateX(0deg) rotateY(0deg) scale(1)';
  });
});
</script>

<style>
@keyframes neon {
  from { text-shadow: 0 0 30px rgba(168,85,247,0.6); }
  to   { text-shadow: 0 0 80px rgba(168,85,247,0.9), 0 0 120px rgba(236,72,153,0.6); }
}
.card-3d:hover {
  box-shadow: 0 60px 160px rgba(0,0,0,0.95),
              inset 0 0 80px rgba(168,85,247,0.2);
}
.stars::before {
  content: '';
  position: absolute;
  inset: 0;
  background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100"><circle cx="10" cy="10" r="1" fill="white" opacity="0.7"/></svg>') repeat;
  animation: drift 120s linear infinite;
  opacity: 0.15;
}
@keyframes drift { 0% { transform: translate(0,0); } 100% { transform: translate(-100px, -100px); } }
</style>

<br>

<h3 align="center" style="font-size: 2.5rem; color: #c084fc; text-shadow: 0 0 30px #c084fc55; margin: 60px 0 30px;">
  THEO DÕI TỚ Ở ĐÂY NHÉ 👇
</h3>

<div align="center" style="margin: 40px 0;">
  <a href="https://www.facebook.com/Vinhne2k4">
    <img src="https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white" height="48"/>
  </a>
  &nbsp;&nbsp;&nbsp;&nbsp;
  <a href="https://github.com/Daocongvinh">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" height="48"/>
  </a>
</div>

<hr style="border: 0; height: 3px; background: linear-gradient(90deg, transparent, #8b5cf6, #ec4899, #8b5cf6, transparent); margin: 70px 0;" />

<h3 align="center" style="font-size: 2.6rem; color: #a78bfa; margin-bottom: 40px; text-shadow: 0 0 35px #a78bfa66;">
  🛠 Tech Stack
</h3>

<div align="center" style="display: flex; flex-wrap: wrap; gap: 16px; justify-content: center; max-width: 1100px; margin: 0 auto 60px;">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" height="42"/>
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" height="42"/>
  <img src="https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white" height="42"/>
  <img src="https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white" height="42"/>
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" height="42"/>
  <img src="https://img.shields.io/badge/PostgreSQL-336791?style=for-the-badge&logo=postgresql&logoColor=white" height="42"/>
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white" height="42"/>
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" height="42"/>
</div>

<!-- Experience Section -->
<div align="center" style="
  background: linear-gradient(135deg, #1e0033, #2e004d);
  border-radius: 24px;
  padding: 50px 40px;
  margin: 60px auto;
  max-width: 900px;
  border: 1px solid rgba(168,85,247,0.25);
  box-shadow: 0 30px 80px rgba(0,0,0,0.8);
">
  <h3 style="color: #ec4899; font-size: 2.4rem; margin-bottom: 24px;">💼 Experience</h3>
  <p style="font-size: 1.45rem; color: #ddd6fe; line-height: 1.9;">
    <b>Software Developer | Freelancer</b><br>
    May 2024 — Present<br><br>
    • Phát triển ứng dụng Desktop & Android<br>
    • Automation, Scraping, Data Processing Pipeline<br>
    • Xây dựng giải pháp cá nhân hóa cho khách hàng
  </p>
</div>

<br>

<div align="center">
  <img src="https://media.giphy.com/media/3o7aD4cy9buCWf4fdG/giphy.gif" width="380" alt="coding" 
       style="border-radius: 20px; box-shadow: 0 0 70px rgba(168,85,247,0.45);"/>
</div>

<br><br>

<p align="center" style="font-size: 2rem; color: #c084fc; text-shadow: 0 0 40px #c084fc88; margin: 80px 0;">
  <b>Cảm ơn bạn đã ghé thăm! 💜<br>
  Let's create something epic together ✨</b>
</p>

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=slice&color=gradient&height=140&section=footer&text=Kenzy%20%E2%9C%A8&fontSize=50&fontColor=fff&animation=twinkling" alt="footer" />
</div>
