# 3) Servlet & JSP연동

**들어가기 전에**

서블릿과 JSP는 서로 상호 보완적인 관계를 가지고 있습니다.

서블릿은 로직을 구현하기에 알맞지만, HTML을 출력하기엔 불편합니다.

JSP는 로직을 구현하는 것은 불편하지만 HTML을 출력하기엔 편리합니다.

이러한 서블릿과 JSP를 좀 더 잘 사용하기 위해서 forward가 사용되는 경우가 많습니다.

이번 시간엔 서블릿과 JSP의 연동에 대해 알아보도록 하겠습니다.

**학습 목표**

1) 서블릿과 JSP를 적절히 이용해서 포워딩을 효율적으로 사용할 수 있다.

**핵심 개념**

- forward
- request.setAttribute()
- request.getAttribute()

**Servlet과 JSP연동**

- Servlet은 프로그램 로직이 수행되기에 유리하다. IDE 등에서 지원을 좀 더 잘해준다.
- JSP는 결과를 출력하기에 Servlet보다 유리하다. 필요한 html문을 그냥 입력하면 됨.
- 프로그램 로직 수행은 Servlet에서, 결과 출력은 JSP에서 하는 것이 유리하다.
- Servlet과 JSP의 장단점을 해결하기 위해서 Servlet에서 프로그램 로직이 수행되고, 그 결과를 JSP에게 포워딩하는 방법이 사용되게 되었다. 이를 Servlet과 JSP연동이라고 한다.

![Untitled](3)%20Servlet%20&%20JSP%E1%84%8B%E1%85%A7%E1%86%AB%E1%84%83%E1%85%A9%E1%86%BC%207b7b100a8a974650bc999694792f8b72/Untitled.png)

01.Servlet파일

```java
import java.io.IOException;

import javax.servlet.RequestDispatcher;
import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;

/**
 * Servlet implementation class LogicServlet
 */
@WebServlet("/logic")
public class LogicServlet extends HttpServlet {
	private static final long serialVersionUID = 1L;
       
    /**
     * @see HttpServlet#HttpServlet()
     */
    public LogicServlet() {
        super();
        // TODO Auto-generated constructor stub
    }

	/**
	 * @see HttpServlet#service(HttpServletRequest request, HttpServletResponse response)
	 */
	protected void service(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
		// TODO Auto-generated method stub
		int v1 = (int)(Math.random()*100)+1;	
		int v2 = (int)(Math.random()*100)+1;
		int result = v1 + v2 ;
		
		request.setAttribute("v1", v1);
		request.setAttribute("v2", v2);
		request.setAttribute("result", result);
		
		RequestDispatcher  rd = request.getRequestDispatcher("/result.jsp");
		rd.forward(request, response);
		
	}

}
```

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
<%
	int v1 = (int)request.getAttribute("v1");
	int v2 = (int)request.getAttribute("v2");
	int result = (int)request.getAttribute("result");
%>

<%=v1%> + <%=v2%> + <%=result%>;
</body>
</html>
```

- 결과
    
    ![Untitled](3)%20Servlet%20&%20JSP%E1%84%8B%E1%85%A7%E1%86%AB%E1%84%83%E1%85%A9%E1%86%BC%207b7b100a8a974650bc999694792f8b72/Untitled%201.png)