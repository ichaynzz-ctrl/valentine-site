# valentine-site
A special surprise 
<!DOCTYPE html>
<html>
<head>
    <title>Will You Be Mine? 💖</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            background: linear-gradient(to right, #ff758c, #ff7eb3);
            color: white;
            margin-top: 100px;
            overflow: hidden;
        }

        h1 {
            font-size: 40px;
        }

        button {
            padding: 15px 25px;
            font-size: 18px;
            margin: 10px;
            border: none;
            border-radius: 20px;
            cursor: pointer;
        }

        #yes {
            background-color: #00ff88;
        }

        #no {
            background-color: #ff4d4d;
            position: absolute;
        }
    </style>
</head>
<body>

    <h1>Will you be my Valentine? 💘</h1>

    <button id="yes" onclick="yesClick()">Yes 💖</button>
    <button id="no" onmouseover="moveButton()">No 😏</button>

    <audio id="bgMusic" loop>
        <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mp3">
    </audio>

    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>
    <script>
        const noButton = document.getElementById("no");
        const music = document.getElementById("bgMusic");

        function moveButton() {
            const x = Math.random() * (window.innerWidth - noButton.offsetWidth);
            const y = Math.random() * (window.innerHeight - noButton.offsetHeight);
            noButton.style.left = x + "px";
            noButton.style.top = y + "px";
        }

        function yesClick() {
            music.play();

            document.body.innerHTML = `
                <h1>Yayyyy 💕 I knew ittt 🥹💖</h1>
                <canvas id="confetti"></canvas>
            `;

            confetti({
                particleCount: 200,
                spread: 120
            });
        }
    </script
</head>
<body>
    <h1>Will you be my Valentine? 💘</h1>
    <button id="yes" onclick="yesClick()">Yes 💖</button>
    <button id="no" onmouseover="moveButton()">No 😏</button>

    <script>
        // Yes click
        function yesClick() {
            document.body.innerHTML = "<h1>Yayyyy 💕 I knew ittt 🥹💖</h1>";
        }

        // Move No button
        function moveButton() {
            var button = document.getElementById("no");
            var x = Math.random() * (window.innerWidth - 100);
            var y = Math.random() * (window.innerHeight - 50);
            button.style.left = x + "px";
            button.style.top = y + "px";

            // Create I LOVE YOU pop
            var love = document.createElement("div");
            love.className = "love-pop";
            love.innerHTML = "I ❤️ YOU";
            love.style.left = x + "px";
            love.style.top = y + "px";
            document.body.appendChild(love);

            setTimeout(function() {
                love.remove();
            }, 1000);
        }

        // Floating hearts continuously
        setInterval(function() {
            var heart = document.createElement("div");
            heart.className = "heart";
            heart.innerHTML = "💖";
            heart.style.left = Math.random() * window.innerWidth + "px";
            heart.style.bottom = "0px";
            document.body.appendChild(heart);

            setTimeout(function() {
                heart.remove();
            }, 4000);
        }, 500);
    </script>
</body>
</html>
