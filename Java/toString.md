# toString()

`Object.toString()` 메소드는 **_객체의 문자 정보(객체를 문자열로 표현한 값)를 반환한다._** 반환되는 문자열은 클래스 이름과 함께 구분자로 @가 사용되며, 그 뒤로 16진수 hashCode가 추가된다.

`toString`은 말 그대로 객체의 정보를 `String`(문자열)형으로 변환한다. `Object` 클래스를 상속 받은 클래스들은 `toString()`을 오버라이딩(재정의)하여 사용 가능하다.
객체의 주소값이 아닌 **객체의 고유 정보를 출력하고 싶을 때 오버라이딩(Overriding)을 통해 `toString()` 메소드를 재정의** 해주면 된다.
