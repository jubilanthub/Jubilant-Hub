<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Jubilant Hub</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial,sans-serif;
}

body{
    background:#000;
    color:#fff;
}

.header{
    background:#000;
    border-bottom:2px solid #D4AF37;
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:15px;
}

.logo{
    height:60px;
}

.brand{
    color:#D4AF37;
    font-size:28px;
    font-weight:bold;
}

.hero{
    text-align:center;
    padding:40px 20px;
}

.hero h1{
    color:#D4AF37;
    margin-bottom:10px;
}

.grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:10px;
    padding:10px;
}

.card{
    position:relative;
    overflow:hidden;
    border-radius:10px;
}

.card img{
    width:100%;
    height:250px;
    object-fit:cover;
}

.card h2{
    position:absolute;
    bottom:15px;
    left:15px;
    color:white;
    font-size:24px;
    font-weight:bold;
}

footer{
    text-align:center;
    padding:30px;
    border-top:2px solid #D4AF37;
    margin-top:20px;
}
</style>

</head>
<body>

<div class="header">
    <img src="logo.png" class="logo">
    <div class="brand">Jubilant Hub</div>
</div>

<div class="hero">
    <h1>Premium Fashion Collection</h1>
    <p>Discover quality clothing and footwear for every style.</p>
</div>

<div class="grid">

    <div class="card">
        <img src="men.jpg">
        <h2>MEN</h2>
    </div>

    <div class="card">
        <img src="women.jpg">
        <h2>WOMEN</h2>
    </div>

    <div class="card">
        <img src="shoes.jpg">
        <h2>SHOES</h2>
    </div>

    <div class="card">
        <img src="new.jpg">
        <h2>NEW ARRIVALS</h2>
    </div>

</div>

<footer>
    <p>WhatsApp: 063 727 2001</p>
    <p>© 2026 Jubilant Hub. All Rights Reserved.</p>
</footer>

</body>
</html>
