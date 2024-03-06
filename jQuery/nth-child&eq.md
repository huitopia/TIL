```Javascript
$("nav div:nth-child(" + (i + 1) + ")").html(menuA[i]);
$(".text li:eq(" + i + ")").html(at0A[i]);
```

`nth-child`는 그 순서의 모든 object를 선택하지만, `eq`는 딱 하나의 object만 선택한다.
