<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Garuda Internusa - Tour and Travel Terbaik di Indonesia</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css ">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }
        :root {
            --primary: #1a3c6c;
            --secondary: #d4af37;
            --accent: #e63946;
            --light: #f8f9fa;
            --dark: #212529;
            --transition: all 0.3s ease;
        }
        body {
            background-color: #f5f7fa;
            color: #333;
            overflow-x: hidden;
        }
        header {
            background-color: var(--primary);
            padding: 15px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .logo {
            display: flex;
            align-items: center;
        }
        .logo img {
            height: 50px;
            margin-right: 10px;
        }
        .logo h1 {
            color: white;
            font-size: 1.8rem;
        }
        .logo span {
            color: var(--secondary);
        }
        .nav-links {
            display: flex;
            list-style: none;
            gap: 25px;
        }
        .nav-links li {
            position: relative;
        }
        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            font-size: 1.1rem;
            padding: 5px 10px;
            transition: color 0.3s ease;
        }
        .nav-links a:hover {
            color: var(--secondary);
        }
        .nav-links a::after {
            content: '';
            position: absolute;
            left: 0;
            bottom: -5px;
            width: 0;
            height: 2px;
            background-color: var(--secondary);
            transition: width 0.3s ease;
        }
        .nav-links a:hover::after {
            width: 100%;
        }
        .cta-button {
            background-color: var(--secondary);
            color: var(--primary);
            padding: 10px 25px;
            border-radius: 30px;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
        }
        .cta-button:hover {
            background-color: #c19b2c;
            transform: translateY(-2px);
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
        }
        .mobile-menu {
            display: none;
            font-size: 1.5rem;
            color: white;
            cursor: pointer;
        }
        .hero {
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('https://images.unsplash.com/photo-1520250497591-112f2f40a3f4?ixlib=rb-4.0.3&auto=format&fit=crop&w=1950&q=80');
            background-size: cover;
            background-position: center;
            height: 100vh;
            display: flex;
            align-items: center;
            text-align: center;
            color: white;
            margin-top: 80px;
        }
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
        }
        .hero h2 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            text-shadow: 0 2px 5px rgba(0,0,0,0.5);
        }
        .hero p {
            font-size: 1.3rem;
            margin-bottom: 30px;
            text-shadow: 0 1px 3px rgba(0,0,0,0.5);
        }
        .search-box {
            background: rgba(255, 255, 255, 0.9);
            padding: 20px;
            border-radius: 10px;
            max-width: 800px;
            margin: 30px auto 0;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
        }
        .search-input {
            flex: 1;
            padding: 15px;
            margin: 5px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
        }
        section {
            padding: 80px 0;
        }
        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }
        .section-title h2 {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 15px;
        }
        .section-title p {
            color: #666;
            max-width: 700px;
            margin: 0 auto;
            font-size: 1.1rem;
        }
        .destinations {
            background-color: white;
        }
        .destination-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        .destination-card {
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: var(--transition);
            background: white;
            position: relative;
        }
        .destination-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.15);
        }
        .destination-img {
            height: 250px;
            overflow: hidden;
        }
        .destination-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
        }
        .destination-card:hover .destination-img img {
            transform: scale(1.1);
        }
        .destination-info {
            padding: 20px;
        }
        .destination-info h3 {
            font-size: 1.4rem;
            margin-bottom: 10px;
            color: var(--primary);
        }
        .destination-info p {
            color: #666;
            margin-bottom: 15px;
        }
        .price {
            font-size: 1.3rem;
            font-weight: 700;
            color: var(--secondary);
        }
        .new-badge {
            position: absolute;
            top: 15px;
            right: 15px;
            background-color: var(--accent);
            color: white;
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
            z-index: 10;
        }
        .packages {
            background-color: #f0f4f8;
        }
        .package-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
        }
        .package-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: var(--transition);
        }
        .package-card:hover {
            transform: translateY(-10px);
        }
        .package-header {
            background: var(--primary);
            color: white;
            padding: 20px;
            text-align: center;
        }
        .package-header h3 {
            font-size: 1.8rem;
            margin-bottom: 10px;
        }
        .package-price {
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--secondary);
        }
        .package-duration {
            font-size: 1.1rem;
            opacity: 0.8;
        }
        .package-features {
            padding: 25px;
        }
        .package-features ul {
            list-style: none;
            margin-bottom: 30px;
        }
        .package-features li {
            padding: 10px 0;
            border-bottom: 1px solid #eee;
            display: flex;
            align-items: center;
        }
        .package-features li i {
            color: var(--secondary);
            margin-right: 10px;
            width: 20px;
        }
        .testimonials {
            background: white;
        }
        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        .testimonial-card {
            background: #f8f9fa;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            position: relative;
        }
        .testimonial-card::before {
            content: '"';
            position: absolute;
            top: 20px;
            left: 20px;
            font-size: 5rem;
            color: var(--primary);
            opacity: 0.1;
            font-family: Georgia, serif;
        }
        .testimonial-content {
            margin-top: 20px;
            color: #555;
            line-height: 1.7;
        }
        .testimonial-author {
            display: flex;
            align-items: center;
            margin-top: 20px;
        }
        .testimonial-author img {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            object-fit: cover;
            margin-right: 15px;
        }
        .author-info h4 {
            color: var(--primary);
            margin-bottom: 5px;
        }
        .author-info p {
            color: var(--secondary);
            font-size: 0.9rem;
        }
        .contact {
            background: linear-gradient(to right, var(--primary), #2a5298);
            color: white;
        }
        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 50px;
        }
        .contact-info h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
        }
        .contact-detail {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
        }
        .contact-detail i {
            font-size: 1.5rem;
            color: var(--secondary);
            margin-right: 15px;
            width: 40px;
        }
        .contact-form .form-group {
            margin-bottom: 20px;
        }
        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 15px;
            border: none;
            border-radius: 5px;
            background: rgba(255,255,255,0.9);
            font-size: 1rem;
        }
        .contact-form textarea {
            height: 150px;
            resize: vertical;
        }
        footer {
            background: #0d1f3a;
            color: #aaa;
            padding: 50px 0 20px;
        }
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-bottom: 40px;
        }
        .footer-section h3 {
            color: white;
            margin-bottom: 20px;
            font-size: 1.3rem;
        }
        .footer-links a {
            display: block;
            color: #aaa;
            text-decoration: none;
            margin-bottom: 10px;
            transition: var(--transition);
        }
        .footer-links a:hover {
            color: var(--secondary);
        }
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: #1a3c6c;
            border-radius: 50%;
            color: white;
            transition: var(--transition);
        }
        .social-links a:hover {
            background: var(--secondary);
            transform: translateY(-5px);
        }
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.1);
            font-size: 0.9rem;
        }
        @media (max-width: 992px) {
            .hero h2 {
                font-size: 2.8rem;
            }
        }
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            .mobile-menu {
                display: block;
            }
            .hero h2 {
                font-size: 2.3rem;
            }
            .hero p {
                font-size: 1.1rem;
            }
            .search-box {
                flex-direction: column;
            }
            .search-input {
                width: 100%;
            }
            .section-title h2 {
                font-size: 2rem;
            }
        }
        @media (max-width: 480px) {
            .hero h2 {
                font-size: 2rem;
            }
            .logo h1 {
                font-size: 1.5rem;
            }
            .cta-button {
                padding: 8px 15px;
                font-size: 0.9rem;
            }
        }
        .video-section {
            padding: 80px 0;
            background-color: #f0f4f8;
            text-align: center;
        }
        .video-wrapper {
            position: relative;
            padding-bottom: 56.25%;
            height: 0;
            overflow: hidden;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            margin-top: 30px;
        }
        .video-wrapper iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: none;
        }
        .video-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(26,60,108,0.8) 0%, rgba(212,175,55,0.6) 100%);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            color: white;
            border-radius: 10px;
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        .video-wrapper:hover .video-overlay {
            opacity: 1;
        }
        .play-button {
            width: 80px;
            height: 80px;
            background-color: var(--secondary);
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            margin-bottom: 20px;
            transition: transform 0.3s ease;
        }
        .play-button:hover {
            transform: scale(1.1);
        }
        .play-button i {
            font-size: 2.5rem;
            color: white;
        }
        .error-message {
            display: none;
            color: var(--accent);
            font-size: 1rem;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav class="navbar">
                <div class="logo">
                    <img src=" https://i.imgur.com/4olZLmP.png " alt="Garuda Internusa Logo">
                    <h1>GARUDA <span>INTERNUSA</span></h1>
                </div>
                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#destinations">Destinasi</a></li>
                    <li><a href="#packages">Paket Wisata</a></li>
                    <li><a href="#testimonials">Testimoni</a></li>
                    <li><a href="#contact">Kontak</a></li>
                </ul>
                <button class="cta-button">Pesan Sekarang</button>
                <div class="mobile-menu">
                    <i class="fas fa-bars"></i>
                </div>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h2>Jelajahi Keindahan Indonesia Bersama Kami</h2>
            <p>Perjalanan tak terlupakan ke destinasi terbaik dengan layanan premium dan harga terbaik</p>
            <button class="cta-button">Mulai Petualangan</button>
            <div class="search-box">
                <input type="text" class="search-input" placeholder="Cari Destinasi...">
                <select class="search-input">
                    <option value="">Semua Kategori</option>
                    <option value="beach">Pantai</option>
                    <option value="mountain">Gunung</option>
                    <option value="culture">Budaya</option>
                    <option value="adventure">Petualangan</option>
                </select>
                <input type="date" class="search-input">
                <button class="cta-button">Cari</button>
            </div>
        </div>
    </section>

    <!-- Video Section -->
    <section class="video-section" id="video">
        <div class="container">
            <div class="section-title">
                <h2>Pengalaman Wisata Tak Terlupakan</h2>
                <p>Saksikan momen-momen indah perjalanan bersama Garuda Internusa</p>
            </div>
            <div class="video-wrapper">
                <iframe id="youtubeVideo" src="https://www.youtube.com/embed/qDf0rCtN-5o " allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                <div class="video-overlay" id="videoOverlay">
                    <div class="play-button" id="playButton"><i class="fas fa-play"></i></div>
                    <h3 class="video-title">Petualangan Seru di Kepulauan Seribu</h3>
                    <p class="video-description">Lihat pengalaman langsung wisatawan kami menjelajahi Pulau Pramuka Kepulauan seribu Jakarta Indonesia</p>
                </div>
            </div>
            <div class="error-message" id="errorMessage">
                <i class="fas fa-exclamation-triangle"></i>
                <p>Maaf, video tidak dapat diputar. Silakan coba lagi nanti.</p>
                <button class="cta-button" id="reloadButton" style="margin-top: 10px;">Coba Lagi</button>
            </div>
        </div>
    </section>

    <!-- Destinations Section -->
    <section class="destinations" id="destinations">
        <div class="container">
            <div class="section-title">
                <h2>Destinasi Populer</h2>
                <p>Temukan tempat-tempat menakjubkan yang siap Anda kunjungi bersama Garuda Internusa</p>
            </div>
            <div class="destination-grid">
                <div class="destination-card">
                    <div class="new-badge">BARU</div>
                    <div class="destination-img">
                        <img src="https://i.imgur.com/xBAQNOr.jpeg " alt="Way Kambas">
                    </div>
                    <div class="destination-info">
                        <h3>Way Kambas, Lampung</h3>
                        <p>Menjelajahi hutan tropis dan melihat gajah sumatra di habitat aslinya</p>
                        <div class="price">Mulai Rp 2.900.000</div>
                        <button class="cta-button">Detail</button>
                    </div>
                </div>
                <div class="destination-card">
                    <div class="new-badge">BARU</div>
                    <div class="destination-img">
                        <img src="https://i.imgur.com/s2EA5Oy.jpeg " alt="Pulau Pisang">
                    </div>
                    <div class="destination-info">
                        <h3>Pulau Pisang, Lampung</h3>
                        <p>Pulau eksotis dengan pantai berpasir putih dan air laut jernih kebiruan</p>
                        <div class="price">Mulai Rp 2.500.000</div>
                        <button class="cta-button">Detail</button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Packages Section -->
    <section class="packages" id="packages">
        <div class="container">
            <div class="section-title">
                <h2>Paket Wisata Unggulan</h2>
                <p>Pilih paket perjalanan yang sesuai dengan kebutuhan dan impian Anda</p>
            </div>
            <div class="package-cards">
                <div class="package-card">
                    <div class="package-header">
                        <h3>Paket Silver</h3>
                        <div class="package-price">Rp 2.999K</div>
                        <div class="package-duration">3 Hari 2 Malam</div>
                    </div>
                    <div class="package-features">
                        <ul>
                            <li><i class="fas fa-check"></i> Akomodasi hotel bintang 3</li>
                            <li><i class="fas fa-check"></i> Transportasi selama wisata</li>
                            <li><i class="fas fa-check"></i> Makan 3x sehari</li>
                            <li><i class="fas fa-check"></i> Tour guide profesional</li>
                            <li><i class="fas fa-times"></i> Tiket masuk wisata</li>
                            <li><i class="fas fa-times"></i> Asuransi perjalanan</li>
                        </ul>
                        <button class="cta-button">Pilih Paket</button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section class="testimonials" id="testimonials">
        <div class="container">
            <div class="section-title">
                <h2>Apa Kata Pelanggan Kami</h2>
                <p>Pengalaman nyata dari pelanggan yang telah berwisata bersama kami</p>
            </div>
            <div class="testimonial-grid">
                <div class="testimonial-card">
                    <div class="testimonial-content">
                        "Our expedition to Way Kambas Forest with Garuda Internusa was simply smashing! We were absolutely chuffed to observe Sumatran elephants in their natural habitat rather up close."
                    </div>
                    <div class="testimonial-author">
                        <img src="https://i.imgur.com/bdey9KP.jpeg " alt="Customer">
                        <div class="author-info">
                            <h4>Matt</h4>
                            <p>Wisata Way Kambas Lampung, Oktober 2024</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="container">
            <div class="section-title">
                <h2>Hubungi Kami</h2>
                <p>Punya pertanyaan atau ingin memesan paket wisata? Tim kami siap membantu Anda</p>
            </div>
            <div class="contact-container">
                <div class="contact-info">
                    <h3>Informasi Kontak</h3>
                    <div class="contact-detail">
                        <i class="fas fa-map-marker-alt"></i>
                        <div>
                            <h4>Alamat</h4>
                            <p>Gg. Buntu, Jl. Ibrahim Adji, Batununggal, Bandung</p>
                        </div>
                    </div>
                </div>
                <div class="contact-form">
                    <form>
                        <div class="form-group">
                            <input type="text" placeholder="Nama Lengkap" required>
                        </div>
                        <div class="form-group">
                            <input type="email" placeholder="Email" required>
                        </div>
                        <div class="form-group">
                            <input type="tel" placeholder="Telepon" required>
                        </div>
                        <div class="form-group">
                            <textarea placeholder="Pesan Anda" required></textarea>
                        </div>
                        <button type="submit" class="cta-button">Kirim Pesan</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <div class="logo">
                        <img src="https://i.imgur.com/4olZLmP.png " alt="Garuda Internusa Logo">
                        <h3>GARUDA INTERNUSA</h3>
                    </div>
                    <p>Menyediakan pengalaman wisata terbaik di seluruh Indonesia dengan layanan premium dan harga kompetitif.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
                <div class="footer-section">
                    <h3>Link Cepat</h3>
                    <div class="footer-links">
                        <a href="#home">Home</a>
                        <a href="#destinations">Destinasi</a>
                        <a href="#packages">Paket Wisata</a>
                        <a href="#contact">Kontak</a>
                    </div>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; <span id="currentYear"></span> Garuda Internusa. Hak Cipta Dilindungi.</p>
            </div>
        </div>
    </footer>

    <!-- JavaScript -->
    <script>
        // Smooth Scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    window.scrollTo({ top: target.offsetTop - 80, behavior: 'smooth' });
                }
            });
        });

        // Mobile Menu Toggle
        const mobileMenu = document.querySelector('.mobile-menu');
        const navLinks = document.querySelector('.nav-links');
        mobileMenu.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });

        // Auto Update Year
        document.getElementById('currentYear').textContent = new Date().getFullYear();

        // Video Player
        const playButton = document.getElementById('playButton');
        const videoIframe = document.getElementById('youtubeVideo');
        const videoOverlay = document.getElementById('videoOverlay');
        const errorMessage = document.getElementById('errorMessage');
        const reloadButton = document.getElementById('reloadButton');

        playButton.addEventListener('click', () => {
            videoIframe.src = "https://www.youtube.com/embed/qDf0rCtN-5o?autoplay=1";
            videoOverlay.style.display = 'none';
        });

        window.addEventListener('scroll', () => {
            const videoSection = document.getElementById('video');
            const rect = videoSection.getBoundingClientRect();
            if (rect.bottom < 0 || rect.top > window.innerHeight) {
                videoIframe.src = " https://www.youtube.com/embed/qDf0rCtN-5o ";
                videoOverlay.style.display = 'flex';
            }
        });

        reloadButton.addEventListener('click', () => {
            errorMessage.style.display = 'none';
            playButton.click();
        });

        // Form Submission
        document.querySelector('.contact-form form').addEventListener('submit', function (e) {
            e.preventDefault();
            if (this.checkValidity()) {
                alert('Pesan berhasil dikirim!');
                this.reset();
            } else {
                this.reportValidity();
            }
        });
    </script>
</body>
</html>
