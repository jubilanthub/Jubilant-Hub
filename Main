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
text-align:center;
}

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

#cartItems{
max-height:200px;
overflow:auto;
margin-top:10px;
font-size:12px;
}

.whatsapp-btn{
background:green;
color:white;
padding:10px;
display:block;
text-align:center;
text-decoration:none;
margin-top:10px;
border-radius:5px;
font-weight:bold;
}

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

<div id="loader">
<img src="logo png.png" alt="Logo">
<h1>Michael Maluleka Vision Hub</h1>
</div>

<div class="header">
<img src="logo png.png" class="logo">
<h1>MM VISION HUB</h1>
</div>

<input
type="text"
id="searchInput"
class="search-box"
placeholder="Search products..."
onkeyup="searchProducts()">

<div class="top-menu">

<button class="menu-btn" onclick="showSection('women')">
Women
</button>

<button class="menu-btn" onclick="showSection('sneakers')">
Sneakers
</button>

<button class="menu-btn" onclick="showSection('slippers')">
Slippers
</button>

<button class="menu-btn" onclick="showSection('bags')">
Bags
</button>

<button class="menu-btn" onclick="showSection('watches')">
Watches
</button>

<button class="menu-btn" onclick="showSection('tight')">
Women Tight
</button>

<button class="menu-btn" onclick="showSection('tracksuits')">
Tracksuits
</button>

<button class="menu-btn" onclick="showSection('led')">
LED Lights
</button>

<button class="menu-btn" onclick="showSection('menclothes')">
Men Clothes
</button>

<button class="menu-btn" onclick="showSection('womenclothes')">
Women Clothes
</button>

<button class="menu-btn" onclick="showSection('others')">
Others
</button>

<button class="menu-btn" onclick="toggleSection('delivery')">
Delivery
</button>

<button class="menu-btn" onclick="toggleSection('banking')">
Banking
</button>

<button class="menu-btn" onclick="toggleSection('about')">
About Us
</button>

<button class="menu-btn" onclick="toggleSection('terms')">
Terms
</button>

</div>

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

function createProduct(
container,
name,
image,
price='',
size='',
extra=''
){

const card = document.createElement('div');

card.className='product';

card.innerHTML=`
<img src="${image}" alt="${name}">
<div class="info">
<h3>${name}</h3>

${price ? `<p>Price: ${price}</p>` : ''}

${size ? `<p>Size: ${size}</p>` : ''}

${extra ? `<p>${extra}</p>` : ''}

<button class="cart-btn"
onclick="addToCart('${name}')">
Add To Cart
</button>

</div>
`;

container.appendChild(card);

}

/* WOMEN 1-80 */

const women =
document.getElementById('women');

for(let i=1;i<=80;i++){

createProduct(
women,
'Women '+i,
'women'+i+'.png',
'R150',
'Free Size'
);

}

/* SNEAKERS 1-30 */

const sneakers =
document.getElementById('sneakers');

for(let i=1;i<=30;i++){

let price='';

if(i<=6){
price='R350';
}

createProduct(
sneakers,
'Sneakers '+i,
'sneakers'+i+'.png',
price,
'Size 3 - 8',
'Any Colour Available / Not Available'
);

}

/* SLIPPERS */

const slippers =
document.getElementById('slippers');

for(let i=1;i<=30;i++){

let price='';

if(i<=6){
price='R160';
}

createProduct(
slippers,
'Slippers '+i,
'slippers'+i+'.png',
price,
'Free Size',
'Any Colour Available / Not Available'
);

}

/* BAGS */

const bags =
document.getElementById('bags');

for(let i=1;i<=30;i++){

let price='';

if(i===1) price='R110';
if(i===2) price='R250';
if(i===4) price='R90';

createProduct(
bags,
'Bag '+i,
'bag'+i+'.png',
price,
'',
'Any Colour Available / Not Available'
);

}

/* WATCHES */

const watches =
document.getElementById('watches');

for(let i=1;i<=30;i++){

let price='';

if(i===1) price='R60';
if(i===2) price='R230';

createProduct(
watches,
'Watch '+i,
'watch'+i+'.png',
price
);

}

/* WOMEN TIGHT */

const tight =
document.getElementById('tight');

for(let i=1;i<=5;i++){

let price='';

if(i===1){
price='R250 for 3';
}

if(i===2){
price='R200 for 3';
}

createProduct(
tight,
'Women Tight '+i,
'women tight'+i+'.png',
price,
'Free Size',
'Any Colour Available / Not Available'
);

}
/* TRACKSUITS */

const tracksuits =
document.getElementById('tracksuits');

for(let i=1;i<=60;i++){

createProduct(
tracksuits,
'Tracksuit '+i,
'tracksuit'+i+'.png',
'',
'Size S - XL',
'Any Colour Available / Not Available'
);

}

/* LED */

const led =
document.getElementById('led');

for(let i=1;i<=3;i++){

let price='';

if(i===1){
price='R130 (5 Metre)';
}

createProduct(
led,
'LED '+i,
'led'+i+'.png',
price
);

}

/* MEN CLOTHES */

const menclothes =
document.getElementById('menclothes');

for(let i=1;i<=100;i++){

createProduct(
menclothes,
'Men Clothes '+i,
'menclothes'+i+'.png',
'',
'Size S - XL',
'Any Colour Available / Not Available'
);

}

/* WOMEN CLOTHES */

const womenclothes =
document.getElementById('womenclothes');

for(let i=1;i<=100;i++){

createProduct(
womenclothes,
'Women Clothes '+i,
'womenclothes'+i+'.png',
'',
'Size S - XL',
'Any Colour Available / Not Available'
);

}

/* OTHERS */

const others =
document.getElementById('others');

for(let i=1;i<=50;i++){

createProduct(
others,
'Others '+i,
'others'+i+'.png'
);

}

/* SHOW CATEGORY */

function showSection(id){

document
.querySelectorAll('.section')
.forEach(section=>{

section.style.display='none';

});

document
.getElementById(id)
.style.display='grid';

}

/* CART */

function addToCart(item){

cart.push(item);

updateCart();

}

function updateCart(){

let list='';

cart.forEach(product=>{

list += product + '<br>';

});

document.getElementById('cartItems')
.innerHTML=list;

}

/* SEARCH */

function searchProducts(){

let input =
document.getElementById('searchInput')
.value
.toLowerCase();

let products =
document.querySelectorAll('.product');

products.forEach(product=>{

let text =
product.innerText.toLowerCase();

if(text.includes(input)){

product.style.display='block';

}else{

product.style.display='none';

}

});

}

/* INFO BOX */

function toggleSection(id){

let boxes =
document.querySelectorAll('.info-box');

boxes.forEach(box=>{

if(box.id===id){

box.style.display=
box.style.display==='block'
?'none'
:'block';

}else{

box.style.display='none';

}

});

}

/* LOADER */

window.onload=function(){

showSection('women');

setTimeout(function(){

document
.getElementById('loader')
.style.display='none';

},5000);

}

/* WHATSAPP */

function sendWhatsApp(){

let order='';

cart.forEach(item=>{

order += item + '%0A';

});

window.open(
'https://wa.me/27732176610?text=Hello%20MM%20Vision%20Hub,%20I%20want%20to%20order:%0A%0A'+order,
'_blank'
);

}

</script>

<div id="delivery" class="info-box">
<h2>Delivery Methods</h2>
<p>Mapela Area Delivery: R50</p>
<p>PAXI Standard: R110</p>
<p>PAXI Large: R140</p>
</div>

<div id="banking" class="info-box">
<h2>Banking Details</h2>
<p>Account Name: MR KM MALULEKA</p>
<p>Bank: CAPITEC</p>
<p>Account Number: 2189801660</p>
</div>

<div id="about" class="info-box">
<h2>About Us</h2>
<p>
Michael Maluleka Vision Hub offers affordable clothing,
sneakers, bags, watches, accessories and more.
</p>
</div>

<div id="terms" class="info-box">
<h2>Terms & Conditions</h2>
<p>Payment must be made before delivery.</p>
<p>Delivery fees are separate from product prices.</p>
<p>Product availability depends on stock.</p>
<p>Colours may differ from images.</p>
<p>No refunds after successful delivery.</p>
</div>

<div id="cart">

🛒 CART

<div id="cartItems"></div>

<button
class="cart-btn"
onclick="sendWhatsApp()">

Place Order On WhatsApp

</button>

</div>

<footer>
Michael Maluleka Vision Hub © 2026
</footer>

</body>
</html>
