# System.identityHashCode(Object o)

**객체의 주소값 비교 메소드**로 객체의 주소를 기준으로 한 해시 값을 리턴 받고 싶을 때 사용한다.

`String`의 경우 해당 객체의 주소가 아닌 객체가 가진 문자열로 `hashCode`를 생성한다.

```Java
String str1 = new String("hello");
String str2 = new String("hello");

System.out.println(System.identityHashCode(str1)); // 758529971
System.out.println(System.identityHashCode(str2)); // 2104457164

String str3 = "hello";
String str4 = "hello";

System.out.println(System.identityHashCode(str3)); // 1521118594
System.out.println(System.identityHashCode(str4)); // 1521118594
```

`str3`과 `str4`는 객체가 가진 문자열로 `hashCode`를 생성하였지만 `str1`과 `str2`는 새로운 객체를 생성하였기 때문에 값이 다르다.

**new를 사용한 `str1`과 `str2`가 다른 이유**

new 연산자는 새로운 객체를 만드는 연산자로 같은 객체를 공유하지 않고 **각각 서로 다른 객체의 번지를 가지기 때문**이다.
