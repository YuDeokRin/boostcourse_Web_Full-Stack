# 7) WAS

**들어가기 전에**

WAS는 무엇이고, 왜 필요한지 그리고, 어떤 종류의 WAS가 있는지 알아봅니다.

또한, 웹서버와의 차이점은 무엇인지 알아봅니다.

**학습 목표**

1) /WAS가 무엇인지 알 수 있다.

2) WAS의 종류를 알아본다.

3) 웹서버와 WAS의 차이점을 설명할 수 있다.

**핵심 개념**

- WAS (Web Application Server)
- Apache Tomcat

---

**클라이언트/서버 구조**

클라이언트(Client)는 서비스(Service)를 제공하는 서버(Server)에게 정보를 요청하여 응답 받은 결과를 사용합니다.


![Untitled](https://user-images.githubusercontent.com/56623911/136216758-059fdca6-0818-4425-9fea-9f52a0cc130c.png)

---

**DBMS (DataBase Management System)**

다수의 사용자가 데이터베이스 내의 데이터에 접근할 수 있도록 해주는 소프트웨어입니다.

![Untitled 1](https://user-images.githubusercontent.com/56623911/136216800-63d64e0e-d48f-482c-9d2a-cdad4eeffb6b.png)


---

**미들웨어 (MiddleWare)**

클라이언트 쪽에 비즈니스 로직이 많을 경우, 클라이언트 관리(배포 등)로 인해 비용이 많이 발생하는 문제가 있습니다.

비즈니스 로직을 클라이언트와 DBMS사이의 미들웨어 서버에서 동작하도록 함으로써 클라이언트는 입력과 출력만 담당하도록 합니다.

![Untitled 2](https://user-images.githubusercontent.com/56623911/136216860-61aae897-039a-4203-bad3-95e1f8fb6f35.png)

---

**WAS (Web Application Server)**

WAS는 일종의 미들웨어로 웹 클라이언트(보통 웹 브라우저)의 요청 중 웹 애플리케이션이 동작하도록 지원하는 목적을 가집니다.

![Untitled 3](https://user-images.githubusercontent.com/56623911/136216886-89937b0f-f7cc-417d-ac52-9d27e436b4cb.png)

**웹 서버 vs WAS**

- WAS도 보통 자체적으로 웹 서버 기능을 내장하고 있습니다.
- 현재는 WAS가 가지고 있는 웹 서버도 정적인 콘텐츠를 처리하는 데 있어서 성능상 큰 차이가 없습니다.
- 규모가 커질수록 웹 서버와 WAS를 분리합니다.
- 자원 이용의 효율성 및 장애 극복, 배포 및 유지보수의 편의성을 위해 웹서버와 WAS를 대체로 분리합니다.
