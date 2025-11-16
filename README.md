
<html lang="ms">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday Shuraya 🎀🎉</title>

<link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@400;600;700&display=swap" rel="stylesheet">

<style>
    body {
        margin: 0;
        font-family: 'Quicksand', sans-serif;
        background: #ffd9ec;
        text-align: center;
        overflow-x: hidden;
    }

    h1, h2, h3 { color: #ff5fa2; }

    .nav {
        background: white;
        padding: 15px;
        position: sticky;
        top: 0;
        z-index: 1000;
        border-bottom: 3px solid #ffb3d9;
    }
    .nav button {
        background: #ff5fa2;
        border: none;
        padding: 10px 18px;
        margin: 5px;
        color: white;
        border-radius: 10px;
        font-weight: bold;
        cursor: pointer;
        transition: 0.2s;
    }
    .nav button:hover { transform: scale(1.05); }

    .section {
        background: white;
        margin: 30px auto;
        width: 90%;
        max-width: 800px;
        padding: 30px;
        border-radius: 18px;
        box-shadow: 0 4px 14px rgba(255, 105, 180, 0.25);
        border: 3px solid #ffb3d9;
    }

    img, video {
        width: 100%;
        height: auto;
        max-width: 350px;
        border-radius: 15px;
        border: 4px solid #ffb3d9;
    }

    .love {
        position: fixed;
        top: -10px;
        color: #ff5fa2;
        font-size: 24px;
        animation: fall 4s linear infinite;
    }
    @keyframes fall {
        to { transform: translateY(110vh); opacity: 0; }
    }

    .confetti {
        position: fixed;
        width: 10px;
        height: 10px;
        top: -10px;
        animation: confettiFall 3s linear infinite;
    }
    @keyframes confettiFall {
        to { transform: translateY(120vh) rotate(720deg); opacity: 0; }
    }

    .balloon {
        position: fixed;
        bottom: -150px;
        font-size: 40px;
        animation: balloonUp 6s ease-in infinite;
    }
    @keyframes balloonUp {
        to { transform: translateY(-120vh); }
    }

    .glow {
        font-size: 32px;
        font-weight: bold;
        color: #ff2e7e;
        text-shadow: 0 0 10px #ff5fa2, 0 0 20px #ff7fbf;
    }

    #lockScreen{
      position:fixed;inset:0;background:linear-gradient(180deg,#fff6fb,#fff);
      display:flex;align-items:center;justify-content:center;
      z-index:10000;flex-direction:column;padding:20px;text-align:center
    }
    #lockScreen h2{color:#ff5fa2;font-size:34px;margin:6px 0}
    .btn{
      background:#ff5fa2;color:#fff;border:none;padding:10px 16px;
      border-radius:12px;cursor:pointer;font-weight:700
    }

    .overlay{position:fixed;inset:0;display:none;align-items:center;
      justify-content:center;background:rgba(0,0,0,0.6);z-index:10001}
    .overlay.open{display:flex}
    .modal{background:#fff;border-radius:12px;padding:16px;
      max-width:420px;width:90%;position:relative}
    .closeBtn{position:absolute;right:12px;top:8px;border:none;background:none;
      font-size:20px;cursor:pointer}

    /* SLIDESHOW */
    .slideshow-container { max-width: 350px; margin: 20px auto; position: relative; }
    .mySlides { display: none; }
    .mySlides img { width: 100%; border-radius: 15px; }
    .dot-container { margin-top: 10px; }
    .dot {
        height: 12px;
        width: 12px;
        margin: 0 3px;
        background: #ff9bc9;
        border-radius: 50%;
        display: inline-block;
        cursor: pointer;
    }
    .active { background: #ff2e7e; }
</style>
</head>

<body>

<!-- BACKGROUND MUSIC AUTOPLAY -->
<audio id="bgm" autoplay loop>
    <source src="https://github.com/ibrahimhafiez1-lgtm/HAPPY_BIRTHDAY_BABY/blob/main/happy_birthday_cute.mp3" type="audio/mpeg">
</audio>

<!-- LOCK SCREEN -->
<div id="lockScreen">
    <h2>Happy Birthday, Shuraya 🎀</h2>
    <p>Website ni ada password. Tekan butang di bawah untuk masuk.</p>
    <button class="btn" id="enterBtn">MASUK</button>
</div>

<!-- PASSWORD MODAL -->
<div class="overlay" id="pwdModal">
    <div class="modal">
        <button class="closeBtn" onclick="closePwd()">✕</button>
        <h3>Masukkan Password</h3>
        <input id="pwdInput" type="password" placeholder="Password" style="padding:10px;width:90%;margin-top:10px;border-radius:10px;border:2px solid #ffb3d9;">
        <br><br>
        <button class="btn" id="pwdCheck">Buka</button>
        <p>Password default: <b>sayangsangat</b></p>
    </div>
</div>

<!-- NAVIGATION -->
<div class="nav">
    <button onclick="showSection('home')">Home</button>
    <button onclick="showSection('slideshow')">Gambar</button>
    <button onclick="showSection('video')">Video</button>
    <button onclick="showSection('surat')">Surat</button>
    <button onclick="showSection('memory')">Memori</button>
    <button onclick="showSection('why')">Why You’re Special</button>
    <button onclick="showSection('wish')">Ucapan Panjang</button>
</div>

<!-- HOME -->
<section id="home" class="section">
    <h1 class="glow">Happy Birthday, NURUL SHURAYA 🎀💗</h1>
    <h3>23 November 2005</h3>
    <p>Hari ni hari istimewa untuk seorang yang bermakna… iaitu awak 💗</p>

    <h2>🎀 Countdown Ke Birthday Shuraya</h2>
    <h1 id="countdown"></h1>

    <h3>🎶 Background Music</h3>
    <audio controls id="bgAudio">
        <source src="YOUR-SONG.mp3">
    </audio>
</section>

<!-- SLIDESHOW -->
<section id="slideshow" class="section" style="display:none">
    <h2>📸 Gambar Cantik Shuraya</h2>

    <div class="slideshow-container">
        <div class="mySlides fade">
            <img src="photo_2025-11-16_22-36-49.jpg">
        </div>
        <div class="mySlides fade">
            <img src="photo_2025-11-16_22-58-39.jpg">
        </div>
        <div class="mySlides fade">
            <img src="photo_2025-11-15_23-01-55.jpg">
        </div>
        <div class="mySlides fade">
            <img src="photo_2025-11-16_22-58-30.jpg">
        </div>
    </div>

    <div class="dot-container">
        <span class="dot" onclick="currentSlide(1)"></span>
        <span class="dot" onclick="currentSlide(2)"></span>
        <span class="dot" onclick="currentSlide(3)"></span>
        <span class="dot" onclick="currentSlide(4)"></span>
    </div>
</section>

<!-- VIDEO -->
<section id="video" class="section" style="display:none">
    <h2>🎥 Video Untuk Shuraya</h2>
    <video controls>
        <source src="video_2025-11-16_22-36-23.mp4" type="video/mp4">
    </video>
</section>

<!-- SURAT -->
<section id="surat" class="section" style="display:none">
    <h2>💌 Surat Untuk Shuraya</h2>
    <p style="font-size:19px;">
        Shuraya… awak sangat istimewa, lembut hati, kuat, dan berharga.
        Semoga hari lahir ni penuh kebahagiaan dan senyuman 💗
    </p>
</section>

<!-- MEMORY -->
<section id="memory" class="section" style="display:none">
    <h2>📚 Memory Page</h2>
    <img src="photo_2025-11-16_23-15-56.jpg" alt="Memori Bersama" style="max-width:350px;border-radius:15px;border:4px solid #ffb3d9;">
</section>

<!-- WHY -->
<section id="why" class="section" style="display:none">
    <h2>🌸 Kenapa Shuraya Istimewa</h2>
    <ul style="list-style:none;font-size:19px;line-height:2;">
        <li>• Awak baik hati 💗</li>
        <li>• Awak penyayang 🎀</li>
        <li>• Cantik luar & dalam 💞</li>
        <li>• Kuat walaupun pendam 💗</li>
        <li>• Buat orang rasa dihargai 🎀</li>
    </ul>
</section>

<!-- WISH -->
<section id="wish" class="section" style="display:none">
    <h2>🎂 Ucapan Panjang Untuk Shuraya</h2>
    <p style="font-size:20px;">
        Selamat Hari Lahir, Shuraya 🎀💗 Semoga hidup awak sentiasa dipenuhi kegembiraan.
    </p>
</section>

<script>
const DEFAULT_PASSWORD = 'sayangsangat';
const pwdModal = document.getElementById('pwdModal');
const pwdInput = document.getElementById('pwdInput');
const lockScreen = document.getElementById('lockScreen');

document.getElementById('enterBtn').onclick = ()=> pwdModal.classList.add('open');
function closePwd(){ pwdModal.classList.remove('open'); pwdInput.value=''; }

document.getElementById('pwdCheck').onclick = ()=>{
    if(pwdInput.value === DEFAULT_PASSWORD){
        lockScreen.style.display = 'none';
        pwdModal.classList.remove('open');
        showSection('home');
        document.getElementById('bgAudio').play().catch(()=>{});
    } else {
        alert('Password salah!');
        pwdInput.value = '';
    }
};

function showSection(id){
    ['home','slideshow','video','surat','memory','why','wish'].forEach(s=>{
        document.getElementById(s).style.display = (s===id?'block':'none');
    });
    window.scrollTo({top:0});
}

function countdown(){
    const target = new Date('Nov 23, 2025 00:00:00').getTime();
    setInterval(()=>{
        const now = new Date().getTime();
        const diff = target - now;
        const d = Math.floor(diff/(1000*60*60*24));
        const h = Math.floor((diff%(1000*60*60*24))/(1000*60*60));
        const m = Math.floor((diff%(1000*60*60))/(1000*60));
        const s = Math.floor((diff%(1000*60))/1000);
        document.getElementById('countdown').textContent = d+" hari "+h+" jam "+m+" minit "+s+" saat";
    },1000);
}
countdown();

let slideIndex = 1;
showSlides(slideIndex);
function currentSlide(n){ showSlides(slideIndex = n); }
function showSlides(n){
    let i;
    let slides = document.getElementsByClassName("mySlides");
    let dots = document.getElementsByClassName("dot");
    if(n>slides.length){ slideIndex=1 }
    if(n<1){ slideIndex=slides.length }
    for(i=0;i<slides.length;i++) slides[i].style.display="none";
    for(i=0;i<dots.length;i++) dots[i].className = dots[i].className.replace(" active", "");
    slides[slideIndex-1].style.display="block";
    dots[slideIndex-1].className += " active";
}
setInterval(()=>{ slideIndex++; showSlides(slideIndex); },3000);
</script>

<script>
window.addEventListener("click", function () {
    const bgm = document.getElementById("bgm");
    if (bgm) {
        bgm.muted = false;
        bgm.play().catch(() => {});
    }
});
</script>
</body>
</html>
