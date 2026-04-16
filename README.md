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
            --text-dark: #8B7500;      /* بني ذهبي غامق للنصوص */
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
