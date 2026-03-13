<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=280&section=header&text=Công%20Vinh%20(Kenzy)&fontSize=80&fontColor=fff&animation=twinkling&fontAlignY=38&desc=Tớ%20là%20Vinh%20đây!%20✨&descAlign=62&descAlignY=55&descSize=28" alt="header" />
</div>

<br>

<!-- 3D Floating Main Card -->
<div align="center">
  <div style="
    perspective: 1800px;
    margin: 40px 0;
  ">
    <div class="card-3d" style="
      background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
      border-radius: 24px;
      padding: 50px 60px;
      max-width: 900px;
      box-shadow: 0 30px 90px rgba(0,0,0,0.8),
                  inset 0 0 40px rgba(100, 200, 255, 0.15);
      border: 1px solid rgba(100, 200, 255, 0.25);
      transform-style: preserve-3d;
      transition: all 0.6s cubic-bezier(0.23, 1, 0.32, 1);
      position: relative;
      overflow: hidden;
    "
    onmousemove="handleMouseMove(event, this)"
    onmouseleave="handleMouseLeave(this)">
      
      <!-- Glow overlay -->
      <div style="
        position: absolute;
        inset: 0;
        background: radial-gradient(circle at var(--x, 50%) var(--y, 50%), rgba(100,200,255,0.18) 0%, transparent 60%);
        pointer-events: none;
        transition: opacity 0.4s;
        opacity: 0.7;
      "></div>

      <h1 style="
        font-size: 3.8rem;
        margin: 0;
        background: linear-gradient(90deg, #00f2ff, #a78bfa, #ff79cd);
        -webkit-background-clip: text;
        background-clip: text;
        color: transparent;
        font-weight: 900;
        text-shadow: 0 0 40px rgba(167, 139, 250, 0.6);
        animation: glow 3s ease-in-out infinite alternate;
      ">✨ Công Vinh (Kenzy) ✨</h1>

      <h2 style="
        font-size: 2.1rem;
        color: #a5d8ff;
        margin: 16px 0 32px;
        font-weight: 500;
        letter-spacing: 1.5px;
      ">Tớ là Vinh đây! 🚀</h2>

      <img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExMWEyMGc0Ymx2eTFzYnNwd2did2ZsZGp4czVvbHdmOWJtdGE3NGozMSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/bi6RQ5x3tqoSI/giphy.webp" width="180" alt="Corgi waving" style="border-radius:50%; box-shadow: 0 0 40px rgba(100,200,255,0.5); margin: 20px 0;" />

      <p style="font-size: 1.3rem; color: #c3daff; max-width: 680px; line-height: 1.7; margin: 30px auto;">
        Full-stack developer • Freelancer • Đam mê xây dựng sản phẩm đẹp và mạnh mẽ<br>
        Python • Mobile • Web • Automation • Data
      </p>

      <p>
        <img src="https://img.shields.io/github/followers/Daocongvinh?label=Follow&style=social&logo=github&color=00f2ff" alt="followers" />
      </p>

    </div>
  </div>
</div>

<!-- JavaScript cho hiệu ứng 3D tilt -->
<script>
function handleMouseMove(e, el) {
  const rect = el.getBoundingClientRect();
  const x = e.clientX - rect.left;
  const y = e.clientY - rect.top;
  const centerX = rect.width / 2;
  const centerY = rect.height / 2;
  
  const rotateX = (y - centerY) / 12;
  const rotateY = (centerX - x) / 12;
  
  el.style.transform = `rotateX(${rotateX}deg) rotateY(${rotateY}deg) scale(1.03)`;
  el.style.setProperty('--x', `${x}px`);
  el.style.setProperty('--y', `${y}px`);
}

function handleMouseLeave(el) {
  el.style.transform = 'rotateX(0deg) rotateY(0deg) scale(1)';
}
</script>

<style>
@keyframes glow {
  from { text-shadow: 0 0 20px rgba(167,139,250,0.5); }
  to   { text-shadow: 0 0 60px rgba(167,139,250,0.9), 0 0 100px rgba(0,242,255,0.7); }
}
.card-3d:hover {
  box-shadow: 0 50px 140px rgba(0,0,0,0.9),
              inset 0 0 60px rgba(100,200,255,0.25);
}
</style>

<br>

<h3 align="center" style="color:#00f2ff; font-size: 2.2rem; text-shadow: 0 0 20px #00f2ff44;">THEO DÕI TỚ Ở ĐÂY NHÉ 👇✨</h3>

<div align="center" style="margin: 40px 0;">
  <a href="https://www.facebook.com/Vinhne2k4" target="_blank">
    <img src="https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white&labelColor=0a0a0a" alt="Facebook" height="40"/>
  </a>
  &nbsp;&nbsp;&nbsp;
  <a href="https://github.com/Daocongvinh" target="_blank">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white&labelColor=0a0a0a" alt="GitHub" height="40"/>
  </a>
</div>

<hr style="border: none; height: 2px; background: linear-gradient(90deg, transparent, #a78bfa, #00f2ff, #a78bfa, transparent); margin: 60px 0;" />

<!-- Tech Stack với glowing 3D badges -->
<h3 align="center" style="color:#a78bfa; font-size: 2.4rem; margin-bottom: 30px; text-shadow: 0 0 25px #a78bfa66;">🛠 Tech Stack</h3>

<div align="center" style="display: flex; flex-wrap: wrap; gap: 14px; justify-content: center; max-width: 1100px; margin: 0 auto;">
  <!-- Ngôn ngữ -->
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white&color=3776AB" height="38"/>
  <img src="https://img.shields.io/badge/C-A8B9CC?style=flat&logo=c&logoColor=white&color=A8B9CC" height="38"/>
  <img src="https://img.shields.io/badge/Java-007396?style=flat&logo=java&logoColor=white&color=007396" height="38"/>
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black&color=F7DF1E" height="38"/>
  <img src="https://img.shields.io/badge/Flutter-02569B?style=flat&logo=flutter&logoColor=white&color=02569B" height="38"/>
  
  <!-- DB -->
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white&color=4479A1" height="38"/>
  <img src="https://img.shields.io/badge/PostgreSQL-336791?style=flat&logo=postgresql&logoColor=white&color=336791" height="38"/>
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white&color=47A248" height="38"/>
  
  <!-- Framework -->
  <img src="https://img.shields.io/badge/Django-092E20?style=flat&logo=django&logoColor=white&color=092E20" height="38"/>
  <img src="https://img.shields.io/badge/Flask-000000?style=flat&logo=flask&logoColor=white&color=000000" height="38"/>
  <img src="https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white&color=150458" height="38"/>
</div>

<br><br>

<!-- Experience -->
<div align="center" style="
  background: linear-gradient(135deg, #1a1033, #2a1a5a);
  border-radius: 20px;
  padding: 40px;
  margin: 50px auto;
  max-width: 900px;
  border: 1px solid rgba(167,139,250,0.3);
  box-shadow: 0 20px 60px rgba(0,0,0,0.7);
">
  <h3 style="color:#ff79cd; font-size: 2.2rem; margin-bottom: 20px;">💼 Experience</h3>
  <p style="font-size: 1.4rem; color: #d1c4ff; line-height: 1.8;">
    <b>Software Developer | Freelancer</b><br>
    May 2024 — Present<br><br>
    • Xây dựng phần mềm Desktop & Android<br>
    • Automation, Web Scraping, Data Pipeline<br>
    • Tư vấn & phát triển sản phẩm cá nhân hóa
  </p>
</div>

<br>

<div align="center">
  <img src="https://media.giphy.com/media/3o7aD4cy9buCWf4fdG/giphy.gif" width="360" alt="coding" style="border-radius:16px; box-shadow: 0 0 50px rgba(100,200,255,0.4);"/>
</div>

<br><br>

<p align="center" style="font-size: 1.8rem; color: #00f2ff; text-shadow: 0 0 30px #00f2ff88; margin: 60px 0;">
  <b>Cảm ơn bạn đã ghé thăm profile của tớ! 💙</b><br>
  Let's build something amazing together ✨
</p>

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=slice&color=gradient&height=120&section=footer&%text=Kenzy%20%E2%9C%A8&fontSize=40&fontColor=fff&animation=twinkling" alt="footer" />
</div>
