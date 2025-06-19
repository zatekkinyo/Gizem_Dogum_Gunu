<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>İyi ki Doğdun Gizem 🎉</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #fddde6, #f9f3f3);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      text-align: center;
      overflow: auto;
    }
    h1 {
      font-size: 2.5em;
      margin-bottom: 0.5em;
      color: #d94f70;
    }
    .message {
      background: #fff0f5;
      border-radius: 20px;
      padding: 25px;
      max-width: 600px;
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
    }
    p {
      font-size: 1.2em;
      color: #444;
    }
    .footer {
      margin-top: 30px;
      font-size: 0.9em;
      color: #888;
    }
    .hearts {
      position: absolute;
      width: 100%;
      height: 100%;
      overflow: hidden;
      top: 0;
      left: 0;
      z-index: -1;
    }
    .hearts span {
      position: absolute;
      display: block;
      width: 20px;
      height: 20px;
      background: url('https://upload.wikimedia.org/wikipedia/commons/thumb/f/f4/Heart_coraz%C3%B3n.svg/2048px-Heart_coraz%C3%B3n.svg.png') no-repeat center center / contain;
      animation: float 6s linear infinite;
      opacity: 0.6;
    }
    @keyframes float {
      0% { transform: translateY(100vh); opacity: 0; }
      50% { opacity: 1; }
      100% { transform: translateY(-10vh); opacity: 0; }
    }
    .button {
      margin-top: 30px;
      padding: 12px 24px;
      font-size: 1em;
      background-color: #ff8fa3;
      color: white;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    .button:hover {
      background-color: #ff6f8d;
    }
    .options {
      display: none;
      flex-direction: column;
      gap: 10px;
      margin-top: 20px;
    }
    .option-button {
      padding: 10px 20px;
      background-color: #fff0f5;
      border: 1px solid #ff8fa3;
      border-radius: 20px;
      cursor: pointer;
      font-size: 1em;
    }
    #surprise {
      display: none;
      margin-top: 20px;
      max-width: 90%;
    }
    #surprise img {
      max-width: 300px;
      border-radius: 20px;
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
    }
    #surprise p {
      margin-top: 15px;
      font-size: 1.1em;
      color: #d94f70;
      white-space: pre-line;
      padding: 0 20px;
    }
  </style>
</head>
<body>
  <h1>İyi ki Doğdun Gizem 🎂</h1>
  <div class="message">
    <p>Bugün bir Giresun klasiği gibi; sade ama derin, tatlı ama abartısız bir gün… çünkü senin doğum günün 🌸</p>
    <p>Minicup gibi: küçük bir şey ama insana iyi gelen bir tat. Yeni yaşın sana en çok sevdiğin şeyleri getirsin…</p>
    <p>Mesela huzur, kahkaha, minicup... ve belki yanında seni gerçekten önemseyen birini.</p>
    <p>İyi ki doğdun, iyi ki varsın Gizem 😊</p>
  </div>

  <button class="button" onclick="showOptions()">Devamı gelsin mi?</button>

  <div class="options" id="options">
    <button class="option-button" onclick="showSurprise()">Evet 😄</button>
    <button class="option-button" onclick="alert('Hadi ama… o gülümsemenin devamını görmeden bırakacak değilim 😌')">Hayır 🙃</button>
  </div>

  <div id="surprise">
    <p>Bugün bir Giresun klasiği gibi; sade ama derin, tatlı ama abartısız bir gün… çünkü senin doğum günün 🌸

Tekrar tekrar doğum günün kutlu olsun. Farklı ve güzel bir şey hazırlamak istedim. Umarım beğenirsin de.

Zaten ilk baştan beri biliyorsun sana olan duygularımı, o yüzden anlamlı ve farklı bir hediye vermek istedim sana.

Yeni yaşın sana en çok sevdiğin şeyleri getirsin…
Mesela huzur, kahkaha, yanında seni gerçekten önemseyen birini.

İyi ki doğdun, iyi ki varsın.</p>
  </div>

  <div class="footer">Giresun'dan minicup tadında bir sürprizle 💖</div>

  <div class="hearts">
    <span style="left: 10%; animation-delay: 0s;"></span>
    <span style="left: 25%; animation-delay: 2s;"></span>
    <span style="left: 40%; animation-delay: 4s;"></span>
    <span style="left: 60%; animation-delay: 1s;"></span>
    <span style="left: 80%; animation-delay: 3s;"></span>
  </div>

  <script>
    function showOptions() {
      document.getElementById('options').style.display = 'flex';
    }
    function showSurprise() {
      document.getElementById('surprise').style.display = 'block';
    }
  </script>
</body>
</html>
