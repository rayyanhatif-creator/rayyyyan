<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>حديقة طيور الريان | تجربة لا تُنسى</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;700;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    
    <style>
        :root {
            --bg-dark: #0a0a0a;
            --accent: #d4af37; /* لون ذهبي خافت للفخامة */
            --card-bg: #1a1a1a;
            --text-light: #ffffff;
        }

        body {
            font-family: 'Cairo', sans-serif;
            background-color: var(--bg-dark);
            color: var(--text-light);
            margin: 0;
            padding: 0;
            line-height: 1.6;
        }

        /* Hero Section */
        header {
            height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), 
                        url('https://images.unsplash.com/photo-1520114878144-6123749968dd?auto=format&fit=crop&w=1920&q=80');
            background-size: cover;
            background-position: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 20px;
        }

        header h1 {
            font-size: clamp(2.5rem, 8vw, 5rem);
            font-weight: 900;
            margin: 0;
            letter-spacing: -2px;
            text-transform: uppercase;
        }

        header p {
            font-size: 1.5rem;
            color: var(--accent);
            margin: 20px 0;
            font-weight: 300;
        }

        /* Booking Button */
        .cta-btn {
            background-color: transparent;
            color: var(--text-light);
            border: 1px solid var(--text-light);
            padding: 15px 40px;
            font-size: 1.2rem;
            text-decoration: none;
            transition: 0.4s;
            margin-top: 30px;
            cursor: pointer;
        }

        .cta-btn:hover {
            background-color: var(--text-light);
            color: var(--bg-dark);
        }

        /* Booking Section */
        .booking-section {
            padding: 100px 20px;
            max-width: 600px;
            margin: 0 auto;
        }

        .input-group {
            margin-bottom: 30px;
        }

        label {
            display: block;
            font-size: 0.9rem;
            color: #888;
            margin-bottom: 10px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        input, select {
            width: 100%;
            background: transparent;
            border: none;
            border-bottom: 1px solid #333;
            color: white;
            padding: 15px 0;
            font-size: 1.1rem;
            font-family: 'Cairo';
            transition: border-color 0.3s;
        }

        input:focus {
            outline: none;
            border-bottom-color: var(--accent);
        }

        .submit-btn {
            width: 100%;
            background-color: var(--accent);
            color: black;
            border: none;
            padding: 20px;
            font-weight: 900;
            font-size: 1.1rem;
            cursor: pointer;
            margin-top: 30px;
        }

        /* Footer */
        footer {
            padding: 50px;
            text-align: center;
            border-top: 1px solid #1a1a1a;
            font-size: 0.8rem;
            color: #555;
        }

    </style>
</head>
<body>

<header>
    <h1>RAYYAN PARK</h1>
    <p>حيث تلتقي الطبيعة بالفخامة</p>
    <a href="#booking" class="cta-btn">احجز الآن</a>
</header>

<div class="booking-section" id="booking">
    <h2 style="font-size: 2.5rem; margin-bottom: 50px; text-align: center;">التذكرة الرقمية</h2>
    
    <form id="reservationForm">
        <div class="input-group">
            <label>الاسم الكامل</label>
            <input type="text" id="name" placeholder="أدخل اسمك هنا..." required>
        </div>

        <div class="input-group">
            <label>التاريخ المفضل</label>
            <input type="date" id="date" required>
        </div>

        <div class="input-group">
            <label>عدد الضيوف</label>
            <select id="guests">
                <option value="1">شخص واحد</option>
                <option value="2">شخصين</option>
                <option value="3-5">عائلة (3-5 أشخاص)</option>
                <option value="6+">مجموعة كبيرة</option>
            </select>
        </div>

        <div class="input-group">
            <label>رقم الجوال</label>
            <input type="tel" id="phone" placeholder="05xxxxxxxx" required>
        </div>

        <button type="submit" class="submit-btn">تأكيد الحجز</button>
    </form>
</div>

<footer>
    RAYYAN BIRD PARK &copy; 2026<br>
    RIYADH, SAUDI ARABIA
</footer>

<script>
    document.getElementById('reservationForm').addEventListener('submit', function(e) {
        e.preventDefault();
        
        const name = document.getElementById('name').value;
        const date = document.getElementById('date').value;
        const guests = document.getElementById('guests').value;
        const phone = document.getElementById('phone').value;
        
        const message = `طلب حجز جديد لـ حديقة الريان:%0A` +
                        `👤 الاسم: ${name}%0A` +
                        `📅 التاريخ: ${date}%0A` +
                        `👥 العدد: ${guests}%0A` +
                        `📱 الجوال: ${phone}`;
        
        const whatsappNumber = "9665XXXXXXXXX"; // عدله لرقمك
        window.open(`https://wa.me/${whatsappNumber}?text=${message}`, '_blank');
    });
</script>

</body>
</html>
