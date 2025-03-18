## ✏️ RESTful API


<details>
  <summary>REST의 뜻이 무엇인가요?</summary> 
  
  HTTP URI 를 통해 자원(Resource)을 명시하고 HTTP Method를 통해 해당 자원에 대한 CRUD 작업을 적용하는 것으로 웹 서비스가 어떻게 작동하는 지에 대한 아키텍처 스타일 혹은 설계원칙이다.
</details>

<details>
  <summary>REST 설계 규칙 몇가지만 설명해주세요</summary> 

  - URI는 동사보다는 명사를, 대문자보다는 소문자를 사용해야한다.
  - 마지막에 슬래시를 포함하지 않는다.
  - 언더바 대신 하이픈을 사용한다.
  - 파일 확장자는 URI에 포함하지 않는다.
  - 행위를 포함하지 않는다.
</details>

<details>
  <summary>REST의 특징에 대해 설명해주세요</summary> 

  - Server-Client (서버-클라이언트 구조)
  - Stateless (무상태)
      - 서버는 클라이언트의 요청을 저장하지 않는다. 따라서 각각의 요청은 독립적으로 처리된다.
  - Cacheable (캐시 처리 가능)
      - HTTP 특징인 캐싱 기능을 적용할 수 있다. 이를 통해 응답 시간이 빨라진다.
  - Layered System (계층화)
      - 클라이언트는 REST API Server 만 호출하고 서버는 다중 계층으로 구성될 수 있다.
  - Uniform Interface (인터페이스 일관성)
      - URI 로 지정한 Resource에 대한 조작을 통일되고 한정적인 인터페이스로 수행한다.
</details>

<details>
  <summary>REST API의 구성에 대해 말씀해 주세요.</summary> 

  REST API의 구성으로는 자원, 행위, 표현이 있습니다. 자원의 식별은 URI 하며, 자원에 대한 행위는 HTTP 메서드로 나타냅니다. 표현은 클라이언트와 서버가 데이터를 주고받는 형태로, 전달되는 데이터는 JSON, XML 등으로 표현됩니다.
</details>

<details>
  <summary>RESTful API란 무엇을 의미하는 건가요?</summary> 

  REST 설계 규칙을 지키며 API를 제공하는 서비스를 RESTful하다고 하며, REST 규칙을 잘 준수할수록 RESTful한 API라고 할 수 있습니다.
</details>

<details>
  <summary>REST API 를 최대한 RESTful 하게 사용하기 위한 규칙을 생각나는 대로 말씀해 주세요.</summary> 

  - 자원에 대한 행위는 HTTP 메서드로 나타낸다.
  - HTTP 메서드나 행위에 대한 표현이 URI에 들어가면 안된다.
  - URI 경로는 슬래시로 계층 관계를 표현하며, URI 마지막에 슬래시가 들어가면 안 된다.
  - URI 경로에는 언더바를 사용하면 안 되고, 소문자 사용을 지향한다.
</details>

----

<details>
  <summary>참고</summary> 
  https://khj93.tistory.com/entry/%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC-REST-API%EB%9E%80-REST-RESTful%EC%9D%B4%EB%9E%80

  https://velog.io/@nias0327/REST-API%EC%9D%98-%EC%A0%95%EC%9D%98%EC%99%80-%ED%8A%B9%EC%A7%95
</details>
