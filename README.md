<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Eloah 💗</title>

    <style>
        * { box-sizing: border-box; }

        body {
            margin: 0;
            font-family: 'Segoe UI', cursive;
            background: radial-gradient(circle at top, #ffc0cb, #ff69b4, #ff1493);
            min-height: 100vh;
            overflow-x: hidden;
        }

        /* Corações */
        .heart {
            position: fixed;
            color: rgba(255,255,255,0.6);
            animation: float 7s linear infinite;
            pointer-events: none;
        }

        @keyframes float {
            0% { transform: translateY(110vh) scale(0.6); opacity: 1; }
            100% { transform: translateY(-10vh) scale(1.3); opacity: 0; }
        }

        h1 {
            text-align: center;
            color: white;
            margin: 20px 10px 5px;
            font-size: 32px;
            text-shadow: 0 0 15px #ff1493;
        }

        .subtitle {
            text-align: center;
            color: white;
            margin-bottom: 20px;
        }

        .container {
            margin: 0 15px 30px;
            background: rgba(255,255,255,0.25);
            backdrop-filter: blur(10px);
            padding: 20px;
            border-radius: 22px;
            box-shadow: 0 0 25px rgba(255,20,147,0.7);
        }

        .photos {
            display: flex;
            flex-direction: column;
            gap: 18px;
            align-items: center;
        }

        .photo {
            width: 100%;
            max-width: 320px;
            height: 200px;
            object-fit: cover;
            border-radius: 20px;
            border: 4px solid white;
            box-shadow: 0 0 15px rgba(255,105,180,0.9);
        }

        .message {
            margin-top: 25px;
            text-align: center;
            color: white;
            font-size: 18px;
            text-shadow: 1px 1px 6px #ff1493;
        }

        /* BOTÕES */
        .music-box {
            margin-top: 35px;
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
        }

        .love-button {
            background: linear-gradient(135deg, #ff69b4, #ff1493);
            color: white;
            border: none;
            padding: 16px 28px;
            font-size: 18px;
            border-radius: 45px;
            cursor: pointer;
            box-shadow: 0 0 30px rgba(255,20,147,1);
            animation: pulse 2s infinite;
            transition: transform 0.3s;
            text-decoration: none;
        }

        .love-button.youtube {
            background: linear-gradient(135deg, #ffb6c1, #ff69b4);
        }

        .love-button:hover {
            transform: scale(1.1);
        }

        @keyframes pulse {
            0% { box-shadow: 0 0 20px #ff69b4; }
            50% { box-shadow: 0 0 45px #ff1493; }
            100% { box-shadow: 0 0 20px #ff69b4; }
        }

        footer {
            text-align: center;
            color: white;
            margin: 25px 10px;
            font-size: 13px;
        }

        @media (min-width: 768px) {
            .photos { flex-direction: row; }
        }
    </style>
</head>

<body>

<script>
    const hearts = 45;
    for (let i = 0; i < hearts; i++) {
        const heart = document.createElement("div");
        heart.className = "heart";
        heart.innerHTML = "💖";
        heart.style.left = Math.random() * 100 + "vw";
        heart.style.fontSize = (18 + Math.random() * 28) + "px";
        heart.style.animationDuration = (4 + Math.random() * 6) + "s";
        document.body.appendChild(heart);
    }
</script>

<h1>💗 Nosso Amor 💗</h1>
<p class="subtitle">Cada momento com você é eterno</p>

<div class="container">

    <div class="photos">
        <img class="photo" src="1000001185.jpg">
        <img class="photo" src="1000006544.jpg">
        <img class="photo" src="1000012733.jpg">
    </div>

    <div class="message">
        <p>💌 Você é o meu lugar seguro.</p>
        <p>Com você, todos os dias são especiais 💕</p>
    </div>

    <!-- BOTÕES -->
    <div class="music-box">
        <button class="love-button" onclick="toggleMusica()">🎶 Música</button>
        <a class="love-button youtube"
           href="https://youtu.be/j_a55VGxiEU?si=FAPqiXQEDJJfqFxL"
           target="_blank">
           ▶️ Vídeo no YouTube
        </a>
    </div>

</div>

<footer>
    Feito com amor infinito 💞
</footer>

<audio id="musica" loop>
    <source src="Carol e Junior - Grava essa ideia(MP3_160K).mp3" type="audio/mpeg">
</audio>

<script>
let tocando = false;

function toggleMusica() {
    const musica = document.getElementById("musica");
    if (!tocando) {
        musica.play();
        tocando = true;
    } else {
        musica.pause();
        tocando = false;
    }
}
</script>

</body>
</html>
