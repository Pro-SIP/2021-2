<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>우주 테마 게임</title>
    <style>
        body, html {
            height: 100%;
            margin: 0;
            font-family: 'Noto Sans KR', sans-serif;
            background: linear-gradient(135deg, #0d1117 0%, #161b22 100%);
            display: flex;
            justify-content: center;
            align-items: center;
            color: #c9d1d9;
            overflow: hidden;
        }
        .stars {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            background-image: 
                radial-gradient(2px 2px at 20px 30px, #eee, rgba(0,0,0,0)),
                radial-gradient(2px 2px at 40px 70px, #fff, rgba(0,0,0,0)),
                radial-gradient(2px 2px at 50px 160px, #ddd, rgba(0,0,0,0)),
                radial-gradient(2px 2px at 90px 40px, #fff, rgba(0,0,0,0)),
                radial-gradient(2px 2px at 130px 80px, #fff, rgba(0,0,0,0)),
                radial-gradient(2px 2px at 160px 120px, #ddd, rgba(0,0,0,0));
            background-repeat: repeat;
            background-size: 200px 200px;
            animation: zoom 10s infinite;
            opacity: 0.3;
        }
        @keyframes zoom {
            0% { transform: scale(1); }
            50% { transform: scale(1.5); }
            100% { transform: scale(1); }
        }
        .container {
            text-align: center;
            background-color: rgba(13, 17, 23, 0.8);
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
            z-index: 1;
        }
        h1 {
            font-size: 3em;
            margin-bottom: 30px;
            color: #58a6ff;
            text-shadow: 0 0 10px #58a6ff, 0 0 20px #58a6ff, 0 0 30px #58a6ff;
        }
        .button-section {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }
        button {
            padding: 15px 30px;
            font-size: 1.2em;
            cursor: pointer;
            border: 2px solid #58a6ff;
            border-radius: 5px;
            background-color: rgba(88, 166, 255, 0.1);
            color: #58a6ff;
            transition: all 0.3s;
            text-transform: uppercase;
            letter-spacing: 2px;
        }
        button:hover {
            background-color: rgba(88, 166, 255, 0.3);
            box-shadow: 0 0 15px #58a6ff;
        }
    </style>
</head>
<body>
    <div class="stars"></div>
    <div class="container">
        <h1>게임 타이틀</h1>
        <div class="button-section">
            <button id="start-game">게임 시작</button>
            <button id="settings">설정</button>
            <button id="rankings">랭킹 보기</button>
        </div>
    </div>

    <script>
         document.getElementById('start-game').addEventListener('click', () => {
            window.location.href = 'start.html'; // 게임 시작 페이지로 이동
        });

        document.getElementById('settings').addEventListener('click', () => {
            alert('설정 메뉴를 엽니다.');
        });

        document.getElementById('rankings').addEventListener('click', () => {
            alert('랭킹을 표시합니다.');
        });
    </script>
</body>
</html>

<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>게임 시작</title>
    <style>
        body, html {
            height: 100%;
            margin: 0;
            font-family: 'Noto Sans KR', sans-serif;
            background: linear-gradient(135deg, #0d1117 0%, #161b22 100%);
            display: flex;
            justify-content: center;
            align-items: center;
            color: #c9d1d9;
        }
        .game-container {
            text-align: center;
            background-color: rgba(13, 17, 23, 0.8);
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
        }
        h1 {
            color: #58a6ff;
            margin-bottom: 20px;
        }
        #word-display {
            font-size: 2em;
            margin-bottom: 20px;
            color: #fff;
        }
        input {
            padding: 10px;
            font-size: 1em;
            width: 80%;
            margin-bottom: 20px;
            background-color: #0d1117;
            border: 1px solid #30363d;
            color: #c9d1d9;
            border-radius: 5px;
        }
        #score, #timer {
            font-size: 1.2em;
            margin-bottom: 10px;
        }
    </style>
</head>
<body>
    <div class="game-container">
        <h1>단어 타이핑 게임</h1>
        <div id="word-display">단어가 여기에 나타납니다</div>
        <input type="text" id="word-input" placeholder="단어를 입력하세요">
        <div id="score">점수: 0</div>
        <div id="timer">남은 시간: 60초</div>
    </div>

    <script>
        // 여기에 게임 로직을 추가할 수 있습니다
        // 예: 단어 표시, 타이머 설정, 점수 계산 등
    </script>
</body>
</html>
