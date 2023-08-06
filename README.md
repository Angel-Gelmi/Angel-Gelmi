<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>¿Quieres ser mi novia?</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f3f3f3;
            font-family: Arial, sans-serif;
        }
        #container {
            text-align: center;
        }
        h1 {
            font-size: 32px;
            color: #333;
        }
        #buttons {
            margin-top: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        button {
            margin: 10px;
            padding: 10px 20px;
            font-size: 18px;
            color: #fff;
            background-color: #4CAF50;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        button:hover {
            background-color: #45a049;
        }
        #btnNo {
            background-color: #f44336;
        }
        #btnNo:hover {
            background-color: #d32f2f;
        }
        img {
            margin-top: 30px;
            max-width: 100%;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
    </style>
</head>
<body>
    <div id="container">
        <h1>¿Quieres ser mi novia?</h1>
        <div id="buttons">
            <button onclick="accionParaCuandoEllaDigaQueSi()" id="btnSi">Si</button>
            <button id="btnNo" onmouseover="mueveElBoton()">No</button>
        </div>
        <img src="https://acortar.link/0ND7yy" alt="" width="200">
    </div>

    <script>
        function accionParaCuandoEllaDigaQueSi() {
            const respuesta = confirm("¿Estás segura de querer ser mi novia?");
            if (respuesta) {
                // Redireccionar a la nueva página si responde "Si"
                window.location.href = "opcion.html";
            } else {
                alert("Espero que puedas reconsiderarlo 😊");
            }
        }
        function mueveElBoton() {
            const width = window.innerWidth;
            const height = window.innerHeight;

            const newWidth = Math.random() * width;
            const newHeight = Math.random() * height;
            const btnNo = document.getElementById("btnNo");
            btnNo.style.position = "absolute";
            btnNo.style.left = newWidth + "px";
            btnNo.style.top = newHeight + "px";
        }
    </script>
</body>
</html>
