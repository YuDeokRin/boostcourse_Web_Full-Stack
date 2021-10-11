# 3) Servlet 라이프 싸이클-2

**들어가기 전에**

어떤 객체의 생성부터 소멸까지의 과정을 라이프 사이클(Life Cycle)라고 합니다.

이번 학습에서는 서블릿의 라이프 사이클을 알아봅니다.

---

**학습 목표**

1) 서블릿의 생명주기를 이해합니다.

**핵심 개념**

- init
- service
- destory

**Servlet**


![Untitled](https://user-images.githubusercontent.com/56623911/136806905-5e5fb3e5-cab0-40aa-81a2-3e75c3a5523d.png)


**Servlet 생명주기**

- WAS는 서블릿 요청을 받으면 해당 서블릿이 메모리에 있는지 확인합니다.
- if (메모리에 없음) { - 해당 서블릿 클래스를 메모리에 올림 - init() 메소드를 실행} - service()메소드를 실행
- was가 종료되거나, 웹 어플리케이션이 새롭게 갱신될 경우 destroy() 메소드가 실행됩니다.

**service(request, response) 메소드**

HttpServlet의 service메소드는 템플릿 메소드 패턴으로 구현합니다.

- 클라이언트의 요청이 GET일 경우에는 자신이 가지고 있는 doGet(request, response)메소드를 호출
- 클라이언트의 요청이 Post일 경우에는 자신이 가지고 있는 doPost(request, response)를 호출
