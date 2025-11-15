<!DOCTYPE html>
<html lang="ms">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Happy Birthday Shuraya 🎀</title>

    <style>
        body {
            margin: 0;
            font-family: "Poppins", sans-serif;
            background: #ffe6f2;
            overflow-x: hidden;
        }

        /* Navigation */
        nav {
            background: #ffb6d9;
            padding: 10px 20px;
            text-align: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        nav a {
            margin: 0 15px;
            text-decoration: none;
            color: white;
            font-weight: 600;
            font-size: 18px;
        }

        /* Pages style */
        section {
            padding: 40px;
            height: 100vh;
            text-align: center;
        }

        h1 {
            color: #ff4da6;
            font-size: 40px;
        }

        p {
            color: #ff1a75;
            font-size: 20px;
            max-width: 700px;
            margin: auto;
        }

        /* Button */
        .btn {
            background: #ff80bf;
            color: white;
            padding: 12px 25px;
            border: none;
            border-radius: 25px;
            font-size: 18px;
            margin-top: 20px;
        }

        /* Balloon */
        .balloon {
            position: absolute;
            bottom: -150px;
            width: 60px;
            animation: floatUp 8s infinite ease-in;
        }
        @keyframes floatUp {
            0% {transform: translateY(0);}
            100% {transform: translateY(-120vh);}
        }

        /* Confetti */
        .confetti {
            position: fixed;
            width: 10px;
            height: 10px;
            background: pink;
            top: -10px;
            animation: fall 5s infinite ease-in;
        }
        @keyframes fall {
            to { transform: translateY(110vh) rotate(360deg); }
        }
    </style>
</head>

<body>

    <!-- Navigation -->
    <nav>
        <a href="#home">Home</a>
        <a href="#wish">Wish</a>
        <a href="#memory">Memories</a>
        <a href="#gallery">Gallery</a>
    </nav>

    <!-- CONFETTI -->
    <script>
        for (let i = 0; i < 80; i++) {
            let c = document.createElement("div");
            c.className = "confetti";
            c.style.left = Math.random() * 100 + "vw";
            c.style.background = ["#ff99cc","#ff66b3","#ff4da6"][Math.floor(Math.random()*3)];
            c.style.animationDelay = Math.random() * 5 + "s";
            document.body.appendChild(c);
        }
    </script>

    <!-- HOME -->
    <section id="home">
        <h1>🎀 Happy Birthday, Nurul Shuraya! 🎀</h1>
        <p>Lahir pada: <b>23 November 2005</b></p>
        <p>
            Hari ni khas untuk awak, Shuraya.  
            Semoga hari lahir awak penuh dengan kegembiraan, senyuman & keberkatan.
            Orang yang sayang awak buat ni khas untuk awak 💗
        </p>
    </section>

    <!-- WISH -->
    <section id="wish">
        <h1>💗 Special Birthday Wish 💗</h1>
        <p>
            Selamat Hari Lahir, Shuraya!  
            Semoga panjang umur, dipermudahkan rezeki,
            dan sentiasa dilindungi Allah.  
            Awak seorang yang baik, lembut, dan berhati cantik.  
            Semoga segala impian awak satu-satu jadi kenyataan 💗
        </p>
    </section>

    <!-- MEMORY -->
    <section id="memory">
        <h1>📸 Memories</h1>
        <p>Baby boleh letak gambar & kenangan manis awak dengan Shuraya dekat sini.</p>
    </section>

    <!-- GALLERY -->
    <section id="gallery">
        <h1>🎀 Gallery</h1>
        <p>Letak gambar / video Shuraya dekat bahagian ni nanti 💞</p>
    </section>

    <!-- Balloons -->
    <script>
        for (let i = 0; i < 6; i++) {
            let b = document.createElement("img");
            b.src = "balloon.png"; /* Baby tukar ke gambar belon sendiri */
            b.className = "balloon";
            b.style.left = Math.random() * 100 + "vw";
            b.style.animationDelay = i * 2 + "s";
            document.body.appendChild(b);
        }
    </script>
</body>
</html>
