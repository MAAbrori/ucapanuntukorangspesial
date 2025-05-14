<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Undangan Ulang Tahun Intan</title>
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet" />

  <style>
    body {
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(to right, #ffe0f0, #fff0f5);
      margin: 0;
      padding: 50px 20px;
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      overflow: hidden;
      animation: backgroundShift 10s ease-in-out infinite alternate;
      position: relative;
    }

    .container {
      background: #fff0f8;
      padding: 40px 30px;
      border-radius: 20px;
      text-align: center;
      box-shadow: 0 10px 30px rgba(255, 105, 180, 0.2);
      border: 2px dashed #ff8fb4;
      animation: fadeIn 1.2s ease;
      position: relative;
      z-index: 2;
    }

    h1 {
      font-family: 'Great Vibes', cursive;
      font-size: 3.5em;
      color: #d63384;
      margin-bottom: 10px;
    }

    h2 {
      font-family: 'Great Vibes', cursive;
      font-size: 2.5em;
      color: #e60073;
      margin: 15px 0;
    }

    .center-flowers {
      display: flex;
      justify-content: center;
      gap: 15px;
      margin: 10px 0;
    }

    .flower-animate {
      display: inline-block;
      animation: floatY 2s ease-in-out infinite;
    }

    .flower-animate:nth-child(1) { animation-delay: 0s; }
    .flower-animate:nth-child(2) { animation-delay: 0.3s; }
    .flower-animate:nth-child(3) { animation-delay: 0.6s; }
    .flower-animate:nth-child(4) { animation-delay: 0.9s; }
    .flower-animate:nth-child(5) { animation-delay: 1.2s; }

    @keyframes floatY {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }

    p {
      font-size: 1.1em;
      color: #555;
    }

    strong {
      color: #c2185b;
    }

    @keyframes backgroundShift {
      0% { background: linear-gradient(to right, #ffe0f0, #fff0f5); }
      100% { background: linear-gradient(to right, #ffd6e8, #ffe0ec); }
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    /* === Hujan Bunga === */
    .flower-rain {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      overflow: hidden;
      z-index: 1;
    }

    .falling-flower {
      position: absolute;
      font-size: 20px;
      animation: fall linear infinite;
    }

    @keyframes fall {
      0% {
        transform: translateY(-100px) rotate(0deg);
        opacity: 1;
      }
      100% {
        transform: translateY(100vh) rotate(360deg);
        opacity: 0;
      }
    }
  </style>
</head>
<body>

  <!-- Musik ulang tahun -->
  <audio autoplay loop>
    <source src="https://www.bensound.com/bensound-music/bensound-happyrock.mp3" type="audio/mpeg">
    Browser Anda tidak mendukung audio.
  </audio>

  <!-- Efek hujan bunga -->
  <div class="flower-rain" id="flowerRain"></div>

  <!-- Undangan -->
  <div class="container">
    <h1>Happy Graduation</h1>
    <p>"Selamat atas kelulusannya sayank, Ini adalah awal dari babak baru yang penuh potensi. Jangan takut untuk melangkah, teruslah belajar dan berjuang untuk meraih impianmu!"</p>

    <!-- Bunga dekoratif atas -->
    <div class="center-flowers">
      <span class="flower-animate">🌸</span>
      <span class="flower-animate">🌹</span>
      <span class="flower-animate">💐</span>
      <span class="flower-animate">🌺</span>
      <span class="flower-animate">🌷</span>
    </div>

    <h2>Anis Dwi Lestari ❤</h2>

    <!-- Bunga dekoratif bawah -->
    <div class="center-flowers">
      <span class="flower-animate">🌷</span>
      <span class="flower-animate">💐</span>
      <span class="flower-animate">🌺</span>
      <span class="flower-animate">🌹</span>
      <span class="flower-animate">🌸</span>
    </div>

    <p>Yang akan dilaksanakan pada:</p>
    <p><strong>14 Mei 2025</strong></p>
    <p>Tabarakallah, selamat karena sudah lulus sekolah! Belajarmu tidak pernah sia-sia dan semoga ilmu yang kamu miliki membawa manfaat bagi dirimu dan umat 🎉✨</p>
  </div>

  <script>
    const flowerContainer = document.getElementById('flowerRain');
    const flowerTypes = ['🌸', '🌺', '🌷', '💐', '🌹'];
    const flowerCount = 50; // jumlah bunga

    for (let i = 0; i < flowerCount; i++) {
      const flower = document.createElement('div');
      flower.classList.add('falling-flower');
      flower.textContent = flowerTypes[Math.floor(Math.random() * flowerTypes.length)];
      flower.style.left = Math.random() * 100 + 'vw';
      flower.style.fontSize = (16 + Math.random() * 20) + 'px';
      flower.style.animationDuration = (5 + Math.random() * 5) + 's';
      flower.style.animationDelay = Math.random() * 5 + 's';
      flowerContainer.appendChild(flower);
    }
  </script>

</body>
</html>
