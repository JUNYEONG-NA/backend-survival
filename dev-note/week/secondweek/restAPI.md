# REST API


> 학습 키워드
>  * API
>  * 정보은닉(Information Hiding) & 캡슐화(Encapsulation) 그리고 차이점
>  * Architecture & Architecture Style의 차이
>  * REST(7가지 제약조건)
>       - 필딩 제약 조건


## F/E & B/E

시스템을 여러 Tier & Layer로 구분하는데 Tier는 물리적인 구분을 뜻하고, Layer는 논리적인 구분을 뜻한다.

사용자에게 가까운 부분을 Front-End(F/E), 사용자에게 먼 부분을 Back-End(B/E)라고 부른다. 

F/E와 B/E 사이를 연결하는 방법은 다양한데, HTTP와 Web 기술들, REST **API**를 사용하고 그 외에도 SOAP, GraphQL등 여러 방법이 있다. 

 > **API**
 > : API,  Application Programming Interface    
 > 디지털 기기, 소프트웨어 어플리케이션, 데이터 서버가 서로 통신할 수 있게 해주는 작은 코드조각으로 우리가 의존하는 많은 서비스의 근간이다.    
 > 쉽게 생각 하자면 모바일 어플, 웹 사이트는 인터넷 세상에서 사람, 사용자들이 사용할 수 있게 설계된 반면에, API는 서로 다른 시스템과 어플리케이션이 사용하도록 설계 되었다.
 > 웹사이트와 API 모두 데이터와 콘텐츠, 이미지 등 데이터를 주고 받는 어떻게 보면 동일한 기능을 한다. 하지만 API는 사람에게 보기 좋은 형태가 아니라 컴퓨터가 판독하기 쉬운 형태의 정보를 제공한다.     
 >[What Is an API?](https://blog.postman.com/intro-to-apis-what-is-an-api/)

 



물리적으로 나눠 놓고 

REST API > 아키텍쳐
SOAP, GraphQL 
> HTTP는 단순히 통신 규약

Spring boot 

servlet

was - tomcat, undertow

서비스를 제공하기 ㅇ위한 부분들을 만든다

정보은닉은 어딘가의 뒤로 숨기는 것이고
캡슐화는 데이터를 묶어서 인터페이스등으로 접근할 수 있게 함. > 정보은닉을 하는 강력한 방법

