# equals()

## Object.equals()

`Object`의 `equals()` 메소드는 **객체의 주소**를 비교하고 boolean 값으로 동일하면 true, 아니면 false를 반환한다.

`Object.equals()` 메소드는 재정의 후 동등 비교용으로 사용한다. **동등 비교란 객체가 비록 달라도 내부의 데이터가 같은지**를 비교하는 것이다.

같은 값을 가진 객체라 할지라도 따로 생성되었다면 false를 반환한다.

```Java
Member obj1 = new Member("blue");
Member obj2 = new Member("blue");

boolean result = obj1.equals(obj2)
```

new 연산자로 생성시 객체의 번지는 다 다른 번지이기에 결과로 false를 반환한다.

```Java
    @Override
    public boolean equals(Object obj) {
        if (obj instanceof Member target) {
          // obj가 Member 타입인지 검사하고 타입 변환 후 target 변수에 대입
            if (id.equals(target.id)) { // id 문자열이 같은지 비교
                return true;
            }
        }
        return true;
    }
```

하지만 Member class 안에서 `equals()`를 재정의 하면

```Java
boolean result = obj1.equals(obj2)
```

매개값이 Member 타입이고 `id`도 동일하여 true를 반환한다.

### equals()와 hashCode()

`Object.equals()` 메소드를 재정의 하면 `hashCode()`도 반드시 재정의해야 한다. `hashCode()`를 재정의 하지 않으면 같은 값 객체라도 해시값이 다를 수 있기 때문이다. `equals()`를 재정의 하지 않으면 `hashCode()`가 만든 해시값을 이용해 객체가 저장된 버킷은 찾겠지만 해당 객체가 자신과 같은 객체인지 값을 비교할 수 없어 `null`을 리턴한다.
