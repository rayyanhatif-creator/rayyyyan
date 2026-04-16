<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>كافيه العز | النسخة الذهبية</title>
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root { 
            --primary-yellow: #FFD700; /* أصفر ذهبي */
            --bg-yellow: #FFEC8B;      /* أصفر فاتح للخلفية */
            --text-dark: #8B7500;      /* بني ذهبي غامق للنصوص لضمان الوضوح */
            --gold-bright: #FFF68F; 
        }

        body { 
            font-family: 'Tajawal', sans-serif; 
            background-color: var(--bg-yellow); 
            color: var(--text-dark); 
            display: flex; 
            flex-direction: column; 
            align-items: center; 
            margin: 0; 
            padding: 20px; 
            min-height: 100vh; 
        }

        h1 { 
            font-size: 50px; 
            margin: 20px 0; 
            color: var(--text-dark);
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1); 
        }

        .hero-img { 
            width: 100%; 
            max-width: 600px; 
            border-radius: 25px; 
            border: 4px solid var(--primary-yellow); 
            height: 300px; 
            object-fit: cover; 
            margin-bottom: 25px; 
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        
        .team-box { 
            width: 100%; 
            max-width: 600px; 
            background: var(--gold-bright); 
            padding: 25px; 
            border-radius: 20px; 
            text-align: center; 
            border: 2px solid var(--primary-yellow); 
            margin-bottom: 25px; 
            box-sizing: border-box; 
        }

        .on-duty { 
            margin-top: 12px; 
            font-size: 15px; 
            color: var(--text-dark); 
            background: rgba(255, 215, 0, 0.3); 
            padding: 8px 18px; 
            border-radius: 25px; 
            border: 1px solid var(--primary-yellow); 
            display: inline-block; 
            font-weight: bold;
        }

        .menu-container { width: 100%; max-width: 600px; margin-bottom: 30px; }
        
        .menu-category { 
            background: var(--gold-bright); 
            border: 2px solid var(--primary-yellow); 
            border-radius: 20px; 
            padding: 20px; 
            margin-bottom: 20px; 
            box-sizing: border-box; 
        }

        .category-title { 
            border-bottom: 3px solid var(--primary-yellow); 
            padding-bottom: 10px; 
            margin-bottom: 15px; 
            font-size: 20px; 
            font-weight: bold; 
            color: var(--text-dark);
            display: flex; 
            align-items: center; 
            gap: 10px; 
        }

        .menu-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
        
        .menu-item { 
            background: #fff; 
            padding: 12px; 
            border-radius: 12px; 
            border-right: 5px solid var(--primary-yellow); 
            font-size: 15px; 
            color: var(--text-dark); 
            font-weight: bold;
        }

        .order-container { 
            background: var(--primary-yellow); 
            color: #000; 
            width: 100%; 
            max-width: 600px; 
            padding: 30px; 
            border-radius: 30px; 
            text-align: center; 
            box-sizing: border-box; 
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }

        input { 
            width: 100%; 
            padding: 15px; 
            border-radius: 12px; 
            border: 2px solid var(--text-dark); 
            margin-top: 15px; 
            font-family: 'Tajawal'; 
            font-weight: bold; 
            text-align: center; 
            font-size: 16px; 
            box-sizing: border-box;
            background: #fff;
        }

        .btn-group { display: flex; gap: 10px; margin-top: 15px; }
        
        button { 
            flex: 2; 
            background: var(--text-dark); 
            color: var(--primary-yellow); 
            padding: 15px; 
            border-radius: 12px; 
            border: none; 
            font-weight: bold; 
            cursor: pointer; 
            font-size: 18px; 
        }

        .btn-clear { 
            flex: 1; 
            background: #fdfd96; 
            color: var(--text-dark); 
            font-size: 14px; 
            border: 1px solid var(--text-dark);
        }

        #ai-reply-box { 
            display: none; 
            margin-top: 20px; 
            padding: 20px; 
            background: #fff; 
            color: #000; 
            border-radius: 20px; 
            border: 4px solid var(--text-dark); 
            font-weight: bold; 
            cursor: pointer; 
        }
        
        .story-box { 
            width: 100%; 
            max-width: 600px; 
            margin: 40px 0 20px; 
            padding: 30px; 
            background: var(--gold-bright); 
            border-radius: 20px; 
            border: 2px solid var(--primary-yellow); 
            line-height: 1.8; 
            text-align: justify; 
            box-sizing: border-box; 
            color: var(--text-dark);
        }

        .survey-container { 
            width: 100%; 
            max-width: 600px; 
            background: var(--gold-bright); 
            padding: 25px; 
            border-radius: 20px; 
            border: 2px solid var(--primary-yellow); 
            text-align: center; 
            box-sizing: border-box; 
            margin-bottom: 30px; 
        }

        .stars { display: flex; justify-content: center; gap: 10px; margin: 15px 0; font-size: 30px; cursor: pointer; }
        .star { color: #ccc; }
        .star.active { color: var(--text-dark); }

        .footer { 
            margin-top: 40px; 
            margin-bottom: 20px; 
            font-size: 14px; 
            color: var(--text-dark); 
            text-align: center; 
            font-weight: bold;
        }
    </style>
</head>
<body>

    <h1>كـافـيـه الـعـز</h1>

    <img src="https://images.unsplash.com/photo-1447933601403-0c6688de566e?q=80&w=1000&auto=format&fit=crop" class="hero-img">

    <div class="team-box">
        <div style="font-weight: bold; font-size: 20px;">القائد: أبو وليد 👑 | الرئيس: أسامة ✨</div>
        <div style="font-size: 16px; color: var(--text-dark); opacity: 0.8; margin: 8px 0;">ريان • حيان • باسل • ذكاء العز</div>
        <div class="on-duty">🟡 متواجد الآن لخدمتكم: أسامة، ريان، حيان، باسل، <b>ذكاء العز 🤖</b></div>
    </div>

    <div class="menu-container">
        <div class="menu-category">
            <div class="category-title">🍟 مـوالـح الـعـز</div>
            <div class="menu-grid">
                <div class="menu-item">بطاطس مقلية</div>
                <div class="menu-item">ذرة</div>
                <div class="menu-item">سمبوسة</div>
                <div class="menu-item">بليلة</div>
            </div>
        </div>

        <div class="menu-category">
            <div class="category-title">🍰 حـلا الـعـز</div>
            <div class="menu-grid">
                <div class="menu-item">بسبوسة</div>
                <div class="menu-item">كريمة</div>
                <div class="menu-item">جلي</div>
                <div class="menu-item">آيسكريم</div>
            </div>
        </div>

        <div class="menu-category">
            <div class="category-title">🍹 مـشـروبـات بـاردة</div>
            <div class="menu-grid">
                <div class="menu-item">موهيتو مانجو</div>
                <div class="menu-item">موهيتو برتقال</div>
                <div class="menu-item">عصير مانجو</div>
                <div class="menu-item">عصير برتقال</div>
            </div>
        </div>

        <div class="menu-category">
            <div class="category-title">☕ مـشـروبـات حـارة</div>
            <div class="menu-grid">
                <div class="menu-item">نعناع</div>
                <div class="menu-item">قهوة</div>
            </div>
        </div>
    </div>

    <div class="order-container">
        <h3 style="margin:0">اطلب عبر ذكاء العز 🤖☕</h3>
        <input type="text" id="userInput" placeholder="وش بخاطرك تطلب؟" onkeypress="if(event.key==='Enter') askAI()">
        <div class="btn-group">
            <button onclick="askAI()">إرسال الطلب</button>
            <button class="btn-clear" onclick="resetAll()">الرجوع ↩️</button>
        </div>
        <div id="ai-reply-box" onclick="resetAll()">
            <div id="ai-text"></div>
            <div style="font-size: 10px; margin-top: 15px; color: #999;">(اضغط للمسح والرجوع)</div>
        </div>
    </div>

    <div class="story-box">
        <h2 style="text-align: center; color: var(--text-
