<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RAYYAN PARK | تجربة استثنائية</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@900&family=Noto+Sans+Arabic:wght@900&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #FFD700; /* ذهبي ملكي */
            --bg: #000000;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            background-color: var(--bg);
            color: #fff;
            font-family: 'Noto Sans Arabic', sans-serif;
            overflow-x: hidden;
        }

        /* الصفحة الأولى - الواجهة السينمائية */
        .hero-section {
            height: 100vh;
            width: 100%;
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            background: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4)), 
                        url('https://images.unsplash.com/photo-1544967082-d9d25d867d66?q=80&w=2000&auto=format&fit=crop'); /* صورة مكاو احترافية جداً */
            background-size: cover;
            background-position: center;
            background-attachment: fixed; /* حركة البارالاكس الجامدة */
        }

        .hero-title {
            font-size: clamp(4rem, 15vw, 12rem);
            line-height: 0.8;
            letter-spacing: -5px;
            text-transform: uppercase;
            opacity: 0.9;
            z-index: 2;
        }

        .hero-subtitle {
            position: absolute;
            bottom: 50px;
            font-size: 1.5rem;
            color: var(--primary);
            letter-spacing: 5px;
        }

        /* الصفحة الثانية - الشرح (الجامد) */
        .content-section {
            min-height: 100vh;
            padding: 100px 5%;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            align-items: center;
            background: #080808;
        }

        .content-text h2 {
            font-size: 5rem;
            margin-bottom: 30px;
            color: var(--primary);
            line-height: 1;
        }

        .content-text p {
            font-size: 1.8rem;
            color: #888;
            font-weight: 300;
            line-height: 1.4;
        }

        .image-box {
            height: 80vh;
            background: url('https://images.unsplash.com/photo-1552728089-57bdde30eba3?q=80&w=1500&auto=format&fit=crop'); /* صورة أمازون واقعية */
            background-size: cover;
            background-position: center;
            border-radius: 5px;
            transition: 0.5s;
        }

        .image-box:hover {
            transform: scale(0.98);
            filter: brightness(1.2);
        }

        /* الصفحة الثالثة - الحجز (الأنيق) */
        .booking-section {
            height: 100vh;
            background: #000;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        .book-card {
            width: 100%;
            max-width: 800px;
            text-align: center;
        }

        .book-link {
            font-size: clamp(3rem, 10vw, 8rem);
            color: #fff;
            text-decoration: none;
            border-bottom: 10px solid var(--primary);
            transition: 0.3s;
        }

        .book-link:hover {
            color: var(--primary);
            border-bottom-color: #fff;
        }

        /* أنيميشن بسيط */
        .fade-in {
            animation: fadeIn 2s ease-in;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @media (max-width: 768px) {
            .content-section { grid-template-columns: 1fr; text-align: center; }
            .hero-title { font-size: 5rem; }
        }
    </style>
</head>
<body>

    <section class="hero-section">
        <h1 class="hero-title fade-in">RAYYAN<br>PARK</h1>
        <div class="hero-subtitle">انغمس في عالم الطيور</div>
    </section>

    <section class="content-section">
        <div class="content-text">
            <h2>نحنُ<br>الأصل.</h2>
            <p>ليست مجرد حديقة، بل موطن لأجمل ببغاوات المكاو والأمازون في قلب الرياض. صممنا لك تجربة تليق بذائقتك.</p>
        </div>
        <div class="image-box"></div>
    </section>

    <section class="booking-section">
        <div class="book-card">
            <p style="font-size: 1.2rem; color: #555; margin-bottom: 20px;">جاهز للتجربة؟</p>
            <a href="https://wa.me/9665XXXXXXXXX" class="book-link">احجز الآن</a>
        </div>
    </section>

</body>
</html>
