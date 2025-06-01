## ✏️ JPA


<details>
  <summary>일반 JPA와 Spring Data JPA의 차이점이 무엇인가요?</summary> 
  
  기존 JPA는 EntityManager를 주입받아 사용했지만, Spring Data JPA는 JPA를 한단계 더 추상화 시킨 Repository 인터페이스를 제공합니다. 즉 JPA를 Spring Data JPA의 Repository의 구현에서 사용하고 있습니다.
</details>

<details>
  <summary>Hibernate가 무엇인지 설명해주세요.</summary> 

  JPA의 구현체중 하나로 SQL을 직접 사용하지 않고 메서드를 사용해 데이터를 조작할 수 있습니다.

  하지만 Hibernate가 SQL을 직접 사용하지 않는다고 해서 JDBC API를 사용하지 않는 것은 아니며, 메서드 내부에서 JDBC API가 동작하고 있습니다.

</details>

<details>
  <summary>JPA 영속성 컨텍스트의 변경감지(Dirty Checking)에 대해 설명해주세요.</summary> 

  변경 감지란 영속성 컨텍스트를 DB에 보내기 전 영속성 컨텍스트에 변화가 있었는지 확인 한 후 변화가 있었다면 수정을 한 후 DB에 보내는 작업입니다.

  `transaction.commit` 이 발생하면 자동으로 `em.flush` 가 작동되며 1차 캐시에 저장되었던 영속성 컨텍스트가 DB로 들어가게 되는데, 들어가기전에 1차 캐시 안 엔티티와 스냅샷(맨 처음에 영속성 컨텍스트에 들어온 객체 상태)를 비교합니다. 만약 이 둘이 다르다면 SQL 저장소에 update 쿼리문을 추가하고 commit을 합니다.
</details>

<details>
  <summary>트랜잭션 격리 수준에 대해 설명해주세요.</summary> 

  동시에 트랜잭션 작업이 이루어질 때, A 트랜잭션에서 B 트랜잭션의 조회중이거나 변경중인 데이터에 대한 접근을 허용할지 말지에 대한 수준을 결정하는 것을 의미합니다. 

  Read-Uncommited, Read-Committed, Repatable-Read, Serializable 네가지 수준이 존재합니다.
  
  - Read-Uncommited: 다른 Transaction에서 업데이트가 커밋되지 않았더라도 변경된 데이터를 조회할 수 있다.
  - Read-Commited: 트랜잭션이 시작되기 전에 커밋된 내용만 반영된 데이터에 대해서만 조회할 수 있는 격리 수준이다.
  - Repatable-Read: 트랜잭션 내에서 조회하는 데이터에 대해 공유락을 걸어 잠금된 데이터의 변경 불가능이 보장된다.
  - Serializable: 가장 단순하면서 가장 엄격한 관리 수준이다. ****트랜잭션 내에서의 Select된 자원들은 공유 잠금된다
</details>

<details>
  <summary>N+1 문제에 대해 설명해주세요.</summary> 

  연관 관계가 설정된 엔티티를 조회할 경우에 조회된 데이터 갯수(n) 만큼 연관관계의 조회 쿼리가 추가로 발생하여 데이터를 읽어오는 현상으로,1번의 쿼리를 날렸을 때 의도하지 않은 N번의 쿼리가 추가적으로 실행되는 것을 의미한다.
  ```
    EAGER(즉시 로딩)인 경우
      1. JPQL에서 만든 SQL을 통해데이터(1)를 조회
      2. 이후 JPA에서 EAGER 전략을 가지고 해당 데이터의 연관 관계인하위 엔티티들(N)을 추가 조회
      3. 2번 과정으로 N + 1 문제 발생

    LAZY(지연 로딩)인 경우
      1. JPQL에서 만든 SQL을 통해 데이터를 조회
      2. JPA에서 Fetch 전략을 가지지만, 지연 로딩이기 때문에 추가 조회는 하지 않음
      3. 하지만, 하위 엔티티를 가지고 작업하게 되면 추가 조회가 발생하기 때문에 결국 N + 1 문제 발생
  ```
</details>

<details>
  <summary>지연 로딩과 즉시 로딩에 대해 설명해주세요.</summary> 

  지연로딩 적용 시 DB가 아닌 프록시에서 가져온다. 지연로딩을 사용하게 되면 Member와 Team이 각각 분리되어 Member는 DB를 조회하고, Team은 프록시를 조회한다.

  즉시로딩은 실제 DB에서 한 방에 조회 fetch = FetchType.EAGER로 묶여있을 경우 Member만 조회를 필요로 했으나, Team 정보도 같이 나오기 때문 이문제가 n + 1로 발생할 수 있다.
</details>

----

<details>
  <summary>참고</summary> 
  https://dev-coco.tistory.com/165
  
  https://study-easy-coding.tistory.com/137
</details>
