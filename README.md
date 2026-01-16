<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Portfolio - I Gde Arkana Satwikaa</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>
*{margin:0;padding:0;box-sizing:border-box;}

:root{
 --primary:#4f7cff;
 --accent:#ff6b6b;
 --bg1:#f5f7ff;
 --bg2:#eef1ff;
 --cardGlass:rgba(255,255,255,0.75);
 --text:#1e1e2f;
}

body{
 font-family:Poppins,sans-serif;
 background:linear-gradient(120deg,var(--bg1),var(--bg2));
 color:var(--text);
 scroll-behavior:smooth;
 overflow-x:hidden;
}

/* ==== Floating Glow Background ==== */
body::before, body::after{
 content:"";
 position:fixed;
 width:300px;
 height:300px;
 border-radius:50%;
 filter:blur(90px);
 z-index:-1;
}
body::before{
 background:#4f7cff;
 top:-80px;
 left:-80px;
}
body::after{
 background:#ff6b6b;
 bottom:-80px;
 right:-80px;
}

/* ==== Navbar ==== */
.navbar{
 position:fixed;
 top:0;
 width:100%;
 background:rgba(255,255,255,0.7);
 backdrop-filter:blur(12px);
 box-shadow:0 4px 20px rgba(0,0,0,0.08);
 z-index:1000;
}
.nav-container{
 max-width:1200px;
 margin:auto;
 padding:1rem 2rem;
 display:flex;
 justify-content:space-between;
 align-items:center;
}
.nav-logo{
 font-size:1.6rem;
 font-weight:700;
 color:var(--primary);
 text-decoration:none;
}
.nav-menu{
 display:flex;
 gap:2rem;
 list-style:none;
}
.nav-link{
 text-decoration:none;
 color:var(--text);
 font-weight:500;
}
.nav-link:hover{color:var(--primary);}

/* ==== Hero ==== */
.hero{
 min-height:100vh;
 display:flex;
 justify-content:center;
 align-items:center;
 text-align:center;
 padding-top:80px;
 background:linear-gradient(135deg,#4f7cff,#6a5bff);
 color:white;
}
.hero h1{
 font-size:3.5rem;
 font-weight:700;
 text-shadow:0 0 20px rgba(255,255,255,0.4);
}
.hero p{
 font-size:1.2rem;
 opacity:0.9;
}

/* ==== Section ==== */
section{
 padding:4rem 1.5rem;
}
.container{
 max-width:1200px;
 margin:auto;
}
.section-title{
 text-align:center;
 font-size:2.5rem;
 margin-bottom:2.5rem;
}

/* ==== About ==== */
.about-content{
 display:grid;
 grid-template-columns:1fr 2fr;
 gap:2rem;
 align-items:center;
}
.profile-photo{
 width:230px;
 height:230px;
 border-radius:50%;
 object-fit:cover;
 margin:auto;
 border:6px solid white;
 box-shadow:0 0 25px rgba(79,124,255,0.8);
}

/* ==== Glass Card ==== */
.card{
 background:var(--cardGlass);
 backdrop-filter:blur(10px);
 padding:1.5rem;
 border-radius:18px;
 box-shadow:0 8px 25px rgba(0,0,0,0.08);
 transition:0.3s;
 text-align:center;
}
.card:hover{
 transform:translateY(-10px);
 box-shadow:0 15px 35px rgba(79,124,255,0.3);
}

/* ==== Grid ==== */
.grid{
 display:grid;
 grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
 gap:1.5rem;
}

/* ==== Skill Bar ==== */
.bar{
 background:#ddd;
 height:8px;
 border-radius:10px;
 margin-top:8px;
 overflow:hidden;
}
.bar-fill{
 height:100%;
 border-radius:10px;
 background:linear-gradient(90deg,var(--primary),var(--accent));
}

/* ==== Certificate Images ==== */
.cert-img{
 width:100%;
 border-radius:12px;
 margin-bottom:10px;
 transition:0.3s;
}
.cert-img:hover{
 transform:scale(1.03);
}

/* ==== Project Badge ==== */
.project-tag{
 display:inline-block;
 padding:4px 10px;
 border-radius:20px;
 background:linear-gradient(90deg,var(--primary),var(--accent));
 color:white;
 font-size:0.75rem;
 margin-top:10px;
}

/* ==== Contact ==== */
.contact-grid{
 display:grid;
 grid-template-columns:1fr 1fr;
 gap:2rem;
}

/* ==== Footer ==== */
footer{
 text-align:center;
 padding:2rem;
 background:rgba(255,255,255,0.6);
 backdrop-filter:blur(10px);
}

/* ==== Scroll Reveal Animation ==== */
.reveal{
 opacity:0;
 transform:translateY(50px);
 transition:1s;
}
.reveal.active{
 opacity:1;
 transform:translateY(0);
}

/* ==== Certificate Section Style ==== */
#certificates {
  padding: 80px 20px;
  text-align: center;
}
.certificate-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit,minmax(280px,1fr));
  gap: 30px;
  margin-top: 40px;
}
.certificate-card {
  background: linear-gradient(135deg,#0f172a,#1e293b);
  border-radius: 20px;
  padding: 25px;
  color: white;
  box-shadow: 0 0 20px rgba(0,255,255,0.15);
  transition: transform 0.4s ease, box-shadow 0.4s ease;
}
.certificate-card:hover {
  transform: translateY(-10px) scale(1.02);
  box-shadow: 0 0 35px rgba(0,255,255,0.35);
}
.certificate-content h3 {
  color: #38bdf8;
  margin-bottom: 15px;
}
.btn-view {
  display: inline-block;
  margin-top: 15px;
  padding: 10px 20px;
  background: #38bdf8;
  color: #0f172a;
  border-radius: 8px;
  text-decoration: none;
  font-weight: bold;
}
.btn-view:hover {
  background: #0ea5e9;
}

/* ==== Responsive ==== */
@media(max-width:768px){
 .about-content{grid-template-columns:1fr;}
 .contact-grid{grid-template-columns:1fr;}
 .hero h1{font-size:2.3rem;}
 .nav-menu{display:none;}
}
</style>
</head>

<body>

<!-- NAVBAR -->
<nav class="navbar">
 <div class="nav-container">
  <a class="nav-logo" href="#">AwanLangit</a>
  <ul class="nav-menu">
   <li><a href="#home" class="nav-link">Home</a></li>
   <li><a href="#about" class="nav-link">About</a></li>
   <li><a href="#skills" class="nav-link">Skills</a></li>
   <li><a href="#projects" class="nav-link">Projects</a></li>
   <li><a href="#certificates" class="nav-link">Certificates</a></li>
   <li><a href="#contact" class="nav-link">Contact</a></li>
  </ul>
 </div>
</nav>

<!-- HERO -->
<section class="hero" id="home">
 <div class="reveal">
  <h1>I Gde Arkana Satwikaa</h1>
  <p>Cybersecurity & IoT Developer</p>
 </div>
</section>

<!-- ABOUT -->
<section id="about">
 <div class="container reveal">
  <h2 class="section-title">Tentang Saya</h2>
  <div class="about-content">
   <img src="arkana.jpg.jpeg" class="profile-photo">
   <div class="card">
    <p>Mahasiswa Cybersecurity & IoT dengan pengalaman kompetisi internasional di China. 
       Fokus pada keamanan sistem, pengembangan IoT, dan pengujian penetrasi.</p>
   </div>
  </div>
 </div>
</section>

<!-- SKILLS -->
<section id="skills">
 <div class="container reveal">
  <h2 class="section-title">Skills</h2>
  <div class="grid">
   <div class="card">Cybersecurity
    <div class="bar"><div class="bar-fill" style="width:85%"></div></div>
   </div>
   <div class="card">IoT Development
    <div class="bar"><div class="bar-fill" style="width:80%"></div></div>
   </div>
   <div class="card">Programming
    <div class="bar"><div class="bar-fill" style="width:75%"></div></div>
   </div>
  </div>
 </div>
</section>

<!-- PROJECTS -->
<section id="projects">
 <div class="container reveal">
  <h2 class="section-title">Projects & Achievements</h2>
  <div class="grid">
   <div class="card">
    <h3>Cybersecurity Competition - China</h3>
    <p>Finalist kompetisi keamanan siber internasional.</p>
    <span class="project-tag">International</span>
   </div>
   <div class="card">
    <h3>IoT Innovation Contest - China</h3>
    <p>Pengembangan sistem IoT untuk smart monitoring.</p>
    <span class="project-tag">International</span>
   </div>
   <div class="card">
    <h3>Debate Champion - Province</h3>
    <p>Juara debat tingkat provinsi.</p>
    <span class="project-tag">Achievement</span>
   </div>
  </div>
 </div>
</section>

<!-- ===== CERTIFICATE SECTION ===== -->
<section id="certificates">
  <h2 data-aos="fade-up">Certificates & Training</h2>
  <p data-aos="fade-up" data-aos-delay="100">
    Berikut adalah pelatihan dan sertifikasi yang telah saya selesaikan.
  </p>
  <div class="certificate-grid">
    <!-- Certificate Card -->
    <div class="certificate-card" data-aos="zoom-in">
      <div class="certificate-content">
        <h3>Introduction to Cyber Security and Career Awareness</h3>
        <p><strong>Program:</strong> Micro Skill – Digital Talent Scholarship 2025</p>
        <p><strong>Penyelenggara:</strong> Pusat Pengembangan Literasi Digital (Komdigi)</p>
        <p><strong>Durasi:</strong> 1 Jam Pelatihan</p>
        <p><strong>Tanggal:</strong> 7 November 2025</p>
        <p><strong>Nomor Sertifikat:</strong><br>
           2299734850-22383/MS/BLSDM.Komdigi/2025
        </p>
        <a href="sertifikat-cybersecurity.pdf" class="btn-view" target="_blank">
          Lihat Sertifikat PDF
        </a>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
 <div class="container reveal">
  <h2 class="section-title">Contact</h2>
  <div class="contact-grid">
   <div class="card">
    <p>📧 kanzzarkana@gmail.com</p>
    <p>📱 +62 85136117399</p>
    <p>📍 Bandar Lampung</p>
   </div>
   <div class="card">
    <form onsubmit="sendMessage(event)">
     <input type="text" placeholder="Nama" required style="width:100%;padding:10px;border-radius:8px;border:none;margin-bottom:10px;">
     <input type="email" placeholder="Email" required style="width:100%;padding:10px;border-radius:8px;border:none;margin-bottom:10px;">
     <textarea placeholder="Pesan" required style="width:100%;padding:10px;border-radius:8px;border:none;margin-bottom:10px;"></textarea>
     <button style="padding:8px 20px;border:none;border-radius:20px;background:var(--primary);color:white;cursor:pointer;">Kirim</button>
    </form>
   </div>
  </div>
 </div>
</section>

<footer>
 © 2026 I Gde Arkana Satwikaa — Premium Portfolio
</footer>

<!-- ==== Scroll Reveal Script ==== -->
<script>
function sendMessage(e){
 e.preventDefault();
 alert("Pesan berhasil dikirim!");
}

window.addEventListener("scroll", ()=>{
 let reveals = document.querySelectorAll(".reveal");
 for(let i=0;i<reveals.length;i++){
   let windowHeight = window.innerHeight;
   let revealTop = reveals[i].getBoundingClientRect().top;
   if(revealTop < windowHeight - 80){
     reveals[i].classList.add("active");
   }
 }
});
</script>

</body>
</html>
