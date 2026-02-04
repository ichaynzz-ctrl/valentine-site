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
            margin: 0;
            padding-top: 50px;
            overflow: hidden;
        }
   h1 {
            font-size: 40px;
            margin-bottom: 50px;
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

 /* Floating hearts */
        .heart {
            position: fixed;
            color: pink;
            font-size: 20px;
            animation: float 4s linear infinite;
            pointer-events: none;
        }

 @keyframes float {
            0% { transform: translateY(0); opacity: 1; }
            100% { transform: translateY(-800px); opacity: 0; }
        }

/* I LOVE YOU pop */
        .love-pop {
            position: fixed;
            color: red;
            font-size: 25px;
            animation: pop 1s ease forwards;
            pointer-events: none;
        }

  @keyframes pop {
            0% { transform: scale(1); opacity: 1; }
            100% { transform: scale(2); opacity: 0; }
        }
    </style>
</head>
<body>

  <h1>Will you be my Valentine? 💘</h1>

 <button id="yes" onclick="yesClick()">Yes 💖</button>
    <button id="no" onmouseover="moveButton()">No 😏</button>
    <!-- Background music (optional) --->
    <audio id="bgMusic" loop>
        <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mp3">
    </audio>

 <script>
     // Yes button click 
        function yesClick() {
            document.getElementById("bgMusic").play();
            document.body.innerHTML = "<h1>Yayyyy 💕 I knew ittt 🥹💖</h1>";
        }
     / No button moves and shows I LOVE YOU pop
        function moveButton() {
            var button = document.getElementById("no");
            var x = Math.random() * (window.innerWidth - 100);
            var y = Math.random() * (window.innerHeight - 50);
            button.style.left = x + "px";
            button.style.top = y + "px";

            / Create I LOVE YOU pop
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

        / Floating hearts continuously
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
            
