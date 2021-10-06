# 1)HTML Tags

**들어가기 전에**

HTML 태그는 많은 종류를 가지고 있고 각각의 쓰임새에 대한 정확한 의미가 있지요.

'각각의 의미를 지닌다'는 것을 'Semantic한 태그' 혹은 'Semantic하다'라고 표현을 하곤 합니다.

그렇다면 많은 태그를 각각의 용도와 쓰임에 맞게 잘 사용해야겠지요?

이번 시간에는 그 의미에 맞게 사용할 수 있도록, HTML의 중요한 태그에 대해서 알아보도록 하겠습니다.

**학습 목표**

1) HTML 태그를 이해하고, 이를 사용할 줄 압니다.

**HTML tag의 종류**

태그는 그 의미에 맞춰서 사용해야 합니다.

- 링크
- 이미지
- 목록
- 제목

anchor 태그, img 태그, ul/li 태그, heading 태그, p 태그 등이 자주 사용됩니다.

그 밖에 가장 많이 사용하는 div태그가 있습니다.

div 태그는 block 엘리먼트라고 하는데 일반적인 영역을 표현할 때 가장 많이 사용합니다.

많은 태그를 모두 외울 필요는 없으며, 필요한 태그를 찾아서 적절한 의미에 맞는 태그를 사용하는 것이 중요합니다.

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
  <div> 
    <h1>반갑습니다.</h1>
    여기 여러 분들이 좋아하는 과일이 있어요.
    <ul>
      <li><a href="www.apple.com">사과</a></li>
      <li>바나나</li>
      <li>메론</li>
      <li>귤</li>
    </ul>
  </div>
  
</body>
</html>
```

---

### 수업 외에 태그들 정리  & 연습

- HTML 태그로만 구성된 웹페이지 : test1.html

```html
<!DOCTYPE html>
<html>
<head>
<title>웹페이지의 구성 요소</title>    
</head>
<body>
    <h3>Elvis Presley</h3>
    <hr>
    He was an American singer and actor. In November 1956, he mad his film debut in <span>Love Me Tender</span>. 
    He is often referred to as "<span>the King of Rock and Roll</span> ".
</body>

</html>
```

- 결과
    ![Untitled](https://user-images.githubusercontent.com/56623911/136217577-0356e233-b33e-46aa-a97e-a4418ad257b9.png)

  
