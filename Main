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

/* HEADER */
header{
    text-align:center;
    padding:25px;
    background:#111;
    border-bottom:2px solid #D4AF37;
}

header img{
    width:120px;
    margin-bottom:10px;
}

header h1{
    color:#D4AF37;
    font-size:3rem;
}

header p{
    margin-top:10px;
}

/* NAV */
nav{
    margin-top:15px;
}

nav a{
    color:white;
    text-decoration:none;
    margin:0 10px;
    font-weight:bold;
}

/* HERO */
.hero{
    text-align:center;
    padding:70px 20px;
    background:#111;
}

.hero h2{
    color:#D4AF37;
    font-size:40px;
}

.shop-btn{
    display:inline-block;
    margin-top:20px;
    background:#D4AF37;
    color:black;
    padding:15px 30px;
    text-decoration:none;
    border-radius:5px;
    font-weight:bold;
}

/* SEARCH */
#searchInput{
    width:90%;
    max-width:500px;
    padding:15px;
    border:none;
    border-radius:5px;
    margin:20px auto;
    display:block;
}

/* GALLERY */
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
    transition:0.3s;
}

.product:hover{
    transform:translateY(-5px);
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

/* SECTIONS */
.section{
    padding:30px;
    text-align:center;
}

.section h2{
    color:#D4AF37;
    margin-bottom:15px;
}

/* FLOATING WHATSAPP */
.floating-whatsapp{
    position:fixed;
    right:20px;
    bottom:20px;
    width:60px;
    height:60px;
    background:#25D366;
    color:white;
    text-decoration:none;
    border-radius:50%;
    text-align:center;
    line-height:60px;
    font-size:28px;
}

/* FOOTER */
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
    <img src="logo png.png" alt="MM Vision Hub Logo">
    <h1>MM VISION HUB</h1>
    <p>Women's Fashion • R150 Each • Nationwide Delivery</p>

    <nav>
        <a href="#gallery">Shop</a>
        <a href="#about">About</a>
        <a href="#delivery">Delivery</a>
        <a href="#contact">Contact</a>
    </nav>
</header>

<section class="hero">
    <h2>NEW WOMEN'S COLLECTION</h2>
    <p>Affordable Fashion Delivered Nationwide</p>
    <a href="#gallery" class="shop-btn">SHOP NOW</a>
</section>

<input type="text" id="searchInput" placeholder="Search Dresses..." onkeyup="searchProducts()">

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

<section class="section" id="about">
    <h2>Why Shop With Us?</h2>
    <p>✅ Secure Payments</p>
    <p>✅ Affordable Fashion</p>
    <p>✅ Nationwide Delivery</p>
    <p>✅ Quality Products</p>
</section>

<section class="section">
    <h2>Customer Reviews</h2>
    <p>⭐⭐⭐⭐⭐ Excellent quality dresses!</p>
    <p>⭐⭐⭐⭐⭐ Fast delivery and good service!</p>
    <p>⭐⭐⭐⭐⭐ Highly recommended!</p>
</section>

<section class="section" id="delivery">
    <h2>Delivery Information</h2>
    <p>Mapela Delivery: R40</p>
    <p>PAXI Standard: R110 (3-5 days)</p>
    <p>PAXI Large: R140 (3-5 days)</p>
</section>

<section class="section">
    <h2>Size Guide</h2>
    <p>Small (30-32)</p>
    <p>Medium (34-36)</p>
    <p>Large (38-40)</p>
    <p>XL (42-44)</p>
</section>

<section class="section">
    <h2>Banking Details</h2>
    <p>Bank: Capitec</p>
    <p>Account Name: Mr KM Maluleka</p>
    <p>Account Number: 2189801660</p>
</section>

<section class="section">
    <h2>Terms & Conditions</h2>
    <p>Payment before delivery</p>
    <p>Send proof of payment via WhatsApp</p>
    <p>Delivery takes 3–5 working days</p>
</section>

<footer>
    <h3>MM VISION HUB</h3>
    <p>WhatsApp: 073 217 6610</p>
    <p>Nationwide Delivery Available</p>
</footer>

<a href="https://wa.me/27732176610" class="floating-whatsapp">💬</a>

<script>
function searchProducts(){
    let input = document.getElementById("searchInput");
    let filter = input.value.toUpperCase();
    let products = document.getElementsByClassName("product");

    for(let i = 0; i < products.length; i++){
        let title = products[i].getElementsByTagName("h3")[0];
        if(title.innerHTML.toUpperCase().indexOf(filter) > -1){
            products[i].style.display = "";
        } else {
            products[i].style.display = "none";
        }
    }
}
</script>

</body>
</html>
