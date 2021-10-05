# 5) browser에서의 웹 개발-2

---

**들어가기 전에**

웹 클라이언트 코드는 브라우저 안에서 동작합니다.

HTML, CSS, JavaScript의 실제 소스코드를 보면서 웹페이지 소스의 구성을 살펴봅니다.

---

**학습 목표**

1) HTML 요청 이후 브라우저에서 해석되는 웹페이지(HTML) 안의 내용구성과 소스코드를 어떻게 위치시키면될지 이해한다.

---

**핵심 개념**

- Browser 안에서 동작할 수 있는 HTML, CSS, JavaScript의 코드구현 방법

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>boostcourse</title>
  <link rel="stylesheet" href="./main.js"
</head>
<body>
  <div>웹프론트엔드</div>
  <script src="./main.js">    </script>
</body>
    
</html>
```

- 실습코드

```html
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>저를소개해요</title>
    <link rel="stylesheet" href="css/style.css">
    <script src="js/start.js"></script>
  </head>
  <body>
    <h1>안녕하세요</h1>
    <div>코드스쿼드 크롱이라고 합니다</div>
    <script src="js/library.js"></script>
    <script src="js/main.js"></script>
  </body>
</html>
```