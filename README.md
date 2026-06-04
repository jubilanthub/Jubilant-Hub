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
    background:#0b0b0b;
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
    text-align:center;
}

#loader img{
    width:180px;
    animation:pulse 1.5s infinite;
}

#loader h1{
    color:#D4AF37;
    margin-top:20px;
    font-size:28px;
}

#loader p{
    margin-top:10px;
    color:#D4AF37;
    font-size:14px;
    letter-spacing:1px;
}

@keyframes pulse{
    0%{transform:scale(1);}
    50%{transform:scale(1.1);}
    100%{transform:scale(1);}
}

/* MAIN SITE */
#main{
    display:none;
}

/* TOP BAR */
.topbar{
    position:sticky;
    top:0;
    background:#111;
    padding:10px;
    display:flex;
    justify-content:space-between;
    align-items:center;
    border-bottom:2px solid #D4AF37;
}

.topbar img{
    width:50px;
}

.topbar h1{
    font-size:18px;
    color:#D4AF37;
}

/* HERO */
.hero{
    text-align:center;
    padding:40px 20px;
    background:#111;
}

.hero h2{
    color:#D4AF37;
    font-size:28px;
}

/* SEARCH */
#searchInput{
    width:90%;
    padding:12px;
    margin:15px auto;
    display:block;
    border-radius:20px;
    border:none;
}

/* PRODUCTS */
.gallery{
    display:grid;
    grid-template-columns:repeat(2,1fr);
    gap:10px;
    padding:10px;
}

.product{
    background:#151515;
    border-radius:10px;
    overflow:hidden;
    transition:0.3s;
}

.product:hover{
    transform:scale(1.03);
}

.product img{
    width:100%;
    height:180px;
    object-fit:cover;
}

.info{
    padding:10px;
}

.price{
    color:#D4AF37;
    font-weight:bold;
}

button{
    width:100%;
    padding:10px;
    border:none;
    background:#D4AF37;
    color:#000;
    font-weight:bold;
    border-radius:5px;
    cursor:pointer;
}

/* CART */
.cart{
    position:fixed;
    bottom:20px;
    left:20px;
    background:#D4AF37;
    color:#000;
    padding:10px 15px;
    border-radius:20px;
}

/* WHATSAPP */
.whatsapp{
    position:fixed;
    right:15px;
    bottom:15px;
    width:60px;
    height:60px;
    background:#25D366;
    border-radius:50%;
    text-align:center;
    line-height:60px;
    font-size:28px;
    color:#fff;
    text-decoration:none;
}
</style>
</head>

<body>

<!-- LOADER -->
<div id="loader">
    <img src="logo png.png" alt="Logo">

    <h1>MM VISION HUB</h1>

    <p>Michael Maluleka Vision Hub</p>

    <p style="margin-top:15px;color:#aaa;">
        Loading your fashion store...
    </p>
</div>

<!-- MAIN -->
<div id="main">

<div class="topbar">
    <img src="logo png.png">
    <h1>MM VISION HUB</h1>
</div>

<div class="hero">
    <h2>NEW WOMEN'S COLLECTION</h2>
</div>

<input type="text" id="searchInput" placeholder="Search products..." onkeyup="searchProducts()">

<div class="gallery" id="gallery"></div>

<div class="cart">
🛒 Items: <span id="cartCount">0</span>
</div>

<a href="https://wa.me/27732176610" class="whatsapp">💬</a>

</div>

<script>

/* LOADER TIMER (6 SECONDS) */
setTimeout(()=>{
    document.getElementById("loader").style.display="none";
    document.getElementById("main").style.display="block";
},6000);

/* PRODUCTS */
let cart=0;
const gallery=document.getElementById("gallery");

for(let i=1;i<=80;i++){
    gallery.innerHTML+=`
    <div class="product">
        <img src="women${i}.png">
        <div class="info">
            <h3>Dress ${i}</h3>
            <p class="price">R150</p>

            <button onclick="buy(${i})">Buy Now</button>
        </div>
    </div>`;
}

function buy(i){
    cart++;
    document.getElementById("cartCount").innerText=cart;

    let msg="Hello MM VISION HUB, I want Dress "+i;
    window.open("https://wa.me/27732176610?text="+encodeURIComponent(msg));
}

/* SEARCH */
function searchProducts(){
    let input=document.getElementById("searchInput").value.toUpperCase();
    let products=document.getElementsByClassName("product");

    for(let i=0;i<products.length;i++){
        let title=products[i].getElementsByTagName("h3")[0];
        products[i].style.display=
        title.innerText.toUpperCase().includes(input)?"":"none";
    }
}

</script>

</body>
</html>
