## ✏️ 자바 III


<details>
  <summary>제네릭이 무엇이며 특징에 대해 말해주세요.</summary> 
  클래스 내부에서 사용할 데이터 타입을 외부에서 지정하는 기법으로 객체별로 다른 타입의 자료가 저장될 수 있도록 합니다. 따라서 타입을 유연하게 처리하고 안정성을 확보할 수 있습니다. 

  제네릭을 이용하면 하나의 클래스에 여러 타입을 선언할 수 있고 클래스 뿐만 아니라 메소드에도 선언이 가능합니다. 이때 제네릭에서 할당 받을 수 있는 타입은 Reference 타입 뿐이며 원시 타입을 사용할 수는 없습니다.
</details>

<details>
  <summary>static과 final, static final의 차이에 대해 설명해주세요</summary> 
  static은 정적인, 고정된 이라는 전역의 의미를 갖고, 객체 생성 없이 사용할 수 있는 필드와 메서드를 생성할 때 사용하며 언제나 값이 변경될 수 있습니다.

  final은 한번 저장되면 수정이 불가능한 변수를 선언할 때 사용합니다. 주로 생성자 주입을 받을 때 변수를 final로 선언하여 임의로 인스턴스의 변경을 막아줄 때 사용되며, 값을 받아오기 전까지는 어떤 값이던 final 변수에 할당이 가능하다는 특징이 있습니다.

  static final은 상수를 선언하고자 할 때 사용됩니다. final과 달리 빈 값으로 둘 수 없고 static final을 선언한 순간 값을 할당하여 변하지 않는 값으로 만들 수 있습니다.
</details>

<details>
  <summary>extends와 implements의 차이에 대해 설명해주세요.</summary> 
   extends 는 상속의 대표적인 형태로, 부모의 메서드를 그대로 사용할 수 있으며 오버라이딩 할 필요 없이 부모에 구현되어 있는 것을 그대로 사용 가능합니다. 또한 abstarct  클래스에 상속에 사용이 됩니다.

   implements 는 반드시 부모 클래스에서 메소드가 선언만 되어 있기 때문에 자식 클래스에서 반드시 재정의 해야한다는 특징이 있으며, interface 클래스 상속에 사용됩니다.
</details>

<details>
  <summary>자바에서 불변 객체에 대해 설명해주세요.</summary> 
  불변 객체란 한번 객체를 생성하면 내부의 상태가 변하지 않는 객체를 의미합니다. final 키워드를 통해 참조값을 변경하지 못하도록 해 불변성을 확보할 수 있습니다. 쓰레드 안전성을 가지므로 안정성을 보장할 수 있으며 부수 효과를 방지하는 등의 이점을 가집니다.
</details>

<details>
  <summary>String은 불변성을 가지는데 왜 재할당이 되는 걸까요?</summary> 

   문자열을 재할당할 때 해당 문자열을 참고하는 객체 값을 수정하는 것이 아니라 새로운 String 객체를 만들고 그 문자열을 할당합니다. 즉, 처음 생성된 String 객체가 변경되는 것이 아니라 새로운 String 객체가 생성되어 그 참조가 변수에 할당되는 것입니다. 
</details>

<details>
  <summary>자바의 레코드 클래스에 대해 설명해주세요.</summary> 
   레코드 클래스는 기존 클래스와 비슷하지만, 더 간결하고 효율적으로 객체를 생성할 수 있도록 설계된 클래스입니다. record 헤더에 나열한 데이터는 private final로 정의되기 때문에 불변성이 보장되며, 생성자나 equals 등의 메서드를 자동으로 생성합니다.
</details>

----

<details>
  <summary>참고</summary>

- https://jehuipark.github.io/java/java-generic
- [제네릭Generics-개념-문법-정복하기](https://inpa.tistory.com/entry/JAVA-%E2%98%95-%EC%A0%9C%EB%84%A4%EB%A6%ADGenerics-%EA%B0%9C%EB%85%90-%EB%AC%B8%EB%B2%95-%EC%A0%95%EB%B3%B5%ED%95%98%EA%B8%B0)
- https://wooono.tistory.com/261
- [Java-static-final-static-final의-차이](https://squirmm.tistory.com/entry/Java-static-final-static-final%EC%9D%98-%EC%B0%A8%EC%9D%B4)
- [Immutable Object(불변객체)](https://velog.io/@conatuseus/Java-Immutable-Object%EB%B6%88%EB%B3%80%EA%B0%9D%EC%B2%B4)
- [불변 객체(Immutable Object) 및 final을 사용해야 하는 이유](https://mangkyu.tistory.com/131)
- [String class가 final인 이유, String의 불변성 (Immutable)](https://wildeveloperetrain.tistory.com/34)
- [String이 불변(Immutable) 객체인 이유](https://charliecharlie.tistory.com/343)
- [Record란?](https://jangjjolkit.tistory.com/69)
- [Record Class란?](https://mr-popo.tistory.com/243)
</details>
