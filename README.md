<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Women's Day Ginni!</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }

        body {
            background: linear-gradient(45deg, #ff7eb9, #ff758c);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
        }

        .container {
            background: rgba(255, 255, 255, 0.95);
            padding: 2rem;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            text-align: center;
            max-width: 600px;
            position: relative;
            transform: scale(0.95);
            transition: transform 0.3s;
        }

        .container:hover {
            transform: scale(1);
        }

        h1 {
            color: #ff3366;
            margin-bottom: 1rem;
            font-size: 2.5rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
        }

        .message {
            font-size: 1.2rem;
            line-height: 1.6;
            color: #333;
            margin-bottom: 1.5rem;
        }

        .buttons {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-top: 2rem;
        }

        .btn {
            padding: 12px 25px;
            border: none;
            border-radius: 30px;
            background: #ff3366;
            color: white;
            font-size: 1.1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(255, 51, 102, 0.3);
        }

        .btn:hover {
            transform: translateY(-3px);
            background: #ff1a4d;
            box-shadow: 0 6px 20px rgba(255, 51, 102, 0.4);
        }

        .hearts {
            position: absolute;
            width: 100%;
            height: 100%;
            pointer-events: none;
            top: 0;
            left: 0;
        }

        .heart {
            position: absolute;
            font-size: 1.5rem;
            animation: float 3s infinite;
            opacity: 0;
        }

        @keyframes float {
            0% { transform: translateY(0) rotate(0deg); opacity: 0; }
            50% { opacity: 1; }
            100% { transform: translateY(-100px) rotate(360deg); opacity: 0; }
        }

        .hidden-message {
            display: none;
            margin-top: 1rem;
            color: #ff3366;
            font-weight: bold;
        }

    </style>
</head>
<body>
    <div class="container">
        <div class="hearts">
            <!-- Hearts will be added via JavaScript -->
        </div>
        
        <h1>🌸 Happy Women's Day Ginni! 🌸</h1>
        
        <div class="message">
            <p>Ginni, you're the most amazing woman I know - strong, kind, and endlessly beautiful!</p>
            <p>Your smile lights up every room, and your heart makes the world a better place.</p>
            <p>In a universe full of stars, you shine the brightest. 🌟</p>
            <p>You're not just important - you're essential, precious, and deeply loved.</p>
            <p>Today and every day, remember: You're absolutely extraordinary! 💖</p>
        </div>

        <div class="buttons">
            <button class="btn" onclick="showLove()">💖 Show More Love</button>
            <button class="btn" onclick="createHearts()">🌸 Surprise!</button>
        </div>

        <div id="hiddenMessage" class="hidden-message">
            You're the queen of my heart! 👑 Forever and always! 💞
        </div>
    </div>

    <script>
        function showLove() {
            const hiddenMessage = document.getElementById('hiddenMessage');
            hiddenMessage.style.display = 'block';
            setTimeout(() => {
                hiddenMessage.style.display = 'none';
            }, 3000);
        }

        function createHearts() {
            const heartsContainer = document.querySelector('.hearts');
            for (let i = 0; i < 10; i++) {
                const heart = document.createElement('div');
                heart.className = 'heart';
                heart.innerHTML = '💖';
                heart.style.left = Math.random() * 100 + '%';
                heart.style.animationDelay = Math.random() * 2 + 's';
                heartsContainer.appendChild(heart);
            }
            setTimeout(() => {
                heartsContainer.innerHTML = '';
            }, 3000);
        }

        // Add initial floating hearts
        setInterval(() => {
            createHearts();
        }, 4000);
    </script>
</body>
</html>
