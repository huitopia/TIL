# hashCode()

## Object.hashCode()

객체를 식별하는 정수로 `Object`의 `hashCode()` 메소드는 객체의 메모리 번지를 이용해 해시코드를 생성하여 **_객체마다 다른 정수값(메모리 주소값)을 리턴한다._**

`equals()` 메소드처럼 두 객체가 동등한지를 비교할 때 주로 사용한다.

### equals()와 hashCode()

`Object.equals()` 메소드를 재정의 하면 `hashCode()`도 반드시 재정의해야 한다. `hashCode()`를 재정의 하지 않으면 같은 값 객체라도 해시값이 다를 수 있기 때문이다. `equals()`를 재정의 하지 않으면 `hashCode()`가 만든 해시값을 이용해 객체가 저장된 버킷은 찾겠지만 해당 객체가 자신과 같은 객체인지 값을 비교할 수 없어 `null`을 리턴한다.
