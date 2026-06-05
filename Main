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
color:white;
}

/* LOADER */

#loader{
position:fixed;
width:100%;
height:100vh;
background:black;
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
z-index:9999;
}

#loader img{
width:180px;
animation:pulse 1.5s infinite;
}

#loader h1{
color:#D4AF37;
margin-top:20px;
}

@keyframes pulse{
0%{transform:scale(1);}
50%{transform:scale(1.1);}
100%{transform:scale(1);}
}

#main{
display:none;
}

/* TOP INFO */

.topinfo{
background:#111;
padding:15px;
text-align:center;
border-bottom:2px solid #D4AF37;
}

.topinfo h2{
color:#D4AF37;
margin-bottom:10px;
}

.topbar{
position:sticky;
top:0;
background:#111;
padding:10px;
display:flex;
justify-content:space-between;
align-items:center;
border-bottom:2px solid #D4AF37;
z-index:1000;
}

.topbar img{
width:55px;
}

.topbar h1{
color:#D4AF37;
font-size:18px;
}

.hero{
padding:30px;
text-align:center;
}

.hero h2{
color:#D4AF37;
font-size:30px;
}

#searchInput{
width:90%;
display:block;
margin:20px auto;
padding:14px;
border:none;
border-radius:30px;
font-size:16px;
}

/* GALLERY */

.gallery{
display:grid;
grid-template-columns:repeat(2,1fr);
gap:12px;
padding:12px;
}

.product{
background:#151515;
border-radius:10px;
overflow:hidden;
transition:.3s;
}

.product:hover{
transform:scale(1.03);
}

.product img{
width:100%;
height:220px;
object-fit:cover;
}

.info{
padding:10px;
}

.price{
color:#D4AF37;
font-weight:bold;
margin:8px 0;
}

button{
width:100%;
padding:10px;
background:#D4AF37;
border:none;
font-weight:bold;
border-radius:5px;
cursor:pointer;
}

.category-title{
text-align:center;
color:#D4AF37;
margin-top:30px;
font-size:26px;
}

/* CART */

.cart{
position:fixed;
left:15px;
bottom:15px;
background:#D4AF37;
color:black;
padding:12px;
border-radius:25px;
font-weight:bold;
}

.whatsapp{
position:fixed;
right:15px;
bottom:15px;
width:60px;
height:60px;
background:#25D366;
border-radius:50%;
display:flex;
align-items:center;
justify-content:center;
font-size:30px;
text-decoration:none;
color:white;
}

#cartPanel{
background:#111;
margin:20px;
padding:20px;
border-radius:10px;
border:1px solid #D4AF37;
}

#cartPanel h2{
color:#D4AF37;
margin-bottom:10px;
}

</style>
</head>
<body>

<div id="loader">
<img src="logo png.png">
<h1>MM VISION HUB</h1>
<p>Michael Maluleka Vision Hub</p>
</div>

<div id="main">

<div class="topinfo">

<h2>Banking Details</h2>

<p>
MR KM MALULEKA<br>
CAPITEC<br>
2189801660
</p>

<br>

<p>
<b>About Us:</b><br>
MM Vision Hub offers affordable fashion,
sneakers, bags and accessories delivered nationwide.
</p>

<br>

<p>
<b>Terms & Conditions:</b><br>
Payment before delivery.
Proof of payment required.
Delivery 3-5 working days.
</p>

</div>

<div class="topbar">
<img src="logo png.png">
<h1>MM VISION HUB</h1>
</div>

<div class="hero">
<h2>WELCOME TO MM VISION HUB</h2>
</div>

<input
type="text"
id="searchInput"
placeholder="Search Products..."
onkeyup="searchProducts()"
>

<h2 class="category-title">Women's Dresses</h2>
<div class="gallery" id="dressGallery"></div>

<h2 class="category-title">Slippers</h2>
<div class="gallery" id="slippersGallery"></div>

<h2 class="category-title">Sneakers</h2>
<div class="gallery" id="sneakersGallery"></div>

<h2 class="category-title">Bags</h2>
<div class="gallery" id="bagsGallery"></div>

<div id="cartPanel">
<h2>Shopping Cart</h2>
<div id="cartItems"></div>

<h3>
Total: R<span id="totalPrice">0</span>
</h3>

<button onclick="checkoutWhatsApp()">
Checkout On WhatsApp
</button>
</div>

<div class="cart">
🛒 <span id="cartCount">0</span>
</div>

<a
href="https://wa.me/27732176610"
class="whatsapp">
💬
</a>
<script>

setTimeout(()=>{
document.getElementById("loader").style.display="none";
document.getElementById("main").style.display="block";
},6000);

let cart = [];
let total = 0;

const dressGallery =
document.getElementById("dressGallery");

const slippersGallery =
document.getElementById("slippersGallery");

const sneakersGallery =
document.getElementById("sneakersGallery");

const bagsGallery =
document.getElementById("bagsGallery");

/* ==========================
DRESSES
women1.png - women80.png
========================== */

for(let i=1;i<=80;i++){

dressGallery.innerHTML += `

<div class="product">

<img src="women${i}.png">

<div class="info">

<h3>Dress ${i}</h3>

<p class="price">
R150
</p>

<button
onclick="addToCart(
'Dress ${i}',
150
)">
Add To Cart
</button>

</div>

</div>

`;

}

/* ==========================
SLIPPERS
slipers1.png - slipers6.png
========================== */

for(let i=1;i<=6;i++){

slippersGallery.innerHTML += `

<div class="product">

<img src="slipers${i}.png">

<div class="info">

<h3>Slippers ${i}</h3>

<p class="price">
R120
</p>

<button
onclick="addToCart(
'Slippers ${i}',
120
)">
Add To Cart
</button>

</div>

</div>

`;

}

/* ==========================
SNEAKERS
sneakers1.png - sneakers30.png
========================== */

for(let i=1;i<=30;i++){

sneakersGallery.innerHTML += `

<div class="product">

<img src="sneakers${i}.png">

<div class="info">

<h3>Sneakers ${i}</h3>

<p class="price">
R350
</p>

<button
onclick="addToCart(
'Sneakers ${i}',
350
)">
Add To Cart
</button>

</div>

</div>

`;

}
/* ==========================
BAGS
bag1.png - bag30.png
========================== */

for(let i=1;i<=30;i++){

bagsGallery.innerHTML += `

<div class="product">

<img src="bag${i}.png">

<div class="info">

<h3>Bag ${i}</h3>

<p class="price">
R250
</p>

<button
onclick="addToCart(
'Bag ${i}',
250
)">
Add To Cart
</button>

</div>

</div>

`;

}

/* ==========================
ADD TO CART
========================== */

function addToCart(product,price){

cart.push({
name:product,
price:price
});

total += price;

updateCart();

}

/* ==========================
UPDATE CART
========================== */

function updateCart(){

document.getElementById(
"cartCount"
).innerText = cart.length;

let html = "";

cart.forEach((item,index)=>{

html += `

<p style="
margin:8px 0;
padding:8px;
border-bottom:1px solid #333;
">

${item.name}
-
R${item.price}

<button
style="
width:auto;
padding:5px 10px;
margin-left:10px;
"
onclick="removeItem(${index})">

❌

</button>

</p>

`;

});

document.getElementById(
"cartItems"
).innerHTML = html;

document.getElementById(
"totalPrice"
).innerText = total;

}

/* ==========================
REMOVE ITEM
========================== */

function removeItem(index){

total -= cart[index].price;

cart.splice(index,1);

updateCart();

}
/* ==========================
WHATSAPP CHECKOUT
========================== */

function checkoutWhatsApp(){

if(cart.length===0){

alert(
"Your cart is empty."
);

return;

}

let msg =
"Hello MM VISION HUB,%0A%0A";

msg +=
"I would like to order:%0A%0A";

cart.forEach(item=>{

msg +=
"• " +
item.name +
" - R" +
item.price +
"%0A";

});

msg +=
"%0A--------------------%0A";

msg +=
"TOTAL: R" +
total;

msg +=
"%0A%0APlease send banking details.";

window.open(
"https://wa.me/27732176610?text=" +
msg
);

}

/* ==========================
SEARCH PRODUCTS
========================== */

function searchProducts(){

let input =
document
.getElementById(
"searchInput"
)
.value
.toUpperCase();

let products =
document.getElementsByClassName(
"product"
);

for(
let i=0;
i<products.length;
i++
){

let title =
products[i]
.getElementsByTagName(
"h3"
)[0];

if(
title.innerText
.toUpperCase()
.includes(input)
){

products[i]
.style
.display="block";

}else{

products[i]
.style
.display="none";

}

}

}

</script>

</div>

</body>
</html>
