<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Proposta Especial</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
        }

        h1 {
            font-size: 2.5em;
            color: #333;
            margin-bottom: 40px;
        }

        .buttons {
            display: flex;
            gap: 20px;
        }

        button {
            padding: 15px 30px;
            font-size: 1.2em;
            cursor: pointer;
            border: none;
            border-radius: 5px;
            transition: all 0.3s;
        }

        #yesBtn {
            background-color: #4CAF50;
            color: white;
        }

        #noBtn {
            background-color: #ff4444;
            color: white;
            position: relative;
        }
    </style>
</head>
<body>
    <h1>Quer casar comigo?</h1>
    <div class="buttons">
        <button id="yesBtn">Sim</button>
        <button id="noBtn">Não</button>
    </div>

    <script>
        const yesBtn = document.getElementById('yesBtn');
        const noBtn = document.getElementById('noBtn');

        // Quando clicar em "Sim", redireciona para o vídeo do YouTube
        yesBtn.addEventListener('click', () => {
            // Substitua o link abaixo pelo link do vídeo que você quer usar
            window.location.href = 'https://www.youtube.com/watch?v=dQw4w9WgXcQ';
        });

        // Quando tentar clicar ou passar o mouse no "Não", ele muda de posição
        noBtn.addEventListener('mouseover', moveButton);
        noBtn.addEventListener('click', moveButton);

        function moveButton() {
            const maxX = window.innerWidth - noBtn.offsetWidth;
            const maxY = window.innerHeight - noBtn.offsetHeight;

            const newX = Math.random() * maxX;
            const newY = Math.random() * maxY;

            noBtn.style.position = 'absolute';
            noBtn.style.left = `${newX}px`;
            noBtn.style.top = `${newY}px`;
        }
    </script>
</body>
</html>
