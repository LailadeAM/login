<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #F9F9E0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        form {
            background-color: #FFF;
            padding: 40px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            width: 400px;
            text-align: center;
        }

        input {
            width: 100%;
            padding: 14px;
            margin: 10px 0;
            box-sizing: border-box;
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        button {
            background-color: #FF90BC;
            color: #FFF;
            padding: 14px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            width: 100%;
        }

        button:hover {
            background-color: #FF6F9F;
        }

        h2 {
            color: #333;
        }

        .error-message {
            color: #FF5757;
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <form id="loginForm">
        <h2>Login</h2>
        <label for="username">Usuário:</label>
        <input type="text" id="username" name="username" required>

        <label for="password">Senha:</label>
        <input type="password" id="password" name="password" required>

        <button type="button" onclick="submitForm()">Entrar</button>

        <p class="error-message" id="errorMessage"></p>
    </form>

    <script>
        function submitForm() {
            var username = document.getElementById("username").value;
            var password = document.getElementById("password").value;

            // Exemplo de verificação no lado do cliente (não seguro para produção)
            if (username === "seu_usuario" && password === "sua_senha") {
                window.location.href = "dashboard.html";
            } else {
                document.getElementById("errorMessage").innerHTML = "Usuário ou senha incorretos.";
            }
        }
    </script>
</body>
</html>
