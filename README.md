<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>حديقة طيور الريان | حجز تذاكر</title>
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    
    <style>
        :root {
            --primary-color: #2e7d32; /* أخضر طبيعي */
            --secondary-color: #fbc02d; /* أصفر (مثل ريش الببغاوات) */
            --text-color: #333;
            --bg-color: #f4f7f6;
        }

        body {
            font-family: 'Tajawal', sans-serif;
            background-color: var(--bg-color);
            margin: 0;
            padding: 0;
            color: var(--text-color);
        }

        header {
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), 
                        url('https://images.unsplash.com/photo-1552728089-57bdde30eba3?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            height: 300px;
            color: white;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
        }

        header h1 { margin: 0; font-size: 2.5rem; text-shadow: 2px 2px 4px rgba(0,0,0,0.5); }
        header p { font-size: 1.2rem; margin-top: 10px; }

        .container {
            max-width: 800px;
            margin: -50px auto 50px;
            background: white;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }

        .booking-form {
            display: grid;
            gap: 20px;
        }

        .form-group {
            display: flex;
            flex-direction: column;
        }

        label {
            font-weight: bold;
            margin-bottom: 8px;
            color: var(--primary-color);
        }

        input, select {
            padding: 12px;
            border: 2px solid #ddd;
            border-radius: 8px;
            font-family: inherit;
            font-size: 1rem;
            transition: border-color 0.3s;
        }

        input:focus {
            outline: none;
            border-color: var(--primary-color);
        }

        .btn-submit {
            background-color: var(--primary-color);
            color: white;
            padding: 15px;
            border: none;
            border-radius: 8px;
            font-size: 1.1rem;
            font-weight: bold;
            cursor: pointer;
            transition: background 0.3s;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 10px;
        }

        .btn-submit:hover {
            background-color: #1b5e20;
        }

        .info-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 40px;
        }

        .card {
            text-align: center;
            padding: 20px;
            background: #fff;
            border-bottom: 4px solid var(--secondary-color);
            border-radius: 8px;
        }

        .card i {
            font-size: 2rem;
            color: var(--primary-color);
            margin-bottom: 10px;
        }

        footer {
            text-align: center;
            padding: 20px;
            font-size: 0.9rem;
            color: #777;
        }
    </style>
</head>
<body>

<header>
    <h1>حديقة طيور الريان</h1>
    <p>عالم من الألوان والطبيعة بانتظارك</p>
</header>

<div class="container">
    <h2 style="text-align: center; margin-bottom: 30px;">احجز زيارتك الآن</h2>
    
    <form class="booking-form" id="bookingForm">
        <div class="form-group">
            <label><i class="fas fa-user"></i> الاسم الكامل:</label>
            <input type="text" id="name" placeholder="أدخل اسمك" required>
        </div>

        <div class="form-group">
            <label><i class="fas fa-calendar-alt"></i> تاريخ الزيارة:</label>
            <input type="date" id="visitDate" required>
        </div>

        <div class="form-group">
            <label><i class="fas fa-users"></i> عدد الزوار:</label>
            <input type="number" id="guests" min="1" value="1" required>
        </div>

        <div class="form-group">
            <label><i class="fas fa-phone"></i> رقم الجوال (واتساب):</label>
            <input type="tel" id="phone" placeholder="05xxxxxxxx" required>
        </div>

        <button type="submit" class="btn-submit">
            تأكيد الحجز عبر واتساب <i class="fab fa-whatsapp"></i>
        </button>
    </form>

    <div class="info-cards">
        <div class="card">
            <i class="fas fa-clock"></i>
            <h3>أوقات العمل</h3>
            <p>4:00 م - 10:00 م</p>
        </div>
        <div class="card">
            <i class="fas fa-map-marker-alt"></i>
            <h3>الموقع</h3>
            <p>الرياض - حديقة الريان</p>
        </div>
    </div>
</div>

<footer>
    &copy; 2026 جميع الحقوق محفوظة لـ حديقة طيور الريان
</footer>

<script>
    document.getElementById('bookingForm').addEventListener('submit', function(e) {
        e.preventDefault();
        
        // جلب البيانات من النموذج
        const name = document.getElementById('name').value;
        const date = document.getElementById('visitDate').value;
        const guests = document.getElementById('guests').value;
        const phone = document.getElementById('phone').value;
        
        // صياغة رسالة الواتساب
        const message = `مرحباً حديقة طيور الريان، أرغب في تأكيد حجز:%0A%0A` +
                        `*الاسم:* ${name}%0A` +
                        `*التاريخ:* ${date}%0A` +
                        `*عدد الزوار:* ${guests}%0A` +
                        `*رقم التواصل:* ${phone}`;
        
        // رقم الواتساب الخاص بالحديقة (ضع رقمك هنا بدلاً من 9665XXXXXXXXX)
        const whatsappNumber = "9665XXXXXXXXX"; 
        
        // فتح واتساب
        window.open(`https://wa.me/${whatsappNumber}?text=${message}`, '_blank');
    });
</script>

</body>
</html>
