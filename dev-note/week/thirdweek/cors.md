# CORS

* F/E 애플이케이션에서 B/E REST API를 사용하는 상황
  
  ## Same-Origin Policy

  > 동일출처정책 - 웹 브라우저가 처리하는 보안정책                    
  > : 한 출처에서 로드한 문서 또는 스크립트가 다른 **출처**의 리소스와 상호 작용 하는 방식을 제한하는 보안 메커니즘        
  > 출처는 도메인 또는 HOST NAME, 포트 까지 포함    
  > B/E 에서는 이미 처리가 끝난 결과를 리턴 해주었지만 F/E 웹브라우저에서 B/E,F/E간의 URL,Port,HOST가 모두 같지 않다면(동일출처가 아니라면) 접근할 수 없다.

  ### JSONP

  <script> 태그는 동일출처를 따지지 않는 점을 이용함. 서버에서 JSON을 전달하는 것이 아니라, 실행되는 자바스크립트 코드를 전달하는 방식.      

    <script>
        window.success = (data)=>{
            //얻은 데이터 처리하는 코드
            console.log(data);
        }
    </script>
    <script src="http://server/post?callback=success"></script>          



## CORS ( Cross-Origin Resurce Sharing )

> B/E, 즉 REST API의 응답 헤더에 "Access-Control-Allow-Origin" 속성을 포함.    
>  이 속성을 정의 하면 "~~에서 요청한건 보여줘도 괜찮아요" 라는 의미.    
>
> > HTTP/1.1 200 OK    
> > Access-Control-Allow-Origin : ~~     
> > (자세한 헤더는 더 많음)      
> > (빈 줄)     
> > [      
> >     {     
> >     "id" : "1",       
> >     }           
> > ]      

## Spring Web MVC 에서 CORS

### HttpServletResponse

spring reactive app 에서는 처리하는게 약간 다름. 이 강의에서는 Spring web MVC에서 처리하는법을 다룸      

    response.addHeader("Access-Control-Allow-Origin","URL")

Origin과 무관하게 모든 요청을 허용할 거면 '*'로 잡아준다.    

    response.addHeader("Access-Control-Allow-Origin","*")

### @CrossOrigin

Spring Web 에서는 @CrossOrigin 애너테이션을 써주면 된다.     

    @CrossOrigin("Http://~~.~~:~~")




