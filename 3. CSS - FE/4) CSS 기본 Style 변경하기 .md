# 4) CSS 기본 Style 변경하기

**들어가기 전에**

글자색, 배경색, 글꼴은 어떻게 바꾸는 것일까요?

이번 시간에는 텍스트 속성 및 옵션값을 변경하는 방법에 대해서 배워보도록 하겠습니다.

---

**학습 목표**

1. CSS 없이 먼저 HTML구조를 설계할 수 있다.

---

**핵심 개념**

- font-size
- background-color
- font-family

---

CSS style 적용은 글자색, 배경색 등이 가장 자주 사용되는 것들입니다.

이런 속성은 위치 값과 크기를 지정하는 것과 달리, 색상 위주로 값을 부여합니다.

색상 관련 값은 다양한 색을 일관된 방법으로 표현하기 위해 주로 16진수 표기법을 사용합니다.

---

**font 색상 변경**

- color : red;
- color : rgba(255, 0, 0, 0.5);
- color : #ff0000; //16진수 표기법으로 가장 많이 사용되는 방법이죠.

---

**font 사이즈 변경**

- font-size : 16px;
- font-size : 1em;

---

**배경색**

- background-color : #ff0;
- background-image, position, repeat 등의 속성이 있습니다.
- background : #0000ff url(“.../gif”) no-repeat center top; //한 줄로 정의도 가능

---

**글씨체/글꼴**

- font-family:"Gulim";
- font-family : monospace;

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>JS Bin</title>
  <style>
    body > div {
      font-size:16px;
      background-color: #ff0;
      font-family:"Gulim";
    }
    
    .myspan {
      color : #f00;
      font-size:2em;
    }
  </style>
</head>
<body>
  <div>
    <span class="myspan">my text is upper!</span>
  </div>
</body>
</html>
```