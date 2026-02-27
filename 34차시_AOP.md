## ✏️ AOP


<details>
  <summary>AOP를 사용하는 이유는 무엇일까요?</summary> 
  Spring AOP는 주로 모든 메소드 간의 호출 시간을 측정하고 싶을 때 사용하는데, 예를 들어 회원 가입 시간, 회원 조회 시간을 측정하고 싶을 때 사용할 수 있습니다. 또한 공통 관심 사항과 핵심 관심사항을 구분하고 싶을 때 사용합니다.
</details>

<details>
  <summary>프록시 패턴이 무엇인지 설명해주세요.</summary> 
  어떠한 객체를 사용하고자 할 때 객체를 직접적으로 참조하는 것이 아닌 해당 객체를 대변하는 객체를 통해 대상 객체에 접근하는 방식입니다. 이를 통해 해당 객체가 메모리에 존재하지 않아도 기본적인 정보를 참조하거나 설정할 수 있고 실제 객체의 기능이 필요한 시점까지 객체 생성을 미룰 수 있습니다.
</details>

<details>
  <summary>AOP를 도입했을 때의 단점은 무엇이 있을까요?</summary> 
   코드의 흐름이 직관적이지 않게 되어 디버깅이 어려울 수 있고 지나치게 사용될 경우 성능이 저하될 수 있다는 점이 있
</details>

<details>
  <summary>AOP 개념에 대해 설명해 주세요</summary> 
  AOP란 관점 지향 프로그래밍이라는 의미로 애플리케이션에서 필요한 기능 중, 여러 모듈에서 공통적으로 적용되는 기능에 대한 관심과, 주목적을 다루는 비즈니스 로직에 대한 관심을 분리하여 모듈화하는 방법을 의미합니다. (횡단 관심사를 핵심 로직으로부터 분리하며 모듈성을 증가시키는 방법입니다.)

  예를 들어, 상품을 판매하는 프로그램이 있을 때 비즈니스적으로 사용되는 상품 등록이나 구매 등의 기능은 핵심 관심 사항에 해당되지만 회원이 접속할 때 권한을 확인하는 보안이나 결제 시의 트랜잭션 등은 프로그램에서 공통적으로 적용되는 기능이기 때문에 공통 관심 사항에 해당됩니다.

  객체지향 프로그래밍은 비즈니스 로직의 모듈화라면 관점 지향 프로그래밍은 인프라나 부가 기능의 모듈화라고 생각할 수 있습니다.
</details>

<details>
  <summary>@Transactional의 동작 원리를 설명해 주세요.</summary> 
   @Transactional은 Spring AOP를 통해 프록시 객체를 생성하여 사용됩니다. 해당 어노테이션이 선언된 클래스나 메서드가 있으면 Spring이 이에 대한 프록시 객체를 생성합니다. 이 타겟에 대한 호출이 발생하면 AOP 프록시가 인터셉터 체인을 통해 가로채오고 트랜잭션 관리자에게 넘기며, 이를 받은 트랜잭션 관리자가 새로운 트랜잭션을 생성합니다. 이 때 JPA를 사용할 경우 영속성 컨텍스트가 생성되며 이와 트랜잭션을 연결합니다. 이후 실행 성공 여부에 따라 커밋이나 롤백 등의 트랜잭션 결과를 반환합니다.
</details>

<details>
  <summary>실무에서 AOP를 어떻게 활용할 수 있을지 예시를 말씀해 주세요.</summary> 
   실제로 활용할 수 있는 분야로 로깅이나 보안 관리, 트랜잭션 관리 등이 있다고 생각합니다. 이러한 기능들은 애플리케이션의 여러 기능에서 공통적으로 필요하지만 핵심 비즈니스 로직과는 독립적으로 관리되야 된다고 생각하기 때문에 횡단 관심사로써 분리하여 모듈화 할 수 있다고 생각합니다.
</details>

----

<details>
  <summary>참고</summary>

- https://mumomu.tistory.com/175

- https://hs-backend.tistory.com/235
- [AOP란 무엇인가? (관점 지향 프로그래밍)](https://ittrue.tistory.com/213)
- [AOP란 무엇인가](https://rma7.tistory.com/70)
- [스프링 AOP와 프록시의 이해](https://f-lab.kr/insight/understanding-spring-aop-and-proxy)
- [@Transactional 동작원리(+readOnly=true)](https://wookjongbackend.tistory.com/45)
- [스프링 트랜잭션 동작 원리 (@Transactional, AOP)](https://sasca37.tistory.com/267#google_vignette)
- [스프링 AOP의 이해와 실제 적용 사례](https://f-lab.kr/insight/understanding-spring-aop?wbraid=ClQKCQjwpP63BhCmARJDAGQpkKAP6uuBGtP6UqTN-oNNf0VdNLdd1wDEwWEMm8otOBAO8FfngFjgZ4rdRA42bQXYPjPq2q_bDK7W6NzGN6P89xoC1yQ)
</details>
