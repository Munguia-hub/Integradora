<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f0f0f0;
        }
        .login-container {
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .login-container h2 {
            margin-bottom: 20px;
        }
        .login-container label {
            display: block;
            margin-bottom: 5px;
        }
        .login-container input {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        .login-container button {
            width: 100%;
            padding: 10px;
            background-color: #007BFF;
            border: none;
            border-radius: 4px;
            color: #fff;
            font-size: 16px;
        }
    </style>
    <script>
        function validarLogin(event) {
            event.preventDefault(); // Evitar el envío del formulario por defecto

            // Obtener los valores de los campos de texto
            var username = document.getElementById("username").value;
            var password = document.getElementById("password").value;

            // Verificar si el usuario es "Empleado" y la contraseña es "Password"
            if (username === "Empleado" && password === "Password") {
                // Redirigir al enlace especificado
                window.location.href = "https://sites.google.com/view/integradoraiii/p%C3%A1gina-principal";
            } else {
                alert("Nombre de usuario o contraseña incorrectos.");
            }
        }
    </script>
</head>
<body>
    <div class="login-container">
        <h2>Iniciar Sesión</h2>
        <form onsubmit="validarLogin(event)">
            <label for="username">Nombre de usuario:</label>
            <input type="text" id="username" name="username" required>
            <label for="password">Contraseña:</label>
            <input type="password" id="password" name="password" required>
            <button type="submit">Login</button>
        </form>
    </div>
</body>
</html>
