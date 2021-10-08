# 4) class 와 id 속성

**들어가기 전에**

HTML 속성 중 class와 id란 무엇이며 어떻게 사용할까요?

이번 시간에는 고유한 값인 id와 중복 사용이 가능한 class의 활용 방법에 대해 알아보도록 하겠습니다.

다른 웹 사이트에서 class와 id를 어떻게 사용했는지 확인해보며 이해를 도모하는 것도 좋은 방법입니다.

**학습 목표**

1) CLASS와 ID의 목적을 이해하고, 구분해서 작성할 수 있다.

**핵심 개념**

- HTML 태그 안에서 사용되는 class속성과 ID속성

**ID**

- 고유한 속성으로 한 HTML 문서에 하나만 사용 가능합니다.
- 고유한 ID 값이 있으면 하나하나에 특별한 제어를 할 수 있으며 검색에도 용이합니다.

**Class**

- 하나의 HTML문서 안에 중복해서 사용 가능합니다.
- 하나의 태그에 여러 개의 다른 class 이름을 공백을 기준으로 나열할 수가 있습니다.
- 홈페이지 전체적인 스타일을 일관성 있게 지정하기 위해서는 class의 사용이 필수적입니다.

- 실습코드

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>JS Bin</title>
</head>
<body>
  <header>
  <h1>Company Name</h1>
  <img src="..." alt="logo">
  </header>
  
  <section id="nav-section">
    <nav><ul>
      <li>Home</li>
      <li>Home</li>
      <li>About</li>
      <li>Map</li>
      </ul>
    </nav>
    
    <section id="roll-section">
      <button></button>
      <div><img src="dd" alt=""></div>
      <div><img src="dd" alt=""></div>
      <div><img src="dd" alt=""></div>
      <button></button>
    </section>
    <section>
      <ul>
        <li class="our_diescriptipn">
          <h3>What we do</h3>
          <div>Lorem ipsum dolor sit amet, consectetur adipisicing</div>
        </li>
        <li class="our_diescriptipn">
          <h3>What we do</h3>
          <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Similique accusamus, corporis, dolorum fugiat tenetur porro. Aspernatur commodi, ea suscipit non? Molestiae nulla explicabo debitis provident nostrum dolorem minima reiciendis suscipit?</div>
        </li>
        <li class="our_diescriptipn">
          <h3>What we do</h3>
          <div>Lorem ipsum dolor sit amet, consectetur adipisicing</div>
        </li>
      </ul>
    </section>
  </section>
  <footer>
    <span>Copyright @codesquad</span>
  </footer>
</body>
</html>
```