<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>حديقة طيور الريان | عالم الألوان</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700;900&family=Oswald:wght@500&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-dark: #050505;
            --accent-macaw: #e63946; /* أحمر مكاو */
            --accent-amazon: #a7c957; /* أخضر أمازون */
            --text-light: #ffffff;
            --text-gray: #a0a0a0;
            --transition: all 0.6s cubic-bezier(0.22, 1, 0.36, 1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            font-family: 'Cairo', sans-serif;
            background-color: var(--bg-dark);
            color: var(--text-light);
            overflow-x: hidden;
        }

        /* القائمة العلوية */
        nav {
            position: fixed;
            top: 0; width: 100%;
            padding: 25px 50px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 1000;
            background: linear-gradient(180deg, rgba(0,0,0,0.8) 0%, rgba(0,0,0,0) 100%);
        }

        .logo {
            font-family: 'Oswald', sans-serif;
            font-size: 2rem;
            letter-spacing: 2px;
            color: var(--text-light);
            text-transform: uppercase;
        }

        .book-btn-nav {
            padding: 12px 30px;
            background-color: transparent;
            color: var(--text-light);
            border: 2px solid var(--text-light);
            text-decoration: none;
            font-weight: bold;
            border-radius: 30px;
            transition: var(--transition);
        }

        .book-btn-nav:hover {
            background-color: var(--text-light);
            color: var(--bg-dark);
        }

        /* قسم الهيرو المقسم (Split Screen) */
        .hero-split {
            display: flex;
            height: 100vh;
            width: 100vw;
            overflow: hidden;
        }

        .split {
            flex: 1;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
            transition: var(--transition);
            background-size: cover;
            background-position: center;
            cursor: pointer;
        }

        /* خلفيات الصور الواقعية */
        .split.left {
            background-image: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.7)), 
                              url('https://images.unsplash.com/photo-1599818818825-7096c46fb7eb?q=80&w=2560&auto=format&fit=crop'); /* صورة مكاو واقعية */
        }

        .split.right {
            background-image: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.7)), 
                              url('https://images.unsplash.com/photo-1552728089-57bdde30eba3?auto=format&fit=crop&w=1920&q=80'); /* صورة أمازون واقعية */
        }

        /* تأثير التكبير عند التحويم */
        .split:hover { flex: 1.5; }
        .split::after {
            content: '';
            position: absolute;
            top: 0; left: 0; width: 100%; height: 100%;
            background-color: rgba(0,0,0,0.2);
            transition: var(--transition);
        }
        .split:hover::after { background-color: rgba(0,0,0,0); }

        /* محتوى النص فوق الصور */
        .split-content {
            position: relative;
            z-index: 10;
            text-align: center;
            padding: 0 10%;
            opacity: 0;
            transform: translateY(30px);
            animation: fadeInUp 1s ease-out forwards;
            animation-delay: 0.5s;
        }

        .split.left h2 { color: var(--accent-macaw); font-size: 4rem; font-weight: 900; text-transform: uppercase; }
        .split.right h2 { color: var(--accent-amazon); font-size: 4rem; font-weight: 900; text-transform: uppercase; }

        .split-content p {
            font-size: 1.3rem;
            margin: 15px 0 40px 0;
            color: var(--text-gray);
            line-height: 1.6;
        }

        /* الزر الرئيسي الجريء */
        .hero-btn {
            padding: 20px 50px;
            background-color: var(--text-light);
            color: var(--bg-dark);
            text-decoration: none;
            font-weight: 900;
            font-size: 1.2rem;
            border-radius: 5px;
            transition: var(--transition);
            display: inline-block;
        }

        .hero-btn:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 30px rgba(255,255,255,0.2);
        }

        /* أنيميشن الظهور */
        @keyframes fadeInUp {
            to { opacity: 1; transform: translateY(0); }
        }

    </style>
</head>
<body>

    <nav>
        <div class="logo">RAYYAN</div>
        <a href="booking.html" class="book-btn-nav">احجز تجربتك</a>
    </nav>

    <div class="hero-split">
        <div class="split left">
            <div class="split-content">
                <h2>MACAW</h2>
                <p>استكشف فخامة ألوان المكاو الأحمر والأزرق في بيئة طبيعية ساحرة.</p>
                <a href="booking.html" class="hero-btn">احجز الآن</a>
            </div>
        </div>
        <div class="split right">
            <div class="split-content">
                <h2>AMAZON</h2>
                <p>تعرف على ذكاء وجمال ببغاوات الأمازون الخضراء النادرة عن قرب.</p>
                <a href="booking.html" class="hero-btn">احجز الآن</a>
            </div>
        </div>
    </div>

</body>
</html>
