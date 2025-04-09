<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>도서관 관리 앱</title>
    <link rel="stylesheet" href="style.css"> <!-- 스타일 연결 -->
</head>
<body>
    <h1>도서관 관리 시스템</h1>

    <!-- 편집 모드 비밀번호 입력 -->
    <div id="edit-mode">
        <h2>편집 모드</h2>
        <label for="password">비밀번호 입력: </label>
        <input type="password" id="password" placeholder="비밀번호를 입력하세요">
        <button onclick="checkPassword()">편집 모드 들어가기</button>
    </div>

    <!-- 편집 모드에서 책 정보 등록 -->
    <div id="edit-form" style="display:none;">
        <h2>책 정보 등록</h2>
        <label for="book-name">책 이름: </label>
        <input type="text" id="book-name" placeholder="책 이름">
        <label for="call-number">청구 번호: </label>
        <input type="text" id="call-number" placeholder="청구 번호">
        <button onclick="addBook()">책 등록하기</button>
        <button onclick="goToViewMode()">시청 모드로 돌아가기</button> <!-- 시청 모드로 돌아가는 버튼 -->
    </div>

    <!-- 시청 모드 -->
    <div id="view-mode">
        <h2>시청 모드</h2>
        <label for="search">검색 (청구 번호 또는 키워드): </label>
        <input type="text" id="search" placeholder="청구 번호 또는 키워드를 입력하세요">
        <button onclick="searchBooks()">검색</button>
        <div id="search-results"></div>
        <button onclick="goToEditMode()">편집 모드로 돌아가기</button> <!-- 편집 모드로 돌아가기 버튼 -->
    </div>

    <script src="app.js"></script> <!-- 자바스크립트 연결 -->
</body>
</html>

