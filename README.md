# peroduasales
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Perodua Sales Advisor</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Poppins', sans-serif; }
        body { background: #f8f9fa; color: #333; }
        header { background: #b71c1c; color: white; padding: 20px; text-align: center; font-size: 28px; font-weight: 600; box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2); }
        nav { display: flex; justify-content: center; background: #222; padding: 15px; }
        nav a { color: white; text-decoration: none; margin: 0 20px; font-size: 18px; padding: 10px; transition: 0.3s; }
        nav a:hover { background: #b71c1c; border-radius: 5px; padding: 10px; }
        .language-toggle { text-align: center; margin: 20px; }
        button { padding: 10px 20px; margin: 5px; border: none; cursor: pointer; font-size: 16px; border-radius: 5px; }
        .btn-en { background: #007bff; color: white; }
        .btn-my { background: #28a745; color: white; }
        section { padding: 60px 20px; text-align: center; background: white; margin: 30px auto; width: 80%; border-radius: 12px; box-shadow: 0 6px 15px rgba(0, 0, 0, 0.1); display: none; }
        .car-list { display: flex; justify-content: center; gap: 30px; flex-wrap: wrap; }
        .car-list img { width: 280px; height: auto; border-radius: 12px; box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2); transition: 0.3s; }
        .car-list img:hover { transform: scale(1.07); }
        .cta-button { background: #ff5722; color: white; padding: 14px 28px; text-decoration: none; border-radius: 6px; font-size: 20px; transition: 0.3s; display: inline-block; margin-top: 15px; }
        .cta-button:hover { background: #e64a19; }
        footer { background: #222; color: white; text-align: center; padding: 20px; font-size: 16px; margin-top: 30px; border-radius: 0 0 12px 12px; }
    </style>
    <script>
        function switchLanguage(lang) {
            document.querySelectorAll("section").forEach(sec => sec.style.display = "none");
            document.getElementById(lang).style.display = "block";
        }
    </script>
</head>
<body onload="switchLanguage('en')">
    <header>
        Welcome to Perodua Sales - Premium Experience / Selamat Datang ke Perodua Sales - Pengalaman Premium
    </header>
    <div class="language-toggle">
        <button class="btn-en" onclick="switchLanguage('en')">English</button>
        <button class="btn-my" onclick="switchLanguage('my')">Bahasa Malaysia</button>
    </div>
    <section id="en">
        <h2>Our Premium Car Models</h2>
        <div class="car-list">
            <img src="axia.png" alt="Perodua Axia">
            <img src="bezza.jpg" alt="Perodua Bezza">
            <img src="myvi.jpg" alt="Perodua Myvi">
        </div>
        <h2>Exclusive Promotions</h2>
        <p>Unlock the best financing options and limited-time offers!</p>
        <a href="#contact" class="cta-button">Get Offer Now</a>
    </section>
    <section id="my">
        <h2>Model Kereta Premium Kami</h2>
        <div class="car-list">
            <img src="axia.jpg" alt="Perodua Axia">
            <img src="bezza.jpg" alt="Perodua Bezza">
            <img src="myvi.jpg" alt="Perodua Myvi">
        </div>
        <h2>Promosi Eksklusif</h2>
        <p>Dapatkan tawaran pembiayaan terbaik dan promosi terhad!</p>
        <a href="#contact" class="cta-button">Dapatkan Tawaran</a>
    </section>
    <footer>
        &copy; 2025 Perodua Sales Advisor | Premium Automotive Experience
    </footer>
</body>
</html>
