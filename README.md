<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RAYYAN PARK | تجربة استثنائية</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@900&family=Oswald:wght@700&display=swap" rel="stylesheet">
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { background: #000; color: #fff; font-family: 'Cairo', sans-serif; overflow-x: hidden; }

        /* حاوية الصفحات */
        .scroll-container {
            height: 100vh;
            overflow-y: scroll;
            scroll-snap-type: y mandatory; /* يخلي الصفحة توقف بالضبط على كل قسم */
        }

        section {
            height: 100vh;
            width: 100%;
            scroll-snap-align: start;
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
        }

        /* الصور الخلفية */
        .bg-fixed {
            position: absolute;
            top: 0; left: 0; width: 100%; height: 100%;
            object-fit: cover;
            z-index: -1;
            filter: brightness(0.4) saturate(1.2);
            transition: 1s;
        }

        /* العناوين الضخمة */
        .giant-text {
            font-family: 'Oswald', sans-serif;
            font-size: clamp(5rem, 20vw, 15rem);
            line-height: 0.8;
            text-transform: uppercase;
            letter-spacing: -5px;
            text-align: center;
            pointer-events: none;
        }

        /* صندوق الوصف الزجاجي */
        .glass-box {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(15px);
            padding: 40px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            max-width: 600px;
            border-radius: 10px;
            transform: translateY(50px);
            opacity: 0;
            transition: 1s all ease;
        }

        section:hover .glass-box {
            opacity: 1;
            transform: translateY(0);
        }

        /* زر الحجز "الجامد" */
        .btn-reserve {
            display: inline-block;
            margin-top: 20px;
            padding: 15px 50px;
            background: #fff;
            color: #000;
            text-decoration: none;
            font-weight: 900;
            text-transform: uppercase;
            transition: 0.3s;
            clip-path: polygon(10% 0, 100% 0, 90% 100%, 0% 100%); /* شكل هندسي مميز */
        }

        .btn-reserve:hover {
            background: #FFD700;
            transform: scale(1.1) rotate(-2deg);
        }

        /* تفاصيل الجوانب */
        .side-meta {
            position: absolute;
            left: 30px;
            bottom: 30px;
            writing-mode: vertical-rl;
            text-transform: uppercase;
            letter-spacing: 5px;
            font-size: 0.8rem;
            color: rgba(255,255,255,0.4);
        }

    </style>
</head>
<body>

    <div class="scroll-container">
        
        <section>
            <img src="https://images.unsplash.com/photo-1550853024-fae8cd4be47f?q=80&w=2000&auto=format&fit=crop" class="bg-fixed">
            <h1 class="giant-text">RAYYAN<br><span style="color: #FFD700;">PARK</span></h1>
            <div class="side-meta">EST. 2026 • RIYADH</div>
        </section>

        <section>
            <img src="https://images.unsplash.com/photo-1599818818825-7096c46fb7eb?q=80&w=2000&auto=format&fit=crop" class="bg-fixed">
            <div class="glass-box">
                <h2 style="font-size: 2.5rem; margin-bottom: 20px; color: #FFD700;">ما وراء الألوان</h2>
                <p style="font-size: 1.2rem; line-height: 1.6; color: #ddd;">
                    في حديقة الريان، لا نشاهد الطيور فحسب، بل نعيش معها. ببغاوات المكاو النادرة والأمازون الذكية تنتظرك في تجربة تفاعلية هي الأولى من نوعها في المنطقة.
                </p>
            </div>
        </section>

        <section>
            <img src="https://images.unsplash.com/photo-1520114878144-6123749968dd?q=80&w=2000&auto=format&fit=crop" class="bg-fixed">
            <div style="text-align: center;">
                <h2 style="font-size: 4rem; margin-bottom: 30px;">هل أنت جاهز؟</h2>
                <a href="https://wa.me/9665XXXXXXXX" class="btn-reserve">احجز مكانك الآن</a>
            </div>
        </section>

    </div>

</body>
</html>
