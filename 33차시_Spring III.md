## ✏️ Spring III


<details>
  <summary>Dispatcher Servlet 이 무엇인지 설명해주세요.</summary> 
  서블릿 컨테이너를 통해 들어오는 모든 요청을 제일 앞에서 받는 프론트 컨트롤러 입니다. 공통된 작업을 처리한 후에 적절한 세부 컨트롤러로 작업을 위임하고 세부 컨트롤러가 요청을 처리하면 반환할 view를 다시 dispatcher servlet에 넘기게 됩니다.
</details>

<details>
  <summary>Handler Mapping 과 Handler Adapter가 무엇인지 설명해주세요.</summary> 
  핸들러 매핑은 우선 순위에 따라 요청 url에 맞는 컨트롤러를 찾아주는 역할을 합니다. 또한 핸들러 어댑터는 핸들러 매핑으로 통해 찾은 컨트롤러를 직접적으로 실행하기 위해 필요합니다. 차례대로 핸들러 어댑터를 돌면서 맞는 어댑터를 찾으면 dispatcher servlet이 해당 어댑터의 컨트롤러를 실행합니다.

  (왜 handler adapter가 필요한가)

  다양한 컨트롤러가 존재하기 때문에 모든 요구사항을 맞추기 위해 사용됩니다.
</details>

<details>
  <summary>스프링을 사용하는데에 이점은 어떤게 있나요?</summary> 
   스프링은 하나 이상의 JAR 파일로 구성된 모듈이 모여 구성되어 있어서 몇개의 JAR 파일만 있으면 개발과 실행이 모두 가능하고, 애플리케이션의 배포 또한 빠르고 쉽게 할 수 있다는 장점이 있습니다.

  또한 객체의 의존 관계를 개발자가 직접 처리하는 것이 아닌 컨테이너가 직접 처리해주기 때문에 소스에 의존 관계가 명시되지 않아 낮은 결합도를 유지해 유지 보수가 용이해진다는 장점이 있습니다.

  그 외에도 핵심 비즈니스 로직과 반복되는 공통 로직을 분리함으로써 응집도를 높일 수 있다는 장점이 있습니다.
</details>

<details>
  <summary>왜 Spring Framework를 사용하는지, 장점에 대해 말씀해 주세요.</summary> 
  Spring Framework는 먼저 POJO 기반의 구성으로 개발자가 특정 라이브러리나 컨테이너 기술에 종속되지 않기 때문에 자유롭게 객체지향적 설계를 구현할 수 있으며, 의존성 주입을 통해 객체 관계를 연결해 주기 때문에 개발과 유지보수가 편해집니다. 또한 Spring Cloud나 Spring Batch 등 다양한 프로젝트가 구축되어 있어 확장성이 뛰어납니다. 

  즉, 애플리케이션 개발에 필요한 기반을 제공해주기 때문에 개발자가 오직 비즈니스 로직 구현에만 집중할 수 있어 많이 사용합니다.
</details>

<details>
  <summary>Spring의 IoC(제어의 역전)와 DI(의존성 주입)에 대해 설명해 주세요.</summary> 
   IoC(제어의 역전)란 사용할 객체를 개발자가 직접 생성하지 않고 객체의 생명주기를 스프링 컨테이너에 위임하는 것을 의미합니다. 이 제어의 역전을 통해 DI(의존성 주입)가 가능해 집니다.

   DI(의존성 주입)란 객체 간의 의존성을 외부에서 주입하는 것을 의미합니다. 때문에 직접 의존하는 객체를 생성하지 않아도 의존성을 주입 받아 사용할 수 있습니다. 이로 인해 컴포넌트 간의 결합도를 낮춰서 유지보수성이 향상됩니다.
</details>

<details>
  <summary>Spring의 Bean과 그 생명주기에 대해 설명해 주세요.</summary> 
   Bean이란 Spring 컨테이너에 의해 관리되는 객체를 의미합니다. 
   Bean 객체는 스프링 컨테이너가 생성된 후 생성되며 이후 스프링 컨테이너에 의해 의존 관계가 설정됩니다. Bean 객체가 생성되고 의존 관계가 주입되면 초기화 작업이 이루어지며 사용될 준비가 완료됩니다. 그리고 스프링 컨테이너가 종료되면 Bean 객체도 소멸됩니다.
</details>

----

<details>
  <summary>참고</summary>

- [면접-질문-백엔드,-Spring](https://suyeonsu.github.io/posts/CS-%EB%A9%B4%EC%A0%91-%EC%A7%88%EB%AC%B8-%EB%B0%B1%EC%97%94%EB%93%9C,-Spring/)
- https://ksabs.tistory.com/250
- https://lasbe.tistory.com/108
- [Spring FrameWork 특징, 장단점](https://kr98gyeongim.tistory.com/85)
- [우리는 왜 스프링을 사용하는가? - Java spring의 특징](https://joychae.tistory.com/27)
- [제어의 역전(IoC, DI, AOP)](https://innovation123.tistory.com/167)
- [Spring Framework 주요 특징 이해하기 : DI, IoC, POJO, AOP](https://adjh54.tistory.com/298)
- [스프링 컨테이너와 빈 객체의 생명 주기를 알아보겠습니다.](https://kangkangsulae.tistory.com/146)
- [빈 생명 주기 콜백 (Bean LifeCycle) @PostConstruct / @PreDestroy](https://innovation123.tistory.com/213)
</details>
