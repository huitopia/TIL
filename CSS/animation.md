## `anumation` 응용

### 3초동안 scale 1.5로 시작(0%)해서 1로 끝(100%)나는 화면 구현하기

![Feb-02-2024 15-37-32](https://github.com/huitopia/TIL/assets/87823892/ff18424b-af16-4aec-800f-d49671c7bcfe)

```CSS
.sec1 .ground1 {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -1;
  /* border: 1px solid yellowgreen; */
  background: url(../img/black-1072366_1280.jpg);
  background-size: 100% 100%;
  animation: ground1_ani 3s;
}
@keyframes ground1_ani {
  0% {
    transform: scale(1.5);
  }
  100% {
    transform: scale(1);
  }
}
```
