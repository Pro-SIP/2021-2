<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>우주 테마 게임</title>
    <style>
        /* 이전 스타일 코드는 그대로 유지 */
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
