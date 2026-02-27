## ✏️ Spring Batch


<details>
  <summary>Spring Batch와 Spring Scheduler의 차이는 무엇인가요?</summary> 
  배치는 대용량의 데이터를 일괄적으로 처리하는 작업으로, 사용자와의 상호작용 없이 여러 개의 작업을 미리 정해진 순서에 따라 중단 없이 처리하는 것을 의미합니다.

  반면에 스케줄러는 일정한 시간에 특정 로직을 돌리기 위해 사용됩니다. 

  즉 스프링 배치는 데이터 처리에 중점을 두고 스케줄러는 시간 기반 작업에 중점을 두고 있다는 목적에 차이가 있습니다.
</details>

<details>
  <summary>Tasklet 방식과 Chunk 방식에 대해 설명해주세요.</summary> 
  Tasklet 방식은 기본적으로 하나의 작업을 수행하는 방식으로 대체로 단순하거나 복잡하지 않은 작업을 수행하는데 적합하고 전체 데이터를 처리하는 것이 아닌 일부 데이터나 단일 작업을 처리하는데 주로 사용됩니다.

  Chunk 방식은 대용량 데이터를 효과적으로 처리하기 위해 사용하며 큰 데이터를 일련의 작은 데이터 묶음으로 나누고 각 Chunk를 개별적인 트랜잭션 범위 내에서 처리하는 방식을 취합니다.
</details>

<details>
  <summary>만약 배치 잡이 지연될 경우 모니터링 하는 방법은 무엇이 있을까요?</summary> 
   먼저 배치 잡의 로그를 상세히 분석하여 어떤 부분에서 시간이 소요되는지 확인하는 로그 분석 방법이 있습니다. 또는 잡이 실행되는 스케줄러의 설정을 확인하여 예상 시간과 일치하는지 확인하거나 현재 실행 중인 잡이 다른 잡에 의존하는 경우 의존 잡이 끝나길 기다리는 경우가 있습니다.
</details>

<details>
  <summary>스프링 배치는 무엇이며 어떤 경우에 활용하면 좋을까요?</summary> 
  스프링 배치는 대용량 데이터를 처리하기 위한 스프링 프레임워크 기반 프레임워크로 다량의 데이터를 처리하거나 주기적이고 반복적인 작업을 실행하는 데 사용됩니다. 예를 들어 구독 서비스로 일정 시간에 구독자들에게 메일을 일괄 전송하는 등의 작업에 홯용할 수 있습니다.
</details>

<details>
  <summary>배치 작업이 중간에 실패할 경우 어떻게 처리하나요?</summary> 
   스프링 배치는 기본적으로 chunk 단위로 트랜잭션을 관리하기 때문에 오류가 발생할 경우 이를 스킵하고 다음 작업으로 넘어가거나 재시도 할 수 있습니다.
</details>

<details>
  <summary>스프링 배치에 어떻게 스케쥴링을 적용할 수 있을까요?</summary> 
   @Scheduled 을 사용하는 Spring Scheduler나 Quartz Scheduler, 또는 Crontab, Jenkins 등의 외부 스케줄러와 함께 사용할 수 있습니다. @Scheduled 어노테이션을 활용해 잡을 주기적으로 실행할 수 있습니다.
</details>

----

<details>
  <summary>참고</summary>

- [https://velog.io/@dev_tmb/배치와-스케줄러의-차이](https://velog.io/@dev_tmb/%EB%B0%B0%EC%B9%98%EC%99%80-%EC%8A%A4%EC%BC%80%EC%A4%84%EB%9F%AC%EC%9D%98-%EC%B0%A8%EC%9D%B4)
- https://f-lab.kr/insight/spring-batch-scheduler-difference-20240802
- https://dkswnkk.tistory.com/707
- https://chung-develop.tistory.com/158
- [Spring Batch란? 간단한 개념과 코드 살펴보기](https://dkswnkk.tistory.com/707)
- [Spring Batch 예상 질문 리스트](https://chung-develop.tistory.com/158)
</details>
