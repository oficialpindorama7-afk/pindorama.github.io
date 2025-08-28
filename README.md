<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cubo 3D Giratório</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f0f0f0;
            font-family: sans-serif;
            perspective: 800px; /* Adiciona profundidade à cena */
        }

        .container {
            width: 200px;
            height: 200px;
            position: relative;
            transform-style: preserve-3d; /* Permite que os elementos filhos sejam posicionados no espaço 3D */
            animation: girarCubo 10s infinite linear; /* Animação de rotação */
        }

        .face {
            position: absolute;
            width: 200px;
            height: 200px;
            background-color: rgba(0, 0, 255, 0.7); /* Azul com transparência */
            border: 2px solid #000;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 2em;
            color: white;
            opacity: 0.9; /* Pequena opacidade para o efeito 3D */
        }

        .frente {
            transform: translateZ(100px); /* Move a face para a frente */
        }

        .tras {
            transform: rotateY(180deg) translateZ(100px); /* Gira e move para trás */
        }

        .direita {
            transform: rotateY(90deg) translateZ(100px); /* Gira e move para a direita */
        }

        .esquerda {
            transform: rotateY(-90deg) translateZ(100px); /* Gira e move para a esquerda */
        }

        .topo {
            transform: rotateX(90deg) translateZ(100px); /* Gira e move para o topo */
        }

        .baixo {
            transform: rotateX(-90deg) translateZ(100px); /* Gira e move para baixo */
        }

        @keyframes girarCubo {
            0% {
                transform: rotateX(0deg) rotateY(0deg);
            }
            100% {
                transform: rotateX(360deg) rotateY(360deg);
            }
        }
    </style>
</head>
<body>

<div class="container">
    <div class="face frente">1</div>
    <div class="face tras">2</div>
    <div class="face direita">3</div>
    <div class="face esquerda">4</div>
    <div class="face topo">5</div>
    <div class="face baixo">6</div>
</div>

</body>
</html>
