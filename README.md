# website-personal[Uploading index.html…]()<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login Form</title>
    <style>
        /* Basic Styling */
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            font-family: Arial, sans-serif;
            margin: 0;
            background-color: #f0f2f5;
        }

        .login-container {
            background-color: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
            width: 90%;
            max-width: 400px;
        }

        h2 {
            text-align: center;
            margin-bottom: 1.5rem;
        }

        .input-group {
            margin-bottom: 1rem;
            display: flex;
            flex-direction: column;
        }

        .input-group label {
            margin-bottom: 0.5rem;
            font-weight: bold;
        }

        .input-group input {
            padding: 0.75rem;
            border: 1px solid #ddd;
            border-radius: 4px;
        }

        .input-group input[type="password"] {
            font-family: sans-serif;
            font-size: 1rem;
            letter-spacing: 0.1em;
        }

        .error-message {
            color: red;
            font-size: 0.875rem;
            display: none;
            margin-top: -0.5rem;
            margin-bottom: 1rem;
        }

        .login-btn {
            width: 100%;
            padding: 0.75rem;
            background-color: #4CAF50;
            color: white;
            font-size: 1rem;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        .login-btn:hover {
            background-color: #45a049;
        }

        /* Responsive */
        @media (max-width: 500px) {
            .login-container {
                padding: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="login-container">
        <h2>Login</h2>
        <div class="error-message" id="error-message">Username atau password salah!</div>
        <div class="input-group">
            <label for="username">Username</label>
            <input type="text" id="username" placeholder="Masukkan username">
        </div>
        <div class="input-group">
            <label for="password">Password</label>
            <input type="password" id="password" placeholder="Masukkan password">
        </div>
        <button class="login-btn" onclick="login()">Login</button>
    </div>

    <script>
        function login() {
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            const errorMessage = document.getElementById('error-message');

            // Periksa form kosong
            if (!username || !password) {
                errorMessage.textContent = 'Form login tidak boleh kosong!';
                errorMessage.style.display = 'block';
                return;
            }

            // Validasi username dan password
            const validUsername = 'admin';
            const validPassword = '1234';

            if (username === validUsername && password === validPassword) {
                // Jika login berhasil, arahkan ke halaman utama
                window.location.href = 'halaman-utama.html';
            } else {
                // Tampilkan pesan kesalahan
                errorMessage.textContent = 'Username atau password salah!';
                errorMessage.style.display = 'block';
            }
        }
    </script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Halaman Utama</title>
    <style>
        /* Basic Styling */
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: #f0f2f5;
        }

        .container {
            text-align: center;
            background-color: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
            width: 90%;
            max-width: 500px;
        }

        h1 {
            margin-bottom: 1rem;
        }

        .logout-btn {
            padding: 0.75rem;
            background-color: #e74c3c;
            color: white;
            font-size: 1rem;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        .logout-btn:hover {
            background-color: #c0392b;
        }

        /* Responsive */
        @media (max-width: 500px) {
            .container {
                padding: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Selamat Datang di Halaman Utama</h1>
        <p>Anda telah berhasil login.</p>
        <button class="logout-btn" onclick="logout()">Logout</button>
    </div>

    <script>
        function logout() {
            // Kembali ke halaman login
            window.location.href = 'index.html';
        }
    </script>
</body>
</html>


web
