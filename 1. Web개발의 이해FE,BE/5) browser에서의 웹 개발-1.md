# 5) browser에서의 웹 개발-1

**들어가기 전에**

웹 클라이언트 코드는 브라우저 안에서 동작합니다.

HTML, CSS, JavaScript의 실제 소스코드를 보면서 웹페이지 소스의 구성을 살펴봅니다.

**학습 목표**

1) HTML 요청 이후 브라우저에서 해석되는 웹페이지(HTML) 안의 내용구성과 소스코드를 어떻게 위치시키면될지 이해한다.

**핵심 개념**

- Browser 안에서 동작할 수 있는 HTML, CSS, JavaScript의 코드구현 방법

**HTML 문서구조**

뜯어보자 웹사이트!

1) 먼저 크롬브라우저가 없다면 설치하기

2) 크롬 브라우저를 열고 크롬 개발자도구 열기

3) 윈도우 (Ctrl + Shift + I)맥(Option + Command + i)

4) 접속 : [http://www.amazon.com](http://www.amazon.com/)

**알게 된 몇 가지 특징**

- HTML문서는 html이라는 태그로 시작해서 html태그로 끝납니다.
- head는 무엇을 하는 걸까요?
- body는 무엇을 하는 걸까요?
- HTML은 계층적입니다.
- HTML은 tag를 사용해서 표현합니다.

```html
<tag class="title">안녕하세요</tag>
```

- JavaScript와 CSS가 html 안에 여기저기 존재합니다.

실습코드

```jsx
<!DOCTYPE html>
<html>
    <head>
       <meta charset="utf-8">
        <meta name = "viewport" content="width =device-width, initial-scale=1">
        <title>저를 소개해요</title>
        <link rel="stylesheet" href="css/style.css">
        <script src="js/start.js"></script>
    </head>
    <body>
        <h1>안녕하세요 </h1>
        <div>덕린입니다</div>
        <script src=""js/library.js></script>
        <script src="js/main.js"></script>
    </body>
</html>
```