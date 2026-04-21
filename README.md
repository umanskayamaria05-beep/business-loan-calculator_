# business-loan-calculator_
Сайт-калькулятор для розрахунку бізнес-кредиту. Дозволяє визначити щомісячний платіж, загальну переплату, а також переглянути графік погашення кредиту. 
<!-- Сайт розроблено студентом Марією Уманською, група ФЕМП 4-14 -->
<!DOCTYPE html>
<html lang="uk">
<head>
<meta charset="UTF-8">
<title>Business Loan Calculator</title>

<style>
body{
    margin:0;
    font-family:Arial;
    background:linear-gradient(135deg,#e0f7fa,#e8f5e9);
}

/* HEADER */
header{
    background:linear-gradient(90deg,#009688,#26a69a);
    color:red;
    padding:20px;
    text-align:center;
}

nav{
    margin-top:10px;
}

nav button{
    background:none;
    border:none;
    color:red;
    font-weight:bold;
    margin:10px;
    cursor:pointer;
    font-size:16px;
}

nav button:hover{
    text-decoration:underline;
}

/* SECTIONS */
section{
    display:none;
    padding:20px;
}

.active{
    display:block;
}

/* CARD */
.card{
    background:red;
    padding:20px;
    border-radius:15px;
    box-shadow:0 5px 15px rgba(0,0,0,0.1);
    border-left:5px solid #26a69a;
    margin-bottom:20px;
}

/* INPUT */
input{
    width:100%;
    padding:12px;
    margin:10px 0;
    border-radius:8px;
    border:1px solid #ccc;
}

/* BUTTON */
button.calc{
    width:100%;
    padding:12px;
    background:linear-gradient(90deg,#43a047,#26a69a);
    color:blue;
    border:none;
    border-radius:8px;
    cursor:pointer;
}

/* TABLE */
table{
    width:100%;
    border-collapse:collapse;
}

td,th{
    border:1px solid #ddd;
    padding:8px;
    text-align:center;
}

th{
    background:#26a69a;
    color:blue;
}

/* FOOTER */
footer{
    background:#004d40;
    color:white;
    text-align:center;
    padding:15px;
}
</style>
</head>

<body>

<header>
<h1>Business Loan Calculator</h1>

<nav>
<button onclick="show('home')">Головна</button>
<button onclick="show('calc')">Калькулятор</button>
<button onclick="show('contacts')">Контакти</button>
</nav>
</header>

<!-- HOME -->
<section id="home" class="active">
<div class="card">
<h2>Ласкаво просимо</h2>
<p>Це бізнес-платформа для розрахунку кредитів.</p>
<p>Ви можете дізнатися щомісячний платіж та переплату.</p>
</div>
</section>

<!-- CALCULATOR -->
<section id="calc">

<div class="card">
<h2>Калькулятор кредиту</h2>

<input type="number" id="amount" placeholder="Сума кредиту">
<input type="number" id="months" placeholder="Термін (місяці)">
<input type="number" id="rate" placeholder="Ставка (%)">

<button class="calc" onclick="calculate()">Розрахувати</button>

<h3 id="result"></h3>
</div>

<div class="card">
<h2>Графік платежів</h2>
<table id="table">
<tr>
<th>Місяць</th>
<th>Платіж</th>
<th>Залишок</th>
</tr>
</table>
</div>

</section>

<!-- CONTACTS -->
<section id="contacts">
<div class="card">
<h2>Контакти</h2>
<p>Email: business-loan-calculator@gmail.com</p>
<p>Телефон: +380123456789</p>
</div>
</section>

<footer>
<p>Уманська Марія | ФЕМП 4-14</p>
</footer>
