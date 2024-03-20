# List & ArrayList

List는 **Interface**이며, 공통되는 메소드를 추출한 클래스로 List 안에 ArrayList, LinkedList.. 등이 포함되어 있다.

ArrayList는 List를 구현한 **Class** 이므로, List로 선언한 경우 instance를 ArrayList로 받을 수 있고 LinkedList로 받을 수 있다.

```Java
List<> list = new ArrayList<>();
List<> list = new ArrayList<>();
```

List와 ArrayList 모두 같은 결과를 도출하지만, List를 사용해 ArrayList를 생성하는 것은 **유연성**에서 효과를 볼 수 있다.
Array 배열의 크기를 5개로 정했다면 5개 이상의 값을 담을 수 없지만 **_List는 크기가 정해져 있지 않아 원하는 만큼 값을 담을 수 있다._**
