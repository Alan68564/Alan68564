<!DOCTYPE html>
<html lang="kk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ұланның Лаураға Сезімі</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(to bottom right, #ff9a9e, #fad0c4, #fbc2eb);
            text-align: center;
            padding: 20px;
            margin: 0;
            height: 100vh;
            overflow: hidden;
            position: relative;
        }
        .question {
            font-size: 24px;
            color: #fff;
            margin-top: 20px;
            margin-bottom: 40px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
        }
        .button {
            font-size: 18px;
            padding: 12px 24px;
            margin: 10px;
            cursor: pointer;
            border: none;
            border-radius: 30px;
            transition: transform 0.3s, background-color 0.3s;
        }
        .yes {
            background-color: #ff4081;
            color: white;
        }
        .no {
            background-color: #f44336;
            color: white;
            position: absolute;
            left: 50%;
            top: 60%;
            transform: translateX(-50%);
        }
        .response {
            margin-top: 30px;
            font-size: 22px;
            color: #fff;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.3);
        }
        .heart {
            position: absolute;
            color: #ff4d6d;
            font-size: 24px;
            animation: floatUp 4s ease-in-out infinite;
        }
        @keyframes floatUp {
            0% { transform: translateY(0) scale(1); opacity: 1; }
            50% { transform: translateY(-100px) scale(1.2); opacity: 0.6; }
            100% { transform: translateY(-200px) scale(1); opacity: 0; }
        }
    </style>
</head>
<body>
    <div class="question">
        Лаура, мен сені жанымнан артық жақсы көремін! Сен мені жақсы көресің бе?
    </div>
    <button class="button yes" onclick="showResponse()">Иә</button>
    <button class="button no" id="noButton" onmouseover="moveNoButton()" ontouchstart="moveNoButton()">Жоқ</button>

    <div id="responseMessage" class="response"></div>

    <script>
        function showResponse() {
            const responseMessage = document.getElementById('responseMessage');
            responseMessage.innerHTML = 'Мен де сені қатты жақсы көремін, Ұлан!';
            createHearts();
        }

        function moveNoButton() {
            const noButton = document.getElementById('noButton');
            const maxX = window.innerWidth - noButton.offsetWidth - 10;
            const maxY = window.innerHeight - noButton.offsetHeight - 10;

            const x = Math.random() * maxX;
            const y = Math.random() * maxY;

            noButton.style.left = x + 'px';
            noButton.style.top = y + 'px';
        }

        function createHearts() {
            for (let i = 0; i < 15; i++) {
                const heart = document.createElement('div');
                heart.classList.add('heart');
                heart.innerHTML = '❤️';
                heart.style.left = Math.random() * 100 + 'vw';
                heart.style.top = Math.random() * 100 + 'vh';
                heart.style.animationDuration = Math.random() * 3 + 3 + 's';
                document.body.appendChild(heart);

                setTimeout(() => {
                    heart.remove();
                }, 4000);
            }
        }
    </script>
</body>
</html>
