<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For Minaxi ❤️</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #fff0f3; /* Soft Pink */
            text-align: center;
            overflow: hidden;
        }

        h1 {
            color: #c9184a;
            font-size: 2.5rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
        }

        .container {
            position: relative;
            width: 100%;
            max-width: 600px;
            height: 300px;
        }

        .buttons {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 20px;
            margin-top: 30px;
        }

        button {
            padding: 15px 35px;
            font-size: 1.2rem;
            font-weight: bold;
            border-radius: 50px;
            border: none;
            cursor: pointer;
            transition: all 0.2s ease;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }

        #yesBtn {
            background-color: #ff4d6d;
            color: white;
            z-index: 10;
        }

        #noBtn {
            background-color: #800f2f;
            color: white;
            position: absolute;
        }

        .celebration-gif {
            width: 80%;
            max-width: 400px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        }
    </style>
</head>
<body>

    <div id="content">
        <h1>Minaxi, will you be my Valentine? 🌹</h1>
        <div class="container">
            <div class="buttons">
                <button id="yesBtn" onclick="celebrate()">Yes!</button>
                <button id="noBtn" onmouseover="escape()">No</button>
            </div>
        </div>
    </div>

    <script>
        let yesSize = 1.2;

        function escape() {
            // Move the NO button
            const btn = document.getElementById('noBtn');
            const x = Math.random() * (window.innerWidth - btn.offsetWidth);
            const y = Math.random() * (window.innerHeight - btn.offsetHeight);
            
            btn.style.left = x + 'px';
            btn.style.top = y + 'px';

            // Make the YES button bigger!
            yesSize += 0.2;
            document.getElementById('yesBtn').style.transform = `scale(${yesSize})`;
        }

        function celebrate() {
            const content = document.getElementById('content');
            content.innerHTML = `
                <h1>Yay! See you on Valentine's Day, Minaxi! 🥰</h1>
                <img class="celebration-gif" src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExOHJueWp6ZzRyeGZ6ZzRyeGZ6ZzRyeGZ6ZzRyeGZ6ZzRyeGZ6JmVwPXYxX2ludGVybmFsX2dpZl9ieV9pZCZjdD1n/lTQF0ODLLJHzaOBCfy/giphy.gif" alt="Happy">
            `;
        }
    </script>
</body>
</html>
