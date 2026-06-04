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
    padding:30px;
    background:#111;
    border-bottom:2px solid #D4AF37;
}

header h1{
    color:#D4AF37;
    font-size:3rem;
}

header p{
    margin-top:10px;
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

.section{
    padding:30px;
    text-align:center;
}

.section h2{
    color:#D4AF37;
    margin-bottom:15px;
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
    <p>Women's Fashion • R150 Each • Nationwide Delivery</p>
</header>

<div class="gallery" id="gallery"></div>

<script>
const gallery = document.getElementById("gallery");

for(let i = 1; i <= 80; i++){
    gallery.innerHTML += `
    <div class="product">
        <img src="women${i}.png" alt="Dress ${i}">
        <div class="info">
            <h3>Dress ${i}</h3>
            <p class="price">R150</p>

            <a class="btn whatsapp"
            href="https://wa.me/27732176610?text=Hello%20MM%20VISION%20HUB,%20I%20would%20like%20to%20order%20Dress%20${i}">
            Order on WhatsApp
            </a>

            <a class="btn call" href="tel:0732176610">
            Call Now
            </a>
        </div>
    </div>`;
}
</script>

<section class="section">
    <h2>About Us</h2>
    <p>
        MM VISION HUB is an online clothing store providing affordable,
        stylish and quality women's fashion with delivery across South Africa.
    </p>
</section>

<section class="section">
    <h2>Delivery Information</h2>
    <p><strong>Mapela Delivery:</strong> R40</p>
    <br>
    <p><strong>PAXI Standard Plastic:</strong> R110</p>
    <p>Delivery Time: 3 - 5 Working Days</p>
    <br>
    <p><strong>PAXI Large Plastic:</strong> R140</p>
    <p>Delivery Time: 3 - 5 Working Days</p>
</section>

<section class="section">
    <h2>Banking Details</h2>
    <p><strong>Bank:</strong> Capitec</p>
    <p><strong>Account Name:</strong> Mr KM Maluleka</p>
    <p><strong>Account Number:</strong> 2189801660</p>
</section>

<section class="section">
    <h2>Terms & Conditions</h2>
    <p>Payment must be made before delivery.</p>
    <p>Proof of payment must be sent via WhatsApp.</p>
    <p>Delivery charges apply.</p>
    <p>Delivery may take 3 - 5 working days.</p>
    <p>By placing an order, you agree to these terms.</p>
</section>

<footer>
    <h3>MM VISION HUB</h3>
    <p>WhatsApp: 073 217 6610</p>
    <p>Nationwide Delivery Available</p>
</footer>

</body>
</html>
