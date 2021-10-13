# 2) forward

**들어가기 전에**

WAS의 서블릿이나 JSP가 요청을 받은 후 그 요청을 처리하다가, 추가적인 처리를 같은 웹 어플리케이션안에 포함된 다른 서블릿이나 JSP에게 **위임**하는 경우가 있습니다.

이렇게 **위임하는 것**을 **포워드(forward)**라고 합니다.

이번 시간엔 이러한 포워드에 대해서 좀 더 자세히 알아보도록 하겠습니다.

**학습 목표**

1) foward를 이해한다.

2) foward를 사용 할 수 있다.

**핵심 개념**

- RequestDispatcher
- forward()

![Untitled](2)%20forward%2044fa2511d1a341c0a6d66d3ad39fc926/Untitled.png)

**forward란?**

1) 웹 브라우저에서 Servlet1에게 요청을 보냄

2) Servlet1은 요청을 처리한 후, 그 결과를 HttpServletRequest에 저장

3) Servlet1은 결과가 저장된 HttpServletRequest와 응답을 위한 HttpServletResponse를 같은 웹 어플리케이션 안에 있는 Servlet2에게 전송(forward)

4) Servlet2는 Servlet1으로 부터 받은 HttpServletRequest와 HttpServletResponse를 이용하여 요청을 처리한 후 웹 브라우저에게 결과를 전송

01

```java
package examples;

import java.io.IOException;

import javax.servlet.RequestDispatcher;
import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;

/**
 * Servlet implementation class FrontServlet
 */
@WebServlet("/FrontServlet")
public class FrontServlet extends HttpServlet {
	private static final long serialVersionUID = 1L;
       
    /**
     * @see HttpServlet#HttpServlet()
     */
    public FrontServlet() {
        super();
        // TODO Auto-generated constructor stub
    }

	/**
	 * @see HttpServlet#service(HttpServletRequest request, HttpServletResponse response)
	 */
	protected void service(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
		// TODO Auto-generated method stub
		int diceValue = (int)(Math.random()*6)+1;
		request.setAttribute("dice", diceValue);
		
		RequestDispatcher requestDispatcher = request.getRequestDispatcher("/next");
		requestDispatcher.forward(request, response);
	}

}
```

02

```java
package examples;

import java.io.IOException;
import java.io.PrintWriter;

import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;

/**
 * Servlet implementation class NextServlet
 */
@WebServlet("/next")
public class NextServlet extends HttpServlet {
	private static final long serialVersionUID = 1L;
       
    /**
     * @see HttpServlet#HttpServlet()
     */
    public NextServlet() {
        super();
        // TODO Auto-generated constructor stub
    }

	/**
	 * @see HttpServlet#service(HttpServletRequest request, HttpServletResponse response)
	 */
	protected void service(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
		// TODO Auto-generated method stub
        response.setContentType("text/html");
        PrintWriter out = response.getWriter();
        out.println("<html>");
        out.println("<head><title>form</title></head>");
        out.println("<body>");

        int dice = (Integer)request.getAttribute("dice");
        out.println("dice : " + dice);
        for(int i = 0; i < dice; i++) {
            out.print("<br>hello");
        }
        out.println("</body>");
        out.println("</html>");
	}

}
```

- 결과
    
    ![Untitled](2)%20forward%2044fa2511d1a341c0a6d66d3ad39fc926/Untitled%201.png)