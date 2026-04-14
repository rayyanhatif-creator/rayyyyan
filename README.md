<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>لوحة صدارة المسابقة | Leaderboard</title>
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-color: #050505;
            --card-bg: #111111;
            --accent-color: #3b82f6; /* لون أزرق عصري */
            --text-color: #ffffff;
            --secondary-text: #a1a1aa;
            --gold: #fbbf24;
        }

        body {
            font-family: 'Tajawal', sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            margin: 0;
            display: flex;
            justify-content: center;
            padding-top: 50px;
        }

        .container {
            width: 100%;
            max-width: 600px;
            padding: 20px;
        }

        .header {
            text-align: center;
            margin-bottom: 30px;
        }

        .header h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            background: linear-gradient(to bottom, #fff, #666);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .leaderboard-list {
            background-color: var(--card-bg);
            border-radius: 16px;
            border: 1px solid #222;
            overflow: hidden;
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1);
        }

        .item {
            display: flex;
            align-items: center;
            padding: 15px 20px;
            border-bottom: 1px solid #222;
            transition: background 0.3s;
        }

        .item:hover {
            background-color: #161616;
        }

        .rank {
            font-size: 1.2rem;
            font-weight: bold;
            width: 40px;
            color: var(--secondary-text);
        }

        .rank-1 { color: var(--gold); } /* المركز الأول */

        .avatar {
            width: 45px;
            height: 45px;
            background: #222;
            border-radius: 50%;
            margin-left: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
        }

        .info {
            flex-grow: 1;
        }

        .name {
            display: block;
            font-weight: bold;
            font-size: 1.1rem;
        }

        .score-box {
            text-align: left;
        }

        .score-value {
            color: var(--accent-color);
            font-weight: bold;
            font-size: 1.2rem;
        }

        .score-label {
            display: block;
            font-size: 0.7rem;
            color: var(--secondary-text);
            text-transform: uppercase;
        }

        /* تصميم للمراكز الثلاثة الأولى */
        .top-three {
            display: flex;
            justify-content: center;
            align-items: flex-end;
            margin-bottom: 30px;
            gap: 15px;
        }

        .top-item {
            text-align: center;
            flex: 1;
        }

        .top-item .avatar {
            width: 70px;
            height: 70px;
            margin: 0 auto 10px;
            border: 3px solid transparent;
        }

        .first .avatar { border-color: var(--gold); width: 90px; height: 90px; font-size: 2rem; }
        .first .name { font-size: 1.3rem; color: var(--gold); }
    </style>
</head>
<body>

<div class="container">
    <div class="header">
        <h1>الترتيب العام</h1>
        <p style="color: var(--secondary-text);">نتائج المسابقة الحالية</p>
    </div>

    <div id="podium" class="top-three">
        </div>

    <div class="leaderboard-list" id="list">
        </div>
</div>

<script>
    // بيانات المتسابقين - هنا تضيف الأسماء والنقاط
    const players = [
        { name: "محمد العتيبي", score: 2450 },
        { name: "خالد بن أحمد", score: 2100 },
        { name: "سلطان", score: 1950 },
        { name: "عبدالعزيز", score: 1800 },
        { name: "ريان", score: 2800 }, // سيظهر الأول تلقائياً
        { name: "يوسف", score: 1500 }
    ];

    function updateLeaderboard() {
        const listContainer = document.getElementById('list');
        const podiumContainer = document.getElementById('podium');

        // ترتيب اللاعبين من الأعلى للأقل
        const sorted = [...players].sort((a, b) => b.score - a.score);

        // تعبئة المنصة (أول 3)
        const top3 = sorted.slice(0, 3);
        // ترتيب العرض (الثاني، الأول، الثالث)
        podiumContainer.innerHTML = `
            <div class="top-item second">
                <div class="avatar">🥈</div>
                <span class="name">${top3[1]?.name || '-'}</span>
                <span class="score-value">${top3[1]?.score || 0}</span>
            </div>
            <div class="top-item first">
                <div class="avatar">👑</div>
                <span class="name">${top3[0]?.name || '-'}</span>
                <span class="score-value">${top3[0]?.score || 0}</span>
            </div>
            <div class="top-item third">
                <div class="avatar">🥉</div>
                <span class="name">${top3[2]?.name || '-'}</span>
                <span class="score-value">${top3[2]?.score || 0}</span>
            </div>
        `;

        // تعبئة باقي القائمة
        listContainer.innerHTML = sorted.map((p, i) => `
            <div class="item">
                <div class="rank ${i === 0 ? 'rank-1' : ''}">${i + 1}</div>
                <div class="avatar">${p.name.charAt(0)}</div>
                <div class="info">
                    <span class="name">${p.name}</span>
                </div>
                <div class="score-box">
                    <span class="score-value">${p.score}</span>
                    <span class="score-label">نقطة</span>
                </div>
            </div>
        `).join('');
    }

    window.onload = updateLeaderboard;
</script>

</body>
</html>
