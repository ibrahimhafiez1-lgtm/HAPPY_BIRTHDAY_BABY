HAPPY BIRTHDAY BABBYYYYY
<html lang="ms">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Happy Birthday Shuraya 🎀🎉</title>

<link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@400;600;700&display=swap" rel="stylesheet">

<style>
    /* ---------- wallpaper + base ---------- */
    body{
        margin:0;
        font-family:'Quicksand',sans-serif;
        background: linear-gradient(180deg,#fff1f6 0%, #ffd9ec 60%), url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="200" height="200"><defs><linearGradient id="g" x1="0" x2="1"><stop offset="0" stop-color="%23fff6fb"/><stop offset="1" stop-color="%23ffeaf4"/></linearGradient></defs><rect width="100%" height="100%" fill="url(%23g)"/><g fill-opacity="0.06" fill="%23ff5fa2"><circle cx="20" cy="20" r="6"/><circle cx="60" cy="40" r="6"/><circle cx="120" cy="80" r="6"/><circle cx="160" cy="20" r="6"/></g></svg>') repeat;
        background-size: cover;
        text-align:center;
        -webkit-font-smoothing:antialiased;
        overflow-x:hidden;
        color:#4a0033;
    }

    h1,h2,h3{ color:#ff5fa2; margin:8px 0; }
    .glow{ font-size:28px; font-weight:700; color:#ff2e7e; text-shadow:0 0 10px #ffb3d9; }

    /* ---------- nav ---------- */
    .nav{
        background:rgba(255,255,255,0.95);
        padding:12px;
        position:sticky;
        top:0;
        z-index:1000;
        border-bottom:3px solid #ffb3d9;
        display:flex;
        gap:6px;
        justify-content:center;
        flex-wrap:wrap;
    }
    .nav button{
        background:#ff5fa2;
        border:none;
        padding:8px 14px;
        color:#fff;
        border-radius:10px;
        font-weight:700;
        cursor:pointer;
    }
    .nav button:hover{ transform:scale(1.03); }

    /* ---------- card sections ---------- */
    .section{
        background:rgba(255,255,255,0.98);
        margin:24px auto;
        width:90%;
        max-width:840px;
        padding:22px;
        border-radius:18px;
        box-shadow:0 6px 18px rgba(255,105,180,0.18);
        border:2px solid rgba(255,179,217,0.6);
    }

    img, video { width:100%; height:auto; max-width:420px; border-radius:14px; border:4px solid #ffb3d9; display:block; margin:12px auto; }

    /* ---------- slideshow ---------- */
    .slideshow-container{ max-width:420px; margin:12px auto; position:relative; }
    .mySlides{ display:none; }
    .dot-container{ margin-top:8px; text-align:center; }
    .dot{ height:12px; width:12px; margin:0 4px; background:#ffd0e3; border-radius:50%; display:inline-block; cursor:pointer; }
    .active{ background:#ff2e7e; }

    /* ---------- lock screen modal ---------- */
    #lockScreen{
        position:fixed; inset:0;
        background:linear-gradient(180deg,#fff6fb,#fff);
        display:flex; align-items:center; justify-content:center;
        z-index:10000; flex-direction:column; padding:20px; text-align:center;
    }
    .btn{
        background:#ff5fa2; color:#fff; border:none; padding:10px 16px; border-radius:12px; cursor:pointer; font-weight:700;
    }

    .overlay{ position:fixed; inset:0; display:none; align-items:center; justify-content:center; background:rgba(0,0,0,0.5); z-index:10001; }
    .overlay.open{ display:flex; }
    .modal{ background:#fff; border-radius:12px; padding:18px; max-width:420px; width:92%; position:relative; box-shadow:0 10px 30px rgba(0,0,0,0.15); }
    .closeBtn{ position:absolute; right:12px; top:8px; border:none; background:none; font-size:18px; cursor:pointer; }

    /* ---------- balloons & love ---------- */
    .balloonEmoji{
        position:fixed;
        bottom:-120px;
        pointer-events:none;
        z-index:9998;
        transform-origin:center;
        animation:floatUp linear forwards;
    }
    @keyframes floatUp{
        to{ transform:translateY(-120vh) rotate(30deg); opacity:0; }
    }

    .loveFloating{
        position:fixed;
        top:-40px;
        pointer-events:none;
        z-index:9999;
        animation:loveFall linear forwards;
    }
    @keyframes loveFall{
        to{ transform:translateY(110vh) scale(1.4); opacity:0; }
    }

    /* ---------- small controls ---------- */
    .music-controls{ display:flex; gap:10px; justify-content:center; align-items:center; margin-top:10px; }
    .small-btn{ background:#fff; border:2px solid #ffb3d9; padding:6px 10px; border-radius:10px; cursor:pointer; font-weight:700; }
    .title-small{ font-size:14px; color:#ff4b9a; margin:6px 0; }

    /* ---------- responsive ---------- */
    @media (max-width:480px){
        .section{ padding:16px; margin:18px 8px; }
        .glow{ font-size:22px; }
    }
</style>
</head>
<body>

<!-- Tone.js (CDN) -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/tone/14.8.39/Tone.min.js"></script>

<!-- ---------- LOCK SCREEN ---------- -->
<div id="lockScreen">
    <h2 class="glow">Happy Birthday, Shuraya 🎀</h2>
    <p>Website ni ada password. Tekan butang di bawah untuk masuk.</p>
    <button class="btn" id="enterBtn">MASUK</button>
</div>

<!-- PASSWORD MODAL -->
<div class="overlay" id="pwdModal">
    <div class="modal">
        <button class="closeBtn" onclick="closePwd()">✕</button>
        <h3>Masukkan Password</h3>
        <input id="pwdInput" type="password" placeholder="Password" style="padding:10px;width:92%;margin-top:10px;border-radius:10px;border:2px solid #ffb3d9;">
        <br><br>
        <button class="btn" id="pwdCheck">Buka</button>
        <p style="margin-top:8px;font-size:13px;color:#ff5fa2">Password default: <b>HB BABY</b></p>
    </div>
</div>

<!-- ---------- NAV ---------- -->
<div class="nav">
    <button onclick="showSection('home')">Home</button>
    <button onclick="showSection('slideshow')">Gambar</button>
    <button onclick="showSection('video')">Video</button>
    <button onclick="showSection('surat')">Surat</button>
    <button onclick="showSection('memory')">Gambar Kita</button>
    <button onclick="showSection('why')">Kenangan</button>
    <button onclick="showSection('wish')">Ucapan Panjang</button>
</div>

<!-- ---------- HOME ---------- -->
<section id="home" class="section" style="display:block">
    <h1 class="glow">Happy Birthday, Baby 🎀💗</h1>
    <h3>23 November 2005</h3>
    <p>Hari ni hari istimewa untuk seorang yang bermakna… iaitu baby  💗</p>

    <h2>🎀 Countdown Ke Birthday Shuraya</h2>
    <h1 id="countdown"></h1>

    <div class="music-controls" aria-hidden="false">
        <div class="title-small"></div>
        <button id="playPauseBtn" class="small-btn">Play</button>
        <button id="stopBtn" class="small-btn">Stop</button>
    </div>
</section>

<!-- ---------- SLIDESHOW ---------- -->
<section id="slideshow" class="section" style="display:none">
    <h2>📸 Gambar Baby</h2>
    <div class="slideshow-container">
        <div class="mySlides"><img src="photo_2025-11-16_22-36-49.jpg" alt="pic1"></div>
        <div class="mySlides"><img src="photo_2025-11-16_22-58-39.jpg" alt="pic2"></div>
        <div class="mySlides"><img src="photo_2025-11-15_23-01-55.jpg" alt="pic3"></div>
        <div class="mySlides"><img src="photo_2025-11-16_22-58-30.jpg" alt="pic4"></div>
    </div>
    <div class="dot-container">
        <span class="dot" onclick="currentSlide(1)"></span>
        <span class="dot" onclick="currentSlide(2)"></span>
        <span class="dot" onclick="currentSlide(3)"></span>
        <span class="dot" onclick="currentSlide(4)"></span>
    </div>
</section>

<!-- ---------- VIDEO ---------- -->
<section id="video" class="section" style="display:none">
    <h2>🎥 Video Untuk Baby</h2>
    <video controls>
        <source src="video_2025-11-16_22-36-23.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>
</section>

<!-- ---------- SURAT ---------- -->
<section id="surat" class="section" style="display:none">
    <h2>💌 Surat Untuk Baby</h2>
    <p style="font-size:18px;">
        BABYYYYYYY…
Hari ini hari yang sangat istimewa sebab family dan saya dapat seorang insan yang baik, lembut hati dan membawa cahaya pada semua orang sekeliling — termasuk saya.

Saya harap hari lahir baby kali ni penuh dengan ketenangan, rezeki yang baik, dan senyuman yang tak pernah hilang. Awak layak rasa disayangi, diraikan, dan dihargai. Walaupun kadang baby kuat pendam,kuat merajuk,kuat marah,kuat semua mende kuat.hahahah.saya nak baby tahu… baby sebenarnya lebih kuat daripada yang baby fikir.

Terima kasih sebab muncul dalam hidup saya, dan terima kasih sebab selalu buat saya rasa bermakna. Saya doakan semua impian awak jadi kenyataan satu hari nanti.

Selamat Hari Lahir, baby.
Saya bangga dengan baby.
💗🎀  
    </p>
</section>

<!-- ---------- MEMORY ---------- -->
<section id="memory" class="section" style="display:none">
    <h2>📚 Gambar Kita</h2>
    <img src="photo_2025-11-16_23-15-56.jpg" alt="memori">
</section>

<!-- ---------- WHY ---------- -->
<section id="why" class="section" style="display:none">
    <h2>🌸 Kenangan</h2>
    <ul style="list-style:none;font-size:18px;line-height:2;">
        <li>• Hi.Shuraya,Betul ke awak suke saya. Baby masih ingat ayat saya untuk kenal dengan baby. Saya ter crush dengan baby tau dari sejak saya pandang baby tetapi saya tanak couple saya nak suke dalam diam dan iye lah time tu baby budak hot kan ramai orang suke termasuk senior.Tapi bile kawan saya cakap saya suke baby kawan baby cakap baby suke saya itu lah peluang saya untuk chat baby.Selepas itu, hahahah macam nak buat karangan pulak....kita putus walaupun kita putus iye lah salah saya dalam hubungan ni saya banyak salah tetapi semasa kita putus saya masih akui baby tu awek saya....Banyak lagi kenangan kita macam ii kita hadap sedar ii dah 7 tahun saya harap saya ada dengan baby sampai hari tua baby birthday baby yang ke 80 saya akan buat website ni jugak okay lah pergi ke next button okay 💗</li>
       
    </ul>
</section>

<!-- ---------- WISH ---------- -->
<section id="wish" class="section" style="display:none">
    <h2>🎂 Ucapan Panjang Untuk Baby</h2>
    <p style="font-size:19px;">Selamat Hari Lahir, Baby yang ke 20 🎀💗 semoga itu ini hahaha gurau. ii ..semoag baby di panjangkan umur, di permudahkan segala urusan, diberi kesihatan yang baik,semoga baby di murahkan rezeki seperti masa yang tak pernah berhenti,semoga baby dapat apa yang baby nak,semoga baby last sem ni dapat dekan dapat naikkan pointer dan dapat bangga kan family....apa apa pun good luck final baby...pada hari lahir baby ni saya nak mintak maaaf atas kesalahn saya sepanjang kita kenal dari pelbagai kesalahan saya nak baby tahu saya betul sayanag kan baby saya takda orang lain tau...Saya harap baby happy pada hari ni dan apa yang saya buat wish betul ii panjang dekat whatapps lenguh ni type gune laptop  .</p>
</section>

<!-- ---------- SCRIPTS: UI, slideshow, countdown, balloons/love ---------- -->
<script>
/* ---------- UI & PASSWORD (keep your password value) ---------- */
const DEFAULT_PASSWORD = 'HB BABY';
const pwdModal = document.getElementById('pwdModal');
const pwdInput = document.getElementById('pwdInput');
const lockScreen = document.getElementById('lockScreen');

document.getElementById('enterBtn').addEventListener('click', ()=> {
    pwdModal.classList.add('open');
});

function closePwd(){
    pwdModal.classList.remove('open');
    if (pwdInput) pwdInput.value = '';
}

document.getElementById('pwdCheck').addEventListener('click', ()=> {
    if (!pwdInput) return;
    if (pwdInput.value === DEFAULT_PASSWORD){
        // unlock UI
        pwdModal.classList.remove('open');
        lockScreen.style.display = 'none';
        showSection('home');
        // start the Tone.js song (needs user gesture)
        try { unlockWithTone(); } catch(e){ console.warn(e); }
    } else {
        alert('Password salah!');
        pwdInput.value = '';
    }
});

/* ---------- Section navigation ---------- */
function showSection(id){
    const sections = ['home','slideshow','video','surat','memory','why','wish'];
    sections.forEach(s => {
        const el = document.getElementById(s);
        if (el) el.style.display = (s === id ? 'block' : 'none');
    });
    window.scrollTo({top:0, behavior:'smooth'});
}

/* ---------- Countdown ---------- */
function countdown(){
    const target = new Date('Nov 23, 2025 00:00:00').getTime();
    const el = document.getElementById('countdown');
    setInterval(()=>{
        const now = Date.now();
        let diff = target - now;
        if (diff < 0) diff = 0;
        const d = Math.floor(diff / (1000*60*60*24));
        const h = Math.floor((diff % (1000*60*60*24)) / (1000*60*60));
        const m = Math.floor((diff % (1000*60*60)) / (1000*60));
        const s = Math.floor((diff % (1000*60)) / 1000);
        if (el) el.textContent = `${d} hari ${h} jam ${m} minit ${s} saat`;
    }, 1000);
}
countdown();

/* ---------- Slideshow (auto) ---------- */
let slideIndex = 0;
function showSlidesAuto(){
    const slides = document.getElementsByClassName('mySlides');
    const dots = document.getElementsByClassName('dot');
    for (let i=0;i<slides.length;i++) slides[i].style.display='none';
    slideIndex++;
    if (slideIndex > slides.length) slideIndex = 1;
    if (slides.length > 0) slides[slideIndex-1].style.display='block';
    for (let i=0;i<dots.length;i++) dots[i].className = dots[i].className.replace(' active','');
    if (dots[slideIndex-1]) dots[slideIndex-1].className += ' active';
    setTimeout(showSlidesAuto, 3000);
}
showSlidesAuto();
function currentSlide(n){
    slideIndex = n-1;
    showSlidesAuto();
}

/* ---------- Floating love & balloons spawn (visual) ---------- */
function spawnBalloon(){
    const b = document.createElement('div');
    b.className = 'balloonEmoji';
    b.textContent = ['🎈','🎈','🎉','🎀'][Math.floor(Math.random()*4)];
    b.style.left = Math.random()*100 + 'vw';
    b.style.fontSize = (20 + Math.random()*40) + 'px';
    b.style.animationDuration = (5 + Math.random()*6) + 's';
    document.body.appendChild(b);
    setTimeout(()=> b.remove(), 11000);
}
function spawnLove(){
    const l = document.createElement('div');
    l.className = 'loveFloating';
    l.textContent = ['💗','💕','💞','💖'][Math.floor(Math.random()*4)];
    l.style.left = Math.random()*100 + 'vw';
    l.style.fontSize = (18 + Math.random()*24) + 'px';
    l.style.animationDuration = (5 + Math.random()*5) + 's';
    document.body.appendChild(l);
    setTimeout(()=> l.remove(), 9000);
}
// spawn gently
setInterval(spawnBalloon, 900);
setInterval(spawnLove, 700);

/* ---------- Music controls (buttons) ---------- */
const playPauseBtn = document.getElementById('playPauseBtn');
const stopBtn = document.getElementById('stopBtn');
playPauseBtn.addEventListener('click', ()=> {
    if (isPlaying()) { stopBirthdaySong(); playPauseBtn.textContent='Play'; }
    else { unlockWithTone(); playPauseBtn.textContent='Pause'; }
});
stopBtn.addEventListener('click', ()=> {
    stopBirthdaySong();
    playPauseBtn.textContent='Play';
});

/* ---------- First-click mobile compatibility: try to start audio on first user gesture (if unlocked) ---------- */
document.addEventListener('click', function once(){
    // attempts will be handled by Tone.start() in unlockWithTone()
    document.removeEventListener('click', once);
});
</script>

<!-- ---------- Tone.js SONG: Anime Sweet (music-box + piano + pad) ---------- -->
<script>
// ======= CONFIG =======
const BIRTHDAY_CONFIG = { bpm: 78, volume: -8, leadVol: -3, padVol: -10, bellVol: -4 };

// create master gain
const master = new Tone.Gain().toDestination();
master.gain.value = Tone.dbToGain(BIRTHDAY_CONFIG.volume);

// instruments
const piano = new Tone.Synth({
    oscillator:{ type:'triangle' },
    envelope:{ attack:0.006, decay:0.5, sustain:0.5, release:1.2 }
}).connect(new Tone.Gain(Tone.dbToGain(BIRTHDAY_CONFIG.leadVol))).connect(master);

const musicBox = new Tone.MetalSynth({
    frequency:1200,
    envelope:{ attack:0.001, decay:1.4, release:0.8 },
    harmonicity:6,
    modulationIndex:20,
}).connect(new Tone.Gain(Tone.dbToGain(BIRTHDAY_CONFIG.bellVol))).connect(master);

const pad = new Tone.PolySynth(Tone.Synth, {
    oscillator:{ type:'sine' },
    envelope:{ attack:0.8, decay:1.2, sustain:0.6, release:2.6 }
}).connect(new Tone.Gain(Tone.dbToGain(BIRTHDAY_CONFIG.padVol))).connect(master);

const pluck = new Tone.PluckSynth({ dampening: 4000 }).connect(new Tone.Gain(Tone.dbToGain(-8))).connect(master);

// melody (original kawaii sweet) -> sequence of notes (note, duration)
const melody = [
  ['E5','8n'], ['G5','16n'], ['A5','16n'], ['G5','8n'],
  ['E5','8n'], ['D5','8n'],
  ['C5','8n'], ['E5','16n'], ['G5','16n'], ['E5','4n'],
  ['G5','8n'], ['A5','16n'], ['B5','16n'], ['A5','8n'],
  ['G5','8n'], ['E5','2n']
];

// chords (soft) play as pad
const chords = [
  { time:'0:0:0', notes:['C4','E4','G4'] },
  { time:'0:1:0', notes:['F4','A4','C5'] },
  { time:'0:2:0', notes:['G4','B4','D5'] },
  { time:'0:3:0', notes:['C4','E4','G4'] }
];

// gentle music-box pattern
const boxPattern = [
  ['C6','16n'], ['G5','16n'], ['E5','16n'], ['C5','8n'],
  ['F6','16n'], ['C6','16n'], ['A5','16n'], ['F5','8n']
];

// loops & parts
let melodyPart, chordPart, boxLoop, pluckLoop;
let playing = false;

function setupSong(){
  Tone.Transport.cancel();
  Tone.Transport.bpm.value = BIRTHDAY_CONFIG.bpm;

  // melody part
  const melodyEvents = [];
  let timeCursor = 0;
  for (let i=0;i<melody.length;i++){
    const dur = Tone.Time(melody[i][1]).toSeconds();
    melodyEvents.push([timeCursor, melody[i][0], melody[i][1]]);
    timeCursor += dur;
  }
  melodyPart = new Tone.Part((time, note) => {
    piano.triggerAttackRelease(note.note, note.dur, time);
  }, melodyEvents.map(e => [e[0], { note: e[1], dur: e[2] }]));
  melodyPart.start(0);

  // chords (pads)
  chordPart = new Tone.Part((time, value) => {
    pad.triggerAttackRelease(value, '1m', time);
  }, chords.map(c => [c.time, c.notes]));
  chordPart.start(0);

  // music box loop
  let idx = 0;
  boxLoop = new Tone.Loop(time => {
    const e = boxPattern[idx % boxPattern.length];
    musicBox.triggerAttackRelease(e[0], e[1], time);
    idx++;
  }, '16n').start(0);

  // pluck sparkle every bar
  let pi = 0;
  const pluckNotes = ['G4','E4','C4','E4'];
  pluckLoop = new Tone.Loop(time => {
    pluck.triggerAttack(pluckNotes[pi % pluckNotes.length], time, 0.6);
    pi++;
  }, '1n').start('0:0:2');
}

function startBirthdaySong(){
  if (playing) return;
  setupSong();
  master.gain.value = Tone.dbToGain(BIRTHDAY_CONFIG.volume);
  Tone.Transport.start();
  playing = true;
  // update UI
  if (document.getElementById('playPauseBtn')) document.getElementById('playPauseBtn').textContent = 'Pause';
}

function stopBirthdaySong(){
  if (!playing) return;
  Tone.Transport.stop();
  Tone.Transport.cancel();
  playing = false;
  if (document.getElementById('playPauseBtn')) document.getElementById('playPauseBtn').textContent = 'Play';
}

function isPlaying(){ return playing; }

// call this after a user gesture (we already call it on password success)
function unlockWithTone(){
  Tone.start().then(()=> {
    // small safety clear
    stopBirthdaySong();
    startBirthdaySong();
  }).catch((e)=>{
    console.warn('Audio start blocked', e);
  });
}

// expose globally for UI
window.unlockWithTone = unlockWithTone;
window.stopBirthdaySong = stopBirthdaySong;
window.isPlaying = isPlaying;
</script>

</body>
</html>
