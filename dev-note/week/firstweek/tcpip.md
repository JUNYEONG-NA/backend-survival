# 2. HTTP Client

## TCP/IP 통신

TCP/IP 를 기반으로 HTTP가 올라감

>인터넷 프로토콜 스위트      
>   : 인터넷 통신규약 모음

### TCP와 UDP
    전송 계층의 대표적인 프로토콜
* TCP : 연결이 필요함. 전달 및 순서 보장해줌. 데이터가 확실하게 도착(전화)     
* UDP : 연결하지 않고서 데이터를 보냄. 전달 및 순서를 보장 X

### Socket
    socket과 socket API 는 서로 구분할 줄 알아야함.    
    : socket - 프로세스 간 통신의 종단점

* HTTP/3 만 UDP를 이용한 QUIC 프로토콜 사용    
* HTTP/2는 SPDY 프로토콜을 기반으로 함    
    - ! 한번 찾아보기 

### TCP 통신순서

1. 서버는 접속 요청을 받기 위한 소켓을 연다 > Listen
2. 클라이언트는 소켓을 만들고, 서버에 접속 요청 > Connect
3. 서버는 접속 요청을 받아서 클라이언트와 통신 할 소켓을 따로 만듦 > Accept
        접속용 Socket != 통신용 Socket
4. 소켓을 통해 서로 데이터를 주고받음 > send & receive 반복
5. 통신을 마치면 소켓 close



### HTTP Client     

> 1. Connect
> 2. Request
> 3. Response
> 4. Close