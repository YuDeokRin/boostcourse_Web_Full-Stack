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

![Untitled](3)%20Servlet%20%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%91%E1%85%B3%20%E1%84%8A%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%8F%E1%85%B3%E1%86%AF-2%202377d6b406df440ea7b3d9b7010672d2/Untitled.png)

**Servlet 생명주기**

- WAS는 서블릿 요청을 받으면 해당 서블릿이 메모리에 있는지 확인합니다.
- if (메모리에 없음) { - 해당 서블릿 클래스를 메모리에 올림 - init() 메소드를 실행} - service()메소드를 실행
- was가 종료되거나, 웹 어플리케이션이 새롭게 갱신될 경우 destroy() 메소드가 실행됩니다.

**service(request, response) 메소드**

HttpServlet의 service메소드는 템플릿 메소드 패턴으로 구현합니다.

- 클라이언트의 요청이 GET일 경우에는 자신이 가지고 있는 doGet(request, response)메소드를 호출
- 클라이언트의 요청이 Post일 경우에는 자신이 가지고 있는 doPost(request, response)를 호출