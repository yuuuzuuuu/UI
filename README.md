<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FinTrack</title>
    <link rel="stylesheet" href="styles.css">
    <script defer src="script.js"></script>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #121212;
            color: white;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }
        header {
            display: flex;
            justify-content: space-between;
            width: 100%;
            padding: 15px;
            background: #1e1e1e;
        }
        .logo {
            width: 120px;
        }
        main {
            width: 90%;
            max-width: 400px;
            text-align: center;
        }
        .balance {
            background: #232323;
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 20px;
        }
        .budget-progress, .spending-limits {
            background: #232323;
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 20px;
        }
        .progress-circles {
            display: flex;
            justify-content: space-around;
        }
        .circle {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
        }
        .food { background: purple; }
        .transport { background: orange; }
        .shopping { background: red; }
        nav {
            display: flex;
            justify-content: space-around;
            width: 100%;
            background: #1e1e1e;
            padding: 10px 0;
            position: fixed;
            bottom: 0;
        }
        .nav-btn {
            background: none;
            border: none;
            color: white;
            font-size: 18px;
        }
        .limit {
            display: flex;
            justify-content: space-between;
            padding: 10px;
            background: #333;
            border-radius: 5px;
            margin: 5px 0;
        }
        .limit button {
            background: red;
            border: none;
            color: white;
            padding: 5px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <header>
        <img src="logo.png" alt="FinTrack Logo" class="logo">
        <div class="notifications">
            <span class="icon">🔔</span>
            <span class="count">2</span>
        </div>
        <div class="profile-icon">👤</div>
    </header>
    <main>
        <section class="balance">
            <h1>Total Balance</h1>
            <p class="amount">$4,285.65</p>
            <button class="add-income">+ Add Income</button>
            <button class="add-expense">- Add Expense</button>
        </section>
        <section class="budget-progress">
            <h2>Budget Progress</h2>
            <div class="progress-circles">
                <div class="circle food">75%</div>
                <div class="circle transport">60%</div>
                <div class="circle shopping">80%</div>
            </div>
        </section>
        <section class="spending-limits">
            <h2>Spending Limits</h2>
            <div id="limits-container"></div>
            <button id="add-limit">+ Add Limit</button>
        </section>
    </main>
    <nav>
        <button class="nav-btn">🏠 Home</button>
        <button class="nav-btn">📜 Transactions</button>
        <button class="nav-btn">➕</button>
        <button class="nav-btn">💰 Budget</button>
        <button class="nav-btn">👤 Profile</button>
    </nav>
    <script>
        document.getElementById('add-limit').addEventListener('click', function() {
            let limitContainer = document.getElementById('limits-container');
            let newLimit = document.createElement('div');
            newLimit.classList.add('limit');
            newLimit.innerHTML = `<span>New Limit</span> <button onclick="this.parentElement.remove()">Remove</button>`;
            limitContainer.appendChild(newLimit);
        });
    </script>
</body>
</html>
