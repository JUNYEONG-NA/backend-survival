# Spring Web MVC

* MVC 패턴이란?
  > Model - View - Controller 가 분리 된 아키텍쳐 패턴으로    
  > View : 표현 = 사용자 화면    
  > Controller : 입력     
  > Model : 그 외의 모든 것    
  > 1. 관심사의 분리 => MVC의 
  > 2. View에서 참조하는 표현/데이터 => 일반적으로 쓰이는 것
  >     1. Rails는 Active Record
  >     2. Spring Web MVC는 Map 과 유사한 Model 인터페이스를 제공  
  >         * 애플리케이션 전체가 아니라 웹과 관련된 부분(UI Layer)에서만 MVC개념을 활용할 수 있도록 도움
  > * 더 복잡한 프로그램을 다룰 수 있는 더 커다란 아키텍쳐의 필요성이 생김.    
  > 

  ## Controller

    @RestController
    public class WelcomeController {
        @GetMapping("/")
        public String home() {
            return "Hello, World!";
        }
    }

* Annotation은 짚고 넘어가는 것이 좋음.

### Annotations

* RestController
* GetMapping
* PostMapping
* RequestMapping
  * Method
  * Path
* ResponseBody
* ResponseStatus


> ##### 알고 있었던 내용
> > 스프링 MVC 는 Model-view-controller로 분리 되어 있고    
> > MVC1 패턴은 controller가 view와 controller를 담당 해서 구현은 쉽지만    
> > 복잡한 프로젝트 일수록 가독성이 떨어지고 유지보수가 힘들기 때문에 MVC2 패턴이 등장    
> > MVC2 패턴은 view와 Controller가 완전히 분리되어 수정사항이 생기면 해당 부분만    
> > 그 부분만 찾아가 수정하면 되기 떄문에 유지보수에 이점이 있음.
> ##### 새로 배운 내용
> 
> ##### 어려웠던 것
> 
    