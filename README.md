<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pedido Especial</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            flex-direction: column;
            background-color: pink;
            font-family: Arial, sans-serif;
        }
        .heart-container {
            position: relative;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        .heart {
            position: relative;
            width: 100px;
            height: 100px;
            background-color: red;
            transform: rotate(-45deg);
            margin-top: 20px;
        }
        .heart::before,
        .heart::after {
            content: "";
            position: absolute;
            width: 100px;
            height: 100px;
            background-color: red;
            border-radius: 50%;
        }
        .heart::before {
            top: -50px;
            left: 0;
        }
        .heart::after {
            top: 0;
            left: 50px;
        }
        .text {
            font-size: 18px;
            font-weight: bold;
            color: white;
            text-align: center;
            margin-bottom: 10px;
        }
        .buttons {
            margin-top: 20px;
            display: flex;
            justify-content: center;
        }
        .btn {
            font-size: 18px;
            padding: 10px 20px;
            margin: 10px;
            cursor: pointer;
            border: none;
            border-radius: 5px;
        }
        .yes {
            background-color: green;
            color: white;
        }
        .no {
            background-color: red;
            color: white;
            cursor: pointer;
            position: absolute;
        }
    </style>
</head>
<body>
    <div class="heart-container">
        <div class="text">Quer namorar comigo?</div>
        <div class="heart"></div>
    </div>
    <div class="buttons">
        <button class="btn yes" onclick="alert('Eu te amo! ❤️')">Sim</button>
        <button class="btn no" id="noButton">Não</button>
    </div>

    <script>
        const noButton = document.getElementById('noButton');

        // Quando passar o mouse sobre o botão "Não", ele muda de posição
        noButton.addEventListener('mouseover', () => {
            const x = Math.random() * (window.innerWidth - 100);
            const y = Math.random() * (window.innerHeight - 50);
            noButton.style.left = `${x}px`;
            noButton.style.top = `${y}px`;
        });
    </script>
</body>
</html>

