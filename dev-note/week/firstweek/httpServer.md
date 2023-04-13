# 3. HTTP Server

## 1. Listen

다른 곳에서 접속하는 것이 아니라 포트 번호만 정하면 된다.

    int port = 8080;

Java에서는 ServerSocket이라는 별도의 클래스를 사용.

    ServerSocket listener = new ServerSocket(8080, 0);

  > 여기 까지만 하고 나서 Gradle로 실행 했을 때 Listner가 요청을 받을때 까지 기다리는데 Blocking이라고 함
  > Blocking : 파일 읽기, 쓰기 모두 Blocking 이지만, TCP 통신에서는 네트워크 같은 요인에 의해 크게 지연될 수 있고, accept처럼 상대방의 요청이 없으면 영원히 기다리는 경우도 생길 수 있다    
  > : 멀티스레드나 비동기, 이벤츠 기반 처리 등이 필요한 이유

서버의 입장에서는 Request를 받음 <-> 클라이언트는 Request를 보냄

* [ 실습코드 ](dev-note/week/firstweek/httpServerExam.md)