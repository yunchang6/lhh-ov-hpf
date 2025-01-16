<html lang="zh-cn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>给欢欢的表白</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background: linear-gradient(135deg, #e0c3fc 0%, #8ec5fc 100%);
            font-family: 'Arial', sans-serif;
            margin: 0;
            overflow: hidden;
        }
        .background {
            position: absolute;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255, 255, 255, 0.1), rgba(0, 0, 0, 0.1));
            animation: moveBackground 20s linear infinite;
        }
        @keyframes moveBackground {
            0% { transform: translate(-50%, -50%) rotate(0deg); }
            100% { transform: translate(-50%, -50%) rotate(360deg); }
        }
        .container {
            position: relative;
            text-align: center;
            background: rgba(255, 255, 255, 0.8);
            padding: 50px;
            border-radius: 15px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            animation: fadeIn 2s ease-in-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        h1 {
            font-size: 3em;
            color: #8a2be2;
            animation: fadeIn 3s ease-in-out;
        }
        p {
            font-size: 1.5em;
            color: #333;
            animation: fadeIn 4s ease-in-out;
        }
        .heart {
            color: #8a2be2;
            font-size: 5em;
            animation: heartbeat 1.5s infinite, fadeIn 5s ease-in-out;
        }
        @keyframes heartbeat {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.2); }
        }
        .floating-hearts {
            position: absolute;
            top: 0;
            left: 50%;
            width: 100%;
            height: 100%;
            pointer-events: none;
            overflow: hidden;
        }
        .floating-hearts div {
            position: absolute;
            bottom: -100px;
            width: 15px;
            height: 15px;
            background: rgba(138, 43, 226, 0.7);
            animation: float 10s infinite;
            border-radius: 50%;
        }
        @keyframes float {
            0% {
                transform: translateX(0) translateY(0);
                opacity: 1;
            }
            100% {
                transform: translateX(calc(100vw - 50%)) translateY(-100vh);
                opacity: 0;
            }
        }
        .shooting-stars {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            overflow: hidden;
        }
        .shooting-stars div {
            position: absolute;
            top: -50px;
            width: 2px;
            height: 100px;
            background: linear-gradient(to bottom, rgba(255, 255, 255, 1), rgba(255, 255, 255, 0));
            animation: shooting 3s infinite;
        }
        @keyframes shooting {
            0% {
                transform: translateX(0) translateY(0) rotate(45deg);
                opacity: 1;
            }
            100% {
                transform: translateX(100vw) translateY(100vh) rotate(45deg);
                opacity: 0;
            }
        }
        .shooting-stars div:nth-child(2) {
            animation-delay: 1s;
        }
        .shooting-stars div:nth-child(3) {
            animation-delay: 2s;
        }
    </style>
</head>
<body>
    <div class="background"></div>
    <div class="container">
        <h1>欢欢，我爱你！</h1>
        <p>你是我生命中最重要的人，愿我们永远在一起。</p>
        <div class="heart">❤️</div>
    </div>
    <div class="floating-hearts">
        <div></div>
        <div></div>
        <div></div>
    </div>
    <div class="shooting-stars">
        <div></div>
        <div></div>
        <div></div>
    </div>
</body>
</html>
