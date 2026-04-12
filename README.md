<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>حديقة طيور الريان | القصة</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700;900&display=swap" rel="stylesheet">
    <style>
        body { margin: 0; background: #050505; color: white; font-family: 'Cairo', sans-serif; }
        nav { padding: 20px 50px; display: flex; justify-content: space-between; align-items: center; position: fixed; width: 100%; z-index: 100; box-sizing: border-box; }
        .logo { font-weight: 900; font-size: 1.5rem; color: #ffcc00; }
        
        .hero { height: 100vh; display: flex; align-items: center; padding: 0 10%; background: linear-gradient(to left, rgba(0,0,0,0.8), transparent), url('https://images.unsplash.com/photo-1552728089-57bdde30eba3?auto=format&fit=crop&w=1920&q=80'); background-size: cover; background-position: center; }
        .hero-content { max-width: 600px; }
        .hero-content h1 { font-size: 4rem; line-height: 1.1; margin-bottom: 20px; }
        .hero-content p { font-size: 1.2rem; color: #ccc; margin-bottom: 30px; }
        
        .btn-main { padding: 15px 40px; background: #ffcc00; color: black; text-decoration: none; font-weight: bold; border-radius: 5px; transition: 0.3s; }
        .btn-main:hover { background: white; transform: scale(1.05); }

        .about-section { padding: 100px 10%; display: grid; grid-template-columns: 1fr 1fr; gap: 50px; align-items: center; }
        .about-img { width: 100%; border-radius: 20px; filter: grayscale(30%); transition: 0.5s; }
        .about-img:hover { filter: grayscale(0%); }
    </style>
</head>
<body>
    <nav>
        <div class="logo">RAYYAN PARK</div>
        <div>
            <a href="booking.html" class="btn-main" style="padding: 10px 20px; font-size: 0.9rem;">احجز الآن</a>
        </div>
    </nav>

    <section class="hero">
        <div class="hero-content">
            <h1>عالم الببغاوات بين يديك</h1>
            <p>في حديقة الريان، نأخذك في رحلة فريدة لاستكشاف أندر أنواع الببغاوات من المكاو والأمازون في بيئة تحاكي الطبيعة الأم.</p>
            <a href="#about" class="btn-main">اكتشفنا</a>
        </div>
    </section>

    <section id="about" class="about-section">
        <div>
            <img src="https://images.unsplash.com/photo-1520114878144-6123749968dd?auto=format&fit=crop&w=800&q=80" class="about-img" alt="طيور الريان">
        </div>
        <div>
            <h2 style="font-size: 2.5rem; color: #ffcc00;">من نحن؟</h2>
            <p style="color: #aaa; font-size: 1.1rem;">نحن لسنا مجرد حديقة، نحن محمية تعليمية تفاعلية. حديقة طيور الريان تأسست لتكون الوجهة الأولى لعشاق الطيور في الرياض، حيث يمكنك التفاعل مباشرة مع الببغاوات والتعرف على أسرارها.</p>
            <a href="booking.html" style="color: white; text-decoration: underline;">انتقل لصفحة الحجز ←</a>
        </div>
    </section>
</body>
</html>
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>تأكيد الحجز | حديقة الريان</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body { margin: 0; background: #0a0a0a; color: white; font-family: 'Cairo', sans-serif; display: flex; align-items: center; justify-content: center; min-height: 100vh; }
        .booking-container { background: #151515; padding: 50px; border-radius: 30px; width: 90%; max-width: 500px; box-shadow: 0 20px 50px rgba(0,0,0,0.5); border: 1px solid #222; }
        h1 { text-align: center; color: #ffcc00; margin-bottom: 40px; }
        .input-group { margin-bottom: 25px; }
        label { display: block; margin-bottom: 10px; color: #888; font-size: 0.9rem; }
        input, select { width: 100%; background: #222; border: 1px solid #333; padding: 15px; border-radius: 10px; color: white; font-family: 'Cairo'; }
        input:focus { border-color: #ffcc00; outline: none; }
        .confirm-btn { width: 100%; background: #ffcc00; border: none; padding: 20px; border-radius: 10px; font-weight: bold; font-size: 1.1rem; cursor: pointer; transition: 0.3s; }
        .confirm-btn:hover { background: white; }
        .back-link { display: block; text-align: center; margin-top: 20px; color: #555; text-decoration: none; }
    </style>
</head>
<body>
    <div class="booking-container">
        <h1>تأكيد زيارتك</h1>
        <form id="bookForm">
            <div class="input-group">
                <label>الاسم الكامل</label>
                <input type="text" id="name" placeholder="مثال: ريان محمد" required>
            </div>
            <div class="input-group">
                <label>تاريخ الزيارة</label>
                <input type="date" id="visitDate" required>
            </div>
            <div class="input-group">
                <label>عدد الأشخاص</label>
                <input type="number" id="count" min="1" value="1">
            </div>
            <button type="submit" class="confirm-btn">إرسال الطلب عبر الواتساب</button>
        </form>
        <a href="index.html" class="back-link">← العودة للرئيسية</a>
    </div>

    <script>
        document.getElementById('bookForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const msg = `حجز جديد:%0Aالاسم: ${document.getElementById('name').value}%0Aالتاريخ: ${document.getElementById('visitDate').value}%0Aالعدد: ${document.getElementById('count').value}`;
            window.open(`https://wa.me/9665XXXXXXXXX?text=${msg}`, '_blank'); // استبدل X برقمك
        });
    </script>
</body>
</html>
