# parseInt() & intValue()

## parseInt()

**`String`형 객체에서 `int`형 값을 추출하는 메소드**로 `static`이므로 **_`Integer` 생성 없이_** `parameter`만 넣어주면 메소드가 실행된다.

```Java
String str = "123";
int num = Integer.parseInt(str);
```

## intValue()

**`Integer` 객체에서 `int`형 값을 추출하는 메소드**로 `Object` 타입을 `int`형으로 변환한다.

```Java
String str = "123";
int num = Integer.valueOf(str).intValue();
```

## valueOf()

문자열의 값을 정수형으로 변환 후 Integer 객체로 만들어 반환한다.

new Integer(Integer.parseInt(s)) 값이 리턴된다.

---

> parseInt() : 내용물 ➡️ 내용물 형변환
>
> intValue() : 객체 ➡️ 내용물 변환

```Java
String str = "123";
// parseInt 사용 예시
int number = Integer.parseInt(str);
// intValue() 사용 예시 1
Integer a = new Integer(123);
int number = a.intValue();
// intValue() 사용 예시 2
int k = Integer.valueOf(str).intValue(); // 123
```
