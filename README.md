<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RAYYAN PARK | التجربة الكاملة</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@900&family=Oswald:wght@700&display=swap" rel="stylesheet">
    <style>
        :root { --gold: #C5A059; --black: #080808; }
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { background: var(--black); color: #fff; font-family: 'Cairo', sans-serif; overflow-x: hidden; }

        /* الشاشة الأولى: دخول فخم */
        section { height: 100vh; width: 100%; position: relative; display: flex; align-items: center; padding: 0 8%; overflow: hidden; }
        
        .bg-img { position: absolute; top: 0; left: 0; width: 100%; height: 100%; object-fit: cover; z-index: -1; opacity: 0.6; transition: 1s; }
        
        .main-title { font-size: clamp(3rem, 10vw, 8rem); line-height: 0.9; text-transform: uppercase; font-family: 'Oswald'; }
        .gold-text { color: var(--gold); }

        /* الشاشة الثانية: شرح بقوة الصور */
        .description { background: #0c0c0c; display: grid; grid-template-columns: 1fr 1fr; gap: 40px; }
        .desc-text { padding: 40px; display: flex; flex-direction: column; justify-content: center; }
        .desc-text h2 { font-size: 3.5rem; margin-bottom: 20px; border-right: 8px solid var(--gold); padding-right: 20px; }
        .desc-text p { font-size: 1.5rem; color: #888; line-height: 1.6; }

        /* الشاشة الثالثة: الحجز بأسلوب الـ Glassmorphism */
        .booking-zone { 
            background: linear-gradient(rgba(0,0,0,0.8), rgba(0,0,0,0.8)), url('https://images.unsplash.com/photo-1550853024-fae8cd4be47f?q=80&w=2000&auto=format&fit=crop'); 
            background-size: cover; background-position: center; justify-content: center;
        }

        .booking-card {
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(15px);
            padding: 60px;
            border-radius: 2px;
            border: 1px solid rgba(255,255,255,0.1);
            text-align: center;
            max-width: 700px;
            width: 100%;
        }

        .cta-button {
            display: inline-block;
            margin-top: 30px;
            padding: 20px 60px;
            background: var(--gold);
            color: #000;
            text-decoration: none;
            font-weight: 900;
            font-size: 1.5rem;
            transition: 0.4s;
        }

        .cta-button:hover { background: #fff; transform: translateY(-5px); }

        /* أنيميشن التمرير */
        .reveal { opacity: 0; transform: translateY(50px); transition: 1s all ease; }
        .reveal.active { opacity: 1; transform: translateY(0); }
    </style>
</head>
<body>

    <section>
        <img src="https://images.unsplash.com/photo-1584281722570-33230899026c?q=80&w=2560&auto=format&fit=crop" class="bg-img" alt="Macaw">
        <div>
            <h1 class="main-title">RAYYAN<br><span class="gold-text">PARK</span></h1>
            <p style="font-size: 1.2rem; letter-spacing: 10px; margin-top: 20px;">الرياض • تجربة استثنائية</p>
        </div>
    </section>

    <section class="description">
        <div class="desc-text reveal">
            <h2>من نكون؟</h2>
            <p>نحنُ وجهتك الأولى في الرياض للتواصل المباشر مع أندر ببغاوات المكاو والأمازون. مساحة صُممت لتذهل حواسك وتمنحك لحظات لا تُنسى مع جمال الطبيعة.</p>
        </div>
        <div style="height: 100%; position: relative;">
            <img src="https://images.unsplash.com/photo-1520114878144-6123749968dd?auto=format&fit=crop&w=1200&q=80" class="bg-img" style="opacity: 1;" alt="Parrot">
        </div>
    </section>

    <section class="booking-zone">
        <div class="booking-card reveal">
            <h2 style="font-size: 3rem; margin-bottom: 20px;">جاهز للانطلاق؟</h2>
            <p style="color: #ccc; margin-bottom: 40px;">اختر موعدك الآن وانضم إلينا في رحلة الألوان.</p>
            <a href="https://wa.me/9665XXXXXXXX" class="cta-button">تأكيد الحجز</a>
        </div>
    </section>

    <script>
        // أنيميشن عند التمرير لجعل الموقع "جامد" تفاعلياً
        window.addEventListener('scroll', () => {
            var reveals = document.querySelectorAll('.reveal');
            reveals.forEach(r => {
                var windowHeight = window.innerHeight;
                var revealTop = r.getBoundingClientRect().top;
                if (revealTop < windowHeight - 150) { r.classList.add('active'); }
            });
        });
    </script>
</body>
</html>
