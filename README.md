<!DOCTYPE html>
<html lang="mn">
<head>
<meta charset="UTF-8">
<title>Happy Birthday, Maya!</title>
<style>
    * { margin:0; padding:0; box-sizing:border-box; }
    body {
        font-family: 'Arial', sans-serif;
        overflow-x: hidden;
        background: linear-gradient(130deg, #ff9ecb, #ffd1dc, #ffe5f0);
        background-size: 400% 400%;
        animation: bgMove 12s ease infinite;
        color: #333;
    }

    @keyframes bgMove {
        0% {background-position: 0% 50%;}
        50% {background-position: 100% 50%;}
        100% {background-position: 0% 50%;}
    }

    .center-card {
        text-align: center;
        margin-top: 70px;
        animation: fadeIn 2s;
        color: #fff;
        text-shadow: 0 0 10px rgba(0,0,0,0.2);
    }

    h1 {
        font-size: 45px;
    }

    button {
        margin-top: 20px;
        padding: 12px 28px;
        font-size: 20px;
        background: #ff66aa;
        border: none;
        border-radius: 12px;
        cursor: pointer;
        color: white;
        transition: 0.3s;
    }
    button:hover {
        background: #ff4499;
    }

    .gallery {
        margin: 50px auto;
        width: 90%;
        display: flex;
        justify-content: center;
        gap: 20px;
        flex-wrap: wrap;
    }
    .gallery img {
        width: 260px;
        border-radius: 15px;
        transition: transform 0.4s;
        cursor: pointer;
        box-shadow: 0 0 15px rgba(255,255,255,0.5);
    }
    .gallery img:hover {
        transform: scale(1.1);
    }

    @keyframes fadeIn {
        from { opacity:0; transform:translateY(20px); }
        to   { opacity:1; transform:translateY(0); }
    }
</style>
</head>
<body>

<div class="center-card">
    <h1>Төрсөн өдрийн мэнд, Маяа! 🎉</h1>
    <p style="font-size:22px">Чиний бүх өдрүүд инээмсэглэл шиг чинь дулаахан, гэрэлтэй байг ээ .</p>

    <button onclick="startConfetti()">✨ Хайртай жо <3</button>
</div>

<!-- Image Gallery -->
<div class="gallery">
    <img src="img1.jpg">
    <img src="img2.jpg">
    <img src="img3.jpg">
    <img src="img4.jpg">
    <img src="img5.jpg">
</div>

<!-- Confetti Script -->
<script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>
<script>
function startConfetti() {
    const duration = 3 * 1000;
    const end = Date.now() + duration;

    (function frame() {
        confetti({
            particleCount: 7,
            spread: 80
        });
        if (Date.now() < end) requestAnimationFrame(frame);
    }());
}
</script>

</body>
</html>
