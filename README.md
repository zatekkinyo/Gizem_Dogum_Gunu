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
      background: linear-gradient(to top, #4caf50, #a8e063);
      overflow: hidden;
      position: relative;
      font-family: sans-serif;
      cursor: pointer;
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
  <script>
    const flowers = ["🌸", "🌼", "🌹", "🌷", "🌻"];

    document.body.addEventListener("click", (e) => {
      const flower = document.createElement("div");
      flower.className = "flower";
      flower.textContent = flowers[Math.floor(Math.random() * flowers.length)];
      
      // Konumlandırma
      flower.style.left = `${e.clientX - 10}px`;
      flower.style.top = `${e.clientY - 10}px`;

      document.body.appendChild(flower);

      // Sonsuza kadar kalmasın diye temizle
      setTimeout(() => {
        flower.remove();
      }, 5000);
    });
  </script>
</body>
</html>
