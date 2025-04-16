<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Hi, My Love 💖</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      height: 100vh;
      font-family: "Comic Sans MS", cursive, sans-serif;
      background: linear-gradient(135deg, #ffe4ec, #e0c3fc);
      overflow: hidden;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
    }

    h1 {
      font-size: 2.8em;
      color: #ff4d6d;
      margin-bottom: 10px;
      animation: pop 1s ease-in-out infinite alternate;
    }

    p {
      font-size: 1.4em;
      color: #444;
    }

    .buttons {
      margin-top: 20px;
    }

    button {
      padding: 12px 24px;
      font-size: 1.2em;
      border: none;
      border-radius: 30px;
      margin: 0 10px;
      cursor: pointer;
      transition: all 0.3s ease;
    }

    #yes {
      background-color: #ff69b4;
      color: white;
    }

    #no {
      background-color: #ddd;
      color: #333;
      position: relative;
    }

    #sparkle {
      display: none;
      font-size: 2em;
      color: #ff6ec4;
      margin-top: 30px;
      animation: sparkle 0.5s ease-in-out infinite alternate;
    }

    @keyframes pop {
      from { transform: scale(1); }
      to { transform: scale(1.1); }
    }

    @keyframes sparkle {
      0% { transform: scale(1) rotate(0deg); }
      100% { transform: scale(1.2) rotate(10deg); }
    }

    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      transform: rotate(45deg);
      animation: float 6s linear infinite;
      opacity: 0.7;
    }

    .heart:before,
    .heart:after {
      content: "";
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      border-radius: 50%;
    }

    .heart:before {
      top: -10px;
      left: 0;
    }

    .heart:after {
      left: -10px;
      top: 0;
    }

    @keyframes float {
      0% {
        transform: translateY(100vh) rotate(0deg);
        opacity: 0;
      }
      50% {
        opacity: 1;
      }
      100% {
        transform: translateY(-10vh) rotate(360deg);
        opacity: 0;
      }
    }
  </style>
</head>
<body>

  <h1>Hi Beautiful 💘</h1>
  <p>Would you go out with me?</p>

  <div class="buttons">
    <button id="yes">Yes 💖</button>
    <button id="no">No 🙈</button>
  </div>

  <div id="sparkle">✨ YAY! Can't wait! ✨</div>

  <!-- Floating hearts -->
  <script>
    for (let i = 0; i < 20; i++) {
      const heart = document.createElement("div");
      heart.className = "heart";
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.animationDuration = 3 + Math.random() * 3 + "s";
      document.body.appendChild(heart);
    }

    const yes = document.getElementById("yes");
    const no = document.getElementById("no");
    const sparkle = document.getElementById("sparkle");

    yes.addEventListener("click", () => {
      sparkle.style.display = "block";
    });

    no.addEventListener("mouseover", () => {
      const x = Math.random() * (window.innerWidth - 100);
      const y = Math.random() * (window.innerHeight - 50);
      no.style.position = "absolute";
      no.style.left = `${x}px`;
      no.style.top = `${y}px`;
    });
  </script>

</body>
</html>

