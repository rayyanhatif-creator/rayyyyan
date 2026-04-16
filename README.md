<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>كافيه العز</title>
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root { --gold: #FFD700; --black: #000000; --dark-grey: #121212; }
        
        body { 
            font-family: 'Tajawal', sans-serif; 
            background-color: var(--black); 
            color: var(--gold); 
            display: flex; flex-direction: column; align-items: center; 
            margin: 0; padding: 20px; min-height: 100vh;
        }

        h1 { font-size: clamp(35px, 8vw, 55px); margin: 20px 0; text-shadow: 0 0 15px rgba(255,215,0,0.5); text-align: center; }

        .hero-img { 
            width: 100%; max-width: 600px; border-radius: 25px; 
            border: 2px solid var(--gold); object-fit: cover; 
            height: 300px; margin-bottom: 25px;
        }

        .team-box { 
            width: 100%; max-width: 600px; background: var(--dark-grey); 
            padding: 20px; border-radius: 20px; text-align: center; 
            border: 1px solid #222; margin-bottom: 25px; box-sizing: border-box;
        }

        .on-duty { 
            margin-top: 12px; font-size: 14px; color: #fff; 
            background: rgba(255, 215, 0, 0.15); padding: 6px 15px; 
            border-radius: 25px; border: 1px solid var(--gold); display: inline-block;
        }

        .order-container { 
            background: var(--gold); color: #000; width: 100%; 
            max-width: 600px; padding: 30px; border-radius: 30px; 
            margin-top: 30px; text-align: center; box-sizing: border-box;
        }

        input { 
            width: 100%; padding: 15px; border-radius: 12px; border: 2px solid #000; 
            margin-top: 15px; font-family: 'Tajawal'; font-weight: bold; 
            text-align: center; font-size: 16px; box-sizing: border-box;
        }

        .btn-group { display: flex; gap: 10px; margin-top: 15px; }
        
        button { 
            flex: 2; background: #000; color: var(--gold); padding: 15px; 
            border-radius: 12px; border: none; font-weight: bold; 
            cursor: pointer; font-size: 18px; transition: 0.3s;
        }

        .btn-clear { 
            flex: 1; background: #444; color: #fff; font-size: 14px; 
        }

        #ai-reply-box { 
            display: none; margin-top: 20px; padding: 15px; 
            background: #fff; color: #000; border-radius: 15px; 
            font-weight: bold; cursor: pointer; border-left: 5px solid #000;
        }

        .story-box { 
            width: 100%; max-width: 600px; margin: 40px 0 20px 0; padding: 30px; 
            background: var(--dark-grey); border-radius: 20px; border: 1px solid #333; 
            line-height: 1.8; text-align: justify; box-sizing: border-box;
        }
        .story-box h2 { text-align: center; color: var(--gold); margin-top: 0; }

        .survey-container { 
            width: 100%; max-width: 600px; background: var(--dark-grey); 
            padding: 25px; border-radius: 20px; border: 1px solid var(--gold); 
            text-align: center; box-sizing: border-box; margin-bottom: 30px;
        }
        .stars { display: flex; justify-content: center; gap: 10px; margin: 15px 0; font-size: 30px; cursor: pointer; }
        .star { color: #444; transition: 0.3s; }
        .star.active { color: var(--gold); text-shadow: 0 0 10px rgba(255,215,0,0.5); }
        #ratingMsg { font-weight: bold; min-height: 20px; color: var(--gold); }

        .footer { margin: 30px 0 50px 0; font-size: 12px; opacity: 0.4; text-align: center; width: 100%; }
        
        /* تأثير حركي بسيط للرسالة */
        @keyframes slideInMsg {
            from { opacity: 0; transform: translateY(-10px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>

    <h1>كـافـيـه الـعـز</h1>

    <img src="https://images.unsplash.com/photo-1447933601403-0c6688de566e?q=80&w=1000&auto=format&fit=crop" class="hero-img">

    <div class="team-box">
        <div style="font-weight: bold; font-size: 20px;">القائد: أبو وليد 👑 | الرئيس: أسامة ✨</div>
        <div style="font-size: 16px; color: #aaa; margin: 8px 0;">ريان • حيان • باسل</div>
        <div class="on-duty">🟢 متواجد الآن لخدمتكم: أسامة، ريان، حيان، باسل، <b style="color:var(--gold); font-size:18px">ذكاء العز 🤖</b></div>
    </div>

    <div class="order-container">
        <h3 style="margin:0; font-size: 24px;">اطلب عبر ذكاء العز 🤖☕</h3>
        <input type="text" id="userInput" placeholder="وش بخاطرك تطلب؟" onkeypress="if(event.key==='Enter') askAI()">
        
        <div class="btn-group">
            <button onclick="askAI()">إرسال الطلب</button>
            <button class="btn-clear" onclick="clearMessage()">الرجوع ↩️</button>
        </div>

        <div id="ai-reply-box" onclick="clearMessage()">
            <span id="ai-text"></span>
            <div style="font-size: 10px; margin-top: 10px; color: #666;">(اضغط هنا للإغلاق والمسح)</div>
        </div>
    </div>

    <div class="story-box">
        <h2>قصة العز 📜</h2>
        بدأت الرحلة بتوفيق من <b>حلقات الصفوة</b>. وبفضل تكاتف الفريق وعملهم الجاد، صمم <b>ريان</b> هذا الموقع في وقت قياسي ليكون واجهتنا الرقمية بقيادة <b>أبو وليد</b> ورئاسة <b>أسامة</b>، ليكون منارة للعمل الجماعي المخلص.
    </div>

    <div class="survey-container">
        <h3 style="margin-top:0;">تقييمك لنا يهمنا ⭐</h3>
        <p style="color: #ccc; font-size: 14px; margin: 0;">كيف كانت تجربتك مع كافيه وذكاء العز؟</p>
        <div class="stars" id="starRating">
            <span class="star" onclick="rate(1)">★</span>
            <span class="star" onclick="rate(2)">★</span>
            <span class="star" onclick="rate(3)">★</span>
            <span class="star" onclick="rate(4)">★</span>
            <span class="star" onclick="rate(5)">★</span>
        </div>
        <div id="ratingMsg"></div>
    </div>

    <img src="https://images.unsplash.com/photo-1495474472287-4d71bcdd2085?q=80&w=1000&auto=format&fit=crop" class="hero-img">

    <div class="footer">كافيه العز © 2026</div>

    <script>
        async function askAI() {
            const input = document.getElementById('userInput');
            const replyBox = document.getElementById('ai-reply-box');
            const replyText = document.getElementById('ai-text');

            if (!input.value.trim()) return;

            // الحفظ والمسح الفوري (الحل الجذري للمشكلة القديمة)
            const currentMessage = input.value;
            input.value = ""; // مسح فوري للخانة عند الإرسال

            replyBox.style.display = "block";
            replyText.innerText = "⏳ جاري التجهيز بلمح البصر من ذكاء العز...";

            try {
                // استخدام الـ Webhook الخاص بك في n8n (الذي ضبطناه)
                const response = await fetch('https://voxa-3a7ac828dfb6.herokuapp.com/webhook/f679c772-d169-4e46-a1cd-35bd223dc4b6', {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify({ chatInput: currentMessage })
                });
                const data = await response.json();
                replyText.innerText = data.output || data.text || "تم استلام طلبك! أبشر بسعدك.";
            } catch (e) {
                // رد سريع إذا تعطل الـ n8n لأي سبب
                replyText.innerText = "أبشر، طلبك وصل!";
            }
        }

        function clearMessage() {
            document.getElementById('ai-reply-box').style.display = "none";
            document.getElementById('userInput').value = "";
            document.getElementById('ai-text').innerText = "";
        }

        function rate(n) {
            const stars = document.querySelectorAll('.star');
            const msg = document.getElementById('ratingMsg');
            stars.forEach((s, idx) => s.classList.toggle('active', idx < n));
            const messages = ["شكراً لصدقك!", "نطمح للأفضل!", "سعيدون برضاك!", "رائع جداً!", "أنت العز كله! 🔥"];
            msg.innerText = messages[n-1];
            msg.style.animation = 'none';
            msg.offsetHeight; // trigger reflow
            msg.style.animation = 'slideInMsg 0.4s ease';
        }
    </script>
</body>
</html>
