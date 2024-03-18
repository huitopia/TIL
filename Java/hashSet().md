# hashSet()

`HashSet`은 `Collection`의 하나로 중복되지 않는 데이터를 순서에 상관 없이 저장한다. `HashSet`은 **중복을 허용하지 않기 때문에** 저장 요청이 왔을 때 기존 데이터에 같은 데이터가 있는지 여부를 판단해야 한다.

**_`hashCode()`와 `equals()` 메소드를 이용하여 동등 객체인지 판단 후 동등 객체이면 `HashSet`은 저장하지 않는다._**

[예제 코드](https://github.com/huitopia/study-java/blob/master/src/ch12/sec03/exam02/HashSetExample.java)
