<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <title>SHAN – FAGO | Quà tặng cao cấp từ Trà & Rượu Hà Giang</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600&family=Playfair+Display:ital,wght@0,700;1,400&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://unpkg.com/aos@next/dist/aos.css" />

    <style>
        :root {
            --gold: #b08d57; /* Màu vàng đồng sang trọng */
            --dark-text: #333333; /* Màu chữ đen đậm dễ đọc */
            --light-bg: #ffffff; /* Nền trắng */
            --card-bg: #fdfdfd; /* Nền card hơi ngà để nổi bật */
        }

        body {
            margin: 0;
            font-family: 'Montserrat', sans-serif;
            background: var(--light-bg);
            color: var(--dark-text);
            line-height: 1.6;
            overflow-x: hidden; /* Tránh thanh cuộn ngang */
        }
        h1, h2, h3 {
            font-family: 'Playfair Display', serif;
            color: var(--dark-text); /* Tiêu đề màu đen đậm */
        }
        section {
            padding: 70px 10%;
            border-bottom: 1px solid #eeeeee; /* Đường kẻ nhẹ */
            position: relative; /* Dành cho hiệu ứng video nền */
            overflow: hidden; /* Đảm bảo video nền không tràn */
        }

        /* --- HEADER CÓ VIDEO NỀN --- */
        header {
            height: 90vh;
            position: relative; /* Để video làm nền */
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            overflow: hidden;
            color: var(--light-bg); /* Chữ trên header màu trắng */
        }
        .header-video {
            position: absolute;
            top: 50%;
            left: 50%;
            min-width: 100%;
            min-height: 100%;
            width: auto;
            height: auto;
            z-index: -1;
            transform: translate(-50%, -50%);
            object-fit: cover;
            filter: brightness(0.5); /* Làm tối video để chữ nổi bật */
        }
        header h1 {
            font-size: 60px;
            letter-spacing: 4px;
            color: var(--light-bg); /* Chữ H1 trên header màu trắng */
            text-shadow: 2px 2px 8px rgba(0,0,0,0.7); /* Thêm bóng để nổi bật */
        }
        header p {
            font-size: 22px;
            max-width: 700px;
            margin: auto;
            color: var(--light-bg); /* Chữ P trên header màu trắng */
            text-shadow: 1px 1px 5px rgba(0,0,0,0.7);
        }
        
        /* Cấu trúc Grid chung */
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }
        /* Thẻ sản phẩm/thông tin */
        .card {
            background: var(--card-bg); /* Nền card hơi ngà */
            padding: 25px;
            border-radius: 10px;
            transition: 0.3s;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05); /* Bóng nhẹ */
            border: 1px solid #e0e0e0;
        }
        .card:hover {
            transform: translateY(-6px);
            box-shadow: 0 10px 25px rgba(176,141,87,0.2); /* Bóng màu vàng đồng khi hover */
        }
        .price {
            color: var(--gold); /* Giá màu vàng đồng */
            font-weight: bold;
            font-size: 1.1em;
            margin-top: 15px;
            display: block; /* Để đảm bảo nằm trên dòng riêng */
        }
        footer {
            background: var(--dark-text); /* Footer màu đen đậm */
            text-align: center;
            padding: 30px;
            color: #aaaaaa; /* Chữ footer màu xám */
            font-size: 0.9em;
        }
        /* Icon và highlight cho các giá trị khác biệt */
        .card.value-prop {
            display: flex;
            align-items: center;
            gap: 15px;
            font-weight: 600;
            color: var(--dark-text);
        }
        .card.value-prop::before {
            content: '✓';
            color: var(--gold);
            font-size: 1.5em;
            line-height: 1;
        }
        /* Style cho liên hệ */
        .contact-info b {
            color: var(--gold);
        }
    </style>
</head>

<body>

<header>
    <video autoplay muted loop playsinline class="header-video">
        <source src="https://assets.mixkit.co/videos/preview/mixkit-slow-motion-of-a-person-picking-tea-leaves-51000-large.mp4" type="video/mp4">
        Trình duyệt của bạn không hỗ trợ video.
    </video>
    
    <div data-aos="fade-up" data-aos-duration="1200">
        <h1>SHAN – FAGO</h1>
        <p>Tinh hoa quà tặng Việt – Kết tinh từ Trà Shan Tuyết cổ thụ & Rượu Tam Giác Mạch Hà Giang</p>
    </div>
</header>

<section data-aos="fade-up" data-aos-delay="200">
    <h2 style="text-align: center; color: var(--dark-text);">Giới thiệu thương hiệu</h2>
    <p style="text-align: center; max-width: 800px; margin: 20px auto; font-size: 1.1em;">
        Shan–Fago là thương hiệu quà tặng cao cấp phát triển từ giá trị văn hóa bản địa Hà Giang.
        Dự án tập trung vào dòng sản phẩm trà cổ thụ và rượu truyền thống, được chế tác thủ công,
        hướng đến phân khúc khách hàng trung – cao cấp và doanh nghiệp.
    </p>
</section>

<section data-aos="fade-up" data-aos-delay="300">
    <h2 style="text-align: center; color: var(--dark-text);">Danh mục sản phẩm Shan – Fago</h2>
    <div class="grid">

        <div class="card" data-aos="fade-up" data-aos-delay="400">
            <h3>🎁 Combo Quà Tặng Cao Cấp</h3>
            <p>
                Bộ quà tặng gồm Trà Shan Tuyết cổ thụ & Rượu Tam Giác Mạch,
                thiết kế sang trọng, cá nhân hóa theo yêu cầu doanh nghiệp.
            </p>
            <p class="price">Giá: ~3.500.000 VNĐ / bộ</p>
        </div>

        <div class="card" data-aos="fade-up" data-aos-delay="500">
            <h3>🍃 Trà Shan Tuyết Cổ Thụ</h3>
            <p>
                Thu hái thủ công từ cây trà hàng trăm năm tuổi,
                hương thơm tự nhiên, vị chát nhẹ – hậu ngọt sâu.
            </p>
            <p class="price">Giá: ~1.800.000 VNĐ / hộp</p>
        </div>

        <div class="card" data-aos="fade-up" data-aos-delay="600">
            <h3>🍶 Rượu Tam Giác Mạch – Cao Cấp</h3>
            <p>
                Rượu nấu thủ công từ hạt tam giác mạch,
                lên men men lá truyền thống, ủ hạ thổ 15 ngày.
            </p>
            <p class="price">Giá: 1.200.000 – 1.500.000 VNĐ</p>
        </div>

        <div class="card" data-aos="fade-up" data-aos-delay="700">
            <h3>🍶 Rượu Tam Giác Mạch – Premium</h3>
            <p>
                Phiên bản dành cho nhà hàng, du lịch,
                hương dịu – dễ uống – không gây đau đầu.
            </p>
            <p class="price">Giá: 450.000 – 750.000 VNĐ</p>
        </div>

        <div class="card" data-aos="fade-up" data-aos-delay="800">
            <h3>🏢 Quà Tặng Doanh Nghiệp (B2B)</h3>
            <p>
                Thiết kế hộp riêng, in logo, thông điệp thương hiệu.
                Phù hợp quà Tết, đối tác, sự kiện lớn.
            </p>
            <p class="price">Giá theo số lượng & yêu cầu</p>
        </div>

        <div class="card" data-aos="fade-up" data-aos-delay="900">
            <h3>🌟 Phiên bản Giới Hạn</h3>
            <p>
                Bộ quà sưu tầm số lượng giới hạn,
                dùng cho lễ lớn hoặc khách hàng VIP.
            </p>
            <p class="price">Sản xuất theo đơn đặt hàng</p>
        </div>
    </div>
</section>

<section data-aos="fade-up">
    <h2 style="text-align: center; color: var(--dark-text);">Giá trị khác biệt</h2>
    <div class="grid">
        <div class="card value-prop" data-aos="fade-up">Nguyên liệu vùng cao Hà Giang</div>
        <div class="card value-prop" data-aos="fade-up" data-aos-delay="100">Sản xuất thủ công – kiểm soát chất lượng</div>
        <div class="card value-prop" data-aos="fade-up" data-aos-delay="200">Truy xuất nguồn gốc QR</div>
        <div class="card value-prop" data-aos="fade-up" data-aos-delay="300">Gắn với văn hóa & trách nhiệm xã hội</div>
        <div class="card value-prop" data-aos="fade-up" data-aos-delay="400">Thiết kế sang trọng – quà tặng cao cấp</div>
        <div class="card value-prop" data-aos="fade-up" data-aos-delay="500">Phù hợp B2B & khách hàng VIP</div>
    </div>
</section>

<section data-aos="fade-up">
    <h2 style="text-align: center; color: var(--dark-text);">Liên hệ</h2>
    <p style="text-align: center; font-size: 1.1em; line-height: 1.8;">
        📍 <b>Dự án:</b> SHAN – FAGO  
        <br>📞 <b>Hotline:</b> 0337 039 881  
        <br>📧 <b>Email:</b> phanthitinh022@gmail.com  
        <br>🏫 <b>Địa chỉ:</b> Học viện Phụ nữ Việt Nam  
    </p>
</section>

<footer>
    © 2026 SHAN – FAGO | Quà tặng văn hóa Việt Nam
</footer>

<script src="https://unpkg.com/aos@next/dist/aos.js"></script>
<script>
    AOS.init({
        duration: 1000,
        once: true, // Chỉ chạy animation một lần khi scroll xuống
    });
</script>

</body>
</html>
