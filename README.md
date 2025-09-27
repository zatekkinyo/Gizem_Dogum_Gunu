<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Çiçek Bahçesi</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      height: 100vh;
      overflow: hidden;
      font-family: sans-serif;
    }
    /* Giriş ekranı */
    #intro {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: linear-gradient(to top, #2e7d32, #81c784);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      color: white;
      text-align: center;
      z-index: 10;
    }
    #intro h1 {
      font-size: 2.5rem;
      margin-bottom: 20px;
    }
    #enterBtn {
      padding: 12px 24px;
      background: #fff;
      color: #2e7d32;
      border: none;
      border-radius: 8px;
      font-size: 1.2rem;
      cursor: pointer;
      transition: transform 0.3s;
    }
    #enterBtn:hover {
      transform: scale(1.1);
    }
    /* Bahçe */
    #garden {
      width: 100%;
      height: 100%;
      background: linear-gradient(to top, #4caf50, #a8e063);
      position: relative;
      cursor: pointer;
      display: none;
    }
    .flower {
      position: absolute;
      font-size: 2rem;
      opacity: 0;
      transform: scale(0.5);
      animation: grow 0.8s forwards;
    }
    @keyframes grow {
      to {
        opacity: 1;
        transform: scale(1);
      }
    }
  </style>
</head>
<body>
  <!-- Giriş ekranı -->
  <div id="intro">
    <h1>Çiçek Bahçesine Hoş Geldin 🌿</h1>
    <button id="enterBtn">Bahçeye Gir</button>
  </div>

  <!-- Bahçe alanı -->
  <div id="garden"></div>

  <script>
    const flowers = ["🌸", "🌼", "🌹", "🌷", "🌻"];
    const intro = document.getElementById("intro");
    const garden = document.getElementById("garden");
    const enterBtn = document.getElementById("enterBtn");

    // Giriş ekranından bahçeye geçiş
    enterBtn.addEventListener("click", () => {
      intro.style.display = "none";
      garden.style.display = "block";
    });

    // Çiçek ekleme
    garden.addEventListener("click", (e) => {
      const flower = document.createElement("div");
      flower.className = "flower";
      flower.textContent = flowers[Math.floor(Math.random() * flowers.length)];
      
      flower.style.left = `${e.clientX - 10}px`;
      flower.style.top = `${e.clientY - 10}px`;

      garden.appendChild(flower);

      setTimeout(() => {
        flower.remove();
      }, 5000);
    });
  </script>
</body>
</html>
