<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Anushreya ❤️</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      background: radial-gradient(circle at top, #ff5f9e, #1a001a);
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: 'Comic Sans MS', cursive;
      color: white;
      overflow: hidden;
      text-align: center;
    }

    h1 {
      font-size: 3em;
      animation: glow 2s infinite alternate;
    }

    @keyframes glow {
      from { text-shadow: 0 0 10px #ffb6c1; }
      to { text-shadow: 0 0 25px #ff1493; }
    }

    .card {
      background: rgba(0,0,0,0.4);
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 0 30px rgba(255,20,147,0.5);
    }

    button {
      padding: 12px 25px;
      margin: 15px;
      font-size: 18px;
      border: none;
      border-radius: 25px;
      cursor: pointer;
      transition: 0.3s;
    }

    #yes {
      background: #ff1493;
      color: white;
    }

    #no {
      background: #555;
      color: white;
      position: absolute;
    }

    .heart {
      position: absolute;
      color: pink;
      font-size: 20px;
      animation: float 4s linear infinite;
    }

    @keyframes float {
      from { transform: translateY(100vh); opacity: 1; }
      to { transform: translateY(-10vh); opacity: 0; }
    }
  </style>
</head>
<body>

  <div class="card">
    <h1>Anushreya 💖</h1>
    <p>Will you be my Valentine? 🌹😈</p>
    <button id="yes" onclick="yesClick()">YES 💘</button>
    <button id="no" onmouseover="moveNo()">NO 🙈</button>
  </div>

  <script>
    function moveNo() {
      const no = document.getElementById("no");
      no.style.left = Math.random() * 80 + "vw";
      no.style.top = Math.random() * 80 + "vh";
    }

    function yesClick() {
      document.body.innerHTML = `
        <h1>Yaaay! 💞</h1>
        <p>Anushreya, you just made my heart yours 😘🔥</p>
      `;
    }

    setInterval(() => {
      const heart = document.createElement("div");
      heart.className = "heart";
      heart.innerHTML = "❤️";
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.fontSize = Math.random() * 20 + 15 + "px";
      document.body.appendChild(heart);
      setTimeout(() => heart.remove(), 4000);
    }, 300);
  </script>

</body>
</html>
