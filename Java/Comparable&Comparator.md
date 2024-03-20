# Comparable 과 Comparator

둘 다 Interface로 선언된 메소드는 무조건 구현해야한다. **_객체를 비교하는 것 자체는 같지만 비교 대상이 다르다._** 사용자가 정의한 기준을 토대로 비교를 하여 양수, 0, 음수 중 하나를 반환한다.

## Comparable

`Java.lang` package에 있는 `Interface`이며, **자기 자신과 매개변수 객체**를 비교한다. `compareTo(<T> e)` 메소드가 선언되며, **기본 정렬 기준**을 구현하는데 사용한다.
자기 자신이 매개변수보다 작으면 음수, 아니면 양수를 반환한다.

## Comparator

`Java.util` package에 있는 `Interface`이며, **두 매개변수 객체**를 비교한다. `compare(T o1, T o2)` 메소드가 선언되며, **기본 정렬 기준 외에 다른 기준으로 정렬**하고자 할 때 사용한다.
