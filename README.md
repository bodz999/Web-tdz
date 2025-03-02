<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DTAIF VIP PROFILE</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@600&display=swap" rel="stylesheet">
    <style>
        body {
            margin: 0;
            padding: 0;
            overflow: hidden;
            text-align: center;
            font-family: 'Poppins', sans-serif;
            background: black;
            color: white;
            cursor: crosshair;
        }

        .background video {
            position: fixed;
            width: 100%;
            height: 100%;
            object-fit: cover;
            filter: brightness(0.3) blur(3px);
            z-index: -1;
        }

        .profile {
            width: 90%;
            max-width: 400px;
            margin: 100px auto;
            padding: 20px;
            background: rgba(0, 0, 0, 0.8);
            border: 4px solid cyan;
            box-shadow: 0 0 30px cyan;
            border-radius: 20px;
            animation: neon 2s infinite alternate;
        }

        @keyframes neon {
            0% { box-shadow: 0 0 10px cyan; }
            100% { box-shadow: 0 0 30px cyan; }
        }

        .profile img {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            border: 4px solid cyan;
            box-shadow: 0 0 20px cyan;
            animation: spin 5s linear infinite;
        }

        @keyframes spin {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        .username {
            font-size: 28px;
            background: linear-gradient(90deg, #ff0000, #ff7300, #ffeb00, #00ff00, #00ffff, #0000ff, #8000ff);
            -webkit-background-clip: text;
            color: transparent;
            animation: rainbow 3s linear infinite;
        }

        @keyframes rainbow {
            0% { background-position: 0% 50%; }
            100% { background-position: 200% 50%; }
        }

        .menu a {
            display: block;
            text-decoration: none;
            color: white;
            margin: 10px 0;
            padding: 10px;
            border: 2px solid cyan;
            border-radius: 10px;
            transition: 0.3s;
            text-shadow: 0 0 10px cyan;
        }

        .menu a:hover {
            background: cyan;
            color: black;
            transform: scale(1.1);
        }

        @keyframes floatUp {
            from { transform: translateY(0px); opacity: 1; }
            to { transform: translateY(-100px); opacity: 0; }
        }
    </style>
</head>
<body>

<div class="background">
    <video autoplay loop muted>
        <source src="https://res.cloudinary.com/djkug0a3i/video/upload/v1740638266/y2mate.com_-_puppy_Dangrangto_Wrong_Times_ft_FOWLEX_Snowz_OFFICIAL_LYRICS_VIDEO_dfgsaz.mp3" type="audio/mp3">
    </video>
</div>

<audio id="music" autoplay loop>
    <source src="https://res.cloudinary.com/djkug0a3i/video/upload/v1740638266/y2mate.com_-_puppy_Dangrangto_Wrong_Times_ft_FOWLEX_Snowz_OFFICIAL_LYRICS_VIDEO_dfgsaz.mp3" type="audio/mpeg">
</audio>

<div class="profile">
    <img src="https://res.cloudinary.com/dg9dy1gqx/image/upload/v1740878133/Tdzgimdaudata.jpg">
    <div class="username">Dtaif iu em</div>
    <p>📍 Khanh Hoa Province, VietNam</p>
    <p>🏫 Truong THCS Dinh Tien Hoang</p>
    <p>👻 Huynh Duy Tai [tawundz]</p>
    <p>🎶 Favorite Music: Dung Lam Trai Tim Anh Dau</p>
    <p>🎮 Game: Free Fire, Liên Quân</p>
    <p>🍜 Favorite Food: Spicy Noodles, Ramen</p>
    <p>🖥 Skill: Java, Python, HTML, Lua</p>

    <div class="menu">
        <a href="https://www.tiktok.com/@tawundz" target="_blank">TikTok</a>
        <a href="https://www.facebook.com/r.duy.tai" target="_blank">Facebook</a>
    </div>

    <button id="heartButton" style="padding: 10px 20px; background: red; color: white; border: none; border-radius: 20px; cursor: pointer; box-shadow: 0 0 10px red;">Thả Tim ❤️</button>
</div>

<script>
    document.getElementById("heartButton").onclick = function (e) {
        let heart = document.createElement("div");
        heart.innerHTML = "❤️ Iu Cậu";
        heart.style.position = "absolute";
        heart.style.left = e.pageX + "px";
        heart.style.top = e.pageY + "px";
        heart.style.fontSize = "30px";
        heart.style.color = "red";
        heart.style.animation = "floatUp 10s ease-out";
        document.body.appendChild(heart);
        setTimeout(() => heart.remove(), 5000);
    };

    document.addEventListener("click", function (e) {
        let sparkle = document.createElement("div");
        sparkle.style.position = "absolute";
        sparkle.style.width = "20px";
        sparkle.style.height = "20px";
        sparkle.style.background = "radial-gradient(circle, white, transparent)";
        sparkle.style.borderRadius = "50%";
        sparkle.style.pointerEvents = "none";
        sparkle.style.animation = "floatUp 1s ease-out";
        sparkle.style.left = e.pageX + "px";
        sparkle.style.top = e.pageY + "px";
        document.body.appendChild(sparkle);
        setTimeout(() => sparkle.remove(), 1000);
    });

    function createEffect(className, time, size) {
        setInterval(() => {
            let effect = document.createElement("div");
            effect.classList.add(className);
            effect.style.left = Math.random() * window.innerWidth + "px";
            effect.style.width = size + "px";
            effect.style.height = size + "px";
            effect.style.background = "rgba(255, 255, 255, 0.7)";
            effect.style.borderRadius = "50%";
            effect.style.position = "absolute";
            effect.style.animation = "floatUp 5s linear infinite";
            document.body.appendChild(effect);
            setTimeout(() => effect.remove(), 5000);
        }, time);
    }

    createEffect("snow", 200, 10);
    createEffect("star", 400, 10);
    createEffect("bubble", 300, 20);
</script>
</body>
</html>
