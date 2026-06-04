<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MM VISION HUB</title>

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

/* ================= LOADER ================= */
#loader{
    position:fixed;
    width:100%;
    height:100vh;
    background:#000;
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    z-index:9999;
}

#loader img{
    width:140px;
    animation: pulse 1.5s infinite;
}

#loader h2{
    color:#D4AF37;
    margin-top:20px;
}

@keyframes pulse{
    0%{transform:scale(1);}
    50%{transform:scale(1.1);}
    100%{transform:scale(1);}
}

/* ================= MAIN SITE ================= */
#main{
    display:none;
}

/* HEADER */
header{
    text-align:center;
    padding:20px;
    background:#111;
    border-bottom:2px solid #D4AF37;
}

header img{
    width:100px;
}

header h1{
    color:#D4AF37;
    font-size:2.5rem;
}

nav a{
    color:#fff;
    text-decoration:none;
    margin:0 10px;
}

/* HERO */
.hero{
    text-align:center;
    padding:50px 20px;
    background:#111;
}

.hero h2{
    color:#D4AF37;
    font-size:35px;
}

/* SEARCH */
#searchInput{
    width:90%;
    max-width:500px;
    padding:12px;
    margin:20px auto;
    display:block;
    border-radius:5px;
    border:none;
}

/* GALLERY */
.gallery{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:15px;
    padding:15px;
}

.product{
    background:#111;
    border:1px solid #D4AF37;
    border-radius:10px;
    overflow:hidden;
}

.product img{
    width:100%;
}

.info{
    padding:10px;
    text-align:center;
}

.price{
    color:#D4AF37;
    font-size:20px;
}

button{
    margin-top:8px;
    padding:10px;
    width:100%;
    border:none;
    cursor:pointer;
    border-radius:5px;
}

.add{
    background:#D4AF37;
}

.whatsapp{
    background:#25D366;
    color:#fff;
}

/* FLOAT */
.floating-whatsapp{
    position:fixed;
    right:15px;
    bottom:15px;
    width:60px;
    height:60px;
    background:#25D366;
    color:#fff;
    border-radius:50%;
    text-align:center;
    line-height:60px;
    font-size:28px;
    text-decoration:none;
}
</style>
</head>

<body>

<!-- LOADER SCREEN -->
<div id="loader">
    <img src="logo png.png" alt="Logo">
    <h2>MM VISION HUB</h2>
    <p>Loading Store...</p>
</div>

<!-- MAIN WEBSITE -->
<div id="main">

<header>
    <img src="logo png.png">
    <h1>MM VISION HUB</h1>
    <nav>
        <a href="#gallery">Shop</a>
        <a href="#about">About</a>
    </nav>
</header>

<section class="hero">
    <h2>New Women's Collection</h2>
    <p>Affordable Fashion Delivered Nationwide</p>
</section>

<input type="text" id="searchInput" placeholder="Search Dresses..." onkeyup="searchProducts()">

<div class="gallery" id="gallery"></div>

</div>

<script>

/* ============ LOADER TIMER ============ */
setTimeout(()=>{
    document.getElementById("loader").style.display="none";
    document.getElementById("main").style.display="block";
}, 5000);

/* ============ PRODUCTS ============ */
const gallery = document.getElementById("gallery");

for(let i=1;i<=80;i++){
    gallery.innerHTML += `
    <div class="product">
        <img src="women${i}.png">
        <div class="info">
            <h3>Dress ${i}</h3>
            <p class="price">R150</p>

            <button class="add" onclick="order(${i})">
                Buy Now
            </button>
        </div>
    </div>`;
}

function order(i){
    let msg = "Hello MM VISION HUB, I want Dress " + i;
    window.open("https://wa.me/27732176610?text=" + encodeURIComponent(msg));
}

/* SEARCH */
function searchProducts(){
    let input=document.getElementById("searchInput").value.toUpperCase();
    let products=document.getElementsByClassName("product");

    for(let i=0;i<products.length;i++){
        let title=products[i].getElementsByTagName("h3")[0];
        products[i].style.display =
        title.innerText.toUpperCase().includes(input) ? "" : "none";
    }
}
</script>

<a href="https://wa.me/27732176610" class="floating-whatsapp">💬</a>

</body>
</html>
