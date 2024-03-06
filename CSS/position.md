- absolute : 절대 위치
- relative : 상대위치 고정
- fixed : 고정 위치

> absolute example

```CSS
* {
  margin: 0;
}

div {
  width: 200px;
  height: 200px;
  border: 1px solid black;
  position: absolute; /* 기준 */
}

.red {
  background-color: red;
}

.green {
  background-color: green;
  top: 50px;
}

.blue {
  background-color: blue;
  top: 100px;
}
```

<img width="200" alt="스크린샷 2024-01-31 12 37 25" src="https://github.com/huitopia/TIL/assets/87823892/278d2c1e-6512-4a15-9812-db054e74185c">

## z-index

숫자가 클수록 위로 올라옴(layer층 조절)

> z-index example

```CSS
.green {
  background-color: green;
  top: 50px;
  z-index: 1;
}
```

<img width="200" alt="스크린샷 2024-01-31 12 39 53" src="https://github.com/huitopia/TIL/assets/87823892/9526fc58-e5fc-4851-864d-d59c69e9505c">
