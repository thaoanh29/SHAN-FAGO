<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <title>SHAN – FAGO | Tinh Hoa Quà Tặng Hà Giang</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600&family=Playfair+Display:ital,wght@0,700;1,400&display=swap" rel="stylesheet">
    
    <link rel="stylesheet" href="https://unpkg.com/aos@next/dist/aos.css" />

    <style>
        :root {
            --gold: #b08d57;
            --dark: #1a1a1a;
            --white: #ffffff;
        }

        body {
            margin: 0;
            font-family: 'Montserrat', sans-serif;
            background: var(--white);
            color: var(--dark);
            overflow-x: hidden;
        }

        /* --- HERO VIDEO SECTION --- */
        .hero {
            position: relative;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
            background: #000; /* Nền đen trong khi chờ video load */
        }

        #hero-video {
            position: absolute;
            top: 50%;
            left: 50%;
            min-width: 100%;
            min-height: 100%;
            width: auto;
            height: auto;
            z-index: 0;
            transform: translate(-50%, -50%);
            filter: brightness(0.5); /* Làm tối video để chữ nổi */
            object-fit: cover;
        }

        .hero-content {
            z-index: 1;
            text-align: center;
            color: white;
            padding: 20px;
        }

        .hero h1 {
            font-family: 'Playfair Display', serif;
            font-size: clamp(2.5rem, 8vw, 5rem);
            margin: 0;
            letter-spacing: 5px;
        }

        /* --- LAYOUT CHUNG --- */
        section { padding: 80px 10%; }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-title h2 {
            font-family: 'Playfair Display', serif;
            font-size: 2.5rem;
            position: relative;
            display: inline-block;
            padding-bottom: 10px;
        }

        .section-title h2::after {
            content: '';
            width: 50%;
            height: 2px;
            background: var(--gold);
            position: absolute;
            bottom: 0;
            left: 25%;
        }

        /* --- DANH MỤC SẢN PHẨM --- */
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .card {
            background: #fdfdfd;
            border: 1px solid #eee;
            transition: 0.4s;
            border-radius: 5px;
            overflow: hidden;
        }

        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.05);
            border-color: var(--gold);
        }

        .product-img {
            width: 100%;
            height: 250px;
            object-fit: cover;
        }

        .price {
            color: var(--gold);
            font-weight: 700;
            font-size: 1.1rem;
        }

        /* --- QR SECTION --- */
        .qr-area {
            background: #f9f9f9;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 40px;
            padding: 50px;
            border-radius: 15px;
        }

        footer {
            background: var(--dark);
            color: #aaa;
            text-align: center;
            padding: 40px;
        }
    </style>
</head>
<body>

    <header class="hero">
        <video autoplay muted loop playsinline id="hero-video">
            <source src="https://assets.mixkit.co/videos/preview/mixkit-top-aerial-shot-of-tea-plantations-4381-large.mp4" type="video/mp4">
        </video>
        
        <div class="hero-content" data-aos="fade-up">
            <h1>SHAN – FAGO</h1>
            <p style="font-weight: 300; letter-spacing: 3px;">TINH HOA QUÀ TẶNG HÀ GIANG</p>
        </div>
    </header>

    <section>
        <div class="section-title" data-aos="fade-up">
            <h2>Sản Phẩm Cao Cấp</h2>
        </div>
        <div class="grid">
            <div class="card" data-aos="fade-up">
                <img src="https://images.unsplash.com/photo-1594631252845-29fc4586bd11?auto=format&fit=crop&w=500" alt="Trà" class="product-img">
                <div style="padding: 20px;">
                    <h3>Trà Shan Tuyết Cổ Thụ</h3>
                    <p>Búp trà trắng phủ tuyết, hương thơm tinh khiết từ núi rừng.</p>
                    <p class="price">1.800.000 VNĐ</p>
                </div>
            </div>

            <div class="card" data-aos="fade-up" data-aos-delay="100">
                <img src="https://images.unsplash.com/photo-1569529465841-dfecdab7503b?auto=format&fit=crop&w=500" alt="Rượu" class="product-img">
                <div style="padding: 20px;">
                    <h3>Rượu Tam Giác Mạch</h3>
                    <p>Lên men thủ công, vị nồng nàn đặc trưng cao nguyên đá.</p>
                    <p class="price">1.500.000 VNĐ</p>
                </div>
            </div>
        </div>
    </section>

    <section>
        <div class="qr-area" data-aos="zoom-in">
            <div style="flex: 1; text-align: center;">
                <img src="https://api.qrserver.com/v1/create-qr-code/?size=180x180&data=SHANFAGO" alt="QR Code" style="border: 5px solid #fff; box-shadow: 0 5px 15px rgba(0,0,0,0.1);">
            </div>
            <div style="flex: 2;">
                <h2 style="color: var(--gold);">Truy Xuất Nguồn Gốc</h2>
                <p>Quét mã để xem video quy trình chế biến trà, ủ rượu và các chứng nhận chất lượng (Không hiển thị mặt người lao động).</p>
            </div>
        </div>
    </section>

    <footer>
        <p>© 2026 SHAN – FAGO | 📞 0337 039 881</p>
    </footer>

    <script src="https://unpkg.com/aos@next/dist/aos.js"></script>
    <script>
        AOS.init({ duration: 1000, once: true });
    </script>
</body>
</html>
