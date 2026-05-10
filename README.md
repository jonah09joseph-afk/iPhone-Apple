<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Deutsche iPhones Store</title>

<style>
body{
margin:0;
font-family:Arial;
background:#0f0f0f;
color:white;
display:none;
}

/* LOADER */
#loader{
position:fixed;
width:100%;
height:100%;
background:black;
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
color:gold;
z-index:9999;
}
.spinner{
width:60px;height:60px;
border:6px solid #333;
border-top:6px solid gold;
border-radius:50%;
animation:spin 1s linear infinite;
}
@keyframes spin{100%{transform:rotate(360deg);}}

/* HEADER */
header{
background:linear-gradient(90deg,#b8860b,#ffd700);
padding:15px;
text-align:center;
font-size:22px;
font-weight:bold;
}

/* TOP BAR */
.topbar{
display:flex;
justify-content:space-between;
padding:10px;
}

/* CARD */
.container{padding:15px;}

.card{
background:#1c1c1c;
padding:15px;
margin:15px 0;
border-radius:12px;
text-align:center;
}

.card img{
width:100%;
max-width:250px;
border-radius:10px;
}

.btn{
background:gold;
color:black;
padding:10px;
display:block;
margin-top:10px;
border-radius:8px;
text-decoration:none;
font-weight:bold;
}

/* CART */
.cart{
position:fixed;
bottom:10px;
right:10px;
background:gold;
color:black;
padding:10px;
border-radius:10px;
font-weight:bold;
cursor:pointer;
}

/* TRUST */
.trust{
display:flex;
justify-content:space-around;
font-size:12px;
color:#ccc;
padding:10px;
background:#111;
}

/* REVIEWS */
.reviews{
background:#111;
padding:10px;
margin:15px;
border-radius:10px;
font-size:13px;
}
</style>
</head>

<body>

<!-- LOADER -->
<div id="loader">
<div class="spinner"></div>
Loading Store...
</div>

<header>🇩🇪 Deutsche iPhones Store</header>

<!-- TRUST BAR -->
<div class="trust">
<span>🔒 Secure</span>
<span>🚚 Fast Delivery</span>
<span>⭐ Trusted</span>
</div>

<!-- TOP -->
<div class="topbar">
<select onchange="setCurrency(this.value)">
<option value="EUR">€ EUR</option>
<option value="USD">$ USD</option>
<option value="NGN">₦ NGN</option>
</select>

<button onclick="viewCart()">🛒 Cart (<span id="count">0</span>)</button>
</div>

<div class="container">

<!-- PRODUCTS -->

<div class="card">
<img src="https://images.unsplash.com/photo-1695048133142-4b7f5c6e7f6b?auto=format&fit=crop&w=600&q=80">
<h2>iPhone 15 Pro Max</h2>
<p id="p1">€999</p>
<button class="btn" onclick="add('iPhone 15 Pro Max',999)">Add to Cart</button>
<a class="btn" href="https://wa.me/2347072331657?text=I%20want%20iPhone%2015%20Pro%20Max">Buy on WhatsApp Business</a>
</div>

<div class="card">
<img src="https://images.unsplash.com/photo-1664478546381-3d6b0f4a0c2f?auto=format&fit=crop&w=600&q=80">
<h2>iPhone 14 Pro</h2>
<p id="p2">€799</p>
<button class="btn" onclick="add('iPhone 14 Pro',799)">Add to Cart</button>
<a class="btn" href="https://wa.me/2347072331657?text=I%20want%20iPhone%2014%20Pro">Buy on WhatsApp Business</a>
</div>

<div class="card">
<h2>📦 Payment</h2>
<a class="btn" href="https://flutterwave.com/pay/YOUR_LINK">Pay Card / Bank / Mobile 💳</a>
<a class="btn" href="https://www.paypal.me/YOUR_USERNAME">PayPal 🌍</a>
</div>

<!-- REVIEWS -->
<div class="reviews">
⭐ “Very fast delivery, legit seller” — David<br><br>
⭐ “Phone came exactly as described” — Sarah<br><br>
⭐ “Trusted WhatsApp seller” — John
</div>

</div>

<!-- CART -->
<div class="cart" onclick="viewCart()">🛒 Cart</div>

<script>

window.onload=function(){
setTimeout(()=>{
document.getElementById("loader").style.display="none";
document.body.style.display="block";
},2000);
};

/* CART */
let cart=[];
let total=0;
let currency="EUR";

function add(name,price){
cart.push(name);
total+=price;
document.getElementById("count").innerText=cart.length;
update();
}

function update(){
document.getElementById("p1").innerText=getSymbol()+999;
document.getElementById("p2").innerText=getSymbol()+799;
}

/* VIEW CART */
function viewCart(){
alert(cart.length?cart.join("\n"):"Cart empty");
}

/* CURRENCY */
function setCurrency(v){
currency=v;
update();
}

function getSymbol(){
return currency==="EUR"?"€":currency==="USD"?"$":"₦";
}

</script>

</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Deutsche iPhones Store</title>

<style>
body{
margin:0;
font-family:Arial;
background:#0f0f0f;
color:white;
display:none;
}

/* LOADER */
#loader{
position:fixed;
width:100%;
height:100%;
background:black;
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
color:gold;
z-index:9999;
}
.spinner{
width:60px;height:60px;
border:6px solid #333;
border-top:6px solid gold;
border-radius:50%;
animation:spin 1s linear infinite;
}
@keyframes spin{100%{transform:rotate(360deg);}}

/* HEADER */
header{
background:linear-gradient(90deg,#b8860b,#ffd700);
padding:15px;
text-align:center;
font-size:22px;
font-weight:bold;
}

/* TOP BAR */
.topbar{
display:flex;
justify-content:space-between;
padding:10px;
}

/* CARD */
.container{padding:15px;}

.card{
background:#1c1c1c;
padding:15px;
margin:15px 0;
border-radius:12px;
text-align:center;
}

.card img{
width:100%;
max-width:250px;
border-radius:10px;
}

.btn{
background:gold;
color:black;
padding:10px;
display:block;
margin-top:10px;
border-radius:8px;
text-decoration:none;
font-weight:bold;
}

/* CART */
.cart{
position:fixed;
bottom:10px;
right:10px;
background:gold;
color:black;
padding:10px;
border-radius:10px;
font-weight:bold;
cursor:pointer;
}

/* TRUST */
.trust{
display:flex;
justify-content:space-around;
font-size:12px;
color:#ccc;
padding:10px;
background:#111;
}

/* REVIEWS */
.reviews{
background:#111;
padding:10px;
margin:15px;
border-radius:10px;
font-size:13px;
}
</style>
</head>

<body>

<!-- LOADER -->
<div id="loader">
<div class="spinner"></div>
Loading Store...
</div>

<header>🇩🇪 Deutsche iPhones Store</header>

<!-- TRUST BAR -->
<div class="trust">
<span>🔒 Secure</span>
<span>🚚 Fast Delivery</span>
<span>⭐ Trusted</span>
</div>

<!-- TOP -->
<div class="topbar">
<select onchange="setCurrency(this.value)">
<option value="EUR">€ EUR</option>
<option value="USD">$ USD</option>
<option value="NGN">₦ NGN</option>
</select>

<button onclick="viewCart()">🛒 Cart (<span id="count">0</span>)</button>
</div>

<div class="container">

<!-- PRODUCTS -->

<div class="card">
<img src="https://images.unsplash.com/photo-1695048133142-4b7f5c6e7f6b?auto=format&fit=crop&w=600&q=80">
<h2>iPhone 15 Pro Max</h2>
<p id="p1">€999</p>
<button class="btn" onclick="add('iPhone 15 Pro Max',999)">Add to Cart</button>
<a class="btn" href="https://wa.me/2347072331657?text=I%20want%20iPhone%2015%20Pro%20Max">Buy on WhatsApp Business</a>
</div>

<div class="card">
<img src="https://images.unsplash.com/photo-1664478546381-3d6b0f4a0c2f?auto=format&fit=crop&w=600&q=80">
<h2>iPhone 14 Pro</h2>
<p id="p2">€799</p>
<button class="btn" onclick="add('iPhone 14 Pro',799)">Add to Cart</button>
<a class="btn" href="https://wa.me/2347072331657?text=I%20want%20iPhone%2014%20Pro">Buy on WhatsApp Business</a>
</div>

<div class="card">
<h2>📦 Payment</h2>
<a class="btn" href="https://flutterwave.com/pay/YOUR_LINK">Pay Card / Bank / Mobile 💳</a>
<a class="btn" href="https://www.paypal.me/YOUR_USERNAME">PayPal 🌍</a>
</div>

<!-- REVIEWS -->
<div class="reviews">
⭐ “Very fast delivery, legit seller” — David<br><br>
⭐ “Phone came exactly as described” — Sarah<br><br>
⭐ “Trusted WhatsApp seller” — John
</div>

</div>

<!-- CART -->
<div class="cart" onclick="viewCart()">🛒 Cart</div>

<script>

window.onload=function(){
setTimeout(()=>{
document.getElementById("loader").style.display="none";
document.body.style.display="block";
},2000);
};

/* CART */
let cart=[];
let total=0;
let currency="EUR";

function add(name,price){
cart.push(name);
total+=price;
document.getElementById("count").innerText=cart.length;
update();
}

function update(){
document.getElementById("p1").innerText=getSymbol()+999;
document. I'm here lent UID ("p2").innerText=getSymbol()+799;
}

/* VIEW CART */
function viewCart(){
alert(cart.length?cart.join("\n"):"Cart empty");
}

/* CURRENCY */
function setCurrency(v){
currency=v;
update();
}

function getSymbol(){
return currency==="EUR"?"€":currency==="USD"?"$":"₦";
}

</script>

</body>
