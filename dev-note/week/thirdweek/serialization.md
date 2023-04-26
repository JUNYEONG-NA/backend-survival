# Serialization

* 직렬화  
  > 객체를 그 자체로 저장하거나 네트워크로 전송하는것이 불가능.
  > 객체를 복구할 수 있도록 데이터화 하는게 필요함.
  > 바이너리 라면 Byte Stream, TEXT라면 기계가 파싱할 수 있고 사람도 읽을수 있는 형태를 사용.
  > XML, Json, YAML 이 인기      

**직렬화**와 **마샬링**은 거의 같지만, Java에선 마샬링을 특수하게 다룸      

* 직렬화(Serialization) : 역직렬화(Deserialization)를 통해 객체 또는 데이터의 복사본을 만들 수 있음.
* 마샬링(Marshalling) : 직렬화와 같거나, 원격 객체로 복원할 수 있음. 원격 객체의 경우 메서드 호출은 RPC(또는 RMI)가 됨. >> 직렬화의 의미를 포함 하고 있다


## JSON( JavaScript Object Notation)

대부분 json을 사용함. REST + JSON의 조합, 언어에 구애받지 않는 데이터 형식.    
이 형식은 사람이 읽고 쓰기에 용이하며, 기계가 분석하고 생성함에도 용이함.     

> JSON.parse(역직렬화) // JSON.stringfy(직렬화)    

자바스크립트의 object는 기본적으로 key-value쌍이다.      
Java에선 Map이 이와 유사하지만, 스키마 관리와 타입 안정성을 위해 DTO를 사용한다.      

* Jackson이라는 도구를 사용하면 JSON을 변환할떄 getter로 읽어온다.

## JSON 스키마로서의 DTO(class)



