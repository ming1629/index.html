# index.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Happy Birthday</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background-color: #fddde6;
      font-family: 'Comic Sans MS', cursive;
      height: 100vh;
      overflow: hidden;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .birthday-card {
      text-align: center;
      padding: 2rem;
      border-radius: 15px;
      background-color: #fff0f5;
      box-shadow: 0 8px 16px rgba(0,0,0,0.1);
      z-index: 2;
      position: relative;
    }

    .cake {
      width: 150px;
      margin-bottom: 1rem;
    }

    .Happy__Birthday {
      color: #c2185b;
      font-size: 3em;
      font-weight: 700;
      text-shadow: 2px 2px 5px rgba(255, 255, 255, 0.7);
    }

    /* Confetti */
    .confetti {
      position: absolute;
      width: 10px;
      height: 10px;
      background-color: #ff69b4;
      animation: fall 3s linear infinite;
      z-index: 1;
      opacity: 0.8;
    }

    @keyframes fall {
      0% {
        transform: translateY(-100vh) rotate(0deg);
      }
      100% {
        transform: translateY(100vh) rotate(360deg);
      }
    }

    @media (max-width: 600px) {
      .Happy__Birthday {
        font-size: 2em;
      }
      .cake {
        width: 120px;
      }
    }
  </style>
</head>
<body>

  <!-- Confetti Generator -->
  <script>
    for (let i = 0; i < 80; i++) {
      let confetti = document.createElement('div');
      confetti.className = 'confetti';
      confetti.style.left = Math.random() * 100 + 'vw';
      confetti.style.animationDuration = 2 + Math.random() * 3 + 's';
      confetti.style.backgroundColor = `hsl(${Math.random() * 360}, 100%, 75%)`;
      document.body.appendChild(confetti);
    }
  </script>

  <div class="birthday-card">
    <img src="https://cdn-icons-png.flaticon.com/512/3208/3208758.png" alt="Birthday Cake" class="cake" />
    <h1 class="Happy__Birthday"> merl ey o !</h1>
    <audio autoplay loop>
      <source src="https://www.fesliyanstudios.com/play-mp3/387" type="audio/mpeg">
      Your browser does not support the audio element.
    </audio>
  </div>

</body>
</html>
