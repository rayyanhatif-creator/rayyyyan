<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>حديقة طيور الريان | حجز سريع</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        body {
            font-family: 'Cairo', sans-serif;
            background-color: #0c0c0c; /* خلفية داكنة جداً */
            display: flex;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
            color: #fff;
            /* إضافة خلفية بصورة ببغاء واقعية خاففتة جداً لتعطي عمق */
            background-image: linear-gradient(rgba(0,0,0,0.85), rgba(0,0,0,0.85)), 
                              url('https://images.unsplash.com/photo-1552728089-57bdde30eba3?q=80&w=2000&auto=format&fit=crop');
            background-size: cover;
            background-position: center;
        }

        .main-card {
            background: #111; /* لون البطاقة مثل هاتف */
            width: 90%;
            max-width: 420px;
            padding: 40px 30px;
            border-radius: 24px;
            text-align: center;
            box-shadow: 0 25px 50px rgba(0,0,0,0.5);
            border: 1px solid #1f1f1f;
        }

        .logo-area {
            width: 90px;
            height: 90px;
            background: #1a1a1a;
            border-radius: 20px;
            margin: 0 auto 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            color: #ffd700; /* ذهبي */
            border: 1px solid #333;
        }

        h1 {
            font-size: 1.8rem;
            font-weight: 900;
            margin-bottom: 10px;
            letter-spacing: -1px;
        }

        p.subtitle {
            font-size: 1rem;
            color: #888;
            margin-bottom: 35px;
            line-height: 1.5;
        }

        .action-group {
            display: grid;
            gap: 15px;
        }

        /* زر الحجز الرئيسي - جامد ومستوحى من هاتف */
        .btn {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 12px;
            width: 100%;
            padding: 18px;
            border-radius: 14px;
            font-weight: 700;
            font-size: 1.1rem;
            text-decoration: none;
            transition: 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        .btn-booking {
            background: #fff;
            color: #000;
        }

        .btn-booking:hover {
            transform: scale(1.02);
            background: #ffd700;
        }

        .btn-info {
            background: #1a1a1a;
            color: #fff;
            border: 1px solid #333;
        }

        .btn-info:hover {
            background: #252525;
            border-color: #444;
        }

        .footer-text {
            margin-top: 35px;
            font-size: 0.8rem;
            color: #444;
            letter-spacing: 2px;
        }

        /* تأثير الحركة عند الدخول */
        .main-card {
            animation: slideUp 0.8s ease-out;
        }

        @keyframes slideUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>

    <div class="main-card">
        <div class="logo-area">
            <i class="fas fa-feather-alt"></i>
        </div>
        
        <h1>حديقة طيور الريان</h1>
        <p class="subtitle">استمتع بتجربة تفاعلية فريدة مع أجمل أنواع الببغاوات في قلب الرياض.</p>
        
        <div class="action-group">
            <a href="https://wa.me/9665XXXXXXXX" class="btn btn-booking">
                <i class="fab fa-whatsapp"></i>
                احجز موعدك الآن
            </a>
            
            <a href="#" class="btn btn-info">
                <i class="fas fa-map-marker-alt"></i>
                موقع الحديقة
            </a>
        </div>

        <div class="footer-text">
            RAYYAN PARK • 2026
        </div>
    </div>

</body>
</html>
