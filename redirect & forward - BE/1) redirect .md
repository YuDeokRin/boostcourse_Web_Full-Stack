# 1) redirect

**들어가기 전에**

게시판 같은 곳에서 글을 작성하는 경우가 있습니다.

글을 모두 작성한 후에 글 작성 버튼을 클릭하겠죠?

이때 클라이언트가 서버에게 글을 작성해주세요 라는 요청을 보내게 됩니다.

서버는 해당 글을 저장한 후, 웹 브라우저에게 글 목록으로 이동하라고 응답을 보내게 됩니다.

웹 브라우저는 글 목록으로 이동하라는 서버의 요청을 받은 후, 자동으로 서버에게 글 목록을 요청하여 응답받아 출력하게 됩니다.

서버가 클라이언트에게 어떤 URL로 이동하라는 요청을 보내는 것을 리다이렉트라고 합니다.

**학습 목표**

1) 리다이렉트를 이해한다.

2) 리다이렉트를 사용 할 수 있다.

**핵심 개념**

- HttpServletResponse
- sendRedirect()

**리다이렉트 (redirect)**

- 리다이렉트는 HTTP프로토콜로 정해진 규칙이다.
- **서버는 클라이언트의 요청에 대해 특정 URL로 이동을 요청**할 수 있다. 이를 리다이렉트라고 한다.
- 서버는 클라이언트에게 HTTP 상태코드 302로 응답하는데 이때 헤더 내 Location 값에 이동할 URL 을 추가한다. 클라이언트는 리다이렉션 응답을 받게 되면 헤더(Location)에 포함된 URL로 재요청을 보내게 된다. 이때 브라우저의 주소창은 새 URL로 바뀌게 된다.
- 클라이언트는 서버로부터 받은 상태 값이 302이면 Location헤더값으로 재요청을 보내게 된다. 이때 브라우저의 주소창은 전송받은 URL로 바뀌게 된다.
- 서블릿이나 JSP는 리다이렉트하기 위해 HttpServletResponse 클래스의 sendRedirect() 메소드를 사용한다.

01.redirect1에서 redirect2로 sendRedirect를 보낸다

```java
<%@ page language="java" contentType="text/html; charset=EUC-KR"
    pageEncoding="EUC-KR"%>

<%
	response.sendRedirect("redirect2.jsp");
%>
```

02.

```java
<%@ page language="java" contentType="text/html; charset=EUC-KR"
    pageEncoding="EUC-KR"%>
<!DOCTYPE html>
<html>
<head>
<meta charset="EUC-KR">
<title>Insert title here</title>
</head>
<body>
	redirect된 페이지 
</body>
</html>
```

- 결과

![Untitled](https://user-images.githubusercontent.com/56623911/137100144-e32f1f9b-8090-4d77-a30d-d361701e12e8.png)

![Untitled 1](https://user-images.githubusercontent.com/56623911/137100179-e84ff711-2952-4585-a7de-24033d5ccc93.png)

- 브라우저에서 리다이렉트 확인

![Untitled 2](https://user-images.githubusercontent.com/56623911/137100194-d04ec897-1528-4c09-b391-963e0089de25.png)
