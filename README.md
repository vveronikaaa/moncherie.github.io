# moncherie.github.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Valentine's Day</title>
    <style>
        body {
            text-align: center;
            background: linear-gradient(to bottom, red, black);
            background-attachment: fixed;
            height: 100vh;
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            font-family: 'Arial', sans-serif;
            color: white;
        }
        .container {
            text-align: center;
        }
        .hidden-message {
            display: none;
            font-size: 20px;
            color: #ffcccc;
            margin-top: 100px;
        }
        .hidden-image {
            display: none;
            margin-top: 20px;
            max-width: 100%;
            height: auto;
        }
        .image-container {
            display: flex;
            justify-content: center;
            align-items: center;
            margin-top: 20px;
        }
        h1, p {
            color: #ffdddd;
        }
        .poem {
            display: none;
            font-size: 24px;
            font-weight: bold;
            color: #680e1d;
            text-align: center;
            margin-top: 20px;
        }
        .heart {
            position: absolute;
            color: red;
            font-size: 24px;
            animation: float 4s infinite ease-in-out;
        }
        @keyframes float {
            0% { transform: translateY(0); opacity: 1; }
            50% { opacity: 0.7; }
            100% { transform: translateY(-200px); opacity: 0; }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Happy Valentine's Day, Daniel! ❤️</h1>
        <p>Got a super secret message for you.</p>
        <button onclick="revealMessage()">Top secret confidential info</button>
        <p class="hidden-message" id="message">Today I've discovered a new dinosaur. It's called Imissyouaurus! Alsoo here's a poem you didn't ask for:</p>
        <p class="poem" id="poem">Roses are red, 
salsa is too. 
I fucking love you!
(now send forehead kisses).
</p>
        <div class="image-container">
            <img src="" class="hidden-image" id="valentineImage" alt="Your Special Image">
        </div>
    </div>
    <script>
        function revealMessage() {
            document.getElementById('message').style.display = 'block';
            document.getElementById('poem').style.display = 'block';
            let imageElement = document.getElementById('valentineImage');
            imageElement.src = "https://i.pinimg.com/736x/f7/06/24/f70624a9bcf2e963acdbbe2b4d188837.jpg"; 
            imageElement.style.display = 'block';
        }

        function createHeart() {
            const heart = document.createElement("div");
            heart.innerHTML = "❤️";
            heart.classList.add("heart");
            document.body.appendChild(heart);
            
            const size = Math.random() * 20 + 10 + "px";
            heart.style.fontSize = size;
            heart.style.left = Math.random() * 100 + "vw";
            heart.style.top = "100vh";
            
            heart.style.animationDuration = Math.random() * 2 + 3 + "s";
            setTimeout(() => heart.remove(), 5000);
        }

        setInterval(createHeart, 500);
    </script>
</body>
</html>
