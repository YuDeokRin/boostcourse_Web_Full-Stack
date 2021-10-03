# 3) 웹 Front-End 와 웹 Back-End-1

---

**들어가기 전에**

웹은 프론트엔드(FE)와 백엔드(BE)로 나눠집니다.

우리가 인터넷을 하기 위해서 브라우저에서 웹을 탐색하곤 하는데요.

브라우저를 프론트엔드 또는 클라이언트라고도 합니다.

웹백엔드는 인터넷 사용자에게는 보이지 않는 것이죠.

각각의 역할을 기술적인 관점에서 알아보도록 하죠.

---

**학습 목표**

1) 웹프론트엔드에 대한 역할과 기술적 구성

2) 웹백엔드에 대한 역할과 기술적 구성

---

**핵심 개념**

- HTML
- CSS
- JavaScript
- 클라이언트
- 서버

---

**웹프론트엔드?**

사용자에게 웹을 통해 다양한 콘텐츠(문서, 동영상, 사진 등)를 제공합니다.

또한, 사용자의 요청(요구사항)에 반응해서 동작합니다.

---

**웹프론트엔드의 역할**

- 웹콘텐츠를 잘 보여주기 위해 구조를 만들어야 합니다.(신문,책등과 같이) - HTML
- 적절한 배치와 일관된 디자인 등을 제공해야 합니다.(보기 좋게) - CSS
- 사용자 요청을 잘 반영해야 합니다.(소통하듯이)(주로 동적) - Javascript

---

**HTML 코드 예시**

원하는 문서의 구조를 프로그래밍 언어로 표현해야 합니다.

HTML이라는 것은 그 구조를 잘 표현해 줍니다.

```html
<h1>  덕린이 노션  </h1>
<section >
   <h2> 위치</h2>
    <p> 경기도 의왕시 어딘가 위치하고 있어요~</p>
   <h2> 특징</h2>
    <p>  우리집은 마루가 아주 작아요~  하지만 옹기종기 모여있기 좋은 구조에요</p>
</section>
<footer>email : ejrfls12@Hi.com</footer>
```

---

**스타일 - CSS 코드예시**

웹페이지를 꾸미기 위해서는 각각의 HTML 태그(문서의 구조를 표현한 각 조각 단위)를 꾸미기 위한 규칙이 필요합니다

CSS는 이를 표현할 수 있는 프로그래밍 언어입니다.

```css
.window-header-icon {
left: -28px;
position: absolute;
top: 8px
}

.window-header-inline-content {
cursor: default;
display: inline-block;
margin: 4px 6px 0 0
}
```

---

**동작 - JavaScript 코드예시**

HTML,CSS를 이리저리 움직이고 변경할 필요가 있을 거예요.

JavaScript가 그걸 해줍니다.

```jsx
let aCardList = [];
for (var i = 0; i < cardList.length; i++) {
let str =`${cardList[i]}번째 카드`;
let id = `list-${cardList[i]}`;
aCardList.push(<li id={id} key={i} draggable='true' onDragStart={dragStart}> {str} </li>)
```
