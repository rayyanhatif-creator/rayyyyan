<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Mohammed Travel</title>

<style>
body {
    margin: 0;
    font-family: Arial;
    background: #0f172a;
    color: white;
}

h1 {
    text-align: center;
    padding: 20px;
    background: #020617;
}

.grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
    padding: 30px;
}

.card {
    background: #1e293b;
    border-radius: 15px;
    overflow: hidden;
    transition: 0.3s;
    text-decoration: none;
    color: white;
}

.card:hover {
    transform: scale(1.05);
    box-shadow: 0 0 20px #38bdf8;
}

.card img {
    width: 100%;
    height: 200px;
    object-fit: cover;
}

.card h2 {
    padding: 10px;
    text-align: center;
}
</style>

</head>

<body>

<h1>🌍 Travel Highlights - Mohammed</h1>

<div class="grid">

<a href="japan.html" class="card">
<img src="https://source.unsplash.com/400x300/?japan">
<h2>Japan</h2>
</a>

<a href="amsterdam.html" class="card">
<img src="https://source.unsplash.com/400x300/?amsterdam">
<h2>Amsterdam</h2>
</a>

<a href="madrid.html" class="card">
<img src="https://source.unsplash.com/400x300/?madrid">
<h2>Madrid</h2>
</a>

<a href="canada.html" class="card">
<img src="https://source.unsplash.com/400x300/?canada,mountains">
<h2>Canada</h2>
</a>

<a href="bali.html" class="card">
<img src="https://source.unsplash.com/400x300/?bali">
<h2>Bali</h2>
</a>

<a href="egypt.html" class="card">
<img src="https://source.unsplash.com/400x300/?egypt,pyramids">
<h2>Egypt</h2>
</a>

</div>

</body>
</html>
