<html lang="ml">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>🌹 Ammukkutty Vishu 🌸</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+Malayalam&display=swap');

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      height: 100vh;
      background: radial-gradient(circle at top, #ffd6e8, #ffccd5, #ffc8dd, #ffe5ec);
      overflow: hidden;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      font-family: 'Noto Sans Malayalam', sans-serif;
      text-align: center;
      position: relative;
    }

    .greeting {
      font-size: 2.4em;
      color: #ff3c6f;
      text-shadow: 0 0 10px #fff, 0 0 20px #ffc9de;
      z-index: 10;
      animation: popIn 2s ease-out, fadeOut 1s ease-in 9s forwards;
      padding: 0 20px;
    }

    .subtext {
      font-size: 1.2em;
      margin-top: 15px;
      color: #7a1e3c;
      text-shadow: 0 0 6px #fff;
      opacity: 0;
      animation: fadeIn 2s ease 2s forwards, fadeOut 1s ease-in 9s forwards;
      z-index: 10;
      padding: 0 20px;
    }

    @keyframes popIn {
      from { transform: scale(0.9); opacity: 0; }
      to { transform: scale(1); opacity: 1; }
    }

    @keyframes fadeIn {
      to { opacity: 1; }
    }

    @keyframes fadeOut {
      to { opacity: 0; transform: scale(0.8); }
    }

    .float {
      position: absolute;
      width: 30px;
      height: 30px;
      background-size: cover;
      opacity: 0.8;
      animation: floatUp 10s linear infinite;
    }

    @keyframes floatUp {
      0% {
        transform: translateY(100vh) scale(0.8) rotate(0deg);
        opacity: 0;
      }
      20% {
        opacity: 1;
      }
      100% {
        transform: translateY(-10vh) scale(1.2) rotate(360deg);
        opacity: 0;
      }
    }

    .overlay {
      position: absolute;
      width: 100%;
      height: 100%;
      background: white;
      top: 0;
      left: 0;
      z-index: 99;
      opacity: 0;
      animation: showOverlay 1s ease 10s forwards;
    }

    @keyframes showOverlay {
      to {
        opacity: 1;
      }
    }
  </style>
</head>
<body>

  <div class="greeting">🌸 ഹാപ്പി വിഷു അമ്മുക്കുട്ടി 🌹</div>
  <div class="subtext">ഇന്ന് ഞാൻ നിന്നെ വിഷുവിനായി പൂക്കളെപ്പോലെയായി ആശംസിക്കുന്നു 💕</div>

  <div class="overlay"></div>

  <script>
    const images = [
      'https://i.imgur.com/fU9x3LE.png', // pink heart
      'https://i.imgur.com/JukwT23.png', // red rose
      'https://i.imgur.com/fU9x3LE.png',
      'https://i.imgur.com/JukwT23.png'
    ];

    for (let i = 0; i < 30; i++) {
      const float = document.createElement('div');
      float.classList.add('float');
      float.style.left = Math.random() * 100 + 'vw';
      float.style.animationDelay = Math.random() * 8 + 's';
      float.style.animationDuration = 6 + Math.random() * 6 + 's';
      float.style.backgroundImage = `url(${images[i % images.length]})`;
      document.body.appendChild(float);
    }
  </script>

</body>
</html>
