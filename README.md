<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>حديقة طيور الريان - RAYYAN PARROTS</title>
    <link href="https://fonts.googleapis.com/css2?family=Reem+Kufi:wght@400;700&family=Secular+One&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    
    <style>
        :root {
            /* ألوان مستوحاة من ببغاء المكاو الأحمر */
            --scarlet-red: #FF2400; 
            --deep-ocean-blue: #003399;
            --pure-white: #ffffff;
            --overlay-dark: rgba(0, 0, 0, 0.4);
            --transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Reem Kufi', sans-serif;
            overflow-x: hidden;
            background-color: #000;
            color: var(--pure-white);
        }

        /* الجزء البصري الرئيسي - Background Video/Image */
        .hero-viewport {
            position: relative;
            width: 100vw;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
        }

        .hero-background {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url('https://images.unsplash.com/photo-1599818818825-7096c46fb7eb?q=80&w=2560&auto=format&fit=crop'); /* صورة مكاو بانورامية ضخمة */
            background-size: cover;
            background-position: center;
            filter: saturate(1.2); /* زيادة تشبع الألوان لتلفت النظر */
            z-index: 1;
        }

        .hero-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(180deg, rgba(0,0,0,0.1) 0%, rgba(0,0,0,0.6) 100%);
            z-index: 2;
        }

        /* بطاقة الحجز العائمة */
        .booking-card {
            position: relative;
            z-index: 3;
            background: rgba(255, 255, 255, 0.06);
            backdrop-filter: blur(20px); /* تأثير الزجاج المغبش الفخم */
            padding: 40px;
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            width: 90%;
            max-width: 450px;
            box-shadow: 0 20px 50px rgba(0,0,0,0.5);
            text-align: center;
            transition: var(--transition);
        }

        .booking-card:hover {
            transform: translateY(-5px) scale(1.01);
            border-color: rgba(255, 255, 255, 0.3);
        }

        .booking-card h1 {
            font-family: 'Secular One', sans-serif; /* خط إنجليزي قوي للعناوين */
            font-size: 2.5rem;
            color: var(--scarlet-red);
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-bottom: 10px;
        }

        .booking-card h2 {
            font-size: 1.2rem;
            font-weight: 400;
            color: var(--pure-white);
            margin-bottom: 30px;
        }

        /* حقول النموذج - ديزاين مودرن نظيف */
        .form-input {
            width: 100%;
            padding: 15px;
            margin-bottom: 20px;
            background: rgba(0, 0, 0, 0.3);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 8px;
            color: var(--pure-white);
            font-family: 'Reem Kufi', sans-serif;
            font-size: 1rem;
            transition: var(--transition);
        }

        .form-input:focus {
            outline: none;
            border-color: var(--deep-ocean-blue);
            background: rgba(0, 0, 0, 0.5);
        }

        /* الزر البطل */
        .hero-btn {
            display: inline-block;
            width: 100%;
            padding: 18px;
            background: linear-gradient(45deg, var(--scarlet-red), #ff4d4d);
            color: var(--pure-white);
            border: none;
            border-radius: 8px;
            font-size: 1.2rem;
            font-weight: 700;
            text-transform: uppercase;
            cursor: pointer;
            transition: var(--transition);
            letter-spacing: 1px;
            margin-top: 10px;
            box-shadow: 0 5px 15px rgba(255, 36, 0, 0.3);
        }

        .hero-btn:hover {
            background: linear-gradient(45deg, #ff4d4d, var(--scarlet-red));
            box-shadow: 0 8px 25px rgba(255, 36, 0, 0.5);
            transform: translateY(-2px);
        }

        /* تفاصيل الموقع */
        .park-meta {
            position: absolute;
            bottom: 20px;
            left: 20px;
            right: 20px;
            z-index: 3;
            display: flex;
            justify-content: space-between;
            font-size: 0.9rem;
            color: rgba(255, 255, 255, 0.6);
        }

        .location-tag {
            color: var(--pure-white);
            font-weight: 700;
        }

    </style>
</head>
<body>

    <div class="hero-viewport">
        <div class="hero-background"></div>
        <div class="hero-overlay"></div>

        <div class="booking-card">
            <h1>RAYYAN</h1>
            <h2>احجز تجربتك اللونية الآن</h2>
            
            <form id="heroReservationForm">
                <input type="text" id="name" class="form-input" placeholder="الاسم الكامل" required>
                <input type="date" id="date" class="form-input" required>
                
                <select id="guests" class="form-input">
                    <option value="" disabled selected>عدد الزوار</option>
                    <option value="1">1</option>
                    <option value="2">2</option>
                    <option value="3+">عائلة/مجموعة</option>
                </select>
                
                <button type="submit" class="hero-btn">تأكيد التذكرة</button>
            </form>
        </div>

        <div class="park-meta">
            <span>جميع الحقوق محفوظة &copy; 2026</span>
            <span class="location-tag"><i class="fas fa-map-marker-alt"></i> الرياض، المملكة العربية السعودية</span>
        </div>
    </div>

    <script>
        document.getElementById('heroReservationForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const name = document.getElementById('name').value;
            const date = document.getElementById('date').value;
            const guests = document.getElementById('guests').value;
            
            // رسالة واتساب قصيرة وبطلة
            const message = `طلب حجز فوري في حديقة الريان:%0A` +
                            `👤 ${name}%0A` +
                            `📅 ${date}%0A` +
                            `👥 ${guests} أشخاص`;
            
            const whatsappNumber = "9665XXXXXXXXX"; // عدله لرقمك الفعلي
            window.open(`https://wa.me/${whatsappNumber}?text=${message}`, '_blank');
        });
    </script>

</body>
</html>
