## ✏️ MSA


<details>
  <summary>MSA와 모놀로식 아키텍처의 차이점에 대해 설명해주세요.</summary> 
  
  Monolithic Architecture란 소프트웨어의 모든 구성 요소가 한 프로젝트에 통합되어 있는 형태로 보통 소규모로 이루어지는 프로젝트에 적합하다. MSA는 Micro Service Architecture로 서비스들이 각각 배포나 구현을 독립적으로 수행한다. 따라서 다수의 개발자들이 개발하는 대규모 프로젝트에 적합하다.
</details>

<details>
  <summary>Spring Cloud Netflix Eureka에 대해서 설명해주세요.</summary> 

  분산 시스템에서 서비스 디스커버리와 관련된 기능을 제공하는 컴포넌트입니다.

  클라우드 환경에서 마이크로서비스 간의 상호작용을 관리하고 서비스 등록과 검색을 지원합니다.
  
  - 서비스 등록
      
      각각의 마이크로 서비스는 Eureka 서버에 자신을 등록하는데, 이 등록 과정에서 서비스는 자신의 정보(포트, 상태 정보 등)를 제공한다.
      
  - 서비스 검색
      
      마이크로서비스는 Eureka 서버를 통해 다른 서비스의 위치를 동적으로 검색할 수 있다.
      
      클라이언트는 필요한 서비스의 인스턴스를 찾아 요청을 보낼 수 있다.
      
  - 헬스 체크
      
      서비스 인스턴스의 상태를 주기적으로 확인하고 비정상적인 인스턴스는 자동으로 등록 해제한다.

</details>

<details>
  <summary>MSA를 대규모 프로젝트에서 사용하는 이유는 무엇인가요?</summary> 
  
  - 각각의 서비스는 모듈화가 되어있기 때문에 RPC, message-driven API 등을 이용하여 통신해서 각각 개별 서비스를 빠르게 개발하고 유지 보수가 쉽다.

  - 팀 단위로 적절한 수준에 기술 스택을 다르게 가져갈 수 있다.
  
  - 서비스별로 독립적 배포가 가능하기 때문에 CD 작업도 모놀로식에 비해 가볍다.
  
  - 개별적으로 Scale-out이 가능해서 메모리, CPU적으로 상당 부분 이득이다.
    
</details>

<details>
  <summary>MSA 환경에서 데이터베이스 정합성을 맞추는 방안에 대해 말씀해주세요.</summary> 

  **2PC(Two-Phase Commit)**: 서로 다른 DB 간에 완벽한 정합성을 보장하는 방법으로, 모든 DB에 반영할 수 있는지 물어봐서 합의가 되었을 때만 반영하고 그렇지 않으면 전체를 철회하는 방식입니다. 이 뒤 각 DB에 커밋하는데 커밋되지 않은 쪽의 DB엔 락이 잡혀 데이터가 불일치한 상태로는 절대 조회되지 않습니다. 단, 정합성은 보장되지만 락이 풀리지 않으면 전역 장애를 유발할 수 있어 주의가 필요합니다.

  **CDC(Change Data Capture)**: 최종 일관성을 보장하는 방식으로, 일시적으로 양쪽의 합이 맞지 않을 수 있으나 궁극적으로 맞도록 하는 비동기 방식입니다. 소스DB와 타겟DB 간에 비동기 복제 역할을 수행합니다. 2PC와 정반대로 타겟 DB에 장애가 발생하더라도 복구될 때까지 반복 수행하면서 꼭 반영시킵니다. 때문에 계정 초기화와 같이 반드시 성공해야 하는 경우에 유용합니다.
  
  **SAGA 패턴**: 개발자가 보상 트랜잭션을 잘 정의하고 누락되지 않도록 구성할 책임을 집니다. 표현력이 넓어서 보상 트랜잭션 구성 방식에 따라 2CP와 CDC의 효과를 모두 낼 수 있습니다. 단, 모든 보상 트랜잭션을 완벽하게 구성하는 것은 어려울 수 있고 단계별 에러 케이스를 모두 검증해야 하는 부담이 있습니다.
</details>

<details>
  <summary>MSA와 모놀리식 아키텍처의 장단점에 대해 말씀해주세요.</summary> 

  모놀리식 아키텍처는 트랜잭션 관리가 쉽고 배포와 테스트가 용이합니다. 하지만 일부분의 오류가 전체에 영향을 끼칠 수 있는 단점이 있습니다. 또 빌드 및 배포 시간이 길어 생산성이 낮아집니다.

  반대로 MSA는 서비스 간 독립성이 높아 배포 시 다른 서비스에 영향을 미치지 않습니다. 하지만 고려해야 할 사항이 많아 복잡도가 높고 통합 테스트가 어려운 단점이 있습니다. 트랜잭션 관리와 데이터 정합성 유지가 까다롭습니다.
</details>

<details>
  <summary>MSA로 전환하기 위한 필수 요소로 무엇이 있을까요?</summary> 

  먼저 도메인의 경계를 명확히 설정해 각 서비스의 책임과 역할을 명확히 정의해야 합니다. 또 각 서비스를 독립적으로 운영하기 위한 독립적인 데이터베이스를 구축하고 에러 발생 시 원인을 빠르게 파악하고 복구하기 위한 분산 로깅 시스템을 구축해야 합니다.
</details>

----

<details>
  <summary>참고</summary> 
  
  - https://dodo-devops.tistory.com/19
  
  - https://wooaoe.tistory.com/57

  - https://ksh-coding.tistory.com/135
    
  - [MSA 전환 실패 사례와 교훈](https://f-lab.kr/insight/msa-failure-lessons-20250205)
    
  - [MSA 환경에서 데이터 관리를 위한 필수사항 - 고가용성과 데이터 동기화](https://www.samsungsds.com/kr/insights/mas_data.html)
</details>
