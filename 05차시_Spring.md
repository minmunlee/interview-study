## ✏️ SPRING


<details>
  <summary>Spring과 SpringBoot의 차이점에 대해서 설명해주세요.</summary> 
    Spring은 사용자가 설정 파일이나 빈 객체 등록, 빈 객체간의 의존성을 직접 작성해야하기 때문에 보다 세밀한 작업을 해야할 경우 사용하는 것이 좋습니다.

반면 SpringBoot는 사용자가 보다 쉽게 Spring을 사용할 수 있도록 설정과 의존성 처리를 자동으로 처리해줍니다. 따라서 간단하고 빠르게 Spring 어플리케이션을 개발하고자 하는 경우에 사용하는 것이 좋습니다.

</details>

<details>
  <summary>DI에 대해서 설명해주시고 의존성 주입을 하기 위한 방법이 무엇이 있는지 설명해주세요.</summary> 
  개발자가 Spring 프레임워크에 **의존성을 주입**하면서 객체간의 결합을 느슨하게 만드는 것을 의미합니다.

의존성을 주입하기 위한 방법으로는 생성자 주입, 필드 주입, setter 주입이 있습니다.
</details>

<details>
  <summary>@Controller와 @RestController의 차이점에 대해서 설명해주세요.</summary> 
  @Controller는 Model 객체를 만들어 데이터를 담고 View를 찾을 수 있으며, @ResponseBody를 같이 쓸 경우 객체 데이터를 반환할 수 있습니다.

@RestController는 @Controller에서 @ResponseBody를 합친 것으로, 좀 더 편리하게 사용할 수 있지만 객체 데이터만 반환이 가능합니다.
</details>

<details>
  <summary>Spring Bean 생명 주기는 어떻게 되나요?</summary> 
  
  Spring에서 Bean의 생명 주기는 객체가 생성되고, 의존성이 주입되며, 사용된 후 소멸되는 과정을 의미합니다. 
  
  먼저, Spring 컨테이너가 Bean을 생성한 후, @Autowired 등을 활용하여 필요한 의존성을 주입합니다. 
  
  이후, 초기화 단계에서 @PostConstruct 어노테이션을 사용하면 Bean이 준비된 후 특정 로직을 실행할 수 있습니다. Bean이 애플리케이션에서 정상적으로 사용되다가 컨테이너가 종료될 때는 @PreDestroy를 활용하여 필요한 정리 작업을 수행할 수 있습니다. 
  
  이러한 생명 주기를 활용하면 Bean의 생성과 소멸 과정에서 필요한 설정을 유연하게 제어할 수 있습니다.
</details>

<details>
  <summary>Spring Actuator란 무엇인가요?</summary> 
  
Spring Actuator는 애플리케이션의 상태를 모니터링하고 관리할 수 있도록 도와주는 Spring Boot의 기능입니다. 이를 활용하면 애플리케이션의 헬스 체크, 메트릭 수집, 환경 정보 조회 등의 기능을 쉽게 구현할 수 있습니다. 예를 들어, /actuator/health 엔드포인트를 호출하면 애플리케이션의 현재 상태를 확인할 수 있고, /actuator/metrics를 통해 성능 데이터를 조회할 수 있습니다. 

Spring Actuator는 기본적으로 여러 모니터링 도구와 연동이 가능하며, Prometheus나 Grafana 같은 시스템과 함께 사용하면 보다 효과적인 성능 분석이 가능합니다. 

이를 통해 개발자는 애플리케이션의 상태를 실시간으로 확인하고 장애 발생 시 신속하게 대응할 수 있습니다.

</details>

<details>
  <summary>Spring MVC란 무엇인가요?</summary> 
  
Spring MVC는 Spring Framework에서 제공하는 웹 애플리케이션 개발을 위한 구조입니다. 클라이언트가 HTTP 요청을 보내면, 이를 DispatcherServlet이 가로채고 적절한 컨트롤러로 전달하여 처리한 후, 다시 클라이언트에게 응답하는 방식으로 동작합니다. 컨트롤러에서는 @RequestMapping이나 @GetMapping 등의 어노테이션을 사용하여 요청을 매핑하고, 필요한 비즈니스 로직을 수행한 후 Model과 View를 반환합니다. 

View는 ViewResolver를 통해 적절한 HTML 또는 JSON 형식으로 변환되어 사용자에게 전달됩니다. Spring MVC는 이러한 구조를 통해 명확한 요청-응답 흐름을 제공하며, RESTful API 개발에도 많이 사용됩니다.
</details>

----

<details>
  <summary>참고</summary> 
  
- https://seung-seok.tistory.com/entry/Spring-%EA%B3%BC-SpringBoot-%EC%9D%98-%EC%B0%A8%EC%9D%B4%EC%A0%90

- https://yeo-computerclass.tistory.com/401#%25--Component%25--%25-F%25--%25--Bean%25--%EC%25B-%25A-%EC%25-D%25B-

- https://mangkyu.tistory.com/49

- https://velog.io/@yukina1418/OOP%EC%97%90%EC%84%9C-IoC%EC%99%80-DI%EA%B0%80-%EC%A4%91%EC%9A%94%ED%95%9C-%EC%9D%B4%EC%9C%A0%EC%97%90-%EB%8C%80%ED%95%98%EC%97%AC-%EC%9E%91%EC%84%B1%EC%A4%91
</details>
