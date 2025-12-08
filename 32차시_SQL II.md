## ✏️ SQL II


<details>
  <summary>제약조건 유형 중 UNIQUE가 무엇인지 설명해주세요.</summary> 
  열의 값이나 테이블의 열 집합이 고유한지 확인하는데 사용되며, 특정 데이터 요구사항에 따라 테이블의 하나 혹은 그 이상의 열에 적용할 수 있는 제약 조건 입니다.

  해당 제약 조건으로 데이터 정합성 보장, 데이터 오류 방지, 쿼리 단순화가 가능해집니다.
</details>

<details>
  <summary>인덱스의 역할과 장단점에 대해 설명해주세요.</summary> 
  관계형 데이터베이스 상에서 테이블의 컬럼을 색인화하여 저장해두었다가 조회할 때 테이블의 레코드를 모두 찾아보는 것이 아닌 색인화 되어 있는 인덱스 파일을 검색하도록 도와주는 기술입니다.

  여러개의 칼럼 값을 정렬된 내용으로 신속하게 검색이 가능하는 장점이 있지만 인덱스에 저장된 값들에 변화가 자주 있을 경우 성능을 저하시킬 수 있다는 단점이 있습니다.
</details>

<details>
  <summary>정규화와 반정규화의 차이점에 대해 설명해주세요.</summary> 
   정규화란 중복을 최소화하도록 설계하는 방법으로 데이터의 일관성을 지키고 유연성을 최대화 할 수 있습니다. 하지만 자주 사용하게 될 경우 릴레이션 간의 JOIN 문 증가로 응답시간이 저하될 수 있다는 단점이 있습니다.

  반정규화란 의도적으로 정규화 원칙을 위배하는 행위로, 데이터베이스의 성능 향상을 위해 데이터 중복을 허용하고 JOIN을 줄여 속도를 향상시키는 데이터베이스 기법입니다. 하지만 데이터의 일관성이 깨질 수 있고 용량을 더 많이 차지한다는 단점이 있습니다.
</details>

<details>
  <summary>SQL과 NoSQL의 의미와 차이에 대해 설명해 주세요.</summary> 
  SQL은 구조화 된 쿼리 언어로 해석되며 관계형 데이터베이스를 활용하는 언어로 정해진 명확하게 정의된 데이터 구조에 따라 저장됩니다. 반대로 NoSQL은 Not Only SQL로 해석되며 유연한 스키마를 활용하며 구조화되지 않은 데이터나 동적 데이터를 처리할 수 있습니다.

  그래서 정형화된 데이터라면 SQL을 사용하고 비정형 데이터 처리 시에는 NoSQL을 사용하는 것이 바람직하다고 볼 수 있습니다.
</details>

<details>
  <summary>JOIN과 그 종류에 대해 설명해 주세요.</summary> 
   JOIN이란 둘 이상의 테이블을 연결해 하나의 결과를 만드는 것을 의미합니다.

   JOIN의 대표적인 종류로는 INNER JOIN과 OUTER JOIN이 있으며 INNER JOIN은 교집합을 의미하며 두 테이블이 모두 가지고 있는 데이터만 결과로 검색되며, OUTER JOIN은 어느 쪽에 데이터가 없더라도 검색할 수 있습니다. 그 외에도 모든 경우의 수를 전부 표현하는 CROSS JOIN이나 자기 자신과 JOIN하는 SELF JOIN등이 있습니다.
</details>

<details>
  <summary>스키마와 테이블의 차이에 대해 설명해 주세요.</summary> 
   흔히 스키마라고 부르는 것은 개념 스키마를 의미하며 테이블을 포함한 제약 조건, 무결성 규칙 등을 정의한 것이고, 테이블은 행과 열로 구성된 데이터 집합을 의미합니다. MySQL에서는 동일하게 사용할 수 있는 등 어떤 DBMS를 사용하냐에 따라 의미가 조금씩 다릅니다.
</details>

----

<details>
  <summary>참고</summary>

- https://data-science-diary.tistory.com/58

- https://m.blog.naver.com/dnjswls23/222026710074

- https://bio-logisch.tistory.com/37

- https://seaforest76.tistory.com/28
- [SQL과 NoSQL 비교: 5가지 주요 차이점](https://www.integrate.io/ko/blog/the-sql-vs-nosql-difference-ko/)
- [SQL 대 NoSQL 데이터베이스 이해](https://www.mongodb.com/ko-kr/resources/basics/databases/nosql-explained/nosql-vs-sql)
- [SQL과 NoSQL 데이터베이스의 차이점: 백엔드 개발자의 선택 기준](https://kimjh0727.tistory.com/entry/SQL%EA%B3%BC-NoSQL-%EB%8D%B0%EC%9D%B4%ED%84%B0%EB%B2%A0%EC%9D%B4%EC%8A%A4%EC%9D%98-%EC%B0%A8%EC%9D%B4%EC%A0%90-%EB%B0%B1%EC%97%94%EB%93%9C-%EA%B0%9C%EB%B0%9C%EC%9E%90%EC%9D%98-%EC%84%A0%ED%83%9D-%EA%B8%B0%EC%A4%80)
- [SQL과 NoSQL의 차이 ( 둘 중 어떤 DB을 사용해야 할까? )](https://velog.io/@sukyeongs/Database-SQL-NoSQL)
- [JOIN(조인)](https://yuna-story.tistory.com/164)
- [Join 이란, join의 종류, inner join과 outer join의 차이점](https://s-y-130.tistory.com/143)
- [스키마(schema)와 테이블 차이](https://jaeyoungb.tistory.com/147)
- [DBMS별 Schema(스키마) 와 Database와 차이점](https://staygold-dev.tistory.com/21)
</details>
