<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Holo-Cube Tech Showcase</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: #121212;
            height: 100vh;
            overflow: hidden;
        }

        #cube-container {
            perspective: 1000px;
            width: 400px;
            height: 400px;
            position: relative;
        }

        #holo-cube {
            width: 100%;
            height: 100%;
            position: absolute;
            transform-style: preserve-3d;
            animation: rotateCube 10s infinite linear;
        }

        .cube-face {
            position: absolute;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.9);
            border: 2px solid #33FFCC; /* Neon Green */
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: 'Arial', sans-serif;
            font-size: 2rem;
            color: #33FFCC;
            text-align: center;
            transition: transform 0.5s, background-color 0.3s;
        }

        .cube-face:hover {
            transform: scale(1.1);
            background-color: rgba(0, 0, 0, 0.7);
        }

        #front  { transform: translateZ(200px); }
        #back   { transform: rotateY(180deg) translateZ(200px); }
        #left   { transform: rotateY(-90deg) translateZ(200px); }
        #right  { transform: rotateY(90deg) translateZ(200px); }
        #top    { transform: rotateX(90deg) translateZ(200px); }
        #bottom { transform: rotateX(-90deg) translateZ(200px); }

        @keyframes rotateCube {
            0% { transform: rotateY(0); }
            100% { transform: rotateY(360deg); }
        }

    </style>
</head>
<body>

    <div id="cube-container">
        <div id="holo-cube">
            <div id="front" class="cube-face">HTML, CSS, JS</div>
            <div id="back" class="cube-face">Node.js, Express</div>
            <div id="left" class="cube-face">React, Redux</div>
            <div id="right" class="cube-face">Python, Flask</div>
            <div id="top" class="cube-face">Git, GitHub</div>
            <div id="bottom" class="cube-face">SQL, MongoDB</div>
        </div>
    </div>

</body>
</html>
