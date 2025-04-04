<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Budget Tracker</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-100 text-gray-900">
    <div class="max-w-md mx-auto min-h-screen bg-white shadow-md rounded-lg overflow-hidden">
        <!-- Header -->
        <header class="bg-blue-500 text-white p-4 flex justify-between items-center">
            <h1 class="text-lg font-semibold">Budget Tracker</h1>
            <button class="text-white">⚙️</button>
        </header>
        <!-- Balance Info -->
        <section class="p-4">
            <h2 class="text-xl font-bold">Total Balance</h2>
            <p class="text-2xl font-semibold text-green-600">Rp 4.285.650</p>
        </section>
        <!-- Budget Summary -->
        <section class="p-4 grid grid-cols-2 gap-2">
            <div class="bg-blue-100 p-4 rounded-lg">
                <h3 class="text-sm font-semibold">Income</h3>
                <p class="text-lg text-blue-600">Rp 6.240.000</p>
            </div>
            <div class="bg-red-100 p-4 rounded-lg">
                <h3 class="text-sm font-semibold">Expenses</h3>
                <p class="text-lg text-red-600">Rp 1.954.350</p>
            </div>
        </section>
        <!-- Recent Transactions -->
        <section class="p-4">
            <h2 class="text-lg font-semibold">Recent Transactions</h2>
            <ul>
                <li class="flex justify-between p-2 border-b">
                    <span>Gaji</span>
                    <span class="text-green-600">+Rp 3.250.000</span>
                </li>
                <li class="flex justify-between p-2 border-b">
                    <span>Belanja</span>
                    <span class="text-red-600">-Rp 85.320</span>
                </li>
                <li class="flex justify-between p-2 border-b">
                    <span>Netflix</span>
                    <span class="text-red-600">-Rp 15.990</span>
                </li>
            </ul>
        </section>
        <!-- Floating Add Button -->
        <button class="fixed bottom-20 right-5 bg-blue-500 text-white p-4 rounded-full shadow-lg">+</button>
        <!-- Navigation -->
        <nav class="fixed bottom-0 w-full bg-white flex justify-around p-3 border-t shadow-md">
            <a href="#" class="text-blue-500 flex flex-col items-center">
                <span>🏠</span>
                <span class="text-xs">Home</span>
            </a>
            <a href="#" class="text-gray-500 flex flex-col items-center">
                <span>📊</span>
                <span class="text-xs">Budget</span>
            </a>
            <a href="#" class="text-gray-500 flex flex-col items-center">
                <span>🔔</span>
                <span class="text-xs">Alerts</span>
            </a>
            <a href="#" class="text-gray-500 flex flex-col items-center">
                <span>👤</span>
                <span class="text-xs">Profile</span>
            </a>
        </nav>
    </div>
</body>
</html>
