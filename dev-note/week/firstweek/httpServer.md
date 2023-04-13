# 3. HTTP Server

> ## 학습키워드
> * Java ServerSocket
> * Blocking vs Non-blocking

## 1. Listen

다른 곳에서 접속하는 것이 아니라 포트 번호만 정하면 된다.

    int port = 8080;

Java에서는 ServerSocket이라는 별도의 클래스를 사용.

    ServerSocket listener = new ServerSocket(8080, 0);

  > 여기 까지만 하고 나서 Gradle로 실행 했을 때 Listner가 요청을 받을때 까지 기다리는데 이것을 
  >Blocking이라고 함

    