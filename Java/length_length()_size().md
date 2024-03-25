하나 해보고 안되면 다른 거 쓰고를 반복하다 한 번은 구분해야겠다 싶어서 작성함 😤

# length / length() / size() 사용법 및 차이

length : **_배열_** 의 길이 반환

```Java
String[] arr = {"a", "b", "c"};
System.out.println(arr.length); // 3
```

length() : **_문자열_** 의 길이 반환

```Java
String[] str = "hello";
System.out.println(str.length()); // 5
```

size() : **_Collection, 자료구조_** 의 크기(길이) 반환

```Java
ArrayList<String> arrlist = new ArrayList<String>();
arrlist.add('a');
arrlist.add('b');
System.out.println(arrlist.size()); // 2
```
