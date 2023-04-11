# HTTP 기초

## HTTP란?

* Hypertext Transfer Protocol
* HTML과 같은 하이퍼미디어 문서를 전송하기 위한 규칙의 집합


### OSI 7 Layer

* OSI 7 Layer 중 2,3,4,7 계층만 살펴보자

> - 2계층   
> : 데이터 링크 계층 > MAC address   
> 기기에 할당된 고유 주소   

> - 3계층   
> : 네트워크 계층 > IP address   

> - 4계층   
> : TCP, UDP > PORT Number   
>  IP address로 기기를 찾아가서 '~~로 쓸거야'는 것을 드러냄   

        위 계층들은 인프라에 귀속됨

> - 7계층   
> : 응용계층 > HTTP, HTTPS(보안프로토콜 포함)   
> TCP >     > HTTP   
> TCP > TLS > HTTPS   
>  TCP에서 TLS라는 녀석을 거치면 HTTPS가 된다    


### 클라이언트 - 서버 모델

> 클라이언트(요청) > 서버(처리&응답) > 클라이언트     
> >여기서 처리하는 것은? 서비스/리소스를 처리 한다는것 > URL   
> >리소스 : 서비스의 자세한 내용   
> >URL  : 리소스를 보내기 위해서 가장 많이 사용하는 방법   


### 무상태

* HTTP는 각각의 요청에 독립적

##### 클라이언트는 항상 자신이 누군지 알려주어야함.
> How ?   
> - 요청과 응답을 통해 계속 쿠키를 주고받음   
> - 데이터는 서버에서 관리, 쿠키 등으로 key를 가지고서 관리하는 세션   
> - 웹 브라우저의 기능(localStorage 등)          
세션 자체는 서버에서 관리를 하긴 하지만   
세션에 대한 key는 대개 쿠키가 한다.   


### HTTP 메세지
* 사람이 읽을 수 있는 형태
* 요청과 응답 모두 동일한 구조
  * Start line > 요청과 응답의 형태가 다름
  * Headers
  * 빈 줄
  * Body
    1. 크기를 알기 어려움 - Headers에다가 Content-Length를 활용함
    2. Text 형태가 아닐 수 있음.
    3. multipart/form-data 처럼 데이터를 여러개 보낼 수 있음.

### HTTP 요청 메서드
<pre>
<code>
    POST / HTTP/1.1
</code>
</pre>
> * GET : Read(멱등성 보장)        
>       멱등성 : 같은걸 여러번 요청해도 바뀌지 않는 것   
> * HEAD : 바디 없이 헤드만 얻을 때   
> * POST : Submit(멱등성X) > Collection Pattern에서 Create로 사용   
> * PUT : Update(+Create) > Overwrite!!!!!!!   
> * PATCH : Update(Particial)(멱등성X)        
>       PUT과 PATCH는 비슷하게 만듦(원론적으론 X)   
> * DELETE : 삭제   
> * OPTIONS : 지원 확인   

### HTTP 응답 메서드
* Status code는 요청에 대해서 어떻게 되었다라는 것을 보내줌
<pre>
<code>
    HTTP/1.1 200 OK
</code>
</pre>
> 1~~ - 정보   
> 2~~ - 성공관련   
> 3~~ - 리다이렉션 > 304 Not Modified가 특수한 형태로 자주보임   
> 4~~ - 클라이언트 사이드 문제   
> 5~~ - 서버사이드    
<hr/>

## TCP/IP 통신

TCP/IP 를 기반으로 HTTP가 올라감

>인터넷 프로토콜 스위트      
>   : 인터넷 통신규약 모음

### TCP와 UDP
    전송 계층의 대표적인 프로토콜
* TCP : 연결이 필요함. 전달 및 순서 보장해줌
* UDP : 연결하지 않고서 데이터를 보냄. 전달 및 순서를 보장 X

### Socket
    socket과 socket API 는 서로 다름.
    



