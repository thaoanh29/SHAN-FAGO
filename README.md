<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="utf-8" />
  <title>SHAN – FAGO | Quà tặng cao cấp từ Trà & Rượu Hà Giang</title>
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <meta name="description" content="SHAN – FAGO: Trà Shan Tuyết cổ thụ & Rượu Tam Giác Mạch Hà Giang — quà tặng văn hóa, sản xuất thủ công, truy xuất QR." />
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600&family=Playfair+Display:ital,wght@0,700;1,400&display=swap" rel="stylesheet">

  <style>
    /* Palette: giữ xanh kim tuyến cho logo, nền vàng nhạt, nhưng contact -> monochrome */
    :root{
      --spark-blue-1: #bfe9ff;
      --spark-blue-2: #4fb3ff;
      --spark-blue-3: #0f7bdc;

      --bg-start: #fff7e6;
      --bg-end:   #fff2d9;

      --text:#0f1220;
      --muted:#6b6b75;

      /* Cards remain glassy on gold bg */
      --card-bg: rgba(255,255,255,0.86);
      --card-border: rgba(255,255,255,0.6);
      --border: rgba(18,18,18,0.06);
      --glass-blur: 8px;

      /* Monochrome variables for contact section */
      --mono-900: #0f1220;
      --mono-700: #33363c;
      --mono-500: #7b7f85;
      --mono-300: #d9d9d9;
      --mono-100: #fafafa;
    }

    *{box-sizing:border-box}
    body{
      margin:0;
      font-family:"Montserrat",system-ui,Arial,sans-serif;
      background: linear-gradient(180deg,var(--bg-start),var(--bg-end));
      color:var(--text);
      line-height:1.6;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
    }

    .wrap{ padding:56px 8%; }
    .container{ max-width:1100px; margin:0 auto; }

    header{
      position:relative;
      min-height:62vh;
      display:flex;
      align-items:center;
      justify-content:center;
      text-align:center;
      padding:72px 6%;
      color:#fff;
      overflow:hidden;
    }
    header::before{
      content:"";
      position:absolute;
      inset:0;
      background-image: url('assets/DSCF5776.JPG');
      background-size:cover;
      background-position:center;
      filter:brightness(0.92) contrast(0.98) saturate(1.03) sepia(0.03);
      z-index:0;
      transform:scale(1.01);
    }
    header::after{
      content:"";
      position:absolute;
      inset:0;
      background: linear-gradient(180deg, rgba(255,250,240,0.10) 0%, rgba(255,248,238,0.05) 40%, rgba(255,255,255,0.00) 70%);
      z-index:1;
      pointer-events:none;
      backdrop-filter: blur(2px);
    }

    header .hero{
      position:relative;
      z-index:2;
      max-width:980px;
      width:100%;
      display:grid;
      grid-template-columns:1fr 220px;
      gap:28px;
      align-items:center;
    }
    header .hero-text{ text-align:left; color:#fff; }

    /* LOGO: solid deep spark-blue + subtle hover */
    h1.logo {
      margin:0 0 8px 0;
      font-family:'Playfair Display',serif;
      font-size:52px;
      letter-spacing:2px;
      font-weight:900;
      color: var(--spark-blue-3);
      -webkit-text-stroke: 0.6px rgba(10,40,70,0.06);
      text-shadow:
        0 8px 28px rgba(15,123,220,0.20),
        0 2px 0 rgba(255,255,255,0.02);
      display:inline-block;
      transition: transform .28s ease, text-shadow .28s ease;
    }
    h1.logo:hover{
      transform: translateY(-3px) scale(1.02);
      text-shadow: 0 16px 46px rgba(15,123,220,0.26);
    }

    /*
      Subtitle (hero): chuyển sang "trắng - đen" để tạo tương phản rõ ràng.
      Đặt vùng nền trắng bán trong suốt (badge) để chữ đen rõ trên ảnh nền vàng.
    */
    header p.lead-hero{
      margin:0 0 18px;
      color:var(--mono-900);           /* chữ đen */
      font-size:18px;
      font-weight:700;
      max-width:760px;
      display:inline-block;
      padding:14px 16px;
      border-radius:12px;
      background: rgba(255,255,255,0.94); /* trắng gần đặc */
      color: var(--mono-900);
      box-shadow: 0 10px 30px rgba(16,18,20,0.06);
      line-height:1.45;
    }

    .btn-primary{
      display:inline-block;
      background: linear-gradient(90deg, rgba(255,255,255,0.06), rgba(255,255,255,0.02)), linear-gradient(90deg, var(--spark-blue-2), var(--spark-blue-3));
      color: #062036;
      padding:10px 18px;
      border-radius:10px;
      text-decoration:none;
      font-weight:700;
      box-shadow: 0 12px 30px rgba(15,123,220,0.12);
      border: 1px solid rgba(255,255,255,0.10);
      transition: transform .18s ease, box-shadow .18s ease;
    }
    .btn-primary:hover{
      transform: translateY(-3px);
      box-shadow: 0 18px 40px rgba(15,123,220,0.18);
    }

    .btn-ghost{
      margin-left:10px;
      display:inline-block;
      color:rgba(255,255,255,0.98);
      padding:10px 16px;
      border-radius:8px;
      text-decoration:none;
      background:transparent;
      border:1px solid rgba(255,255,255,0.12);
    }

    .hero-gallery{ display:flex; flex-direction:column; gap:14px; align-items:center; justify-content:center; }
    .hero-thumb{
      width:100%;
      max-width:220px;
      height:140px;
      border-radius:14px;
      overflow:hidden;
      border:1px solid rgba(255,255,255,0.18);
      background: linear-gradient(180deg, rgba(255,255,255,0.06), rgba(255,255,255,0.02));
      display:flex;
      align-items:end;
      position:relative;
      box-shadow: 0 12px 32px rgba(18,18,18,0.08);
      backdrop-filter: blur(4px);
      transition: transform .22s ease, box-shadow .22s ease;
    }
    .hero-thumb:hover{
      transform: translateY(-6px) scale(1.02);
      box-shadow: 0 26px 60px rgba(18,18,18,0.12);
    }
    .hero-thumb img{ width:100%; height:100%; object-fit:cover; display:block; transform:scale(1.02); }
    .hero-thumb .caption{
      position:absolute; left:12px; bottom:10px;
      color:#fff; font-weight:700;
      background:linear-gradient(90deg, rgba(0,0,0,0.36), rgba(0,0,0,0.14));
      padding:6px 10px; border-radius:8px; font-size:13px;
    }

    main{ margin-top:24px; }
    section{ padding:56px 8%; border-top:1px solid var(--border); background:transparent; }
    h2{ font-family:'Playfair Display',serif; font-size:28px; margin:0 0 12px; color:var(--text); text-align:center; }
    p.lead{ margin:0 auto 26px; text-align:center; color:var(--muted); max-width:860px; font-size:16.5px; }

    .grid{ display:grid; gap:20px; grid-template-columns:repeat(auto-fit,minmax(260px,1fr)); margin-top:20px; }

    .card{
      background: var(--card-bg);
      border:1px solid var(--card-border);
      border-radius:14px;
      padding:18px;
      box-shadow:0 14px 36px rgba(18,18,18,0.04);
      display:flex; flex-direction:column; gap:12px;
      transition:transform .28s ease, box-shadow .28s ease, background .25s ease;
      backdrop-filter: blur(var(--glass-blur));
    }
    .card:hover{
      transform: translateY(-6px);
      box-shadow:0 26px 66px rgba(18,18,18,0.10);
      background: rgba(255,255,255,0.92);
    }

    .product-img{ width:100%; height:220px; object-fit:cover; border-radius:10px; border:1px solid rgba(0,0,0,0.03); background:#fafafa; display:block; }

    .product-head{ display:flex; justify-content:space-between; gap:12px; align-items:flex-start; }
    .prod-title{ font-size:18px; font-weight:800; margin:0; color:var(--text); font-family:'Playfair Display',serif; }
    .prod-desc{ margin:6px 0 0; color:var(--muted); font-size:15px; }

    .price{ color:var(--spark-blue-3); font-weight:800; font-size:15px; }

    .product-meta{ display:flex; justify-content:space-between; align-items:center; gap:12px; margin-top:auto; }
    .meta-left{ display:flex; flex-direction:column; gap:6px; }
    .label{ font-size:13px; color:var(--muted); }

    .qr{ width:88px; height:88px; object-fit:contain; border-radius:10px; border:1px solid var(--card-border); padding:8px; background:rgba(255,255,255,0.9); }

    .badge{
      font-size:12px; padding:6px 8px; border-radius:999px;
      background: linear-gradient(90deg, var(--spark-blue-1), var(--spark-blue-2));
      color:#082036; font-weight:800; box-shadow:0 8px 22px rgba(15,123,220,0.12);
    }

    .card-actions{ display:flex; gap:10px; align-items:center; margin-top:12px; }
    .btn{ padding:8px 12px; border-radius:10px; border:1px solid rgba(0,0,0,0.06); background:#fff; cursor:pointer; text-decoration:none; color:var(--text); font-weight:700; font-size:14px; transition: transform .14s ease, box-shadow .14s ease; }
    .btn:hover{ transform: translateY(-4px); box-shadow: 0 12px 30px rgba(0,0,0,0.08); }
    .btn.secondary{ border:1px solid rgba(0,0,0,0.06); background: linear-gradient(180deg,#fff,#fbfbfb); }

    /* CONTACT: chuyển sang phong cách nghiêm túc, chuyên nghiệp (monochrome) */
    .contact-wrap{ display:grid; grid-template-columns:1fr 380px; gap:28px; align-items:start; max-width:1100px; margin:0 auto; }
    .contact-card{
      background: linear-gradient(180deg,var(--mono-100),#fff);
      border-radius:12px;
      border:1px solid var(--mono-300);
      padding:20px;
      box-shadow: 0 12px 28px rgba(16,18,20,0.06);
    }
    form.contact-form{ display:flex; flex-direction:column; gap:12px; }
    label.field{ display:flex; flex-direction:column; gap:6px; font-size:14px; color:var(--mono-700); }
    input[type="text"], input[type="email"], input[type="tel"], select, textarea{
      padding:10px 12px; border-radius:8px; border:1px solid var(--mono-300); font-size:15px; outline:none; background: #fff; color:var(--mono-900); transition:box-shadow .12s ease, border-color .12s ease;
    }
    input:focus, textarea:focus, select:focus{
      box-shadow:0 6px 18px rgba(16,18,20,0.06); border-color:var(--mono-700);
    }
    textarea{ min-height:120px; resize:vertical; }
    .form-row{ display:flex; gap:12px; }
    .form-row .field{ flex:1; }
    .contact-actions{ display:flex; gap:12px; align-items:center; margin-top:6px; }

    /* Send button => neutral, mạnh mẽ */
    .btn-send{
      background: linear-gradient(180deg,var(--mono-900), #111);
      color:#fff;
      border:none;
      padding:10px 16px;
      border-radius:10px;
      font-weight:800;
      cursor:pointer;
      box-shadow:0 10px 28px rgba(16,18,20,0.12);
      transition: transform .12s ease, box-shadow .12s ease;
    }
    .btn-send:hover{
      transform: translateY(-3px);
      box-shadow:0 16px 38px rgba(16,18,20,0.18);
    }
    .btn-clear{
      background:#fff; border:1px solid var(--mono-300); padding:10px 14px; border-radius:10px; cursor:pointer; color:var(--mono-700);
    }

    .contact-info{ display:flex; flex-direction:column; gap:14px; align-items:stretch; }
    .info-item{
      background: linear-gradient(180deg,#fff,#fbfbfb);
      border-radius:10px;
      padding:14px;
      border:1px solid var(--mono-300);
      display:flex; gap:12px; align-items:flex-start;
      box-shadow:0 8px 20px rgba(0,0,0,0.03);
    }
    .info-icon{
      width:44px; height:44px; border-radius:10px;
      display:flex; align-items:center; justify-content:center;
      background: var(--mono-100);
      color:var(--mono-700);
      font-weight:800;
      font-size:18px;
      border:1px solid var(--mono-300);
    }
    .info-body{ display:flex; flex-direction:column; gap:4px; }
    .info-title{ font-weight:800; color:var(--mono-900); font-size:14px; }
    .info-sub{ color:var(--mono-700); font-size:13px; }
    .hours{ font-size:13px; color:var(--mono-700); }
    .small-note{ font-size:13px; color:var(--muted); margin-top:8px; }
    .msg{ margin-top:8px; font-size:14px; color:var(--mono-900); font-weight:700; display:none; }

    footer{ padding:28px 8%; text-align:center; font-size:14px; color:var(--muted); border-top:1px solid rgba(0,0,0,0.04); background:transparent; }

    /* responsive */
    @media (max-width:980px){
      .contact-wrap{ grid-template-columns:1fr; }
      header .hero{ grid-template-columns:1fr 180px; gap:18px; }
      h1.logo{ font-size:40px; }
      .product-img{ height:180px; }
      .hero-thumb{ height:120px; max-width:180px; }
    }
    @media (max-width:760px){
      header{ padding:36px 6%; min-height:46vh; }
      header .hero{ grid-template-columns:1fr; text-align:center; }
      header .hero-text{ text-align:center; }
      .hero-gallery{ flex-direction:row; justify-content:center; gap:12px; }
      h1.logo{ font-size:30px; }
      header p.lead-hero{ font-size:16px; display:block; margin:12px auto; }
      .product-img{ height:150px; }
      .qr{ width:68px; height:68px; }
      .wrap{ padding:24px 6%; }
    }
  </style>
</head>
<body>

  <header role="banner" aria-label="Shan Fago header">
    <div class="hero container">
      <div class="hero-text">
        <h1 class="logo">SHAN – FAGO</h1>
        <p class="lead-hero">Tinh hoa quà tặng Việt — Trà Shan Tuyết cổ thụ &amp; Rượu Tam Giác Mạch Hà Giang. Sản xuất thủ công, truy xuất QR, thiết kế sang trọng — dành cho đối tác &amp; khách VIP.</p>
        <div style="margin-top:14px">
          <a class="btn-primary" href="#products">Xem bộ sưu tập</a>
          <a class="btn-ghost" href="#contact">Liên hệ đặt hàng</a>
        </div>
      </div>

      <aside class="hero-gallery" aria-hidden="false">
        <figure class="hero-thumb" title="Trà Shan Tuyết cổ thụ">
          <img src="assets/DSCF5779.JPG" alt="Trà Shan Tuyết - Shan Fago" />
          <figcaption class="caption">Trà Shan Tuyết</figcaption>
        </figure>

        <figure class="hero-thumb" title="Rượu Tam Giác Mạch">
          <img src="assets/r.jpg" alt="Rượu Tam Giác Mạch - Shan Fago" />
          <figcaption class="caption">Rượu Tam Giác Mạch</figcaption>
        </figure>
      </aside>
    </div>
  </header>

  <main>
    <section aria-labelledby="products" class="wrap">
      <div class="container">
        <h2 id="products">Danh mục sản phẩm</h2>
        <p class="lead">Mỗi sản phẩm hiển thị ảnh thật và mã QR truy xuất nguồn gốc — giúp khách hàng kiểm chứng và yên tâm.</p>

        <div class="grid">
          <article class="card" aria-labelledby="tea-title">
            <img src="assets/DSCF5779.JPG" alt="Trà Shan Tuyết - Shan Fago" class="product-img" />
            <div class="product-head">
              <div>
                <h3 id="tea-title" class="prod-title">🍃 Trà Shan Tuyết Cổ Thụ <span class="badge">Premium</span></h3>
                <p class="prod-desc">Thu hái chọn lọc, chế biến thủ công — hương thanh, hậu ngọt, đóng gói sang trọng phù hợp quà tặng.</p>
              </div>
              <div class="price">~1.800.000 VNĐ</div>
            </div>

            <div class="product-meta">
              <div class="meta-left">
                <div class="label">Truy xuất nguồn gốc: QR đi kèm</div>
                <div class="label">Hương vị: Chát nhẹ — Hậu ngọt</div>
              </div>
              <img src="assets/qr-tea.png" alt="QR Trà Shan Tuyết" class="qr" />
            </div>

            <div class="card-actions">
              <a class="btn" href="assets/DSCF5779.JPG" target="_blank" rel="noopener">Xem ảnh lớn</a>
              <a class="btn secondary" href="#contact">Yêu cầu báo giá</a>
            </div>
          </article>

          <article class="card" aria-labelledby="rum-title">
            <img src="assets/r.jpg" alt="Rượu Tam Giác Mạch - Shan Fago" class="product-img" />
            <div class="product-head">
              <div>
                <h3 id="rum-title" class="prod-title">🍶 Rượu Tam Giác Mạch</h3>
                <p class="prod-desc">Rượu nấu thủ công, lên men tự nhiên, phiên bản Premium & Standard — phù hợp nhà hàng và quà tặng doanh nghiệp.</p>
              </div>
              <div class="price">450.000 – 1.500.000 VNĐ</div>
            </div>

            <div class="product-meta">
              <div class="meta-left">
                <div class="label">Quy trình: Lên men tự nhiên — ủ kỹ</div>
                <div class="label">Dung tích: nhiều lựa chọn</div>
              </div>
              <img src="assets/qr-rum.png" alt="QR Rượu Tam Giác Mạch" class="qr" />
            </div>

            <div class="card-actions">
              <a class="btn" href="assets/r.jpg" target="_blank" rel="noopener">Xem ảnh lớn</a>
              <a class="btn secondary" href="#contact">Đặt thử mẫu</a>
            </div>
          </article>

          <div class="card">
            <h3 class="prod-title">🎁 Combo Quà Tặng Cao Cấp</h3>
            <p class="prod-desc">Gộp trà + rượu trong hộp thiết kế, in logo & thông điệp doanh nghiệp. Sản xuất theo đơn — phù hợp quà Tết & đối tác.</p>
            <div style="display:flex;justify-content:space-between;align-items:center;margin-top:12px">
              <div class="label">Tùy chỉnh bao bì & số lượng</div>
              <div class="price">Giá: 3.500.000 VNĐ</div>
            </div>
            <div class="card-actions">
              <a class="btn" href="#contact">Tùy chỉnh đơn hàng</a>
              <a class="btn secondary" href="#contact">Yêu cầu mẫu</a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section aria-labelledby="values" class="wrap">
      <div class="container">
        <h2 id="values">Giá trị khác biệt</h2>
        <p class="lead">Nguyên liệu vùng cao Hà Giang • Sản xuất thủ công • Truy xuất nguồn gốc QR • Gắn với văn hóa & trách nhiệm xã hội</p>

        <div class="grid" style="margin-top:12px">
          <div class="card">Nguyên liệu vùng cao Hà Giang</div>
          <div class="card">Sản xuất thủ công – kiểm soát chất lượng</div>
          <div class="card">Truy xuất nguồn gốc QR</div>
          <div class="card">Thiết kế sang trọng – quà tặng cao cấp</div>
          <div class="card">Phù hợp B2B & khách hàng VIP</div>
          <div class="card">Phiên bản giới hạn cho khách VIP</div>
        </div>
      </div>
    </section>

    <section aria-labelledby="contact" class="wrap" id="contact">
      <div class="container">
        <h2 id="contact">Liên hệ & Đặt hàng</h2>
        <p class="lead">Hãy cho chúng tôi biết nhu cầu của bạn — báo giá số lượng, yêu cầu mẫu, hoặc đặt hợp tác quà tặng doanh nghiệp. Điền form bên dưới hoặc liên hệ trực tiếp qua hotline / email.</p>

        <div class="contact-wrap">
          <div class="contact-card">
            <form class="contact-form" id="contactForm" novalidate>
              <div class="form-row">
                <label class="field">
                  <span>Họ & tên</span>
                  <input type="text" name="name" id="name" placeholder="Nguyễn Văn A" required />
                </label>

                <label class="field">
                  <span>Công ty (nếu có)</span>
                  <input type="text" name="company" id="company" placeholder="Công ty ABC" />
                </label>
              </div>

              <div class="form-row">
                <label class="field">
                  <span>Điện thoại</span>
                  <input type="tel" name="phone" id="phone" placeholder="0337 039 881" pattern="[0-9+\-\s()]{6,}" required />
                </label>

                <label class="field">
                  <span>Email</span>
                  <input type="email" name="email" id="email" placeholder="email@khachhang.com" required />
                </label>
              </div>

              <label class="field">
                <span>Loại yêu cầu</span>
                <select name="inquiry" id="inquiry">
                  <option value="quote">Yêu cầu báo giá</option>
                  <option value="sample">Yêu cầu mẫu</option>
                  <option value="partnership">Hợp tác B2B</option>
                  <option value="other">Khác</option>
                </select>
              </label>

              <label class="field">
                <span>Nội dung / Ghi chú</span>
                <textarea name="message" id="message" placeholder="Mô tả ngắn: số lượng dự kiến, deadline, yêu cầu in ấn logo..."></textarea>
              </label>

              <div class="contact-actions">
                <button type="submit" class="btn-send" id="sendBtn">Gửi yêu cầu</button>
                <button type="button" class="btn-clear" id="clearBtn">Xóa</button>
                <div id="formMsg" class="msg" role="status" aria-live="polite"></div>
              </div>

              <p class="small-note">Bằng cách gửi, bạn đồng ý chúng tôi sử dụng thông tin để liên hệ phản hồi. Chúng tôi tôn trọng quyền riêng tư và không chia sẻ dữ liệu cho bên thứ ba.</p>
            </form>
          </div>

          <aside class="contact-info" aria-label="Thông tin liên hệ">
            <div class="info-item">
              <div class="info-icon">📞</div>
              <div class="info-body">
                <div class="info-title">Hotline</div>
                <div class="info-sub"><a href="tel:+84337039881" style="color:var(--mono-900);text-decoration:none;font-weight:700">0337 039 881</a> — (Zalo / Call)</div>
              </div>
            </div>

            <div class="info-item">
              <div class="info-icon">✉️</div>
              <div class="info-body">
                <div class="info-title">Email</div>
                <div class="info-sub"><a href="mailto:fagoshan@gmail.com" style="color:var(--mono-900);text-decoration:none;font-weight:700">fagoshan@gmail.com</a></div>
              </div>
            </div>

            <div class="info-item">
              <div class="info-icon">📍</div>
              <div class="info-body">
                <div class="info-title">Địa chỉ</div>
                <div class="info-sub">Học viện Phụ nữ Việt Nam</div>
                <div class="hours">Giờ làm việc: Thứ 2 - Thứ 7, 08:00 – 18:00</div>
              </div>
            </div>

            <div class="info-item">
              <div class="info-icon">⌛</div>
              <div class="info-body">
                <div class="info-title">Quy trình phản hồi</div>
                <div class="info-sub">Chúng tôi sẽ trả lời trong vòng 24 giờ làm việc. Đối với đơn hàng B2B, hỗ trợ báo giá nhanh trong 48 giờ.</div>
              </div>
            </div>

            <div class="info-item">
              <div class="info-icon">🔗</div>
              <div class="info-body">
                <div class="info-title">Kênh nhanh</div>
                <div class="info-sub">
                  <a href="tel:+84337039881" style="color:var(--mono-700);text-decoration:none">Gọi ngay</a> •
                  <a href="mailto:fagoshan@gmail.com" style="color:var(--mono-700);text-decoration:none">Gửi email</a>
                </div>
              </div>
            </div>
          </aside>
        </div>
      </div>
    </section>
  </main>

  <footer role="contentinfo">© 2026 SHAN – FAGO | Quà tặng văn hóa Việt Nam</footer>

  <script>
    // Xử lý form: validate cơ bản và mở mailto để gửi (không cần backend).
    (function(){
      const form = document.getElementById('contactForm');
      const clearBtn = document.getElementById('clearBtn');
      const msg = document.getElementById('formMsg');

      function showMessage(text, ok=true){
        msg.style.display = 'block';
        msg.style.color = ok ? '#0f1220' : '#c33';
        msg.textContent = text;
      }

      form.addEventListener('submit', function(e){
        e.preventDefault();
        const name = form.name.value.trim();
        const email = form.email.value.trim();
        const phone = form.phone.value.trim();
        const inquiry = form.inquiry.value;
        const company = form.company.value.trim();
        const message = form.message.value.trim();

        if(!name || !email || !phone){
          showMessage('Vui lòng điền ít nhất Họ & tên, Email và Điện thoại.', false);
          return;
        }

        const to = 'fagoshan@gmail.com';
        const subject = encodeURIComponent('Yêu cầu từ website — ' + inquiry + ' — ' + name);
        let body = '';
        body += 'Họ và tên: ' + name + '\\n';
        if(company) body += 'Công ty: ' + company + '\\n';
        body += 'Điện thoại: ' + phone + '\\n';
        body += 'Email: ' + email + '\\n';
        body += 'Loại yêu cầu: ' + inquiry + '\\n\\n';
        body += 'Nội dung:\\n' + (message || '(không có)') + '\\n';

        const mailto = 'mailto:' + to + '?subject=' + subject + '&body=' + encodeURIComponent(body);

        showMessage('Đang mở ứng dụng email của bạn để gửi yêu cầu...', true);

        setTimeout(() => {
          window.location.href = mailto;
        }, 700);
      });

      clearBtn.addEventListener('click', function(){
        form.reset();
        msg.style.display = 'none';
      });
    })();
  </script>
</body>
</html>
