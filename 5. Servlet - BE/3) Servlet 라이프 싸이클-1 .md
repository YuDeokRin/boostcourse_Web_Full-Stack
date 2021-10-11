# 3) Servlet 라이프 싸이클-1

**들어가기 전에**

어떤 객체의 생성부터 소멸까지의 과정을 라이프 사이클(Life Cycle)라고 합니다.

이번 학습에서는 서블릿의 라이프 사이클을 알아봅니다.

---

**학습 목표**

1. 서블릿의 생명주기를 이해합니다.

---

**핵심 개념**

- init
- service
- destory

**LifecycleServlet**

HttpServlet의 3가지 메소드를 오버라이딩

- init()
- service(request, response)
- destroy()