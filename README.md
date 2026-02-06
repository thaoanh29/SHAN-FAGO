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
            --glass: rgba(255, 255, 255, 0.85);
        }

        body {
            margin: 0;
            font-family: 'Montserrat', sans-serif;
            background: var(--white);
            color: var(--dark);
            overflow-x: hidden;
        }

        h1, h2, h3 {
            font-family: 'Playfair Display', serif;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        /* --- VIDEO BACKGROUND SECTION --- */
        .hero {
            position: relative;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
            color: white;
            text-align: center;
        }

        #hero-video {
            position: absolute;
            top: 50%;
            left: 50%;
            min-width: 100%;
            min-height: 100%;
            width: auto;
            height: auto;
            z-index: -1;
            transform: translate(-50%, -50%);
            filter: brightness(0.6); /* Làm tối video để chữ nổi bật */
        }

        .hero-content {
            z-index: 1;
            padding: 40px;
            background: rgba(0, 0, 0, 0.2);
            backdrop-filter: blur(4px);
            border: 1px solid rgba(255, 255, 255, 0.3);
            border-radius: 2px;
        }

        .hero h1 {
            font-size: clamp(3rem, 10vw, 5rem);
            margin: 0;
            color: #fff;
            text-shadow: 2px 2px 10px rgba(0,0,0,0.5);
        }

        /* --- LAYOUT --- */
        section {
            padding: 100px 10%;
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
            position: relative;
        }

        .section-title::after {
            content: '';
            width: 60px;
            height: 3px;
            background: var(--gold);
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
        }

        /* --- PRODUCT CARDS --- */
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 30px;
        }

        .card {
            background: var(--white);
            border: 1px solid #eee;
            transition: all 0.5s ease;
            position: relative;
            overflow: hidden;
        }

        .card:hover {
            box-shadow: 0 15px 45px rgba(0,0,0,0.1);
            border-color: var(--gold);
        }

        .product-img-container {
            overflow: hidden;
            height: 300px;
        }

        .product-img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.8s ease;
        }

        .card:hover .product-img {
            transform: scale(1.1);
        }

        .price {
            color: var(--gold);
            font-weight: 700;
            font-size: 1.2rem;
            display: block;
            margin-top: 15px;
        }

        /* --- QR SECTION --- */
        .qr-section {
            background: #fdfaf5;
            border
