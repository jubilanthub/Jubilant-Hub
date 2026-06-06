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

/* LOADER */
#loader{
position:fixed;
top:0;
left:0;
width:100%;
height:100%;
background:#000;
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
z-index:9999;
}

#loader img{
width:200px;
margin-bottom:20px;
}

#loader h1{
color:#D4AF37;
}

/* HEADER */
.header{
text-align:center;
padding:20px;
}

.logo{
width:120px;
display:block;
margin:auto;
margin-bottom:10px;
}

.header h1{
color:#D4AF37;
}

/* SEARCH */
.search-box{
width:90%;
max-width:500px;
margin:20px auto;
display:block;
padding:12px;
border-radius:10px;
border:none;
font-size:16px;
}

/* MENU */
.top-menu{
display:flex;
flex-wrap:wrap;
justify-content:center;
gap:10px;
padding:10px;
}

.menu-btn{
background:#D4AF37;
color:#000;
border:none;
padding:10px 15px;
border-radius:8px;
font-weight:bold;
cursor:pointer;
}

/* PRODUCT GRID */
.section{
display:none;
}

.gallery{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
gap:15px;
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
height:250px;
object-fit:cover;
}

.info{
padding:10px;
text-align:center;
}

.info h3{
color:#D4AF37;
}

.cart-btn{
background:#D4AF37;
color:#000;
border:none;
padding:10px;
width:100%;
font-weight:bold;
cursor:pointer;
}

/* INFO BOX */
.info-box{
display:none;
background:#111;
border:1px solid #D4AF37;
padding:20px;
margin:20px;
border-radius:10px;
}

.info-box h2{
color:#D4AF37;
}

/* FOOTER */
footer{
background:#111;
padding:20px;
text-align:center;
color:#D4AF37;
margin-top:30px;
}

/* CART */
#cart{
position:fixed;
right:10px;
bottom:10px;
background:#D4AF37;
color:#000;
padding:15px;
border-radius:10px;
font-weight:bold;
z-index:999;
max-width:220px;
}

#orderBox{
position:fixed;
right:10px;
bottom:140px;
background:#25D366;
padding:12px;
border-radius:10px;
z-index:999;
}

#payBox{
position:fixed;
right:10px;
bottom:210px;
background:#1e90ff;
padding:12px;
border-radius:10px;
z-index:999;
}

#cartItems{
max-height:200px;
overflow:auto;
font-size:12px;
margin-top:10px;
}

#totalPrice{
margin-top:10px;
font-weight:bold;
}

</style>
</head>

<body>

<!-- LOADER -->
<div id="loader">
<img src="logo png.png">
<h1>Michael Maluleka Vision Hub</h1>
</div>

<!-- HEADER -->
<div class="header">
<img src="logo png.png" class="logo">
<h1>MM VISION HUB</h1>
</div>

<!-- SEARCH -->
<input type="text" id="searchInput" class="search-box"
placeholder="Search products..." onkeyup="searchProducts()">

<!-- TOP TEXT ONLY (NO BUTTONS) -->
<div style="text-align:center;color:#D4AF37;font-weight:bold;padding:10px;">
Delivery Methods | Payment Method | About Us | Terms & Conditions
</div>

<!-- MENU -->
<div class="top-menu">

<button class="menu-btn" onclick="openCategory('women', loadWomen)">Women</button>
<button class="menu-btn" onclick="openCategory('sneakers', loadSneakers)">Sneakers</button>
<button class="menu-btn" onclick="openCategory('slippers', loadSlippers)">Slippers</button>
<button class="menu-btn" onclick="openCategory('bags', loadBags)">Bags</button>
<button class="menu-btn" onclick="openCategory('watches', loadWatches)">Watches</button>
<button class="menu-btn" onclick="openCategory('tight', loadTight)">Women Tight</button>
<button class="menu-btn" onclick="openCategory('tracksuits', loadTracksuits)">Tracksuits</button>
<button class="menu-btn" onclick="openCategory('led', loadLED)">LED Lights</button>
<button class="menu-btn" onclick="openCategory('menclothes', loadMen)">Men Clothes</button>
<button class="menu-btn" onclick="openCategory('womenclothes', loadWomenClothes)">Women Clothes</button>
<button class="menu-btn" onclick="openCategory('others', loadOthers)">Others</button>

</div>

<!-- PRODUCT SECTIONS -->
<div id="women" class="section gallery"></div>
<div id="sneakers" class="section gallery"></div>
<div id="slippers" class="section gallery"></div>
<div id="bags" class="section gallery"></div>
<div id="watches" class="section gallery"></div>
<div id="tight" class="section gallery"></div>
<div id="tracksuits" class="section gallery"></div>
<div id="led" class="section gallery"></div>
<div id="menclothes" class="section gallery"></div>
<div id="womenclothes" class="section gallery"></div>
<div id="others" class="section gallery"></div>

<!-- INFO BOXES -->
<div id="delivery" class="info-box">
<h2>Delivery Methods</h2>
<p>Around Mapela: R50</p>
<p>PAXI Standard: R110</p>
<p>PAXI Large: R140</p>
</div>

<div id="banking" class="info-box">
<h2>Payment Method</h2>
<p>MR KM MALULEKA</p>
<p>CAPITEC</p>
<p>2189801660</p>
</div>

<div id="about" class="info-box">
<h2>About Us</h2>
<p>Affordable fashion store: clothes, sneakers, bags, watches & more.</p>
</div>

<div id="terms" class="info-box">
<h2>Terms & Conditions</h2>
<p>Payment before delivery. No refunds after delivery.</p>
</div>

<!-- CART -->
<div id="cart">
<div id="cartItems"></div>
<div id="totalPrice">Total: R0</div>
</div>

<!-- ORDER BUTTON -->
<div id="orderBox">
<button onclick="sendWhatsApp()" class="cart-btn">Place Order</button>
</div>

<!-- PAY BUTTON -->
<div id="payBox">
<button onclick="capitecPay()" class="cart-btn" style="background:#1e90ff;color:white;">
Pay at Capitec
</button>
</div>

<script>

let cart = [];
let loaded = {};

/* CATEGORY */
function openCategory(id, loaderFn){
document.querySelectorAll(".section").forEach(s=>{
s.style.display = "none";
});

let box = document.getElementById(id);
box.style.display = "grid";

if(!loaded[id]){
loaderFn(box);
loaded[id] = true;
}
}

/* PRODUCT */
function createProduct(container, name, image, price='', size='', extra=''){

let card = document.createElement("div");
card.className = "product";

card.innerHTML = `
<img src="${image}">
<div class="info">
<h3>${name}</h3>
${price?`<p>${price}</p>`:''}
${size?`<p>${size}</p>`:''}
${extra?`<p>${extra}</p>`:''}
<button class="cart-btn" onclick="addToCart('${name}','${price}')">
Add To Cart
</button>
</div>
`;

container.appendChild(card);
}

/* ADD TO CART */
function addToCart(name, price){
cart.push(name + " " + price);
updateCart();
}

/* UPDATE CART */
function updateCart(){
document.getElementById("cartItems").innerHTML = cart.join("<br>");

let total = 0;
cart.forEach(i=>{
let match = i.match(/R(\d+)/);
if(match) total += parseInt(match[1]);
});

document.getElementById("totalPrice").innerText = "Total: R" + total;
}

/* SEARCH */
function searchProducts(){
let input = document.getElementById("searchInput").value.toLowerCase();

document.querySelectorAll(".product").forEach(p=>{
p.style.display = p.innerText.toLowerCase().includes(input) ? "block" : "none";
});
}

/* WHATSAPP ORDER */
function sendWhatsApp(){
let order = "";

cart.forEach(i=>{
order += i + "%0A";
});

window.open(
"https://wa.me/27732176610?text=Hello%20MM%20Vision%20Hub%20Order:%0A%0A" + order,
"_blank"
);
}

/* CAPITEC PAYMENT */
function capitecPay(){
let total = 0;

cart.forEach(i=>{
let match = i.match(/R(\d+)/);
if(match) total += parseInt(match[1]);
});

window.open(
"https://wa.me/27732176610?text=Pay%20MR%20KM%20MALULEKA%20Capitec%202189801660%20Total%20R"+total,
"_blank"
);
}

/* START */
window.onload = function(){
document.getElementById("women").style.display = "grid";
setTimeout(()=>{
document.getElementById("loader").style.display = "none";
},2000);
}

</script>

</body>
</html>
