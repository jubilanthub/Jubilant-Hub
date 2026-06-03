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
    font-family: Arial, sans-serif;
}

body{
    background:#000;
    color:#fff;
}

header{
    text-align:center;
    padding:30px;
    border-bottom:2px solid #D4AF37;
}

.logo{
    width:180px;
    margin-bottom:15px;
}

h1{
    color:#D4AF37;
}

.hero{
    text-align:center;
    padding:60px 20px;
}

.hero h2{
    color:#D4AF37;
    margin-bottom:15px;
}

.btn{
    display:inline-block;
    background:#D4AF37;
    color:#000;
    padding:12px 25px;
    text-decoration:none;
    border-radius:5px;
    font-weight:bold;
    margin-top:20px;
}

.section{
    padding:40px 20px;
    text-align:center;
}

.services{
    display:flex;
    flex-wrap:wrap;
    justify-content:center;
    gap:15px;
}

.card{
    background:#111;
    border:1px solid #D4AF37;
    padding:20px;
    width:180px;
    border-radius:10px;
}

footer{
    text-align:center;
    padding:20px;
    border-top:2px solid #D4AF37;
    margin-top:40px;
}
</style>
</head>

<body>

<header>
    <img src="logo.png" alt="Jubilant Hub Logo" class="logo">
    <h1>Jubilant Hub</h1>
</header>

<section class="hero">
    <h2>Welcome to Jubilant Hub</h2>
    <p>Your one-stop online store for clothing, shoes, electronics, phones, accessories, gifts, jobs, and more.</p>
    <a href="#" class="btn">Shop Now</a>
</section>

<section class="section">
    <h2 style="color:#D4AF37;">What We Offer</h2>
    <br>
    <div class="services">
        <div class="card">Clothing</div>
        <div class="card">Shoes</div>
        <div class="card">Phones</div>
        <div class="card">Electronics</div>
        <div class="card">Jobs</div>
        <div class="card">Accessories</div>
    </div>
</section>

<footer>
    <h3>Contact Us</h3>
    <p>WhatsApp: 063 727 2001</p>
</footer>

</body>
</html>
