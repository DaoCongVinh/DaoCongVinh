<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=slice&color=gradient&height=280&section=header&text=Công%20Vinh%20(Kenzy)&fontSize=80&fontColor=fff&animation=twinkling&fontAlignY=38&desc=Full-Stack%20Developer%20%E2%80%A2%20Freelancer%20%E2%9C%A8&descAlign=62&descAlignY=55&descSize=30" alt="header neon slice" />
</div>

<br><br>

<!-- Cosmic Container with subtle stars -->
<div style="position: relative; overflow: hidden; margin: 60px 0; perspective: 1800px;">
  <div class="cosmic-bg" style="
    position: absolute;
    inset: 0;
    background: radial-gradient(circle at 30% 20%, #0a0015, #000814 100%);
    pointer-events: none;
    z-index: -1;
  "></div>

  <!-- Main 3D Floating Card -->
  <div id="kenzy-card" class="kenzy-card" style="
    background: linear-gradient(145deg, #12001f, #1e003a, #2c0057);
    border: 1px solid rgba(180, 100, 255, 0.4);
    border-radius: 36px;
    padding: 70px 80px;
    max-width: 980px;
    margin: 0 auto;
    box-shadow: 0 50px 160px rgba(0,0,0,0.9),
                inset 0 0 80px rgba(180,100,255,0.18);
    transform-style: preserve-3d;
    transition: transform 0.6s cubic-bezier(0.23,1,0.32,1), box-shadow 0.6s;
    position: relative;
    overflow: hidden;
  ">

    <!-- Mouse-follow Glow Spotlight -->
    <div class="spotlight" style="
      position: absolute;
      inset: -200%;
      background: radial-gradient(circle at var(--mx,50%) var(--my,50%), rgba(180,100,255,0.32) 0%, transparent 70%);
      pointer-events: none;
      transition: all 0.35s ease;
      opacity: 0.9;
    "></div>

    <h1 style="
      font-size: 5rem;
      margin: 0 0 20px;
      background: linear-gradient(90deg, #d8b4fe, #c084fc, #ec4899, #d8b4fe);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      font-weight: 900;
      letter-spacing: -2px;
      text-shadow: 0 0 70px rgba(192,132,252,0.8);
      animation: neon-pulse 6s ease-in-out infinite alternate;
    ">✨ Công Vinh (Kenzy) ✨</h1>

    <h2 style="
      font-size: 2.8rem;
      color: #b7c3ff;
      margin: 0 0 50px;
      font-weight: 500;
      text-shadow: 0 0 25px rgba(183,195,255,0.5);
    ">Xin chào! Tớ là Vinh đây 🚀</h2>

    <img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExMWEyMGc0Ymx2eTFzYnNwd2did2ZsZGp4czVvbHdmOWJtdGE3NGozMSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/bi6RQ5x3tqoSI/giphy.webp"
         width="200" alt="Corgi waving happily"
         style="border-radius: 50%; box-shadow: 0 0 90px rgba(192,132,252,0.65); margin: 40px 0; transform: translateZ(40px);" />

    <p style="font-size: 1.5rem; color: #e0e7ff; max-width: 800px; line-height: 1.9; margin: 40px auto; text-shadow: 0 0 15px rgba(224,231,255,0.4);">
      Đam mê code sạch • Xây dựng sản phẩm đẹp & mạnh mẽ<br>
      Python • Flutter • Web • Automation • Data • Freelance
    </p>

    <p style="margin: 40px 0;">
      <img src="https://img.shields.io/github/followers/Daocongvinh?label=Follow%20tớ%20nhé&style=social&logo=github&color=c084fc" alt="followers badge" />
    </p>

  </div>
</div>

<!-- 3D Tilt + Spotlight JS -->
<script>
document.addEventListener('DOMContentLoaded', () => {
  const card = document.getElementById('kenzy-card');
  if (!card) return;

  card.addEventListener('mousemove', e => {
    const rect = card.getBoundingClientRect();
    const x = e.clientX - rect.left;
    const y = e.clientY - rect.top;

    const cx = rect.width / 2;
    const cy = rect.height / 2;

    const rx = (y - cy) / 22;
    const ry = (cx - x) / 22;

    card.style.transform = `rotateX(${rx}deg) rotateY(${ry}deg) scale(1.03)`;
    card.querySelector('.spotlight').style.setProperty('--mx', `${x}px`);
    card.querySelector('.spotlight').style.setProperty('--my', `${y}px`);
  });

  card.addEventListener('mouseleave', () => {
    card.style.transform = 'rotateX(0deg) rotateY(0deg) scale(1)';
  });
});
</script>

<style>
@keyframes neon-pulse {
  from { text-shadow: 0 0 40px rgba(192,132,252,0.7), 0 0 80px rgba(236,72,153,0.5); }
  to   { text-shadow: 0 0 100px rgba(192,132,252,1), 0 0 160px rgba(236,72,153,0.8); }
}
.kenzy-card:hover {
  box-shadow: 0 80px 200px rgba(0,0,0,1),
              inset 0 0 100px rgba(192,132,252,0.3);
}
.cosmic-bg::before {
  content: '';
  position: absolute;
  inset: 0;
  background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="80" height="80"><circle cx="4" cy="4" r="1.5" fill="white" opacity="0.6"/></svg>') repeat;
  animation: star-drift 180s linear infinite;
  opacity: 0.12;
}
@keyframes star-drift {
  0%   { transform: translate(0,0); }
  100% { transform: translate(-120px, -120px); }
}
</style>

<br><br>

<h3 align="center" style="font-size: 3rem; color: #d8b4fe; text-shadow: 0 0 40px #d8b4fe88; margin: 80px 0 50px;">
  THEO DÕI TỚ Ở ĐÂY NHÉ 👇🌌
</h3>

<div align="center" style="margin: 60px 0;">
  <a href="https://www.facebook.com/Vinhne2k4" target="_blank">
    <img src="https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white" height="56" alt="Facebook" />
  </a>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <a href="https://github.com/Daocongvinh" target="_blank">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" height="56" alt="GitHub" />
  </a>
</div>

<hr style="border: none; height: 4px; background: linear-gradient(90deg, transparent, #c084fc, #ec4899, #c084fc, transparent); margin: 90px 0;" />

<h3 align="center" style="font-size: 3rem; color: #c084fc; text-shadow: 0 0 45px #c084fc99; margin-bottom: 60px;">
  🛠 Tech Stack
</h3>

<div align="center" style="display: flex; flex-wrap: wrap; gap: 20px; justify-content: center; max-width: 1200px; margin: 0 auto 90px;">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" height="50"/>
  <img src="https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white" height="50"/>
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" height="50"/>
  <img src="https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white" height="50"/>
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" height="50"/>
  <img src="https://img.shields.io/badge/PostgreSQL-336791?style=for-the-badge&logo=postgresql&logoColor=white" height="50"/>
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white" height="50"/>
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" height="50"/>
</div>

<!-- Experience Block -->
<div align="center" style="
  background: linear-gradient(145deg, #180028, #280042);
  border-radius: 32px;
  padding: 70px 60px;
  margin: 80px auto;
  max-width: 980px;
  border: 1px solid rgba(192,132,252,0.35);
  box-shadow: 0 50px 120px rgba(0,0,0,0.9);
">
  <h3 style="color: #ec4899; font-size: 2.8rem; margin-bottom: 35px;">💼 Experience</h3>
  <p style="font-size: 1.6rem; color: #e0d7ff; line-height: 2;">
    <b>Software Developer | Freelancer</b><br>
    May 2024 — Present<br><br>
    • Xây dựng app Desktop & Android chất lượng cao<br>
    • Automation, Scraping, Data Pipeline mạnh mẽ<br>
    • Giải pháp phần mềm cá nhân hóa cho khách hàng
  </p>
</div>

<br><br>

<div align="center">
  <img src="https://media.giphy.com/media/3o7aD4cy9buCWf4fdG/giphy.gif" width="420" alt="coding in neon style"
       style="border-radius: 28px; box-shadow: 0 0 100px rgba(192,132,252,0.6);" />
</div>

<br><br><br>

<p align="center" style="font-size: 2.4rem; color: #d8b4fe; text-shadow: 0 0 60px #d8b4feaa; margin: 120px 0;">
  <b>Cảm ơn bạn đã ghé thăm profile của tớ! 💜<br>
  Cùng nhau tạo ra những thứ thật đỉnh cao nhé ✨</b>
</p>

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=slice&color=gradient&height=180&section=footer&text=Kenzy%20%E2%9A%A1&fontSize=60&fontColor=fff&animation=twinkling" alt="footer neon" />
</div>
