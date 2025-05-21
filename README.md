
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Website Sederhana</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: #333;
        }
        header {
            background-color: #4CAF50;
            color: white;
            padding: 20px 0;
            text-align: center;
        }
        nav {
            background-color: #333;
            overflow: hidden;
        }
        nav a {
            float: left;
            display: block;
            color: white;
            text-align: center;
            padding: 14px 16px;
            text-decoration: none;
        }
        nav a:hover {
            background-color: #ddd;
            color: black;
        }
        .container {
            width: 80%;
            margin: 0 auto;
            padding: 20px;
        }
        .main-content {
            background-color: white;
            padding: 20px;
            border-radius: 5px;
            margin-top: 20px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        .card {
            background-color: white;
            padding: 20px;
            margin-top: 20px;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 20px 0;
            margin-top: 20px;
        }
        button {
            background-color: #4CAF50;
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
    </style>
</head>
<body>
    <header>
        <h1>Selamat Datang di Website Saya</h1>
        <p>Website HTML sederhana dengan beberapa fitur dasar</p>
    </header>
    
    <nav>
        <a href="#home">Beranda</a>
        <a href="#about">Tentang</a>
        <a href="#services">Layanan</a>
        <a href="#contact">Kontak</a>
    </nav>
    
    <div class="container">
        <div class="main-content">
            <h2>Beranda</h2>
            <p>Selamat datang di website sederhana saya. Website ini dibuat menggunakan HTML, CSS, dan sedikit JavaScript.</p>
            <p>Anda dapat mengeksplorasi konten lainnya dengan mengklik menu navigasi di atas.</p>
            <button id="changeColorBtn">Ubah Warna</button>
        </div>
        
        <div id="about" class="card">
            <h2>Tentang</h2>
            <p>Ini adalah bagian tentang website ini. Anda dapat menambahkan informasi tentang diri Anda atau tujuan website ini di sini.</p>
        </div>
        
        <div id="services" class="card">
            <h2>Layanan</h2>
            <p>Beberapa layanan yang kami tawarkan:</p>
            <ul>
                <li>Layanan 1</li>
                <li>Layanan 2</li>
                <li>Layanan 3</li>
            </ul>
        </div>
        
        <div id="contact" class="card">
            <h2>Kontak</h2>
            <p>Anda dapat menghubungi kami melalui:</p>
            <form id="contactForm">
                <div>
                    <label for="name">Nama:</label><br>
                    <input type="text" id="name" name="name" style="width:100%;padding:8px;margin:8px 0;">
                </div>
                <div>
                    <label for="email">Email:</label><br>
                    <input type="email" id="email" name="email" style="width:100%;padding:8px;margin:8px 0;">
                </div>
                <div>
                    <label for="message">Pesan:</label><br>
                    <textarea id="message" name="message" style="width:100%;height:100px;padding:8px;margin:8px 0;"></textarea>
                </div>
                <button type="submit">Kirim Pesan</button>
            </form>
        </div>
    </div>
    
    <footer>
        <p>&copy; 2025 Website Sederhana. Hak Cipta Dilindungi.</p>
    </footer>

    <script>
        // Fungsi sederhana untuk mengubah warna latar belakang
        document.getElementById('changeColorBtn').addEventListener('click', function() {
            const colors = ['#f4f4f4', '#e8f5e9', '#e3f2fd', '#fff8e1', '#fce4ec'];
            const randomColor = colors[Math.floor(Math.random() * colors.length)];
            document.body.style.backgroundColor = randomColor;
        });
        
        // Menangani pengiriman formulir
        document.getElementById('contactForm').addEventListener('submit', function(event) {
            event.preventDefault();
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const message = document.getElementById('message').value;
            
            if (name && email && message) {
                alert('Terima kasih, ' + name + '! Pesan Anda telah dikirim.');
                this.reset();
            } else {
                alert('Mohon isi semua kolom yang disediakan.');
            }
        });
    </script>
</body>
</html>
