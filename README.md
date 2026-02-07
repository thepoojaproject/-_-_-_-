
<html lang="hi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Happy Rose Day Madam Ji 💖</title>
  <style>
    body {
      margin: 0;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      background: linear-gradient(135deg, #fff0f5, #ffe6f2);
      font-family: system-ui, sans-serif;
      position: relative;
    }
    .container {
      text-align: center;
      flex: 1;
      display: flex;
      flex-direction: column;
      justify-content: center;
    }
    button {
      padding: 18px 60px;
      font-size: 24px;
      color: white;
      background: #ff85a2;
      border: none;
      border-radius: 999px;
      cursor: pointer;
      box-shadow: 0 10px 30px rgba(255, 133, 162, 0.4);
      transition: all 0.3s ease;
      position: relative;
      overflow: hidden;
    }
    button:hover {
      transform: scale(1.1);
      box-shadow: 0 15px 40px rgba(255, 133, 162, 0.6);
    }
    button:active {
      transform: scale(0.95);
    }
    .main-msg {
      margin-top: 30px;
      font-size: 28px;
      font-weight: bold;
      color: #ff4d82;
      opacity: 0;
      transition: opacity 1s ease;
    }
    .sub-msg {
      margin-top: 10px;
      font-size: 22px;
      color: #e6335a;
      opacity: 0;
      transition: opacity 1.2s ease;
    }
    .heart {
      position: absolute;
      font-size: 35px;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      opacity: 0;
      pointer-events: none;
      animation: floatUp 1.5s ease-out forwards;
    }
    @keyframes floatUp {
      0% { opacity: 0; transform: translate(-50%, -50%) translateY(0); }
      30% { opacity: 1; }
      100% { opacity: 0; transform: translate(-50%, -120%) translateY(-100px); }
    }
    footer {
      padding: 20px 0;
      font-size: 16px;
      color: #ff85a2;
      opacity: 0.8;
      text-align: center;
      width: 100%;
      margin-top: auto;
    }
  </style>
</head>
<body>

  <div class="container">
    <button id="roseBtn">Click for Surprise 🌹</button>
    <div class="main-msg" id="mainMsg">गुलाब को क्या गुलाब दूं? 💖</div>
    <div class="sub-msg" id="subMsg">Happy R❤se Day Madam Jii</div>
  </div>

  <footer>Made in 💖 for Kalpana</footer>

  <script>
    const btn = document.getElementById('roseBtn');
    const mainMsg = document.getElementById('mainMsg');
    const subMsg = document.getElementById('subMsg');
    let clicked = false;

    btn.addEventListener('click', () => {
      if (!clicked) {
        mainMsg.style.opacity = "1";
        subMsg.style.opacity = "1";

        // Color glow
        btn.style.background = "#ff4d82";

        // Floating hearts & roses
        for (let i = 0; i < 6; i++) {
          const heart = document.createElement('span');
          heart.className = 'heart';
          heart.textContent = Math.random() > 0.5 ? '💕' : '🌹';
          heart.style.left = `${40 + Math.random() * 40}%`;
          heart.style.top = '50%';
          heart.style.animationDelay = `${i * 0.15}s`;
          document.body.appendChild(heart);
          setTimeout(() => heart.remove(), 1800);
        }

        clicked = true;
      } else {
        alert("Arre Madam Ji, ek hi gulaab kaafi hai na? 😘🌹");
      }
    });
  </script>

</body>
</html>
