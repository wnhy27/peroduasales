<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Perodua Sales Advisor</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Poppins', sans-serif; }
    body { background: #f8f9fa; color: #333; scroll-behavior: smooth; }
    header {
      background: #b71c1c;
      color: white;
      padding: 20px;
      text-align: center;
      font-size: 28px;
      font-weight: 600;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
    }

    nav {
      display: flex;
      justify-content: center;
      background: #222;
      padding: 15px;
      position: sticky;
      top: 0;
      z-index: 100;
    }

    nav a {
      color: white;
      text-decoration: none;
      margin: 0 20px;
      font-size: 18px;
      padding: 10px;
      transition: 0.3s;
    }

    nav a:hover {
      background: #b71c1c;
      border-radius: 5px;
    }

    section {
      padding: 60px 20px;
      text-align: center;
      background: white;
      margin: 30px auto;
      width: 80%;
      border-radius: 12px;
      box-shadow: 0 6px 15px rgba(0, 0, 0, 0.1);
    }

    .car-list {
      display: flex;
      justify-content: center;
      gap: 30px;
      flex-wrap: wrap;
    }

    .car-item {
      position: relative;
      display: inline-block;
    }

    .car-item img {
      width: 300px;
      height: auto;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
      transition: 0.3s;
    }

    .car-item:hover img {
      transform: scale(1.07);
    }

    .car-name {
      position: absolute;
      bottom: 10px;
      left: 50%;
      transform: translateX(-50%);
      background: rgba(0, 0, 0, 0.7);
      color: white;
      padding: 8px 12px;
      border-radius: 6px;
      font-size: 16px;
      font-weight: bold;
      width: 80%;
      text-align: center;
    }

    .cta-button {
      background: #ff5722;
      color: white;
      padding: 14px 28px;
      text-decoration: none;
      border-radius: 6px;
      font-size: 20px;
      transition: 0.3s;
      display: inline-block;
      margin-top: 15px;
    }

    .cta-button:hover {
      background: #e64a19;
    }

    footer {
      background: #222;
      color: white;
      text-align: center;
      padding: 20px;
      font-size: 16px;
      margin-top: 30px;
      border-radius: 0 0 12px 12px;
    }
.h2 {
  font-family: "Lucida Console", "Courier New", monospace;
}

h2 {
  font-size: 36px;
  font-weight: 700;
  margin-bottom: 20px;
  color: #000000;
  text-transform: uppercase;
  letter-spacing: 1px;
}

  </style>
</head>

<body>
  <header>
    Welcome to Perodua Sales - Premium Experience
  </header>

  <nav>
    <a href="#promotions">Promotions</a>
    <a href="#cars">Car Models</a>
    <a href="#feedback">Customer Feedback</a> <!-- New Customer Feedback Section -->
    <a href="#about">About Us</a>
  </nav>

  <!-- PROMOTION SECTION -->
  <section id="promotions">
    <h2>Exclusive Promotions</h2>
    <img src="pro.jpg" alt="Promotion Banner" style="width:100%; max-width:600px; border-radius: 12px;"/>
    <p>Get the best financing options & limited-time offers!</p>
    <a href="https://wapp.my/60123738541/zaperiperodua" target="_blank" class="cta-button">Claim Offer on WhatApps</a>
  </section>

<!-- CAR MODEL SECTION -->
<section id="cars">
  <h2>Our Premium Car Models</h2>
  <div class="car-list">
    <div class="car-item">
      <img src="axia-red.jpg" alt="Axia" onclick="openModal(0)" style="cursor: pointer;">
      <p class="car-name">Axia</p>
    </div>
    <div class="car-item">
      <img src="bezza-white.jpg" alt="Bezza" onclick="openModal(1)" style="cursor: pointer;">
      <p class="car-name">Bezza</p>
    </div>
    <div class="car-item">
      <img src="myvi-blue.png" alt="Myvi" onclick="openModal(2)" style="cursor: pointer;">
      <p class="car-name">Myvi</p>
    </div>
    <div class="car-item">
      <img src="ativa-grey.jpg" alt="Ativa" onclick="openModal(3)" style="cursor: pointer;">
      <p class="car-name">Ativa</p>
    </div>
    <div class="car-item">
      <img src="alza-brown.jpg" alt="Alza" onclick="openModal(4)" style="cursor: pointer;">
      <p class="car-name">Alza</p>
    </div>
    <div class="car-item">
      <img src="Aruz-Garnet-Red.jpg" alt="Aruz" onclick="openModal(5)" style="cursor: pointer;">
      <p class="car-name">Aruz</p>
    </div>
  </div>
</section>

<!-- CAR IMAGE MODAL WITH NEXT/PREV -->
<div id="carModal" class="imgModal">
  <span class="close" onclick="closeModal()">&times;</span>
  <img id="modalImage" src="" alt="" />
  <p id="modalCaption"></p>
  <div class="nav-buttons">
    <button onclick="changeImage(-1)">❮ Prev</button>
    <button onclick="changeImage(1)">Next ❯</button>
  </div>
</div>

<style>
  .imgModal {
    display: none;
    position: fixed;
    z-index: 999;
    padding-top: 60px;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    overflow: auto;
    background-color: rgba(0, 0, 0, 0.85);
    text-align: center;
  }

  .imgModal img {
    max-width: 90%;
    max-height: 80vh;
    margin-bottom: 15px;
    border-radius: 12px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.5);
  }

  .imgModal p {
    color: white;
    font-size: 20px;
    font-weight: bold;
    margin-bottom: 20px;
  }

  .close {
    position: absolute;
    top: 20px;
    right: 40px;
    color: #fff;
    font-size: 40px;
    cursor: pointer;
    font-weight: bold;
  }

  .nav-buttons {
    display: flex;
    justify-content: center;
    gap: 20px;
  }

  .nav-buttons button {
    padding: 10px 20px;
    font-size: 18px;
    background: #ff5722;
    border: none;
    color: white;
    border-radius: 8px;
    cursor: pointer;
    transition: 0.3s;
  }

  .nav-buttons button:hover {
    background: #e64a19;
  }
</style>

<script>
  const carImages = [
    { src: "hargaaxia.png", caption: "AXIA"},
    { src: "hargabezza.png", caption: "BEZZA" },
    { src: "hargamyvi.png", caption: "MYVI" },
    { src: "hargaativa.png", caption: "ATIVA" },
    { src: "hargaalza.png", caption: "ALZA" },
    { src: "hargaaruz.png", caption: "ARUZ" }
  ];

  let currentIndex = 0;

  function openModal(index) {
    currentIndex = index;
    const modal = document.getElementById("carModal");
    const img = document.getElementById("modalImage");
    const caption = document.getElementById("modalCaption");

    img.src = carImages[index].src;
    caption.textContent = carImages[index].caption;
    modal.style.display = "block";
  }

  function closeModal() {
    document.getElementById("carModal").style.display = "none";
  }

  function changeImage(direction) {
    currentIndex = (currentIndex + direction + carImages.length) % carImages.length;
    openModal(currentIndex);
  }
</script>

  <!-- CUSTOMER FEEDBACK SECTION -->
  <section id="feedback">
    <h2>Customer Feedback</h2>
     <div class="car-list">
    <div class="car-item">
      <img src="fb1.jpg" alt="Customer Feedback 1">
      <p class="car-name">"Servis Tip Top dan mudah berurusan."</p>
    </div>
    <div class="car-item">
      <img src="fb2.jpg" alt="Customer Feedback 2">
      <p class="car-name">"Highly recommended!"</p>
    </div>
    <div class="car-item">
      <img src="fb3.jpg" alt="Customer Feedback 3">
      <p class="car-name">"Fast response & easy process."</p>
    </div>
    <div class="car-item">
      <img src="fb4.jpg" alt="Customer Feedback 3">
      <p class="car-name">"Great service, very helpful!."</p>
    </div>
    <div class="car-item">
      <img src="fb5.jpg" alt="Customer Feedback 3">
      <p class="car-name">"Terima kasih Saya pulang dengan kereta yang saya inginkan, dan prosesnya sangat mudah!."</p>
    </div>
  </div>
  </section>

  <!-- ABOUT SECTION -->
  <section id="about">
    <h2>About Us</h2>
    <p>Saya merupakan Perunding Jualan Perodua yang sah dan berpengalaman, bersedia membantu anda memiliki kereta impian dengan mudah, cepat dan jimat.</p>
    <h2> Kenapa Pilih Kami?</h2>

  <li>Respons cepat</li>
  <li>Harga promosi terkini</li>
  <li>Banyak testimoni pelanggan</li>
  <li>Mudah dihubungi bila-bila masa</li>

<!-- TEAM PHOTO WITH POPUP -->
<div class="car-list" style="margin-top: 30px; justify-content: center;">
  <div class="car-item">
    <img src="operator.png" alt="Team 1" id="thumb1" style="width: 80px; border-radius: 8px; cursor: pointer; box-shadow: 0 4px 10px rgba(0,0,0,0.2);" />
    <p style="margin-top: 10px;">Contact Us</p>
  </div>
<!-- Gambar 2: Pautan ke lokasi Google Maps -->
<div class="car-item">
  <a href="https://www.bing.com/search?q=one%20built%20well&qs=n&form=QBRE&sp=-1&ghc=1&lq=0&pq=one%20built%20well&sc=10-14&sk=&cvid=C177091DEE904E98905C36F6F37573A2" target="_blank">
    <img src="placeholder.png" alt="Lokasi" style="width: 80px; border-radius: 8px; cursor: pointer; box-shadow: 0 4px 10px rgba(0,0,0,0.2);" />
  </a>
  <p style="margin-top: 10px;">Our Location</p>
</div>

  <div class="car-item">
    <a href="https://www.facebook.com/profile.php?id=100063690003177&mibextid=wwXIfr&mibextid=wwXIfr" target="_blank">
      <img src="facebook.png" alt="Facebook" style="width: 80px; border-radius: 8px; cursor: pointer; box-shadow: 0 4px 10px rgba(0,0,0,0.2);" />
    </a>
    <p style="margin-top: 10px;">FaceBook</p>
  </div>

  <div class="car-item">
    <a href="https://wapp.my/60123738541/zaperiperodua" target="_blank">
      <img src="whatsapp.png" alt="Facebook" style="width: 80px; border-radius: 8px; cursor: pointer; box-shadow: 0 4px 10px rgba(0,0,0,0.2);" />
    </a>
    <p style="margin-top: 10px;">WhatsApp</p>
  </div>
</div>

<!-- IMAGE MODAL POPUP -->
<div id="imgModal" style="display:none; position:fixed; z-index:999; padding-top:60px; left:0; top:0; width:100%; height:100%; overflow:auto; background-color:rgba(0,0,0,0.8);">
  <span onclick="document.getElementById('imgModal').style.display='none'" 
        style="position:absolute; top:20px; right:35px; color:#fff; font-size:40px; font-weight:bold; cursor:pointer;">&times;</span>
  <img id="modalImg" src="" style="margin:auto; display:block; max-width:90%; max-height:90%; border-radius: 12px;">
</div>

<script>
  const thumbnails = [
    { id: "thumb1", src: "operator.png" },
    { id: "thumb2", src: "placeholder.png" },
  ];

  thumbnails.forEach(item => {
    document.getElementById(item.id).onclick = function () {
      const modal = document.getElementById("imgModal");
      const modalImg = document.getElementById("modalImg");
      modalImg.src = item.src;
      modal.style.display = "block";
    };
  });
</script>

  <footer>
    &copy; 2025 Perodua Sales Advisor | Premium Automotive Experience
  </footer>
</body>
</html>
