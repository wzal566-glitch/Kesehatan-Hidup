<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<meta name="theme-color" content="#e9f7eb">
<title>Kesehatan Kita</title>
<style>
:root{--green:#16864b;--dark:#075333;--mint:#e5f5e8;--bg:#f5faf5;--text:#214332;--muted:#718579;--white:#fff;--shadow:0 5px 22px #164c3510}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{font-family:Arial,sans-serif;background:var(--bg);color:var(--text);transition:background .2s,color .2s}
body.dark{--bg:#10291e;--white:#193d2b;--text:#e9f6eb;--muted:#b4c8b8;--mint:#214b34;--shadow:0 5px 22px #0003}
button,input{font:inherit}button{cursor:pointer}
.container{width:92%;max-width:1150px;margin:auto}
header{position:sticky;top:0;z-index:20;background:var(--white);box-shadow:var(--shadow)}
nav{min-height:70px;display:flex;align-items:center;justify-content:space-between;gap:10px}
.logo{font-weight:900;font-size:19px;color:var(--green)}
.links{display:flex;gap:17px}
.links a{text-decoration:none;color:var(--text);font-size:13px;font-weight:bold}
.links a:hover{color:var(--green)}
.theme{border:0;background:var(--mint);padding:10px;border-radius:50%}
.hero{background:linear-gradient(120deg,#d9f3df,#f1faef,#c3e9ce);padding:48px 0;overflow:hidden}
.hero-inner{display:grid;grid-template-columns:1fr 1fr;align-items:center;gap:30px}
.hero h1{font-size:clamp(38px,5vw,60px);color:#075333;line-height:1.1}
.hero h1 span{color:#29a357}
.hero p{color:#55725f;line-height:1.8;margin:20px 0}
.tag{background:#c6ebd0;color:#08723c;display:inline-block;padding:9px 15px;border-radius:30px;font-size:12px;font-weight:bold;margin-bottom:18px}
.btn{border:0;border-radius:30px;padding:13px 21px;background:var(--green);color:white;font-weight:bold;transition:.2s}
.btn:hover{transform:translateY(-2px);background:var(--dark)}
.hero-visual{height:300px;position:relative;display:flex;justify-content:center;align-items:center}
.person{width:205px;height:270px;z-index:2;animation:float 3s infinite ease-in-out}
.person .leg{transform-origin:100px 195px;animation:run 1s infinite alternate}
.person .arm{transform-origin:100px 115px;animation:swing .8s infinite alternate}
.heart-bg{position:absolute;width:245px;height:245px;border-radius:50%;background:#bde8c9;display:grid;place-items:center;right:0;border:9px solid #ffffff80}
.heart{font-size:95px;animation:beat 1s infinite}
.float-icon{position:absolute;font-size:35px;animation:float 3s infinite}
.fi1{top:0;left:5%}.fi2{bottom:5px;left:10%}.fi3{top:15px;right:5%}
@keyframes float{50%{transform:translateY(-12px)}}
@keyframes beat{20%{transform:scale(1.17)}60%{transform:scale(1.1)}}
@keyframes run{to{transform:rotate(15deg)}}
@keyframes swing{to{transform:rotate(-18deg)}}
section{padding:38px 0}
.heading{margin-bottom:20px}
.heading h2{font-size:25px;color:var(--dark);margin-bottom:8px}
.dark .heading h2{color:#a6e8b7}
.heading p{font-size:14px;color:var(--muted)}
.grid{display:grid;grid-template-columns:repeat(4,minmax(0,1fr));gap:15px}
.card{padding:20px;background:var(--white);border-radius:20px;box-shadow:var(--shadow);border:1px solid #e1eee3;transition:.2s;min-width:0}
.card:hover{transform:translateY(-3px)}
.card-icon{font-size:42px;margin-bottom:12px}
.card h3{margin-bottom:9px;font-size:16px}
.card p{font-size:13px;color:var(--muted);line-height:1.7}
.pillar:nth-child(1){background:#e1f3ff}.pillar:nth-child(2){background:#d9f6e3}.pillar:nth-child(3){background:#e1f4ff}.pillar:nth-child(4){background:#fff0df}
.dark .pillar{background:#214b34;color:#eaf8ed}
.organ-section{background:var(--mint);padding:24px;border-radius:25px}
.organ{text-align:center}
.organ-visual{height:100px;width:100px;margin:0 auto 13px;border-radius:50%;background:#f1fff3;display:grid;place-items:center;font-size:55px;animation:float 3s infinite}
.organ button{border:0;background:#d1eed9;color:#075333;border-radius:25px;padding:10px 16px;margin-top:12px;font-weight:bold}
.detail{display:none;background:var(--white);padding:18px;border-radius:15px;margin-top:18px;line-height:1.8;color:var(--muted)}
.two{display:grid;grid-template-columns:1fr 1fr;gap:17px}
.panel{background:var(--white);padding:22px;border-radius:22px;box-shadow:var(--shadow)}
.heart-panel{background:linear-gradient(140deg,#ffe0e6,#ffc3cf);text-align:center;color:#65283a}
.heart-panel .heart{font-size:82px;margin:18px}
.heart-panel.active .heart{animation:beat .8s infinite}
.small{font-size:12px;line-height:1.6;margin:10px 0}
.action{border:0;background:var(--green);color:white;padding:11px 18px;border-radius:25px;font-weight:bold}
.progress-track{height:13px;background:#e5eee5;border-radius:20px;overflow:hidden;margin:15px 0}
.progress{height:100%;width:0;background:#28a45a;border-radius:20px;transition:width .3s}
.habits{display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-top:18px}
.habit{display:flex;gap:9px;align-items:center;padding:13px;background:var(--mint);border-radius:12px;font-size:13px}
.habit input{width:18px;height:18px;accent-color:var(--green)}
.chart-panel{background:var(--white);padding:22px;border-radius:20px;box-shadow:var(--shadow)}
.chart-wrap{height:230px;position:relative;width:100%}
canvas{display:block;width:100%;height:100%}
.chart-note{font-size:12px;color:var(--muted);margin-top:10px}
.profile{display:grid;grid-template-columns:auto 1fr;gap:18px;align-items:center;background:linear-gradient(120deg,#d8f2df,#f2faf2);padding:23px;border-radius:20px}
.avatar{width:80px;height:80px;border-radius:50%;background:white;display:grid;place-items:center;font-size:45px}
.profile h3{color:#075333;margin-bottom:6px}.profile p{font-size:13px;color:#55725f;line-height:1.7}
.profile button{border:0;background:#16864b;color:white;padding:9px 15px;border-radius:20px;margin-top:8px;font-weight:bold}
.quiz{max-width:680px;margin:auto}
.quiz-top{display:flex;justify-content:space-between;font-size:13px;color:var(--muted);margin-bottom:20px}
.question{font-size:19px;font-weight:bold;line-height:1.5;margin-bottom:18px}
.answers{display:grid;grid-template-columns:1fr 1fr;gap:10px}
.answer{background:var(--white);color:var(--text);border:1px solid #dbeadd;padding:14px;border-radius:12px;text-align:left}
.answer.correct{background:#d6f4de;border-color:#16864b;color:#075333}
.answer.wrong{background:#ffe3df;border-color:#d66b60;color:#85332d}
.answer:disabled{cursor:default}
#feedback{margin:17px 0;font-weight:bold;font-size:13px;min-height:18px}
#result{display:none;text-align:center;padding:20px}
#result:not([hidden]){display:block}
#result .trophy{font-size:65px}
.articles{display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:15px}
.article{background:var(--white);border-radius:18px;overflow:hidden;box-shadow:var(--shadow)}
.article-cover{height:135px;display:grid;place-items:center;font-size:65px;background:#ddf4e3}
.article-content{padding:18px}
.article-content h3{font-size:16px;margin-bottom:8px}
.article-content p{font-size:13px;color:var(--muted);line-height:1.6}
.article-content button{border:0;background:transparent;color:var(--green);font-weight:bold;margin-top:12px}
.article-body{display:none;margin-top:12px;font-size:13px;line-height:1.8;color:var(--muted)}
.tips{background:linear-gradient(120deg,#075333,#16864b);color:white;padding:28px;border-radius:23px;display:flex;align-items:center;justify-content:space-between;gap:15px}
.tips p{line-height:1.8;margin:14px 0;font-size:14px}
.tips button{border:0;background:#f4d83e;padding:12px 18px;border-radius:25px;font-weight:bold}
.tips-art{font-size:70px}
footer{background:#075333;color:white;text-align:center;padding:28px 10px;line-height:2;font-size:13px}
.modal{display:none;position:fixed;inset:0;z-index:100;background:#0008;align-items:center;justify-content:center;padding:20px}
.modal-box{background:var(--white);padding:24px;border-radius:20px;width:100%;max-width:400px}
.modal-box h2{margin-bottom:18px}
.modal-box label{display:block;margin:12px 0 6px;font-size:13px}
.modal-box input{width:100%;padding:12px;border-radius:10px;border:1px solid #ccdccc;background:var(--bg);color:var(--text)}
.modal-actions{display:flex;gap:10px;margin-top:20px;flex-wrap:wrap}
@media(max-width:800px){.grid{grid-template-columns:repeat(2,minmax(0,1fr))}.hero-inner{grid-template-columns:1fr}.links{display:none}.articles{grid-template-columns:repeat(2,minmax(0,1fr))}}
@media(max-width:500px){.hero{padding:32px 0}.hero h1{font-size:38px}.hero-visual{height:220px}.person{width:160px}.heart-bg{width:175px;height:175px}.heart{font-size:70px}.grid{gap:10px}.card{padding:14px}.organ-section{padding:14px}.organ-visual{width:75px;height:75px;font-size:43px}.habits,.answers{grid-template-columns:1fr}.articles{grid-template-columns:1fr}.tips{padding:21px}.tips-art{font-size:48px}.heading h2{font-size:22px}}

/* Spotify player dan kuis lanjutan */
.music-panel{background:var(--white);border-radius:20px;padding:20px;box-shadow:var(--shadow)}
.music-panel p{color:var(--muted);font-size:13px;line-height:1.7;margin:8px 0 14px}
.music-controls{display:flex;gap:9px;flex-wrap:wrap;margin:12px 0}
.music-controls input{flex:1;min-width:190px;padding:13px;border:1px solid #cbdccd;border-radius:12px;background:var(--bg);color:var(--text)}
.spotify-frame{width:100%;height:152px;border:0;border-radius:13px;background:var(--mint);margin-top:12px}
.music-status{font-size:12px;color:var(--muted);min-height:18px}
.quiz-tools{display:flex;gap:10px;align-items:center;justify-content:space-between;flex-wrap:wrap;margin-bottom:12px}
.quiz-tools select{padding:10px;border-radius:10px;border:1px solid #cbdccd;background:var(--bg);color:var(--text)}
.quiz-explain{padding:12px;background:var(--mint);border-radius:12px;font-size:13px;line-height:1.7;margin:12px 0;color:var(--text)}
.quiz-progress{height:8px;background:var(--mint);border-radius:20px;overflow:hidden;margin:10px 0 16px}
.quiz-progress span{height:100%;display:block;background:var(--green);width:0;transition:width .25s}
@media(max-width:500px){.music-controls{flex-direction:column}.music-controls input,.music-controls button{width:100%}.spotify-frame{height:152px}}


/* Strava activity + heart-rate dashboard */
.sport-grid{display:grid;grid-template-columns:1fr 1fr;gap:16px}
.sport-card{background:var(--white);padding:20px;border-radius:20px;box-shadow:var(--shadow);min-width:0}
.sport-card h3{margin-bottom:12px}
.sport-form{display:grid;grid-template-columns:1fr 1fr;gap:10px}
.sport-form label{font-size:12px;color:var(--muted);display:block}
.sport-form input,.sport-form select{width:100%;margin-top:6px;padding:12px;border:1px solid #cbdccd;border-radius:10px;background:var(--bg);color:var(--text);min-width:0}
.sport-result{background:var(--mint);padding:15px;border-radius:14px;margin-top:14px;line-height:1.8}
.sport-stats{display:grid;grid-template-columns:repeat(2,1fr);gap:9px;margin-top:12px}
.sport-stat{background:var(--mint);padding:12px;border-radius:12px}
.sport-stat b{display:block;font-size:20px;color:var(--green)}
.sport-stat span{font-size:11px;color:var(--muted)}
.zone-bar{height:12px;border-radius:20px;background:linear-gradient(90deg,#65bd79 0 50%,#f1c34b 50% 70%,#e98b46 70% 85%,#dc5d5d 85%);margin:12px 0}
.sport-history{font-size:12px;color:var(--muted);line-height:1.8;margin-top:12px}
.strava-link{display:inline-block;text-decoration:none;background:#fc6b28;color:white;padding:11px 16px;border-radius:22px;font-weight:bold;margin-top:12px}
@media(max-width:700px){.sport-grid{grid-template-columns:1fr}}


.camera-monitor{margin-top:15px;padding:14px;border-radius:15px;background:var(--mint);text-align:left}
.camera-monitor video{width:100%;max-height:190px;object-fit:cover;border-radius:12px;background:#10291e;display:block;margin:10px 0}
.camera-actions{display:flex;gap:8px;flex-wrap:wrap}
.camera-actions button{flex:1;min-width:120px}
.camera-bpm{font-size:34px;font-weight:900;color:var(--green);text-align:center;margin:8px 0}
.camera-hint{font-size:12px;line-height:1.6;color:var(--muted)}
</style>
</head>
<body>
<header><div class="container"><nav>
<div class="logo">🌿 Kesehatan Kita</div>
<div class="links"><a href="#home">Home</a><a href="#manfaat">Manfaat</a><a href="#organ">Organ</a><a href="#grafik">Grafik</a><a href="#musik">Musik</a><a href="#quiz">Kuis</a><a href="#artikel">Artikel</a></div>
<button class="theme" id="themeButton" type="button" aria-label="Ganti tema">🌙</button>
</nav></div></header>

<section class="hero" id="home"><div class="container hero-inner">
<div><div class="tag">🌱 HEALTHY BODY, HAPPY LIFE</div>
<h1>Hidup Sehat,<br><span>Masa Depan Hebat.</span></h1>
<p>Bangun kebiasaan baik, jaga kesehatan tubuh, dan ciptakan masa depan yang lebih bahagia. Mulai perjalanan sehatmu hari ini!</p>
<button class="btn" type="button" id="exploreButton">🚀 Jelajahi Sekarang</button></div>
<div class="hero-visual"><div class="heart-bg"><div class="heart">❤️</div></div>
<svg class="person" viewBox="0 0 200 280" xmlns="http://www.w3.org/2000/svg" aria-label="Ilustrasi orang berolahraga">
<circle cx="100" cy="48" r="34" fill="#e8a77c"/><path d="M67 43Q65 5 105 10Q140 10 135 52Q118 29 95 34Q78 45 67 43" fill="#493327"/>
<circle cx="88" cy="49" r="3" fill="#38271e"/><circle cx="112" cy="49" r="3" fill="#38271e"/>
<path d="M92 65Q100 73 109 65" fill="none" stroke="#9b4e42" stroke-width="3" stroke-linecap="round"/>
<path d="M70 90Q100 75 130 90L143 180H57Z" fill="#249c55"/>
<path d="M72 102L35 151L45 159L83 123" fill="none" stroke="#e8a77c" stroke-width="15" stroke-linecap="round"/>
<path class="arm" d="M128 100L163 70L170 42" fill="none" stroke="#e8a77c" stroke-width="15" stroke-linecap="round"/>
<path d="M75 177L68 235L50 260" fill="none" stroke="#245a9b" stroke-width="20" stroke-linecap="round"/>
<path class="leg" d="M118 177L130 235L154 255" fill="none" stroke="#245a9b" stroke-width="20" stroke-linecap="round"/>
<path d="M50 260L34 263M154 255L174 261" stroke="#263b32" stroke-width="12" stroke-linecap="round"/>
</svg>
<div class="float-icon fi1">🌿</div><div class="float-icon fi2">🥬</div><div class="float-icon fi3">💧</div>
</div></div></section>

<main class="container">
<section id="profil"><div class="heading"><h2>👤 Profil Pengguna</h2><p>Kenali perjalanan kesehatanmu.</p></div>
<div class="profile"><div class="avatar" id="avatar">👤</div><div><h3 id="userName">Halo, Pengguna!</h3><p id="userInfo">Ayo mulai perjalanan hidup sehatmu.</p><button id="editProfile" type="button">Edit Profil ✎</button></div></div></section>

<section id="manfaat"><div class="heading"><h2>🌿 4 Pilar Hidup Sehat</h2><p>Empat kebiasaan penting untuk tubuh yang lebih baik.</p></div>
<div class="grid">
<div class="card pillar"><div class="card-icon">🏃</div><h3>Olahraga</h3><p>Jaga kebugaran dan kesehatan jantung dengan aktivitas fisik.</p></div>
<div class="card pillar"><div class="card-icon">🥗</div><h3>Nutrisi</h3><p>Konsumsi makanan bergizi dan seimbang setiap hari.</p></div>
<div class="card pillar"><div class="card-icon">💧</div><h3>Hidrasi</h3><p>Penuhi kebutuhan cairan tubuh secara teratur.</p></div>
<div class="card pillar"><div class="card-icon">😴</div><h3>Istirahat</h3><p>Tidur cukup untuk membantu pemulihan tubuh.</p></div>
</div></section>

<section id="organ"><div class="organ-section"><div class="heading"><h2>🫀 Kenali Organ Tubuh</h2><p>Pelajari fungsi organ manusia.</p></div>
<div class="grid">
<div class="card organ"><div class="organ-visual">❤️</div><h3>Jantung</h3><p>Memompa darah ke seluruh tubuh.</p><button type="button" data-organ="jantung">Pelajari →</button></div>
<div class="card organ"><div class="organ-visual">🫁</div><h3>Paru-paru</h3><p>Membantu proses pernapasan.</p><button type="button" data-organ="paru">Pelajari →</button></div>
<div class="card organ"><div class="organ-visual">🧠</div><h3>Otak</h3><p>Mengatur aktivitas tubuh.</p><button type="button" data-organ="otak">Pelajari →</button></div>
<div class="card organ"><div class="organ-visual">🫘</div><h3>Ginjal</h3><p>Menyaring darah dan zat sisa.</p><button type="button" data-organ="ginjal">Pelajari →</button></div>
</div><div class="detail" id="organDetail" role="status"></div></div></section>

<section><div class="heading"><h2>❤️ Simulasi Detak Jantung</h2><p>Animasi dan efek suara detak jantung.</p></div>
<div class="heart-panel panel" id="heartPanel"><h3>HEARTBEAT SIMULATOR</h3><div class="heart">❤️</div>
<p id="heartStatus">Simulasi belum dimulai.</p><p class="small">Simulasi ini hanya untuk edukasi, bukan alat pengukur denyut jantung.</p>
<button class="action" id="heartButton" type="button">▶ Mulai Suara</button></div></section>


<section id="strava">
 <div class="heading"><h2>🏃 Strava & Heart Rate Tracker</h2><p>Hitung performa olahraga dan pantau zona detak jantungmu.</p></div>
 <div class="sport-grid">
  <div class="sport-card">
   <h3>📍 Kalkulator Aktivitas</h3>
   <p class="small">Masukkan data latihan untuk menghitung pace, kecepatan, dan estimasi kalori.</p>
   <div class="sport-form">
    <label>Jenis aktivitas<select id="sportType"><option value="running">Lari</option><option value="walking">Jalan kaki</option><option value="cycling">Bersepeda</option></select></label>
    <label>Jarak (km)<input id="sportDistance" type="number" min="0.01" step="0.01" placeholder="Contoh: 5"></label>
    <label>Durasi (menit)<input id="sportDuration" type="number" min="0.1" step="0.1" placeholder="Contoh: 30"></label>
    <label>Berat badan (kg)<input id="sportWeight" type="number" min="1" max="400" step="0.1" placeholder="Contoh: 60"></label>
   </div>
   <button class="action" id="calcSport" type="button" style="margin-top:13px">Hitung Aktivitas</button>
   <div class="sport-result" id="sportResult" aria-live="polite">Hasil pace, kecepatan rata-rata, dan estimasi kalori akan tampil di sini.</div>
   <div class="sport-history" id="sportHistory">Belum ada aktivitas tersimpan.</div>
   <a class="strava-link" href="https://www.strava.com/" target="_blank" rel="noopener">Buka Strava ↗</a>
   <p class="small">Kalkulator ini terinspirasi metrik Strava, bukan sinkronisasi akun. Hubungkan akun melalui aplikasi/situs resmi Strava untuk data otomatis.</p>
  </div>
  <div class="sport-card">
   <h3>❤️ Heart Rate Monitor</h3>
   <p class="small">Masukkan BPM dari jam pintar atau hitung denyut nadi selama 60 detik.</p>
   <div class="sport-form">
    <label>Usia (tahun)<input id="hrAge" type="number" min="10" max="100" placeholder="Contoh: 25"></label>
    <label>Detak jantung (BPM)<input id="hrBpm" type="number" min="30" max="240" placeholder="Contoh: 125"></label>
   </div>
   <button class="action" id="checkHR" type="button" style="margin-top:13px">Cek Zona Detak Jantung</button>
   <div class="sport-stats">
    <div class="sport-stat"><b id="hrMax">—</b><span>Estimasi HR maksimal</span></div>
    <div class="sport-stat"><b id="hrPercent">—</b><span>Persentase HR maksimal</span></div>
   </div>
   <div class="zone-bar" aria-label="Skala zona detak jantung"></div>
   <div class="sport-result" id="hrResult" aria-live="polite">Zona detak jantung akan ditampilkan setelah data dimasukkan.</div>
   <p class="small">Zona dihitung dengan rumus perkiraan HR maksimal = 220 − usia. Ini bukan diagnosis atau alat medis. Hentikan olahraga dan cari bantuan medis bila mengalami nyeri dada, pingsan, atau sesak berat.</p>
   <div class="camera-monitor">
    <b>📷 Ukur BPM Otomatis dengan Kamera</b>
    <p class="camera-hint">Letakkan ujung jari dengan lembut menutupi kamera belakang dan flash. Diam selama pengukuran. Perlu HTTPS dan izin kamera.</p>
    <video id="pulseVideo" autoplay muted playsinline hidden></video>
    <canvas id="pulseCanvas" width="64" height="64" hidden></canvas>
    <div class="camera-bpm" id="cameraBpm">-- BPM</div>
    <p class="camera-hint" id="cameraStatus" role="status">Belum mengukur. Tekan Mulai Ukur dan izinkan kamera.</p>
    <div class="camera-actions">
     <button class="action" id="startCameraHR" type="button">📷 Mulai Ukur</button>
     <button class="action" id="stopCameraHR" type="button" style="background:#829387" disabled>■ Berhenti</button>
    </div>
   </div>
  </div>
 </div>
</section>

<section id="aktivitas"><div class="heading"><h2>🏆 Aktivitas Sehat Harian</h2><p>Centang kebiasaan yang telah kamu lakukan.</p></div>
<div class="panel"><div style="display:flex;justify-content:space-between;gap:10px"><b>Target hari ini</b><b id="percent">0%</b></div>
<div class="progress-track"><div class="progress" id="progress"></div></div><p id="count" class="small">0 dari 5 aktivitas selesai</p>
<div class="habits">
<label class="habit"><input type="checkbox" class="check" data-id="0">💧 Minum air cukup</label>
<label class="habit"><input type="checkbox" class="check" data-id="1">🥗 Makan bergizi</label>
<label class="habit"><input type="checkbox" class="check" data-id="2">🏃 Olahraga</label>
<label class="habit"><input type="checkbox" class="check" data-id="3">🍎 Makan buah</label>
<label class="habit"><input type="checkbox" class="check" data-id="4">😴 Tidur cukup</label>
</div></div></section>

<section id="grafik"><div class="heading"><h2>📊 Grafik Kesehatan</h2><p>Riwayat aktivitas harian selama 7 hari terakhir.</p></div>
<div class="chart-panel"><h3>Progress aktivitas (%)</h3><div class="chart-wrap"><canvas id="healthChart" aria-label="Grafik progress aktivitas tujuh hari"></canvas></div>
<p class="chart-note">Grafik berdasarkan checklist aktivitas yang tersimpan di browser ini.</p></div></section>


<section id="musik"><div class="heading"><h2>🎧 Musik & Relaksasi</h2><p>Dengarkan musik Spotify sambil belajar dan menjaga rutinitas sehat.</p></div>
<div class="music-panel"><b>🎵 Spotify Web Player</b><p>Tempel tautan lagu, album, playlist, atau podcast Spotify. Contoh: tautan yang kamu salin lewat menu Bagikan di aplikasi Spotify.</p>
<div class="music-controls"><input id="spotifyUrl" type="url" placeholder="https://open.spotify.com/playlist/..." aria-label="Tautan Spotify"><button class="action" id="loadSpotify" type="button">Muat Musik ▶</button><button class="action" id="openSpotify" type="button" style="background:#547b61">Buka Spotify ↗</button></div>
<div class="music-status" id="spotifyStatus" role="status">Pemutar akan muncul setelah kamu memasukkan tautan Spotify.</div>
<iframe id="spotifyPlayer" class="spotify-frame" title="Spotify music player" src="about:blank" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy" hidden></iframe>
</div></section>

<section id="quiz"><div class="heading"><h2>🧠 Kuis Kesehatan Tingkat Lanjut</h2><p>50 pertanyaan menantang tentang tubuh, gizi, penyakit, dan kesehatan masyarakat.</p></div>
<div class="panel quiz"><div id="quizGame"><div class="quiz-top"><span id="number">Pertanyaan 1/50</span><span>🏆 HEALTH QUIZ PRO</span></div>
<div class="quiz-progress"><span id="quizProgress"></span></div><div class="quiz-tools"><span class="small">Pilih satu jawaban paling tepat.</span><select id="quizMode" aria-label="Pilih kategori kuis"><option value="all">Semua kategori (50)</option><option value="jantung">Jantung & pembuluh darah</option><option value="metabolisme">Metabolisme & hormon</option><option value="gizi">Gizi & pencernaan</option><option value="imun">Imunitas & penyakit</option><option value="otak">Otak & kesehatan umum</option></select></div>
<div class="question" id="question"></div><div class="answers" id="answers"></div><div id="feedback" role="status"></div><div id="explanation" class="quiz-explain" hidden></div>
<button class="action" id="nextButton" type="button" hidden>Selanjutnya →</button></div>
<div id="result" hidden><div class="trophy">🏆</div><h2>Kuis Selesai!</h2><h1 id="score"></h1><p id="message"></p><br><button class="action" id="restartQuiz" type="button">Ulangi Kuis</button></div></div></section>

<section id="artikel"><div class="heading"><h2>📚 Artikel Kesehatan</h2><p>Pengetahuan sederhana untuk hidup lebih sehat.</p></div>
<div class="articles">
<article class="article"><div class="article-cover">🥗</div><div class="article-content"><h3>Pentingnya Nutrisi Seimbang</h3><p>Kenali manfaat makanan bergizi untuk tubuh.</p><button type="button" data-article="0">Baca selengkapnya ↓</button><div class="article-body">Makanan bergizi seimbang terdiri dari berbagai kelompok makanan, termasuk sumber karbohidrat, protein, sayur, buah, serta lemak sehat. Variasikan makanan agar kebutuhan nutrisi terpenuhi.</div></div></article>
<article class="article"><div class="article-cover">🏃</div><div class="article-content"><h3>Manfaat Aktivitas Fisik</h3><p>Mengapa olahraga penting bagi kesehatan?</p><button type="button" data-article="1">Baca selengkapnya ↓</button><div class="article-body">Aktivitas fisik membantu meningkatkan kebugaran, menjaga kesehatan jantung, memperkuat otot, serta mendukung kesehatan mental. Mulailah dengan berjalan kaki dan tingkatkan secara bertahap.</div></div></article>
<article class="article"><div class="article-cover">😴</div><div class="article-content"><h3>Pentingnya Tidur Cukup</h3><p>Istirahat merupakan bagian dari hidup sehat.</p><button type="button" data-article="2">Baca selengkapnya ↓</button><div class="article-body">Tidur membantu pemulihan tubuh dan otak. Orang dewasa umumnya membutuhkan sekitar 7–9 jam tidur per malam. Remaja biasanya membutuhkan waktu tidur lebih banyak.</div></div></article>
</div></section>

<section><div class="tips"><div><h2>💡 Tips Kesehatan</h2><p id="tipText">Perbanyak buah dan sayur untuk mendapatkan vitamin, mineral, dan serat.</p><button id="nextTip" type="button">Tips Berikutnya →</button></div><div class="tips-art">🍎🥦</div></div></section>
</main>

<footer><h2>🌿 Kesehatan Kita</h2><p>Sehat Hari Ini, Bahagia Nanti.</p><p>© 2026 Hidup Sehat | Website Edukasi Kesehatan</p></footer>

<div class="modal" id="profileModal" role="dialog" aria-modal="true" aria-labelledby="profileTitle">
<div class="modal-box"><h2 id="profileTitle">👤 Profil Pengguna</h2>
<label for="inputName">Nama kamu</label><input id="inputName" maxlength="40" placeholder="Masukkan nama">
<label for="inputAge">Usia</label><input id="inputAge" type="number" min="1" max="120" inputmode="numeric" placeholder="Masukkan usia">
<label for="inputTarget">Target kesehatan</label><input id="inputTarget" maxlength="100" placeholder="Contoh: Rutin olahraga">
<div class="modal-actions"><button class="action" id="saveProfile" type="button">Simpan Profil</button><button class="action" id="closeProfile" type="button" style="background:#829387">Tutup</button></div>
</div></div>

<script>
"use strict";

/* Utilitas penyimpanan: cegah aplikasi berhenti jika localStorage tidak tersedia. */
function storageGet(key, fallback) {
  try {
    const value = localStorage.getItem(key);
    return value === null ? fallback : value;
  } catch (error) {
    console.warn("Penyimpanan tidak tersedia:", error);
    return fallback;
  }
}
function storageSet(key, value) {
  try {
    localStorage.setItem(key, value);
    return true;
  } catch (error) {
    console.warn("Gagal menyimpan data:", error);
    return false;
  }
}
function parseJSON(value, fallback) {
  try { return JSON.parse(value); } catch (error) { return fallback; }
}
function byId(id) { return document.getElementById(id); }
function go(id) {
  const target = byId(id);
  if (target) target.scrollIntoView({behavior:"smooth", block:"start"});
}

/* Tema */
function applyTheme() {
  const dark = storageGet("hlTheme", "light") === "dark";
  document.body.classList.toggle("dark", dark);
  byId("themeButton").textContent = dark ? "☀️" : "🌙";
}
byId("themeButton").addEventListener("click", function () {
  const dark = !document.body.classList.contains("dark");
  storageSet("hlTheme", dark ? "dark" : "light");
  applyTheme();
  drawChart();
});
applyTheme();
byId("exploreButton").addEventListener("click", function(){ go("manfaat"); });

/* Profil */
function renderProfile() {
  const profile = parseJSON(storageGet("hlProfile", "{}"), {});
  byId("userName").textContent = "Halo, " + (profile.name || "Pengguna") + "!";
  const info = [];
  if (profile.age) info.push("Usia: " + profile.age + " tahun");
  if (profile.target) info.push("Target: " + profile.target);
  byId("userInfo").textContent = info.length ? info.join(" • ") : "Ayo mulai perjalanan hidup sehatmu.";
  byId("avatar").textContent = profile.name ? "😊" : "👤";
}
function openProfile() {
  const profile = parseJSON(storageGet("hlProfile", "{}"), {});
  byId("inputName").value = profile.name || "";
  byId("inputAge").value = profile.age || "";
  byId("inputTarget").value = profile.target || "";
  byId("profileModal").style.display = "flex";
}
function closeProfile() { byId("profileModal").style.display = "none"; }
byId("editProfile").addEventListener("click", openProfile);
byId("closeProfile").addEventListener("click", closeProfile);
byId("saveProfile").addEventListener("click", function () {
  const name = byId("inputName").value.trim();
  const ageText = byId("inputAge").value.trim();
  const age = ageText ? Number(ageText) : "";
  const target = byId("inputTarget").value.trim();
  if (!name) { alert("Masukkan nama terlebih dahulu."); return; }
  if (ageText && (!Number.isInteger(age) || age < 1 || age > 120)) {
    alert("Masukkan usia antara 1 sampai 120 tahun."); return;
  }
  storageSet("hlProfile", JSON.stringify({name:name, age:age, target:target}));
  renderProfile();
  closeProfile();
});
byId("profileModal").addEventListener("click", function(event){
  if (event.target === byId("profileModal")) closeProfile();
});
renderProfile();

/* Informasi organ */
const organData = {
  jantung:"Jantung adalah organ berotot yang memompa darah ke seluruh tubuh. Darah membawa oksigen dan nutrisi ke sel-sel tubuh.",
  paru:"Paru-paru membantu proses pernapasan dan pertukaran oksigen dengan karbon dioksida.",
  otak:"Otak merupakan pusat kendali tubuh yang mengatur pikiran, ingatan, gerakan, dan berbagai fungsi tubuh.",
  ginjal:"Ginjal menyaring darah, membuang zat sisa melalui urine, serta membantu mengatur keseimbangan cairan."
};
document.querySelectorAll("[data-organ]").forEach(function(button){
  button.addEventListener("click", function(){
    const key = button.getAttribute("data-organ");
    byId("organDetail").textContent = organData[key] || "Informasi belum tersedia.";
    byId("organDetail").style.display = "block";
  });
});

/* Audio detak jantung. AudioContext hanya dibuat setelah pengguna menekan tombol. */
let heartRunning = false;
let heartTimer = null;
let audioContext = null;
function playHeartbeat() {
  if (!heartRunning) return;
  const AudioCtor = window.AudioContext || window.webkitAudioContext;
  if (!AudioCtor) {
    byId("heartStatus").textContent = "Browser ini belum mendukung audio Web Audio.";
    return;
  }
  try {
    if (!audioContext) audioContext = new AudioCtor();
    if (audioContext.state === "suspended") audioContext.resume();
    function thump(delay, frequency, duration) {
      const oscillator = audioContext.createOscillator();
      const gain = audioContext.createGain();
      const start = audioContext.currentTime + delay;
      oscillator.type = "sine";
      oscillator.frequency.setValueAtTime(frequency, start);
      gain.gain.setValueAtTime(0.001, start);
      gain.gain.exponentialRampToValueAtTime(0.20, start + 0.02);
      gain.gain.exponentialRampToValueAtTime(0.001, start + duration);
      oscillator.connect(gain);
      gain.connect(audioContext.destination);
      oscillator.start(start);
      oscillator.stop(start + duration);
    }
    thump(0, 65, 0.13);
    thump(0.20, 50, 0.15);
  } catch (error) {
    console.warn("Audio tidak dapat diputar:", error);
    byId("heartStatus").textContent = "Audio tidak dapat diputar pada browser ini.";
  }
}
function stopHeartbeat() {
  heartRunning = false;
  if (heartTimer !== null) {
    window.clearInterval(heartTimer);
    heartTimer = null;
  }
  byId("heartPanel").classList.remove("active");
  byId("heartStatus").textContent = "Simulasi dihentikan.";
  byId("heartButton").textContent = "▶ Mulai Suara";
}
byId("heartButton").addEventListener("click", function(){
  if (heartRunning) { stopHeartbeat(); return; }
  heartRunning = true;
  byId("heartPanel").classList.add("active");
  byId("heartStatus").textContent = "❤️ Simulasi sedang berjalan.";
  byId("heartButton").textContent = "■ Hentikan";
  playHeartbeat();
  heartTimer = window.setInterval(playHeartbeat, 1000);
});

/* Tanggal lokal konsisten, tanpa bergantung pada format bahasa perangkat. */
function localDateKey(date) {
  const y = date.getFullYear();
  const m = String(date.getMonth() + 1).padStart(2, "0");
  const d = String(date.getDate()).padStart(2, "0");
  return y + "-" + m + "-" + d;
}
function readHistory() {
  const value = parseJSON(storageGet("hlHistory", "{}"), {});
  return value && typeof value === "object" && !Array.isArray(value) ? value : {};
}
const checks = Array.from(document.querySelectorAll(".check"));
function updateTracker() {
  const selected = [];
  checks.forEach(function(check, index) {
    if (check.checked) selected.push(index);
  });
  const percent = Math.round(selected.length / checks.length * 100);
  byId("progress").style.width = percent + "%";
  byId("percent").textContent = percent + "%";
  byId("count").textContent = selected.length + " dari " + checks.length + " aktivitas selesai";
  const history = readHistory();
  history[localDateKey(new Date())] = selected;
  storageSet("hlHistory", JSON.stringify(history));
  drawChart();
}
function loadChecks() {
  const history = readHistory();
  const today = history[localDateKey(new Date())];
  const selected = Array.isArray(today) ? today : [];
  checks.forEach(function(check, index) {
    check.checked = selected.indexOf(index) !== -1;
    check.addEventListener("change", updateTracker);
  });
  updateTracker();
}

/* Grafik Canvas: digambar tanpa Canvas roundRect agar kompatibel dengan WebView lama. */
function roundedRect(ctx, x, y, width, height, radius) {
  const r = Math.max(0, Math.min(radius, width / 2, height / 2));
  ctx.beginPath();
  ctx.moveTo(x + r, y);
  ctx.lineTo(x + width - r, y);
  ctx.quadraticCurveTo(x + width, y, x + width, y + r);
  ctx.lineTo(x + width, y + height - r);
  ctx.quadraticCurveTo(x + width, y + height, x + width - r, y + height);
  ctx.lineTo(x + r, y + height);
  ctx.quadraticCurveTo(x, y + height, x, y + height - r);
  ctx.lineTo(x, y + r);
  ctx.quadraticCurveTo(x, y, x + r, y);
  ctx.closePath();
}
function drawChart() {
  const canvas = byId("healthChart");
  if (!canvas) return;
  const rect = canvas.getBoundingClientRect();
  if (rect.width <= 0 || rect.height <= 0) return;
  const dpr = Math.max(1, Math.min(window.devicePixelRatio || 1, 3));
  canvas.width = Math.round(rect.width * dpr);
  canvas.height = Math.round(rect.height * dpr);
  const ctx = canvas.getContext("2d");
  if (!ctx) return;
  ctx.setTransform(dpr, 0, 0, dpr, 0, 0);
  const w = rect.width, h = rect.height;
  const pad = {left:34, right:10, top:14, bottom:30};
  const chartW = Math.max(1, w - pad.left - pad.right);
  const chartH = Math.max(1, h - pad.top - pad.bottom);
  const history = readHistory();
  const days = [];
  for (let i = 6; i >= 0; i--) {
    const date = new Date();
    date.setDate(date.getDate() - i);
    const items = history[localDateKey(date)];
    const count = Array.isArray(items) ? items.length : 0;
    const labels = ["Min","Sen","Sel","Rab","Kam","Jum","Sab"];
    days.push({label:labels[date.getDay()], value:Math.min(100, count / 5 * 100)});
  }
  const dark = document.body.classList.contains("dark");
  ctx.clearRect(0, 0, w, h);
  ctx.font = "11px Arial";
  ctx.textAlign = "right";
  for (let n = 0; n <= 100; n += 25) {
    const y = pad.top + chartH - n / 100 * chartH;
    ctx.strokeStyle = dark ? "#365b43" : "#e3eee5";
    ctx.lineWidth = 1;
    ctx.beginPath(); ctx.moveTo(pad.left, y); ctx.lineTo(w - pad.right, y); ctx.stroke();
    ctx.fillStyle = dark ? "#c2d6c6" : "#718579";
    ctx.fillText(n + "%", pad.left - 6, y + 4);
  }
  const gap = chartW / days.length;
  days.forEach(function(day, index) {
    const barWidth = Math.max(3, gap * 0.58);
    const x = pad.left + index * gap + (gap - barWidth) / 2;
    const barHeight = day.value / 100 * chartH;
    const y = pad.top + chartH - barHeight;
    if (barHeight > 0) {
      ctx.fillStyle = "#35a961";
      roundedRect(ctx, x, y, barWidth, barHeight, 5);
      ctx.fill();
    }
    ctx.fillStyle = dark ? "#d7e9dc" : "#61776a";
    ctx.textAlign = "center";
    ctx.fillText(day.label, x + barWidth / 2, h - 8);
  });
}
let resizeTimer = null;
window.addEventListener("resize", function(){
  window.clearTimeout(resizeTimer);
  resizeTimer = window.setTimeout(drawChart, 100);
});


/* Spotify embed: hanya menerima tautan open.spotify.com dengan tipe konten yang didukung. */
function spotifyEmbedUrl(raw) {
  try {
    const u = new URL(raw);
    if (u.hostname !== "open.spotify.com" && u.hostname !== "www.open.spotify.com") return null;
    const parts = u.pathname.split("/").filter(Boolean);
    if (parts.length < 2) return null;
    const type = parts[0], id = parts[1];
    if (!["track","album","playlist","artist","show","episode"].includes(type) || !/^[A-Za-z0-9]+$/.test(id)) return null;
    return "https://open.spotify.com/embed/" + type + "/" + id + "?utm_source=generator";
  } catch (e) { return null; }
}
byId("loadSpotify").addEventListener("click",function(){
  const raw=byId("spotifyUrl").value.trim(), embed=spotifyEmbedUrl(raw);
  if(!embed){byId("spotifyStatus").textContent="Tautan tidak valid. Gunakan tautan lagu, album, playlist, artis, atau podcast dari open.spotify.com.";return;}
  byId("spotifyPlayer").src=embed;byId("spotifyPlayer").hidden=false;
  byId("spotifyStatus").textContent="Pemutar siap. Tekan Play di dalam pemutar Spotify untuk mulai mendengarkan.";
});
byId("openSpotify").addEventListener("click",function(){window.open("https://open.spotify.com/","_blank","noopener,noreferrer");});
byId("spotifyUrl").addEventListener("keydown",function(e){if(e.key==="Enter")byId("loadSpotify").click();});

/* Kuis */
const questions = [["jantung","Apa fungsi utama endotel pembuluh darah?",["Menghasilkan sel darah merah","Mengatur tonus pembuluh dan memberi sinyal antitrombotik","Memompa darah ke aorta","Menyimpan oksigen"],1,"Endotel merupakan lapisan aktif yang mengatur vasodilatasi, permeabilitas, inflamasi, dan pembekuan."],["jantung","Mengapa plak aterosklerotik yang pecah dapat memicu infark miokard?",["Karena langsung menutup katup jantung","Karena memicu pembentukan trombus pada arteri koroner","Karena meningkatkan produksi empedu","Karena menghentikan impuls di saraf vagus"],1,"Ruptur plak mengekspos materi trombogenik sehingga trombosit dan koagulasi membentuk bekuan yang dapat menyumbat arteri koroner."],["jantung","Apa yang dimaksud dengan fraksi ejeksi ventrikel kiri?",["Persentase darah yang dikeluarkan ventrikel kiri tiap kontraksi dibanding volume akhir diastolik","Jumlah denyut jantung per menit","Tekanan darah saat jantung relaksasi","Volume darah total dalam tubuh"],0,"Fraksi ejeksi menggambarkan proporsi volume akhir diastolik yang dipompa keluar pada satu denyut."],["jantung","Resistensi perifer sistemik terutama dipengaruhi oleh perubahan apa?",["Diameter arteriol","Jumlah alveolus","Panjang usus halus","Kadar empedu"],0,"Arteriol adalah pembuluh resistensi; perubahan diameternya sangat memengaruhi resistensi aliran darah."],["jantung","Mengapa hipertensi kronis dapat menyebabkan hipertrofi ventrikel kiri?",["Beban tekanan meningkat sehingga otot ventrikel beradaptasi","Darah menjadi lebih encer","Katup pulmonal selalu menutup","Produksi insulin menurun"],0,"Tekanan yang harus dilawan ventrikel kiri meningkat, sehingga dinding otot dapat menebal sebagai respons adaptasi."],["jantung","Komponen EKG yang merepresentasikan depolarisasi ventrikel adalah ...",["Gelombang P","Kompleks QRS","Gelombang T","Segmen PR"],1,"Kompleks QRS mencerminkan depolarisasi ventrikel."],["jantung","Apa peran utama nodus sinoatrial pada jantung normal?",["Menghasilkan impuls pemacu utama","Menutup katup aorta","Menyaring darah","Mengatur kadar glukosa"],0,"Nodus sinoatrial biasanya menjadi pacemaker fisiologis karena memiliki laju depolarisasi spontan tertinggi."],["jantung","Mengapa kadar LDL yang tinggi meningkatkan risiko aterosklerosis?",["LDL dapat masuk dan tertahan di intima arteri lalu mengalami modifikasi","LDL mengubah oksigen menjadi karbon dioksida","LDL menghancurkan semua trombosit","LDL mempercepat filtrasi ginjal"],0,"Partikel LDL yang tertahan di dinding arteri dapat mengalami oksidasi dan memicu respons inflamasi."],["jantung","Apa efek utama aktivasi sistem saraf simpatis pada jantung?",["Menurunkan frekuensi dan kontraktilitas","Meningkatkan frekuensi serta kontraktilitas","Menghentikan konduksi AV secara permanen","Mengurangi aliran koroner menjadi nol"],1,"Aktivasi simpatis melalui reseptor beta-1 meningkatkan denyut, konduksi, dan kekuatan kontraksi."],["jantung","Tekanan darah arteri rata-rata paling dekat dipengaruhi oleh kombinasi ...",["Curah jantung dan resistensi perifer sistemik","Suhu kulit dan tinggi badan","Frekuensi napas dan kapasitas lambung","Kadar kalsium tulang dan massa rambut"],0,"Secara sederhana, tekanan arteri rata-rata berkaitan dengan curah jantung dikalikan resistensi perifer sistemik."],["metabolisme","Hormon apa yang meningkatkan pengambilan glukosa oleh otot dan jaringan lemak melalui GLUT4?",["Glukagon","Insulin","Kortisol","Adrenalin"],1,"Insulin memicu translokasi GLUT4 ke membran sel otot dan adiposa sehingga pengambilan glukosa meningkat."],["metabolisme","Pada keadaan puasa berkepanjangan, proses pembentukan glukosa baru disebut ...",["Glikogenesis","Glikolisis","Glukoneogenesis","Lipogenesis"],2,"Glukoneogenesis membentuk glukosa dari prekursor nonkarbohidrat seperti laktat, gliserol, dan asam amino."],["metabolisme","Hormon yang terutama meningkatkan reabsorpsi air di duktus kolektivus ginjal adalah ...",["ADH atau vasopresin","Kalsitonin","Melatonin","Gastrin"],0,"ADH meningkatkan pemasangan aquaporin-2 sehingga air lebih banyak direabsorpsi."],["metabolisme","Apa fungsi utama hormon paratiroid (PTH)?",["Menurunkan kalsium darah","Meningkatkan kalsium darah","Menghambat seluruh aktivitas osteoklas","Menurunkan fosfat melalui penyerapan usus saja"],1,"PTH meningkatkan kalsium darah melalui efek pada tulang, ginjal, dan aktivasi vitamin D."],["metabolisme","Pada diabetes melitus tipe 1, mekanisme utama penyakit adalah ...",["Resistensi insulin akibat obesitas saja","Destruksi autoimun sel beta pankreas","Kelebihan hormon tiroid","Kekurangan hormon pertumbuhan"],1,"Diabetes tipe 1 umumnya terjadi akibat destruksi autoimun sel beta yang menghasilkan insulin."],["metabolisme","Apa yang terjadi pada laju metabolisme basal pada hipertiroidisme?",["Cenderung meningkat","Selalu turun menjadi nol","Tidak pernah berubah","Hanya berubah saat tidur"],0,"Kelebihan hormon tiroid meningkatkan aktivitas metabolik dan konsumsi energi."],["metabolisme","Kortisol diproduksi terutama oleh bagian ...",["Korteks adrenal","Medula adrenal","Kelenjar pineal","Hipofisis posterior"],0,"Kortisol adalah glukokortikoid yang dihasilkan zona fasikulata korteks adrenal."],["metabolisme","Dalam keadaan setelah makan, jalur penyimpanan glukosa sebagai glikogen disebut ...",["Glikogenolisis","Glikogenesis","Ketogenesis","Proteolisis"],1,"Glikogenesis menyimpan glukosa dalam bentuk glikogen, terutama di hati dan otot."],["metabolisme","Apa pemicu utama pelepasan renin dari ginjal?",["Penurunan perfusi ginjal","Peningkatan kadar oksigen udara","Kenaikan suhu kulit","Peningkatan empedu"],0,"Penurunan tekanan perfusi ginjal, penurunan NaCl di makula densa, atau stimulasi simpatis beta-1 dapat memicu renin."],["metabolisme","Hormon melatonin terutama berperan dalam ...",["Pengaturan ritme sirkadian tidur-bangun","Pembekuan darah","Pencernaan protein","Kontraksi otot rangka"],0,"Melatonin dari kelenjar pineal membantu menyelaraskan ritme biologis dengan siklus terang-gelap."],["gizi","Vitamin B12 diperlukan secara khusus untuk ...",["Sintesis DNA dan fungsi saraf","Pembentukan empedu saja","Penglihatan malam secara langsung","Produksi insulin di hati"],0,"B12 penting untuk sintesis DNA, pembentukan sel darah, dan pemeliharaan mielin saraf."],["gizi","Defisiensi vitamin C berat dapat menyebabkan ...",["Skorbut","Rakitis","Pellagra","Beri-beri"],0,"Vitamin C dibutuhkan dalam sintesis kolagen; kekurangannya menyebabkan skorbut dengan perdarahan gusi dan gangguan penyembuhan luka."],["gizi","Enzim pepsin bekerja optimal di lingkungan ...",["Sangat asam di lambung","Basa di usus besar","Netral di mulut","Basa di pankreas"],0,"Pepsin diaktifkan dari pepsinogen oleh asam lambung dan bekerja optimal pada pH rendah."],["gizi","Sebagian besar penyerapan zat gizi berlangsung di ...",["Usus halus","Kerongkongan","Lambung bagian atas","Rektum"],0,"Permukaan usus halus yang luas dengan vili dan mikrovili menjadi lokasi utama absorpsi nutrisi."],["gizi","Apa fungsi garam empedu dalam pencernaan lemak?",["Mengemulsikan lemak agar mudah dicerna lipase","Memecah protein menjadi asam amino","Mengubah glukosa menjadi glikogen","Menghasilkan asam lambung"],0,"Garam empedu membantu emulsifikasi lemak dan pembentukan misel untuk mendukung absorpsi lipid."],["gizi","Zat besi heme umumnya memiliki bioavailabilitas lebih tinggi daripada zat besi non-heme karena ...",["Lebih mudah diserap dan lebih sedikit dipengaruhi komponen makanan","Tidak memerlukan proses absorpsi","Hanya ditemukan dalam sayuran","Selalu larut sempurna dalam air"],0,"Zat besi heme dari pangan hewani cenderung diserap lebih efisien dibanding bentuk non-heme."],["gizi","Serat larut dapat membantu menurunkan LDL antara lain dengan ...",["Mengikat asam empedu dan meningkatkan pengeluarannya","Menghentikan produksi sel darah merah","Meningkatkan penyerapan kolesterol","Mengubah protein menjadi glukosa"],0,"Serat larut tertentu meningkatkan ekskresi asam empedu sehingga hati menggunakan kolesterol untuk menggantinya."],["gizi","Asam amino esensial disebut esensial karena ...",["Tubuh tidak dapat membuatnya dalam jumlah cukup sehingga perlu dari makanan","Hanya dipakai saat olahraga","Tidak digunakan untuk membangun protein","Hanya ada dalam buah"],0,"Asam amino esensial harus diperoleh dari makanan karena sintesis tubuh tidak mencukupi kebutuhan."],["gizi","Indeks glikemik suatu makanan menggambarkan ...",["Respons kenaikan glukosa darah setelah konsumsi karbohidrat dibanding standar","Jumlah protein per gram","Kandungan vitamin C","Jumlah kalori dari lemak saja"],0,"Indeks glikemik membandingkan respons glukosa darah terhadap karbohidrat tersedia dari makanan dengan pangan acuan."],["gizi","Mengapa rehidrasi oral efektif pada diare?",["Kotranspor natrium-glukosa di usus tetap berfungsi dan membantu penyerapan air","Larutan membunuh semua virus","Larutan menghentikan gerak usus sepenuhnya","Glukosa mengikat seluruh bakteri"],0,"Transporter natrium-glukosa tetap aktif pada banyak diare, sehingga campuran oralit membantu absorpsi natrium dan air."],["imun","Vaksin umumnya melindungi tubuh dengan cara ...",["Melatih sistem imun mengenali antigen dan membentuk memori imun","Menggantikan seluruh sel darah putih","Membunuh semua mikroorganisme di lingkungan","Meningkatkan suhu tubuh secara permanen"],0,"Vaksin memicu respons imun adaptif dan memori sehingga respons terhadap paparan berikutnya lebih cepat."],["imun","Antibodi terutama diproduksi oleh ...",["Sel plasma yang berasal dari limfosit B","Sel darah merah","Trombosit","Neuron motorik"],0,"Limfosit B yang berdiferensiasi menjadi sel plasma menghasilkan antibodi."],["imun","Antibiotik tidak efektif untuk mengobati influenza karena influenza disebabkan oleh ...",["Virus","Bakteri gram positif","Jamur","Parasit usus"],0,"Antibiotik menargetkan struktur atau proses bakteri, bukan virus influenza."],["imun","Apa fungsi utama sel T sitotoksik (CD8+)?",["Membunuh sel tubuh yang terinfeksi atau abnormal","Menghasilkan hemoglobin","Membawa oksigen","Menghasilkan empedu"],0,"Sel T CD8+ mengenali antigen pada MHC kelas I dan dapat menginduksi kematian sel target."],["imun","Resistensi antibiotik terutama berkembang melalui ...",["Seleksi dan penyebaran mikroorganisme yang memiliki mekanisme tahan obat","Tubuh manusia menjadi kebal terhadap antibiotik","Antibiotik berubah menjadi virus","Minum air dingin setelah obat"],0,"Paparan antibiotik menyeleksi bakteri yang memiliki mekanisme resistensi; penggunaan tidak tepat dapat mempercepat proses ini."],["imun","Masa inkubasi penyakit adalah ...",["Waktu antara masuknya agen infeksi dan munculnya gejala","Lama seseorang minum obat","Waktu setelah sembuh total","Durasi pembentukan antibodi seumur hidup"],0,"Masa inkubasi adalah interval dari paparan/infeksi hingga gejala pertama muncul."],["imun","Manakah contoh imunitas pasif alami?",["Antibodi ibu yang ditransfer melalui plasenta ke janin","Antibodi setelah vaksinasi","Respons setelah infeksi alami","Aktivasi sel T setelah imunisasi"],0,"Antibodi maternal, terutama IgG melalui plasenta, memberikan perlindungan pasif pada bayi."],["imun","Mengapa mencuci tangan dengan sabun efektif terhadap banyak kuman?",["Sabun membantu melepaskan kotoran dan mikroba dari kulit saat dibilas","Sabun membuat kulit steril permanen","Sabun menggantikan vaksin","Sabun meningkatkan antibodi dalam darah seketika"],0,"Gesekan, surfaktan, dan pembilasan membantu mengangkat mikroorganisme dari permukaan tangan."],["imun","Apa arti istilah zoonosis?",["Penyakit infeksi yang dapat menular antara hewan dan manusia","Penyakit khusus tulang","Gangguan hormon tiroid","Penyakit akibat kekurangan vitamin"],0,"Zoonosis adalah penyakit atau infeksi yang secara alami dapat berpindah antara hewan vertebrata dan manusia."],["imun","Peradangan akut umumnya ditandai oleh ...",["Vasodilatasi dan peningkatan permeabilitas pembuluh darah","Penurunan aliran darah lokal hingga nol","Hilangnya semua leukosit","Tidak adanya mediator kimia"],0,"Inflamasi akut melibatkan perubahan vaskular dan perekrutan leukosit ke jaringan yang mengalami cedera atau infeksi."],["otak","Bagian otak yang paling berperan dalam koordinasi gerak dan keseimbangan adalah ...",["Serebelum","Hipotalamus","Medula spinalis bagian sakral saja","Kelenjar pineal"],0,"Serebelum membantu koordinasi, ketepatan gerak, pembelajaran motorik, dan keseimbangan."],["otak","Hipokampus memiliki peran penting dalam ...",["Pembentukan memori deklaratif baru","Pemompaan darah","Penyaringan urin","Produksi hormon insulin"],0,"Hipokampus berperan penting dalam konsolidasi memori baru, terutama memori deklaratif."],["otak","Neurotransmiter utama pada sambungan neuromuskular rangka adalah ...",["Asetilkolin","Dopamin","Serotonin","Histamin"],0,"Neuron motorik melepaskan asetilkolin yang mengaktifkan reseptor nikotinik pada serat otot."],["otak","Apa fungsi mielin pada akson neuron?",["Mempercepat hantaran impuls melalui konduksi saltatori","Menghasilkan sel darah putih","Menyimpan glukosa","Menghentikan semua impuls saraf"],0,"Mielin mengisolasi akson dan memungkinkan impuls melompat antar nodus Ranvier."],["otak","Gangguan tidur kronis dapat memengaruhi fungsi kognitif terutama melalui ...",["Gangguan perhatian, memori, dan regulasi emosi","Peningkatan permanen jumlah neuron","Penguatan semua refleks tanpa batas","Penghentian metabolisme otak"],0,"Kurang tidur mengganggu jaringan perhatian, konsolidasi memori, dan pengaturan emosi."],["otak","Sawar darah-otak (blood-brain barrier) terutama berfungsi untuk ...",["Mengatur selektif pertukaran zat antara darah dan jaringan otak","Menghentikan seluruh aliran darah ke otak","Menyaring urine","Membentuk cairan empedu"],0,"Sawar darah-otak melindungi lingkungan saraf dengan mengatur secara selektif zat yang dapat masuk."],["otak","Apa yang dimaksud homeostasis?",["Pemeliharaan kondisi internal tubuh dalam rentang relatif stabil","Peningkatan suhu tubuh tanpa batas","Penghentian seluruh proses metabolisme","Perubahan organ secara acak"],0,"Homeostasis menjaga parameter internal seperti suhu, pH, dan glukosa tetap dalam rentang yang mendukung fungsi tubuh."],["otak","Dalam epidemiologi, insidensi mengukur ...",["Jumlah kasus baru dalam populasi berisiko selama periode tertentu","Semua kasus lama dan baru pada satu waktu","Jumlah kematian dari seluruh sebab saja","Jumlah tempat tidur rumah sakit"],0,"Insidensi berfokus pada kasus baru dan membantu menggambarkan risiko terjadinya penyakit."],["otak","Sensitivitas suatu tes diagnostik adalah kemampuannya untuk ...",["Mengidentifikasi dengan benar orang yang benar-benar memiliki penyakit","Mengidentifikasi orang sehat dengan benar","Menentukan tingkat keparahan semua penyakit","Memprediksi respons obat secara pasti"],0,"Sensitivitas adalah proporsi orang yang sakit yang memperoleh hasil tes positif (true positive rate)."],["otak","Nilai prediksi positif sebuah tes akan cenderung meningkat ketika ...",["Prevalensi penyakit dalam populasi yang diuji meningkat, dengan karakteristik tes tetap","Prevalensi selalu turun","Sensitivitas tes menjadi nol","Semua hasil tes diabaikan"],0,"Dengan sensitivitas dan spesifisitas tetap, prevalensi lebih tinggi umumnya meningkatkan peluang bahwa hasil positif benar-benar sakit."]];
let questionIndex = 0, quizScore = 0, questionAnswered = false, activeQuestions = questions.slice();
function loadQuiz() {
  questionAnswered = false;
  const question = activeQuestions[questionIndex];
  byId("number").textContent = "Pertanyaan " + (questionIndex + 1) + "/" + activeQuestions.length;
  byId("quizProgress").style.width = (questionIndex / activeQuestions.length * 100) + "%";
  byId("question").textContent = question[1];
  byId("feedback").textContent = "";
  byId("explanation").hidden = true;
  byId("nextButton").hidden = true;
  byId("nextButton").textContent = questionIndex === activeQuestions.length - 1 ? "Lihat Hasil 🏆" : "Selanjutnya →";
  const answers = byId("answers"); answers.textContent = "";
  question[2].forEach(function(answer, index) {
    const button = document.createElement("button"); button.type = "button"; button.className = "answer";
    button.textContent = String.fromCharCode(65 + index) + ". " + answer;
    button.addEventListener("click", function(){ answerQuestion(index, button); }); answers.appendChild(button);
  });
}
function answerQuestion(selectedIndex, selectedButton) {
  if (questionAnswered) return; questionAnswered = true;
  const q = activeQuestions[questionIndex], correctIndex = q[3];
  byId("answers").querySelectorAll("button").forEach(function(button,index){button.disabled=true;if(index===correctIndex)button.classList.add("correct");});
  if(selectedIndex===correctIndex){quizScore++;byId("feedback").textContent="✅ Benar!";}else{selectedButton.classList.add("wrong");byId("feedback").textContent="❌ Belum tepat. Jawaban: "+q[2][correctIndex];}
  byId("explanation").textContent="Pembahasan: "+q[4]; byId("explanation").hidden=false;
  byId("quizProgress").style.width=((questionIndex+1)/activeQuestions.length*100)+"%";
  byId("nextButton").hidden=false;
}
function nextQuestion() {
  questionIndex++;
  if(questionIndex<activeQuestions.length){loadQuiz();return;}
  byId("quizGame").hidden=true;byId("result").hidden=false;
  byId("score").textContent=quizScore+"/"+activeQuestions.length;
  const pct=quizScore/activeQuestions.length;
  byId("message").textContent=pct===1?"Luar biasa! Semua jawaban benar! 🎉":pct>=.8?"Hebat, pemahaman kesehatanmu sangat kuat!":pct>=.6?"Bagus! Pelajari pembahasan untuk meningkatkan skor.":"Terus belajar. Baca pembahasan setiap soal dan coba lagi!";
}
function restartQuiz() {
  const mode=byId("quizMode").value;
  activeQuestions=mode==="all"?questions.slice():questions.filter(function(q){return q[0]===mode;});
  questionIndex=0;quizScore=0;byId("quizGame").hidden=false;byId("result").hidden=true;loadQuiz();
}
byId("quizMode").addEventListener("change",restartQuiz);
byId("nextButton").addEventListener("click",nextQuestion);
byId("restartQuiz").addEventListener("click",restartQuiz);
loadQuiz();

/* Artikel */
document.querySelectorAll("[data-article]").forEach(function(button) {
  button.addEventListener("click", function() {
    const article = button.closest(".article-content");
    const body = article ? article.querySelector(".article-body") : null;
    if (!body) return;
    const isOpen = body.style.display === "block";
    body.style.display = isOpen ? "none" : "block";
    button.textContent = isOpen ? "Baca selengkapnya ↓" : "Tutup artikel ↑";
  });
});

/* Tips */
const tips = [
  "Perbanyak buah dan sayuran untuk mendapatkan vitamin, mineral, dan serat.",
  "Biasakan mencuci tangan dengan sabun sebelum makan.",
  "Lakukan aktivitas fisik secara teratur sesuai kemampuan.",
  "Penuhi kebutuhan cairan tubuh dengan minum air.",
  "Batasi makanan tinggi gula, garam, dan lemak.",
  "Tidur cukup dan jaga jadwal istirahat.",
  "Luangkan waktu untuk relaksasi dan menjaga kesehatan mental."
];
let tipIndex = 0;
byId("nextTip").addEventListener("click", function() {
  tipIndex = (tipIndex + 1) % tips.length;
  byId("tipText").textContent = tips[tipIndex];
});



/* Estimasi denyut nadi dari perubahan warna jari (PPG kamera).
   Browser mewajibkan izin pengguna dan secure context. */
let pulseStream=null,pulseTimer=null,pulseSamples=[],pulseMeasuring=false;
const pulseVideo=byId("pulseVideo"),pulseCanvas=byId("pulseCanvas");
const pulseCtx=pulseCanvas.getContext("2d",{willReadFrequently:true});
function pulseStatus(message){byId("cameraStatus").textContent=message;}
function stopCameraPulse(message){
 pulseMeasuring=false;
 if(pulseTimer!==null){clearInterval(pulseTimer);pulseTimer=null;}
 if(pulseStream){pulseStream.getTracks().forEach(t=>t.stop());pulseStream=null;}
 pulseVideo.srcObject=null;pulseVideo.hidden=true;
 byId("startCameraHR").disabled=false;byId("stopCameraHR").disabled=true;
 if(message)pulseStatus(message);
}
async function startCameraPulse(){
 if(!navigator.mediaDevices||!navigator.mediaDevices.getUserMedia){
  pulseStatus("Kamera memerlukan browser yang mendukung dan halaman HTTPS (atau localhost).");return;
 }
 byId("startCameraHR").disabled=true;pulseStatus("Meminta izin kamera...");
 try{
  pulseStream=await navigator.mediaDevices.getUserMedia({audio:false,video:{facingMode:{ideal:"environment"},width:{ideal:640},height:{ideal:480}}});
  pulseVideo.srcObject=pulseStream;pulseVideo.hidden=false;await pulseVideo.play();
  const track=pulseStream.getVideoTracks()[0];
  if(track&&track.getCapabilities){
   const caps=track.getCapabilities();
   if(caps.torch){try{await track.applyConstraints({advanced:[{torch:true}]});}catch(e){}}
  }
  pulseSamples=[];pulseMeasuring=true;byId("stopCameraHR").disabled=false;
  pulseStatus("Kamera aktif. Tutupi lensa dengan ujung jari, jangan menekan kuat, dan tetap diam selama 20–30 detik.");
  pulseTimer=setInterval(samplePulseCamera,100);
 }catch(error){
  stopCameraPulse("");
  let msg="Kamera tidak dapat diakses. Periksa izin kamera dan coba lagi.";
  if(error&&(error.name==="NotAllowedError"||error.name==="PermissionDeniedError"))msg="Izin kamera ditolak. Izinkan kamera untuk website ini di pengaturan browser.";
  else if(error&&error.name==="NotFoundError")msg="Kamera tidak ditemukan.";
  else if(error&&error.name==="NotReadableError")msg="Kamera sedang digunakan aplikasi lain. Tutup aplikasi tersebut lalu coba lagi.";
  pulseStatus(msg);
 }
}
function samplePulseCamera(){
 if(!pulseMeasuring||pulseVideo.readyState<2)return;
 try{
  pulseCtx.drawImage(pulseVideo,0,0,64,64);
  const px=pulseCtx.getImageData(0,0,64,64).data;let red=0,green=0,n=0;
  for(let i=0;i<px.length;i+=4){red+=px[i];green+=px[i+1];n++;}
  const now=performance.now(),r=red/n,g=green/n;
  pulseSamples.push({t:now,v:r-g,red:r});
  while(pulseSamples.length&&now-pulseSamples[0].t>10000)pulseSamples.shift();
  if(pulseSamples.length<40){pulseStatus("Mengumpulkan sinyal kamera...");return;}
  const recent=pulseSamples.filter(x=>now-x.t<8000);
  const mean=recent.reduce((a,x)=>a+x.v,0)/recent.length;
  const sd=Math.sqrt(recent.reduce((a,x)=>a+(x.v-mean)*(x.v-mean),0)/recent.length);
  if(sd<0.7||recent[recent.length-1].red<30){pulseStatus("Sinyal lemah. Pastikan jari menutupi lensa dan tetap diam.");return;}
  const threshold=mean+sd*0.3,peaks=[];
  for(let i=1;i<recent.length-1;i++){
   if(recent[i].v>threshold&&recent[i].v>=recent[i-1].v&&recent[i].v>recent[i+1].v){
    if(!peaks.length||recent[i].t-peaks[peaks.length-1].t>350)peaks.push(recent[i].t);
   }
  }
  const intervals=[];
  for(let i=1;i<peaks.length;i++){const dt=peaks[i]-peaks[i-1];if(dt>=400&&dt<=1500)intervals.push(dt);}
  if(intervals.length>=2){
   intervals.sort((a,b)=>a-b);const bpm=Math.round(60000/intervals[Math.floor(intervals.length/2)]);
   if(bpm>=40&&bpm<=180){byId("cameraBpm").textContent=bpm+" BPM";byId("hrBpm").value=String(bpm);pulseStatus("Perkiraan BPM terdeteksi. Jaga jari stabil; hasil kamera dapat tidak akurat.");}
   else pulseStatus("Sinyal belum stabil. Tetap diam dan coba lagi.");
  }else pulseStatus("Membaca denyut dari perubahan warna jari... tetap diam.");
 }catch(error){pulseStatus("Gagal membaca video kamera. Coba mulai ulang.");}
}
byId("startCameraHR").addEventListener("click",startCameraPulse);
byId("stopCameraHR").addEventListener("click",()=>stopCameraPulse("Pengukuran dihentikan."));
window.addEventListener("pagehide",()=>stopCameraPulse(""));

/* Strava-style activity calculator and heart-rate zones */
function loadSportHistory(){
  try {
    const data = JSON.parse(localStorage.getItem("healthySportHistory") || "[]");
    byId("sportHistory").innerHTML = data.length
      ? "<b>Riwayat latihan:</b><br>" + data.slice(0,5).map(x => escapeSport(x.date) + " — " + escapeSport(x.type) + ", " + x.distance + " km, " + x.duration + " menit").join("<br>")
      : "Belum ada aktivitas tersimpan.";
  } catch(e) { byId("sportHistory").textContent = "Riwayat belum dapat dibaca di browser ini."; }
}
function escapeSport(value){
  return String(value).replace(/[&<>"']/g, function(c){return {"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#39;"}[c];});
}
byId("calcSport").addEventListener("click", function(){
  const type = byId("sportType").value;
  const distance = Number(byId("sportDistance").value);
  const duration = Number(byId("sportDuration").value);
  const weight = Number(byId("sportWeight").value);
  if (!(distance > 0 && duration > 0 && weight > 0)) {
    byId("sportResult").textContent = "Isi jarak, durasi, dan berat badan dengan angka yang valid.";
    return;
  }
  const pace = duration / distance;
  const speed = distance / (duration / 60);
  const mets = type === "running" ? 9.8 : type === "cycling" ? 7.5 : 3.5;
  const calories = Math.round(mets * 3.5 * weight / 200 * duration);
  const paceText = Math.floor(pace) + ":" + String(Math.round((pace % 1) * 60)).padStart(2,"0");
  const typeName = type === "running" ? "Lari" : type === "cycling" ? "Bersepeda" : "Jalan kaki";
  byId("sportResult").innerHTML = "<b>" + typeName + "</b><br>⏱ Pace: <b>" + paceText + " menit/km</b><br>🚀 Kecepatan rata-rata: <b>" + speed.toFixed(2) + " km/jam</b><br>🔥 Estimasi energi: <b>" + calories + " kkal</b>";
  try {
    const history = JSON.parse(localStorage.getItem("healthySportHistory") || "[]");
    history.unshift({date:new Date().toLocaleDateString("id-ID"),type:typeName,distance:Number(distance.toFixed(2)),duration:Number(duration.toFixed(1))});
    localStorage.setItem("healthySportHistory", JSON.stringify(history.slice(0,20)));
    loadSportHistory();
  } catch(e) { byId("sportHistory").textContent = "Hasil dihitung, tetapi browser tidak mengizinkan penyimpanan riwayat."; }
});
byId("checkHR").addEventListener("click", function(){
  const age = Number(byId("hrAge").value), bpm = Number(byId("hrBpm").value);
  if (!(age >= 10 && age <= 100 && bpm >= 30 && bpm <= 240)) {
    byId("hrResult").textContent = "Masukkan usia 10–100 tahun dan detak jantung 30–240 BPM.";
    return;
  }
  const max = 220 - age, pct = bpm / max * 100;
  let zone, advice;
  if (pct < 50) { zone = "Zona 1 · Sangat ringan"; advice = "Intensitas ringan, cocok untuk pemanasan atau pemulihan."; }
  else if (pct < 60) { zone = "Zona 1 · Ringan"; advice = "Aktivitas ringan; tubuh bekerja dengan santai."; }
  else if (pct < 70) { zone = "Zona 2 · Aerobik ringan"; advice = "Intensitas nyaman untuk membangun daya tahan."; }
  else if (pct < 80) { zone = "Zona 3 · Sedang"; advice = "Latihan mulai terasa menantang."; }
  else if (pct < 90) { zone = "Zona 4 · Berat"; advice = "Intensitas tinggi; lakukan sesuai kemampuan dan kondisi."; }
  else { zone = "Zona 5 · Sangat berat"; advice = "Usaha sangat tinggi; tidak cocok dipertahankan lama oleh kebanyakan orang."; }
  byId("hrMax").textContent = max + " BPM";
  byId("hrPercent").textContent = pct.toFixed(0) + "%";
  byId("hrResult").innerHTML = "<b>" + zone + "</b><br>" + bpm + " BPM dari estimasi maksimal " + max + " BPM.<br>" + advice;
});
loadSportHistory();

/* Inisialisasi terakhir setelah elemen halaman tersedia. */
loadChecks();
window.requestAnimationFrame(drawChart);
</script>
</body>
</html>
