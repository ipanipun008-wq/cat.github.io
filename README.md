# cat.github.io
<!DOCTYPE html>
<html>
<head>
    <title>Happy Birthday!</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: "Comic Sans MS", cursive;
            background: #ffc0cb;
            overflow: hidden;
            text-align: center;
        }

        .card {
            background: white;
            padding: 40px;
            margin: 100px auto;
            width: 400px;
            border-radius: 25px;
            box-shadow: 0 5px 25px rgba(0,0,0,0.2);
            animation: pop 0.8s ease-out;
        }

        @keyframes pop {
            0% { transform: scale(0.5); opacity: 0; }
            100% { transform: scale(1); opacity: 1; }
        }

        h1 {
            color: #ff4d88;
            font-size: 32px;
            margin-bottom: 10px;
        }

        .nama {
            font-size: 26px;
            color: #ff5ea7;
            font-weight: bold;
            margin-bottom: 10px;
        }

        /* confetti */
        .confetti {
            width: 10px;
            height: 10px;
            background-color: #fff;
            position: absolute;
            top: -10px;
            animation: fall 4s linear infinite;
        }

        @keyframes fall {
            0% { transform: translateY(0) rotate(0deg); }
            100% { transform: translateY(120vh) rotate(360deg); }
        }
    </style>
</head>
<body>

<div class="card">
    <h1>🎉 Selamat Ulang Tahun! 🎉</h1>
    <div class="nama" id="namaTampil"></div>
    <p>Semoga harimu penuh tawa, kue, dan kejutan manis! 🎂💖</p>
</div>

<script>
    // Ganti nama di sini
    let namaOrang = "Nama Kamu";

    // tampilkan nama otomatis saat halaman dibuka
    document.getElementById("namaTampil").innerHTML = namaOrang + " 🌸✨";

    // buat confetti lucu
    for (let i = 0; i < 40; i++) {
        let conf = document.createElement("div");
        conf.classList.add("confetti");
        conf.style.left = Math.random() * 100 + "vw";
        conf.style.backgroundColor = ["#fff", "#ffb6c1", "#ff69b4", "#ff1493"][Math.floor(Math.random()*4)];
        conf.style.animationDuration = (Math.random() * 3 + 2) + "s";
        document.body.appendChild(conf);
    }
</script>

</body>
</html>
