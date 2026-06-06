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
margin-bottom:5px;
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

#cartItems{
max-height:200px;
overflow:auto;
margin-top:10px;
font-size:12px;
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
margin-bottom:10px;
}

/* FOOTER */
footer{
background:#111;
padding:20px;
text-align:center;
color:#D4AF37;
margin-top:30px;
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
<input type="text" id="searchInput" class="search-box" placeholder="Search products..." onkeyup="searchProducts()">

<!-- MENU -->
<div class="top-menu">

<button class="menu-btn" onclick="showSection('women')">Women</button>
<button class="menu-btn" onclick="showSection('sneakers')">Sneakers</button>
<button class="menu-btn" onclick="showSection('slippers')">Slippers</button>
<button class="menu-btn" onclick="showSection('bags')">Bags</button>
<button class="menu-btn" onclick="showSection('watches')">Watches</button>
<button class="menu-btn" onclick="showSection('tight')">Women Tight</button>
<button class="menu-btn" onclick="showSection('tracksuits')">Tracksuits</button>
<button class="menu-btn" onclick="showSection('led')">LED Lights</button>
<button class="menu-btn" onclick="showSection('menclothes')">Men Clothes</button>
<button class="menu-btn" onclick="showSection('womenclothes')">Women Clothes</button>
<button class="menu-btn" onclick="showSection('others')">Others</button>

<button class="menu-btn" onclick="toggleSection('delivery')">Delivery</button>
<button class="menu-btn" onclick="toggleSection('banking')">Payment Method</button>
<button class="menu-btn" onclick="toggleSection('about')">About Us</button>
<button class="menu-btn" onclick="toggleSection('terms')">Terms</button>

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
<script>

let cart = [];

/* CREATE PRODUCT CARD */
function createProduct(container, name, image, price = '', size = '', extra = '') {

const card = document.createElement('div');
card.className = 'product';

card.innerHTML = `
<img src="${image}" alt="${name}">
<div class="info">
<h3>${name}</h3>

${price ? `<p>Price: ${price}</p>` : ''}

${size ? `<p>Size: ${size}</p>` : ''}

${extra ? `<p>${extra}</p>` : ''}

<button class="cart-btn" onclick="addToCart('${name}')">
Add To Cart
</button>

</div>
`;

container.appendChild(card);
}

/* WOMEN (1–80) */
const women = document.getElementById('women');

for(let i = 1; i <= 80; i++){
createProduct(
women,
'Women ' + i,
'women' + i + '.png',
'R150',
'Free Size'
);
}

/* SNEAKERS (1–30) */
const sneakers = document.getElementById('sneakers');

for(let i = 1; i <= 30; i++){

let price = '';
if(i <= 6){
price = 'R350';
}

createProduct(
sneakers,
'Sneakers ' + i,
'sneakers' + i + '.png',
price,
'Size 3 - 8',
'Any Colour Available / Not Available'
);
}

/* SLIPPERS (1–30) */
const slippers = document.getElementById('slippers');

for(let i = 1; i <= 30; i++){

let price = '';
if(i <= 6){
price = 'R160';
}

createProduct(
slippers,
'Slippers ' + i,
'slippers' + i + '.png',
price,
'Free Size',
'Any Colour Available / Not Available'
);
}

/* BAGS (1–30) */
const bags = document.getElementById('bags');

for(let i = 1; i <= 30; i++){

let price = '';
if(i === 1) price = 'R110';
if(i === 2) price = 'R250';
if(i === 4) price = 'R90';

createProduct(
bags,
'Bag ' + i,
'bag' + i + '.png',
price,
'',
'Any Colour Available / Not Available'
);
}

/* WATCHES (1–30) */
const watches = document.getElementById('watches');

for(let i = 1; i <= 30; i++){

let price = '';
if(i === 1) price = 'R60';
if(i === 2) price = 'R230';

createProduct(
watches,
'Watch ' + i,
'watch' + i + '.png',
price
);
}

/* WOMEN TIGHT (1–5) */
const tight = document.getElementById('tight');

for(let i = 1; i <= 5; i++){

let price = '';
if(i === 1) price = 'R250 for 3';
if(i === 2) price = 'R200 for 3';

createProduct(
tight,
'Women Tight ' + i,
'women tight' + i + '.png',
price,
'Free Size',
'Any Colour Available / Not Available'
);
}

/* TRACKSUITS (1–60) */
const tracksuits = document.getElementById('tracksuits');

for(let i = 1; i <= 60; i++){
createProduct(
tracksuits,
'Tracksuit ' + i,
'tracksuit' + i + '.png',
'',
'Size S - XL',
'Any Colour Available / Not Available'
);
}

/* LED (1–3) */
const led = document.getElementById('led');

for(let i = 1; i <= 3; i++){

let price = '';
if(i === 1){
price = 'R130 (5 Metre)';
}

createProduct(
led,
'LED ' + i,
'led' + i + '.png',
price
);
}

/* MEN CLOTHES (1–100) */
const menclothes = document.getElementById('menclothes');

for(let i = 1; i <= 100; i++){
createProduct(
menclothes,
'Men Clothes ' + i,
'menclothes' + i + '.png',
'',
'Size S - XL',
'Any Colour Available / Not Available'
);
}

/* WOMEN CLOTHES (1–100) */
const womenclothes = document.getElementById('womenclothes');

for(let i = 1; i <= 100; i++){
createProduct(
womenclothes,
'Women Clothes ' + i,
'womenclothes' + i + '.png',
'',
'Size S - XL',
'Any Colour Available / Not Available'
);
}

/* OTHERS (1–50) */
const others = document.getElementById('others');

for(let i = 1; i <= 50; i++){
createProduct(
others,
'Others ' + i,
'others' + i + '.png'
);
}

/* SHOW SECTION */
function showSection(id){

document.querySelectorAll('.section').forEach(sec => {
sec.style.display = 'none';
});

document.getElementById(id).style.display = 'grid';
}

/* ADD TO CART */
function addToCart(item){
cart.push(item);
updateCart();
}

/* UPDATE CART */
function updateCart(){
let list = '';

cart.forEach(p => {
list += p + '<br>';
});

document.getElementById('cartItems').innerHTML = list;
}

/* SEARCH */
function searchProducts(){

let input = document.getElementById('searchInput').value.toLowerCase();
let products = document.querySelectorAll('.product');

products.forEach(p => {

let text = p.innerText.toLowerCase();

if(text.includes(input)){
p.style.display = 'block';
}else{
p.style.display = 'none';
}

});

}

/* TOGGLE INFO BOX */
function toggleSection(id){

let boxes = document.querySelectorAll('.info-box');

boxes.forEach(box => {
if(box.id === id){
box.style.display = box.style.display === 'block' ? 'none' : 'block';
}else{
box.style.display = 'none';
}
});

}

/* ON LOAD */
window.onload = function(){

showSection('women');

setTimeout(() => {
document.getElementById('loader').style.display = 'none';
}, 5000);

}

/* WHATSAPP ORDER */
function sendWhatsApp(){

let order = '';

cart.forEach(item => {
order += item + '%0A';
});

window.open(
'https://wa.me/27732176610?text=Hello%20MM%20Vision%20Hub%20Order:%0A%0A' + order,
'_blank'
);

}

</script>
<!-- DELIVERY -->
<div id="delivery" class="info-box">
<h2>Delivery Methods</h2>

<p><strong>Around Mapela Delivery:</strong> R50</p>

<p><strong>PAXI Delivery Options:</strong></p>
<p>Standard Plastic: R110</p>
<p>Large Plastic: R140</p>

</div>

<!-- PAYMENT METHOD -->
<div id="banking" class="info-box">
<h2>Payment Method</h2>

<p><strong>Account Name:</strong> MR KM MALULEKA</p>
<p><strong>Bank:</strong> CAPITEC</p>
<p><strong>Account Number:</strong> 2189801660</p>

<br>

<p>Please send proof of payment on WhatsApp after payment.</p>

<p style="color:red; font-weight:bold;">
⚠ Be aware of scams. Only use official MM Vision Hub banking details.
</p>

</div>

<!-- ABOUT US -->
<div id="about" class="info-box">
<h2>About Us</h2>

<p>
Michael Maluleka Vision Hub is an online store offering affordable
fashion items including sneakers, clothes, bags, watches, LED lights
and accessories.
</p>

<p>
We focus on providing quality products at low prices with reliable
service and safe delivery options.
</p>

<p>
Customer satisfaction is our priority.
</p>

</div>

<!-- TERMS & CONDITIONS -->
<div id="terms" class="info-box">
<h2>Terms & Conditions</h2>

<p>1. Payment must be made before delivery.</p>

<p>2. Send proof of payment via WhatsApp after payment.</p>

<p>3. Delivery fees are charged separately from product prices.</p>

<p>4. Delivery prices:</p>
<ul>
<li>Around Mapela: R50</li>
<li>PAXI Standard Plastic: R110</li>
<li>PAXI Large Plastic: R140</li>
</ul>

<p>5. Stock availability is not guaranteed for all items.</p>

<p>6. Colours and designs may slightly differ from images.</p>

<p>7. Customers must confirm payment details before sending money.</p>

<p>8. No refunds after successful delivery unless agreed otherwise.</p>

<p style="color:red; font-weight:bold;">
⚠ Beware of scam accounts pretending to be MM Vision Hub.
</p>

</div>
