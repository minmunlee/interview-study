## ✏️ Spring


<details>
  <summary>Bean을 생성하는 방법에 대해 설명해주세요.</summary> 
  
  - 컴포넌트 스캔과 자동 의존관계 설정
    - @Component 어노테이션 사용
    - class 기반으로 실행 시점에 인스턴스 객체를 생성한다.
    - @Controller, @Service, @Repository 등 모두 @Component 를 포함하고 있으며 실행 시점에 자동으로 의존성을 주입한다.
- 자바 코드로 직접 스프링빈 등록
    - @Bean 어노테이션 사용
    - method 기반으로 메서드에서 반환하는 객체를 인스턴스 객체로 생성한다.
</details>

<details>
  <summary>Spring 에서 사용되는 JPA에 대해 설명해주세요.</summary> 

  JPA란 자바에서 사용하는 ORM 표준이며, 인터페이스의 집합입니다.

  그중 Spring Data JPA는 JPA의 대표적인 구현체 중 Hibernate를 개발자가 쉽게 모듈화하여 제공하는 라이브러리 입니다.

</details>

<details>
  <summary>@RequestParam과 @PathVariable의 공통점과 차이점에 대해 설명해주세요.</summary> 

  두 어노테이션 모두 URI를 통해 전달된 값을 파라미터로 받아오는 역할을 합니다.

  @PathVariable은 값을 하나만 받아 올 수 있고 @RequestParam은 여러 데이터를 받아 올 수 있다는 차이점이 있습니다.  
</details>

<details>
  <summary>Spring IOC(제어의 역전)에 대해 설명해주세요.</summary> 

  Spring IOC란 제어의 역전을 의미하며 개발자가 해야 할 일을 Spring Framwork에서 대신 해줌을 의미합니다. 객체 생성과 생명 주기 및 의존성을 개발자 대신 Spring IOC Container가 관리합니다.
</details>

<details>
  <summary>Spring에서 의존성을 주입하는 방법에 대해 설명해주세요.</summary> 

  Spring에서 의존성을 주입하는 방법으로 생성자 주입, 필드 주입, 세터 주입이 있습니다.

  필드 주입은 @Autowired 어노테이션을 통해 필드에 직접 주입하는 방법이며, 세터 주입은 Setter 메서드를 통해 의존성을 주입하는 방법입니다. 생성자 주입도 말 그대로 생성자를 통해 주입하는 방법이며, 이 방법이 테스트에 용이하고 순환 참조를 방지할 수 있기 때문에 권장됩니다.
</details>

<details>
  <summary>Spring Proxy(프록시)에 대해 설명해주세요.</summary> 

  프록시란 ‘대리인’이라는 뜻을 가지며, 클라이언트와 실제 객체 사이에서 중간 역할을 수행하는 객체를 의미합니다. Spring AOP가 프록시 기반으로 동작하며, 주로 트랜잭션 기능이 프록시를 통해 구현됩니다.
</details>

----

<details>
  <summary>참고</summary> 

  https://dev-coco.tistory.com/70
  
  https://yujin-17.tistory.com/entry/Spring-프록시Proxy란-AOP와-프록시-기반-동작-방식
</details>
