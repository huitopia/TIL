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

## 응용

### tip에 마우스 커서 올리면 가려진 정보 나타남

![Feb-02-2024 11-08-39](https://github.com/huitopia/TIL/assets/87823892/4c46e412-3ea8-41de-8675-d918179900c4)

```CSS
.tip {
  border: 1px solid yellow;
  width: 50px;
  height: 50px;
  border-radius: 70%;
}
.tip:hover div {
  margin-left: 0;
}
.tip p {
  width: 100%;
  height: 100%;
  text-align: center;
  line-height: 50px;
}
.tip div {
  border: 1px solid skyblue;
  width: 300px;
  height: 70px;
  line-height: 70px;
  margin-left: -300px;
  transition: all 0.5s;
}
```

.tip `div`에 `margin-left`로 부모 기준으로 옆에 밀어 숨겼다가 `tip:hover`시 `div`의 `margin-left`를 0으로 만들어 숨겨놨던 .tip `div`를 보이게함

### `top` 응용

![Feb-02-2024 11-22-37](https://github.com/huitopia/TIL/assets/87823892/9cf3594a-7170-4d4c-8da3-6405389e61bb)

```CSS
.tip {
  position: fixed;
  bottom: 200px;
  right: 0px;
  border: 1px solid yellow;
  width: 50px;
  height: 50px;
  border-radius: 70%;
}
.tip:hover div {
  margin-left: -250px;
}
.tip p {
  width: 100%;
  height: 100%;
  text-align: center;
  line-height: 50px;
}
.tip div {
  border: 1px solid skyblue;
  width: 300px;
  height: 70px;
  line-height: 70px;
  margin-left: 50px;
  position: absolute;
  top: 0;
  transition: all 0.5s;
  background-color: rgb(255, 196, 0);
}
```

상위 클래스 .tip에 `position` 있으므로 .tip `div`에 `position` 주고 `top` 지정하여 위치 변경

## `position` 적용 시 `padding` 효과 사라지는 이유

부모 태그에 `padding`적용 후 자식 태그에서 `position` 적용 시 `padding` 효과 사라져 자식 태그에서 다시 `position` `top`, `left`를 지정하거나 `padding` 지정한다.
