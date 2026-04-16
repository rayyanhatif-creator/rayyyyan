<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>كافيه العز | القمة</title>
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root { --gold: #FFD700; --black: #000000; --dark: #0a0a0a; --grey: #1a1a1a; }
        
        /* تأثيرات الظهور */
        @keyframes fadeIn { from { opacity: 0; transform: translateY(20px); } to { opacity: 1; transform: translateY(0); } }
        
        body { 
            font-family: 'Tajawal', sans-serif; background-color: var(--black); color: var(--gold); 
            display: flex; flex-direction: column; align-items: center; margin: 0; padding: 20px; 
            min-height: 100vh; scroll-behavior: smooth;
        }

        /* الساعة الرقمية */
        .clock-box { position: fixed; top: 10px; right: 10px; background: rgba(255, 215, 0, 0.1); border: 1px solid var(--gold); padding: 5px 15px; border-radius: 15px; font-weight: bold; font-size: 14px; z-index: 1000; }

        h1 { font-size: clamp(40px, 10vw, 60px); margin: 30px 0; text-shadow: 0 0 20px rgba(255,215,0,0.4); animation: fadeIn 0.8s ease; }

        .hero-img { width: 100%; max-width: 600px; border-radius: 30px; border: 2px solid var(--gold); height: 300px; object-fit: cover; margin-bottom: 30px; animation: fadeIn 1s ease; }
        
        .team-box { width: 100%; max-width: 600px; background: var(--grey); padding: 25px; border-radius: 25px; text-align: center; border: 1px solid #333; margin-bottom: 30px; animation: fadeIn 1.2s ease; }
        .on-duty { margin-top: 15px; font-size: 14px; color: #fff; background: rgba(255, 215, 0, 0.2); padding: 8px 20px; border-radius: 30px; border: 1px solid var(--gold); display: inline-block; }

        /* المنيو بتصميم احترافي */
        .menu-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 15px; width: 100%; max-width: 600px; margin-bottom: 40px; }
        .menu-card { background: var(--dark); border-right: 4px solid var(--gold); padding: 15px; border-radius: 15px; transition: 0.3s; animation: fadeIn 1.4s ease; }
        .menu-card:hover { transform: scale(1.03); background: #111; }
        .category-name { color: #fff; font-size: 12px; opacity: 0.6; margin-bottom: 5px; }
        .item-name { font-weight: bold; font-size: 17px; }

        /* صندوق الطلب والذكاء */
        .order-container { background: var(--gold); color: #000; width: 100%; max-width: 600px; padding: 35px; border-radius: 35px; text-align: center; box-shadow: 0 10px 30px rgba(255,215,0,0.2); transition: 0.4s; }
        input { width: 100%; padding: 18px; border-radius: 15px; border: 2px solid #000; margin-top: 20px; font-family: 'Tajawal'; font-weight: bold; text-align: center; font-size: 18px; }
        .btn-send { background: #000; color: var(--gold); padding: 15px 40px; border-radius: 15px; border: none; font-weight: bold; cursor: pointer; margin-top: 15px; font-size: 18px; width: 100%; }
        
        #ai-reply { display: none; margin-top: 25px; padding: 20px; background: #fff; color: #000; border-radius: 20px; border-right: 8px solid #000; font-weight: bold; animation: fadeIn 0.4s ease; }

        /* قصة العز والتقييم */
        .content-box { width: 100%; max-width: 600px; margin: 40px 0; background: var(--grey); padding: 30px; border-radius: 25px; border: 1px solid #333; line-height: 1.8; text-align: center; }
        .stars { font-size: 35px; cursor: pointer; margin: 15px 0; }
        .star { color: #444; transition: 0.2s; }
        .star.active { color: var(--gold); text-shadow: 0 0 10px var(--gold); }

        /* زر الواتساب */
        .wa-btn { background: #25D366; color: white; padding: 12px 25px; border-radius: 50px; text-decoration: none; font-weight: bold; margin-top: 20px; display: inline-flex; align-items: center; gap: 10px; }
    </style>
</head>
<body>

    <div class="clock-box" id="clock">00:00:00</div>

    <h1>كـافـيـه الـعـز</h1>

    <img src="https://images.unsplash.com/photo-1447933601403-0c6688de566e?q=80&w=1000&auto=format&fit=crop" class="hero-img">

    <div class="team-box">
        <div style="font-weight: bold; font-size: 22px;">القائد: أبو وليد 👑 | الرئيس: أسامة ✨</div>
        <div style="font-size: 16px; color: #aaa; margin: 10px 0;">ريان • حيان • باسل • ذكاء العز</div>
        <div class="on-duty">🟢 متواجد الآن لخدمتكم: أسامة، ريان، حيان، باسل، <b>ذكاء العز 🤖</b></div>
    </div>

    <div class="menu-grid">
        <div class="menu-card"><div class="category-name">موالح</div><div class="item-name">بطاطس • سمبوسة • بليلة</div></div>
        <div class="menu-card"><div class="category-name">حلا</div><div class="item-name">بسبوسة • كريمة • كيكة</div></div>
        <div class="menu-card"><div class="category-name">بارد</div><div class="item-name">موهيتو • عصير طازج</div></div>
        <div class="menu-card"><div class="category-name">حار</div><div class="item-name">نعناع • قهوة العز</div></div>
    </div>

    <div class="order-container">
        <h3 style="margin:0">اطلب عبر ذكاء العز 🤖☕</h3>
        <input type="text" id="userInput" placeholder="وش بخاطرك تطلب؟" onkeypress="if(event.key==='Enter') askAI()">
        <button class="btn-send" onclick="askAI()">إرسال الطلب</button>
        <div id="ai-reply" onclick="this.style.display='none'">
            <div id="ai-text"></div>
            <div style="font-size: 10px; color: #888; margin-top: 10px;">(اضغط للمسح والرجوع)</div>
        </div>
    </div>

    <div class="content-box">
        <h2>قصة العز 📜</h2>
        بدأت الرحلة من <b>حلقات الصفوة</b>. بفضل تكاتف الفريق، صمم <b>ريان</b> هذا الموقع ليكون واجهتنا الرقمية.
    </div>

    <div class="content-box" style="border: 1px solid var(--gold);">
        <h3>تقييمك لنا يهمنا ⭐</h3>
        <div class="stars">
            <span class="star" onclick="rate(1)">★</span><span class="star" onclick="rate(2)">★</span><span class="star" onclick="rate(3)">★</span><span class="star" onclick="rate(4)">★</span><span class="star" onclick="rate(5)">★</span>
        </div>
        <div id="rateMsg" style="font-weight:bold"></div>
    </div>

    <a href="https://wa.me/966XXXXXXXXX" class="wa-btn">💬 تواصل معنا عبر واتساب</a>

    <img src="https://images.unsplash.com/photo-1495474472287-4d71bcdd2085?q=80&w=1000&auto=format&fit=crop" class="hero-img" style="margin-top:40px">

    <div class="footer">كافيه العز © 2026</div>

    <script>
        // الساعة
        setInterval(() => {
            const now = new Date();
            document.getElementById('clock').innerText = now.toLocaleTimeString('ar-SA');
        }, 1000);

        // الذكاء الاصطناعي
        async function askAI() {
            const input = document.getElementById('userInput');
            const box = document.getElementById('ai-reply');
            const text = document.getElementById('ai-text');
            if(!input.value.trim()) return;
            const msg = input.value;
            input.value = ""; // مسح فوري
            box.style.display = "block";
            text.innerText = "⏳ ذكاء العز يجهز طلبك...";
            try {
                const res = await fetch('https://voxa-3a7ac828dfb6.herokuapp.com/webhook/f679c772-d169-4e46-a1cd-35bd223dc4b6', {
                    method: 'POST',
                    headers: {'Content-Type': 'application/json'},
                    body: JSON.stringify({chatInput: msg})
                });
                const data = await res.json();
                text.innerText = data.output || data.text || "تم استلام طلبك!";
            } catch(e) { text.innerText = "أبشر، طلبك وصل للفريق!"; }
        }

        // التقييم
        function rate(n) {
            const stars = document.querySelectorAll('.star');
            stars.forEach((s, i) => s.classList.toggle('active', i < n));
            document.getElementById('rateMsg').innerText = "شكراً لتقييمك يا بطل! 🔥";
        }
    </script>
</body>
</html>
