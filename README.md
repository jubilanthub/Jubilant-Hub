<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MM VISION HUB - Women's Clothing</title>

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

header{
    text-align:center;
    padding:25px;
}

header h1{
    color:#D4AF37;
    font-size:2.5rem;
}

header p{
    color:#fff;
    margin-top:10px;
}

.back{
    display:block;
    width:220px;
    margin:20px auto;
    text-align:center;
    background:#D4AF37;
    color:#000;
    text-decoration:none;
    padding:12px;
    border-radius:5px;
    font-weight:bold;
}

.gallery{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
    gap:20px;
    padding:20px;
}

.product{
    background:#111;
    border:1px solid #D4AF37;
    border-radius:10px;
    overflow:hidden;
}

.product img{
    width:100%;
    display:block;
}

.info{
    padding:15px;
    text-align:center;
}

.price{
    color:#D4AF37;
    font-size:24px;
    font-weight:bold;
    margin:10px 0;
}

.btn{
    display:block;
    text-decoration:none;
    padding:12px;
    margin-top:10px;
    border-radius:5px;
    font-weight:bold;
}

.whatsapp{
    background:#25D366;
    color:white;
}

.call{
    background:#D4AF37;
    color:black;
}

footer{
    text-align:center;
    padding:30px;
    border-top:1px solid #D4AF37;
    margin-top:30px;
}
</style>
</head>

<body>

<header>
    <h1>MM VISION HUB</h1>
    <p>Fashion Dresses • R150 Each • Nationwide Delivery</p>
</header>

<a href="index.html" class="back">← Back to Home</a>

<div class="gallery">

    <div class="product">
        <img src="women1.png" alt="Dress 1">
        <div class="info">
            <h3>Dress 1</h3>
            <p class="price">R150</p>
            <a class="btn whatsapp" href="https://wa.me/27732176610?text=Hi%20MM%20VISION%20HUB,%20I%20want%20Dress%201">Order on WhatsApp</a>
            <a class="btn call" href="tel:0732176610">Call Now</a>
        </div>
    </div>

    <div class="product">
        <img src="women2.png" alt="Dress 2">
        <div class="info">
            <h3>Dress 2</h3>
            <p class="price">R150</p>
            <a class="btn whatsapp" href="https://wa.me/27732176610?text=Hi%20MM%20VISION%20HUB,%20I%20want%20Dress%202">Order on WhatsApp</a>
            <a class="btn call" href="tel:0732176610">Call Now</a>
        </div>
    </div>

    <div class="product">
        <img src="women3.png" alt="Dress 3">
        <div class="info">
            <h3>Dress 3</h3>
            <p class="price">R150</p>
            <a class="btn whatsapp" href="https://wa.me/27732176610?text=Hi%20MM%20VISION%20HUB,%20I%20want%20Dress%203">Order on WhatsApp</a>
            <a class="btn call" href="tel:0732176610">Call Now</a>
        </div>
    </div>

</div>

<footer>
    <h3>MM VISION HUB</h3>
    <p>WhatsApp: 073 217 6610</p>
    <p>Call: 073 217 6610</p>
    <p>Nationwide Delivery Available</p>
</footer>

</body>
</html>
