<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bank Login Portal</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f3f4f6;
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .login-container {
            background-color: #ffffff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            width: 300px;
            text-align: center;
        }

        .login-container h2 {
            margin-bottom: 20px;
            color: #333;
        }

        .login-container input {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        .login-container button {
            background-color: #4caf50;
            color: white;
            border: none;
            padding: 10px;
            width: 100%;
            border-radius: 5px;
            cursor: pointer;
        }

        .login-container button:hover {
            background-color: #45a049;
        }

        .message {
            margin-top: 20px;
            font-size: 16px;
            color: #333;
        }

        .error {
            color: red;
        }
    </style>
</head>
<body>
    <div class="login-container">
        <h2>Bank Login</h2>
        <input type="password" id="password" placeholder="Enter Password" />
        <button onclick="checkPassword()">Login</button>
        <p class="message" id="message"></p>
    </div>

    <script>
        function checkPassword() {
            const passwordInput = document.getElementById("password").value;
            const messageElement = document.getElementById("message");

            if (passwordInput === "cashflow3690") {
                messageElement.innerHTML = "<strong>Welcome Mr. Hawthorn!</strong><br>Your bank balance is: <strong>$3,456,000</strong>.";
                messageElement.classList.remove("error");
            } else {
                messageElement.textContent = "Incorrect password. Please try again.";
                messageElement.classList.add("error");
            }
        }
    </script>
</body>
</html>
