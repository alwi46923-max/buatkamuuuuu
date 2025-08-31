<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Web Halaman Berganti</title>
  <style>
    body {
      font-family: "Segoe UI", Arial, sans-serif;
      text-align: center;
      background: linear-gradient(135deg, #ff99cc, #ff66b2, #ff3385);
      margin: 0;
      padding: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
    }
    .page {
      display: none;
      font-size: 2em;
      color: white;
      opacity: 0;
      transition: opacity 0.7s ease-in-out;
    }
    .active {
      display: block;
      opacity: 1;
    }

    /* Tombol keren */
    button {
      margin-top: 25px;
      padding: 12px 35px;
      font-size: 1.3em;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      background: #ff1a8c;
      color: white;
      font-weight: bold;
      box-shadow: 0 0 15px #ff4da6, 0 0 30px #ff1a8c;
      transition: transform 0.2s ease, box-shadow 0.3s ease, background 0.3s ease;
    }
    button:hover {
      background: #ff66b2;
      transform: scale(1.1);
      box-shadow: 0 0 25px #ff80bf, 0 0 50px #ff1a8c;
    }
  </style>
</head>
<body>

  <!-- Halaman 1 -->
  <div class="page active" id="page1">
    <button onclick="nextPage('page2')">1</button>
  </div>

  <!-- Halaman 2 -->
  <div class="page" id="page2">
    <p>2</p>
    <button onclick="nextPage('page3')">Lanjut</button>
  </div>

  <!-- Halaman 3 -->
  <div class="page" id="page3">
    <p>3🤭</p>
    <button onclick="nextPage('page4')">Lanjut</button>
  </div>

  <!-- Halaman 4 -->
  <div class="page" id="page4">
    <p>❤️ I LOVE YOU ❤️<br>DARI AKUUUUU</p>
    <button onclick="nextPage('page5')">Selanjutnya</button>
  </div>

  <!-- Halaman 5 -->
  <div class="page" id="page5">
    <p><b>Cara membuat nasgor</b></p>
    <p>1. ambil nasi 🤭</p>
    <p>2. goreng</p>
    <p>😹 Selesai 😹</p>
  </div>

  <script>
    function nextPage(pageId) {
      let pages = document.querySelectorAll(".page");
      pages.forEach(p => {
        p.classList.remove("active");
        p.style.display = "none";
      });

      let next = document.getElementById(pageId);
      next.style.display = "block";
      setTimeout(() => next.classList.add("active"), 50); 
    }
  </script>

</body>
</html>
