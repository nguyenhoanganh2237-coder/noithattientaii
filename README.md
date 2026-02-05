[tientai.html](https://github.com/user-attachments/files/25112013/tientai.html)
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nội Thất Tiến Tài - Sang Trọng & Đẳng Cấp</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Open+Sans:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #2c3e50;
            --accent-color: #b8860b;
            --light-bg: #fdfdfd;
            --dark-text: #333;
            --light-text: #f0f0f0;
            --font-heading: 'Playfair Display', serif;
            --font-body: 'Open Sans', sans-serif;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: var(--font-body);
            line-height: 1.6;
            color: var(--dark-text);
            background-color: var(--light-bg);
            overflow-x: hidden;
        }

        /* --- Header --- */
        .header {
            background-color: rgba(255, 255, 255, 0.95);
            padding: 15px 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            position: fixed;
            width: 100%;
            top: 0;
            left: 0;
            z-index: 1000;
        }

        .navbar {
            max-width: 1200px;
            margin: auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 20px;
        }

        .logo {
            font-family: var(--font-heading);
            font-size: 1.8rem;
            color: var(--primary-color);
            text-decoration: none;
            font-weight: 700;
            letter-spacing: 2px;
        }

        .nav-links {
            list-style: none;
            display: flex;
        }

        .nav-links li {
            margin-left: 30px;
        }

        .nav-links a {
            color: var(--dark-text);
            text-decoration: none;
            font-weight: 600;
            transition: color 0.3s ease;
            font-size: 0.9rem;
            text-transform: uppercase;
        }

        .nav-links a:hover {
            color: var(--accent-color);
        }

        /* --- Hero Section --- */
        .hero {
            height: 100vh;
            /* Đã thay link ảnh nền cực đẹp */
            background: url('https://images.unsplash.com/photo-1618221195710-dd6b41faaea6?auto=format&fit=crop&q=80&w=1920') no-repeat center center/cover;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: var(--light-text);
            position: relative;
        }

        .hero::before {
            content: "";
            position: absolute;
            top: 0; left: 0; width: 100%; height: 100%;
            background-color: rgba(0, 0, 0, 0.45);
        }

        .hero-content {
            position: relative;
            z-index: 10;
            padding: 0 20px;
        }

        .hero h1 {
            font-family: var(--font-heading);
            font-size: clamp(2.5rem, 8vw, 4.5rem);
            margin-bottom: 20px;
            text-shadow: 2px 2px 10px rgba(0,0,0,0.3);
        }

        .hero p {
            font-size: clamp(1rem, 4vw, 1.4rem);
            margin-bottom: 40px;
            max-width: 800px;
        }

        .btn {
            display: inline-block;
            background-color: var(--accent-color);
            color: white;
            padding: 16px 45px;
            text-decoration: none;
            text-transform: uppercase;
            font-weight: 700;
            border-radius: 2px;
            transition: 0.3s;
        }

        .btn:hover {
            background-color: #966d08;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }

        /* --- About Section --- */
        .about-section {
            max-width: 1200px;
            margin: 100px auto;
            padding: 0 20px;
            display: flex;
            align-items: center;
            gap: 60px;
            flex-wrap: wrap;
        }

        .about-image {
            flex: 1;
            min-width: 350px;
        }

        .about-image img {
            width: 100%;
            height: 450px;
            object-fit: cover;
            border-radius: 4px;
            box-shadow: 20px 20px 0px var(--accent-color);
        }

        .about-content {
            flex: 1;
            min-width: 350px;
        }

        .about-content h2 {
            font-family: var(--font-heading);
            font-size: 2.5rem;
            color: var(--primary-color);
            margin-bottom: 25px;
        }

        /* --- Products Section --- */
        .products-section {
            background-color: #f4f4f4;
            padding: 100px 20px;
            text-align: center;
        }

        .products-section h2 {
            font-family: var(--font-heading);
            font-size: 2.8rem;
            margin-bottom: 60px;
        }

        .product-grid {
            max-width: 1200px;
            margin: auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .product-card {
            background: white;
            overflow: hidden;
            transition: 0.4s;
            text-align: left;
            border-bottom: 3px solid transparent;
        }

        .product-card:hover {
            transform: translateY(-10px);
            border-bottom: 3px solid var(--accent-color);
            box-shadow: 0 15px 35px rgba(0,0,0,0.1);
        }

        .product-card img {
            width: 100%;
            height: 280px;
            object-fit: cover;
        }

        .product-info {
            padding: 25px;
        }

        .product-info h3 {
            font-family: var(--font-heading);
            font-size: 1.5rem;
            margin-bottom: 10px;
        }

        .product-price {
            color: var(--accent-color);
            font-weight: 700;
            font-size: 1.2rem;
        }

        /* --- Footer --- */
        .footer {
            background-color: var(--primary-color);
            color: white;
            padding: 80px 20px;
            text-align: center;
        }

        .footer-links a {
            color: #bdc3c7;
            text-decoration: none;
            margin: 0 15px;
            font-size: 1.5rem;
        }

        @media (max-width: 768px) {
            .nav-links { display: none; }
            .about-image img { height: 300px; }
        }
    </style>
</head>
<body>

    <header class="header">
        <nav class="navbar">
            <a href="#" class="logo">TIẾN TÀI</a>
            <ul class="nav-links">
                <li><a href="#home">Trang Chủ</a></li>
                <li><a href="#about">Về Chúng Tôi</a></li>
                <li><a href="#products">Sản Phẩm</a></li>
                <li><a href="#contact">Liên Hệ</a></li>
            </ul>
        </nav>
    </header>

    <section id="home" class="hero">
        <div class="hero-content">
            <h1>Nội Thất Tiến Tài</h1>
            <p>Kiến tạo không gian sống đẳng cấp với những thiết kế tinh tế, độc bản và đầy cảm hứng.</p>
            <a href="#products" class="btn">Xem bộ sưu tập</a>
        </div>
    </section>

    <section id="about" class="about-section">
        <div class="about-image">
            <img src="https://images.unsplash.com/photo-1616486338812-3dadae4b4ace?auto=format&fit=crop&q=80&w=800" alt="Showroom Nội thất">
        </div>
        <div class="about-content">
            <h2>Đẳng Cấp Từ Tâm</h2>
            <p>Với hơn 20 năm tâm huyết, Nội Thất Tiến Tài không chỉ bán đồ gỗ, chúng tôi mang đến hơi thở nghệ thuật cho ngôi nhà của bạn.</p>
            <br>
            <p>Mỗi sản phẩm đều được chọn lọc từ những chất liệu cao cấp nhất, qua bàn tay của các nghệ nhân lành nghề để đảm bảo sự hoàn mỹ trong từng chi tiết.</p>
        </div>
    </section>

    <section id="products" class="products-section">
        <h2>Sản Phẩm Nổi Bật</h2>
        <div class="product-grid">
            <div class="product-card">
                <img src="https://images.unsplash.com/photo-1555041469-a586c61ea9bc?auto=format&fit=crop&q=80&w=600" alt="Sofa">
                <div class="product-info">
                    <h3>Sofa Emerald Luxury</h3>
                    <p>Chất liệu nhung cao cấp kết hợp khung gỗ sồi chắc chắn.</p>
                    <p class="product-price">Giá: Liên hệ</p>
                </div>
            </div>
            <div class="product-card">
                <img src="https://images.unsplash.com/photo-1538688525198-9b88f6f53126?auto=format&fit=crop&q=80&w=600" alt="Bàn ăn">
                <div class="product-info">
                    <h3>Bàn Ăn Royal Walnut</h3>
                    <p>Gỗ óc chó nhập khẩu với đường vân tự nhiên sang trọng.</p>
                    <p class="product-price">Giá: Liên hệ</p>
                </div>
            </div>
            <div class="product-card">
                <img src="https://images.unsplash.com/photo-1505691938895-1758d7feb511?auto=format&fit=crop&q=80&w=600" alt="Giường">
                <div class="product-info">
                    <h3>Giường Ngủ Master</h3>
                    <p>Thiết kế chuẩn công thái học cho giấc ngủ trọn vẹn.</p>
                    <p class="product-price">Giá: Liên hệ</p>
                </div>
            </div>
        </div>
    </section>

    <footer id="contact" class="footer">
        <h3>NỘI THẤT TIẾN TÀI</h3>
        <p style="margin: 20px 0;">Địa chỉ:cẩm sơn , hà tĩnh</p>
        <p>Hotline: 0914 854 101 | Email: contact@tientai.com</p>
        <div class="footer-links" style="margin-top: 30px;">
            <a href="#">FB</a> <a href="#">IG</a> <a href="#">YT</a>
        </div>
    </footer>

</body>
</html>
