# 1) CSS 선언방법

**들어가기 전에**

CSS를 HTML안에 선언하는 방식은 크게 3가지가 있습니다.

이를 잘 이해하고 활용하는 것이 좋습니다.

---

**학습 목표**

1) CSS선언 방식을 이해하고 활용할 수 있다.

---

**핵심 개념**

---

- inline
- internal
- external

---

### CSS3

CSS(Cascading Style Sheet)는 HTML 문서에 색이나 모양, 출력 위치 등 외관을 꾸미는 언어이며, CSS로 작성된 코드를 스타일 시트(Style sheet)라고 부른다.
CSS는 CSS1이 나온 2002년이후 CSS2, CSS3로 발전하였다.

- 색상과 배경
- 텍스트
- 폰트
- 박스모델(Box Model)
- 비주얼과 포맷 및 효과
- 리스트
- 테이블
- 사용자 인터페이스

![Untitled](1)%20CSS%20%E1%84%89%E1%85%A5%E1%86%AB%E1%84%8B%E1%85%A5%E1%86%AB%E1%84%87%E1%85%A1%E1%86%BC%E1%84%87%E1%85%A5%E1%86%B8%20856b35a634614b3ea740ddde799cfb02/Untitled.png)

```css
span {
  color : red;
  }
```

- span : selector(선택자)
- color : property
- red : value

**style을 HTML페이지에 적용하는 3가지 방**

**1) inline**

HTML태그 안에다가 적용합니다.

다른 CSS파일에 적용한 것 보다 가장 먼저 적용합니다.

```css
<p style="border:1px solid gray;color:red;font-size:2em;">
```

**2) internal**

style 태그로 지정합니다.

구조와 스타일이 섞이게 되므로 유지보수가 어렵습니다.

별도의 CSS파일을 관리하지 않아도 되며 서버에 CSS파일을 부르기 위해 별도의 브라우저가 요청을 보낼 필요가 없습니다.

```css
<head>
<style>
p  {
  font-size : 2em;
  border:1px solid gray;
  color: red;
}
</style>
</head>

<body>
<div>...</div>
</body>
```

**3) external**

외부파일(.css)로 지정하는 방식입니다.

CSS 코드가 아주 짧지 않다면 가급적 이 방법으로 구현하는 것이 가장 좋습니다.

현업에서는 여러개의 CSS 파일로 분리하고 이를 합쳐서 서비스에서 사용하기도 합니다.

internal 코드와 같은 css코드를 구현하고, style.css와 같은 별도 파일로 만듭니다.

이후에 아래처럼 link태그로 추가하면 됩니다.

```css
<html>
	<head>
		<link rel="stylesheet" href="style.css">
	</head>
	<body>
		<div>
			<p>
				<ul>
					<li></li>
					<li></li>
					<li></li>
					<li></li>
				</ul>
			</p>
		</div>
	</body>
</html>
```

**4) 우선순위**

inline은 별도의 우선순위를 갖지만, internal 과 external은 우선순위가 동등합니다. 따라서 겹치는 선언이 있을 경우 나중에 선언된 속성이 반영됩니다.

CSS연습

- HTML 태그로만 작성한 웹 페이지 예제
    
    ```html
    <!DOCTYPE html>
    <html>
    <head>
      <meta charset="utf-8">
      <meta name="viewport" content="width=device-width">
      <title>스타일 없는 웹페이지</title>
    </head>
    <h3>CSS 스타일 맛보기</h3>
    <body
    <p>나는 <span>웹프로그래밍</span>을 좋아합니다.</p>
    </body>
    </html>
    ```
    
- 결과
    
    ![Untitled](1)%20CSS%20%E1%84%89%E1%85%A5%E1%86%AB%E1%84%8B%E1%85%A5%E1%86%AB%E1%84%87%E1%85%A1%E1%86%BC%E1%84%87%E1%85%A5%E1%86%B8%20856b35a634614b3ea740ddde799cfb02/Untitled%201.png)
    

- CSS3 스타일 시스토 꾸민 웹페이지
    
    ```html
    <!DOCTYPE html>
    <html>
    <head>
      <meta charset="utf-8">
      <meta name="viewport" content="width=device-width">
      <title>스타일을 가진 웹페이지</title>
      <style>
        /* CSS3 스타일 시트 작성 */
        body {background-color: mistyrose;}
        h3 {color: purple;}
        hr {border: 5px solid yellowgreen;}
        span {color :blue; font-size: 20px;}
      </style>
    </head>
    <h3>CSS 스타일 맛보기</h3>
    <body
    <p>나는 <span>웹프로그래밍</span>을 좋아합니다.</p>
    </body>
    </html>
    ```
    
- 결과
    
    ![Untitled](1)%20CSS%20%E1%84%89%E1%85%A5%E1%86%AB%E1%84%8B%E1%85%A5%E1%86%AB%E1%84%87%E1%85%A1%E1%86%BC%E1%84%87%E1%85%A5%E1%86%B8%20856b35a634614b3ea740ddde799cfb02/Untitled%202.png)