<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Finance Portfolio</title>

<style>
    *{
        margin:0;
        padding:0;
        box-sizing:border-box;
        font-family: Arial, sans-serif;
    }

    body{
        background:#0A2342;
        color:white;
        line-height:1.6;
    }

    header{
        background:#06162E;
        padding:20px;
        text-align:center;
    }

    nav{
        margin-top:10px;
    }

    nav a{
        color:white;
        text-decoration:none;
        margin:0 15px;
        font-weight:bold;
    }

    section{
        padding:40px;
    }

    .card{
        background:#12355B;
        padding:20px;
        border-radius:10px;
        margin-top:20px;
    }

    table{
        width:100%;
        border-collapse:collapse;
        margin-top:20px;
    }

    table, th, td{
        border:1px solid white;
    }

    th, td{
        padding:10px;
        text-align:center;
    }

    input, button{
        padding:10px;
        margin:5px;
        border:none;
        border-radius:5px;
    }

    button{
        background:#1E90FF;
        color:white;
        cursor:pointer;
    }

    footer{
        text-align:center;
        padding:20px;
        background:#06162E;
    }
</style>
</head>

<body>

<header>
    <h1>Financial Portfolio</h1>
    <p>Managing Financial Transactions & Accounting Records</p>

    <nav>
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#transactions">Transactions</a>
        <a href="#contact">Contact</a>
    </nav>
</header>

<section id="home">
    <h2>Welcome</h2>
    <div class="card">
        <p>
            This portfolio helps clients manage financial transactions,
            record income and expenses, and maintain accounting records.
        </p>
    </div>
</section>

<section id="about">
    <h2>About Services</h2>
    <div class="card">
        <ul>
            <li>Financial Transaction Tracking</li>
            <li>Income & Expense Recording</li>
            <li>Accounting Book Management</li>
            <li>Financial Reporting Support</li>
        </ul>
    </div>
</section>

<section id="transactions">
    <h2>Accounting Book</h2>

    <div class="card">
        <input type="date" id="date">
        <input type="text" id="description" placeholder="Description">
        <input type="number" id="amount" placeholder="Amount">
        <input type="amount if its credited or debited"id="credit or debit" placeholder="credit or debited">
        <button onclick="addTransaction()">Add Transaction</button>

        <table id="transactionTable">
            <tr>
                <th>Date</th>
                <th>Description</th>
             <th>Amount</th>
             <th>credit or debit</th>
            </tr>
        </table>
    </div>
</section>

<section id="contact">
    <h2>Contact Information</h2>

    <div class="card">
        <p><strong>Name:</strong> ntwali elisa</p>
        <p><strong>Email:</strong> ntwalik7@gmail.com</p>
        <p><strong>Phone:</strong> +250 788591341</p>
        <p><strong>Location:</strong> Kigali, Rwanda</p>
    </div>
</section>

<footer>
    <p>© 2026 Financial Portfolio. All Rights Reserved.</p>
</footer>

<script>
function addTransaction() {
    let date = document.getElementById("date").value;
    let description = document.getElementById("description").value;
    let amount = document.getElementById("amount").value;

    if(date && description && amount){
        let table = document.getElementById("transactionTable");

        let row = table.insertRow(-1);

        row.insertCell(0).innerHTML = date;
        row.insertCell(1).innerHTML = description;
        row.insertCell(2).innerHTML = amount;

        document.getElementById("date").value = "";
        document.getElementById("description").value = "";
        document.getElementById("amount").value = "";
    } else {
        alert("Please fill all fields.");
    }
}
</script>

</body>
</html>
</body>
</html>
