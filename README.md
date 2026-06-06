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

/* SPEED FIX */
.product img{
loading:lazy;
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

<button class="menu-btn" onclick="toggleSection('delivery')">Delivery</button>
<button class="menu-btn" onclick="toggleSection('banking')">Payment Method</button>
<button class="menu-btn" onclick="toggleSection('about')">About Us</button>
<button class="menu-btn" onclick="toggleSection('terms')">Terms</button>

</div>

<!-- PRODUCT SECTIONS (EMPTY FIRST = FAST LOAD) -->
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
<p style="color:red;font-weight:bold;">
Send proof of payment on WhatsApp. Beware of scams.
</p>
</div>

<div id="about" class="info-box">
<h2>About Us</h2>
<p>Affordable fashion store: clothes, sneakers, bags, watches & more.</p>
</div>

<div id="terms" class="info-box">
<h2>Terms & Conditions</h2>
<p>Payment before delivery. No refunds after delivery.</p>
</div>
<script>

let cart = [];
let loaded = {};

/* ================= OPEN CATEGORY (FAST SYSTEM) ================= */
function openCategory(id, loaderFn){

document.querySelectorAll(".section").forEach(s=>{
s.style.display = "none";
});

let box = document.getElementById(id);
box.style.display = "grid";

/* load only once */
if(!loaded[id]){
loaderFn(box);
loaded[id] = true;
}

}

/* ================= CREATE PRODUCT ================= */
function createProduct(container, name, image, price='', size='', extra=''){

let card = document.createElement("div");
card.className = "product";

card.innerHTML = `
<img src="${image}" alt="${name}" loading="lazy">
<div class="info">
<h3>${name}</h3>
${price?`<p>${price}</p>`:''}
${size?`<p>${size}</p>`:''}
${extra?`<p>${extra}</p>`:''}
<button class="cart-btn" onclick="addToCart('${name} ${price}')">
Add To Cart
</button>
</div>
`;

container.appendChild(card);
}

/* ================= LOAD PRODUCTS (ONLY WHEN CLICKED) ================= */

/* WOMEN */
function loadWomen(box){
for(let i=1;i<=80;i++){
createProduct(box,"Women "+i,"women"+i+".png","R150","Free Size");
}
}

/* SNEAKERS */
function loadSneakers(box){
for(let i=1;i<=30;i++){
let price = i<=6 ? "R350" : "";
createProduct(box,"Sneakers "+i,"sneakers"+i+".png",price,"Size 3 - 8");
}
}

/* SLIPPERS */
function loadSlippers(box){
for(let i=1;i<=30;i++){
let price = i<=6 ? "R160" : "";
createProduct(box,"Slippers "+i,"slippers"+i+".png",price,"Free Size");
}
}

/* BAGS */
function loadBags(box){
for(let i=1;i<=30;i++){
let price="";
if(i===1) price="R110";
if(i===2) price="R250";
if(i===4) price="R90";

createProduct(box,"Bag "+i,"bag"+i+".png",price);
}
}

/* WATCHES */
function loadWatches(box){
for(let i=1;i<=30;i++){
let price="";
if(i===1) price="R60";
if(i===2) price="R230";

createProduct(box,"Watch "+i,"watch"+i+".png",price);
}
}

/* WOMEN TIGHT */
function loadTight(box){
for(let i=1;i<=5;i++){
let price="";
if(i===1) price="R250 for 3";
if(i===2) price="R200 for 3";

createProduct(box,"Women Tight "+i,"women tight"+i+".png",price);
}
}

/* TRACKSUITS */
function loadTracksuits(box){
for(let i=1;i<=60;i++){
createProduct(box,"Tracksuit "+i,"tracksuit"+i+".png","","Size S - XL");
}
}

/* LED */
function loadLED(box){
for(let i=1;i<=3;i++){
let price="";
if(i===1) price="R130 (5 Metre)";

createProduct(box,"LED "+i,"led"+i+".png",price);
}
}

/* MEN CLOTHES */
function loadMen(box){
for(let i=1;i<=100;i++){
createProduct(box,"Men Clothes "+i,"menclothes"+i+".png","","Size S - XL");
}
}

/* WOMEN CLOTHES */
function loadWomenClothes(box){
for(let i=1;i<=100;i++){
createProduct(box,"Women Clothes "+i,"womenclothes"+i+".png","","Size S - XL");
}
}

/* OTHERS */
function loadOthers(box){
for(let i=1;i<=50;i++){
createProduct(box,"Others "+i,"others"+i+".png");
}
}

/* ================= CART ================= */
function addToCart(item){
cart.push(item);
updateCart();
}

function updateCart(){
document.getElementById("cartItems").innerHTML = cart.join("<br>");
calculateTotal();
}

/* ================= TOTAL ================= */
function calculateTotal(){

let total = 0;

cart.forEach(item=>{
let match = item.match(/R(\d+)/);
if(match){
total += parseInt(match[1]);
}
});

document.getElementById("totalPrice").innerText = "Total: R" + total;

return total;
}

/* ================= SEARCH ================= */
function searchProducts(){

let input = document.getElementById("searchInput").value.toLowerCase();

document.querySelectorAll(".product").forEach(p=>{
p.style.display = p.innerText.toLowerCase().includes(input) ? "block" : "none";
});

}

/* ================= TOGGLE INFO ================= */
function toggleSection(id){

document.querySelectorAll(".info-box").forEach(box=>{
box.style.display = (box.id === id)
? (box.style.display === "block" ? "none" : "block")
: "none";
});

}

/* ================= WHATSAPP ================= */
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

/* ================= CAPITEC PAY ================= */
function capitecPay(){

let total = calculateTotal();

window.open(
"https://wa.me/27732176610?text=Pay%20MR%20KM%20MALULEKA%20Capitec%202189801660%20Total%20R"+total,
"_blank"
);

}

/* ================= START ================= */
window.onload = function(){
document.getElementById("women").style.display = "grid";
loaded["women"] = false;

setTimeout(()=>{
document.getElementById("loader").style.display = "none";
},2000);
}

</script>
