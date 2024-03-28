# Byte Stream & Character Stream

## 이미지 파일을 문자 스트림으로 사용했다 생긴 일

원본 이미지 파일을 복사하는 프로그램을 만드는 문제 코드를 구현하다 막히는 부분이 있었다.
실행시 이미지 파일이 제대로 복사가 안 돼서 뭐가 문제일까 하다가 혹시나 싶어 문자 스트림을 바이트 스트림으로 변경했더니 원했던 출력 결과가 나와서 좋았지만 매우 당황스러웠다.
문자 스트림은 문자 자체를 읽어온다 그래서 더 좋겠지 라는 생각에 사용했지만 왜였을까...

**변경 전 코드**

```Java
Reader reader = new FileReader(path);
Writer writer = new FileWriter(copyPath);
char[] data = new char[100];
int len = 0;
while ((len = reader.read(data)) != -1) {
  writer.write(data, 0, len);
}
reader.close();
writer.close();
```

**변경 후 코드**

```Java
InputStream is = new FileInputStream(path);
OutputStream os = new FileOutputStream(copyPath);
byte[] data = new byte[1024];
while (true) {
  int num = is.read(data);
  if (num == -1) break;
  os.write(data, 0, num);
}
os.flush();
os.close();
is.close();
```

> ### 💡
>
> 문자 스트림은 오로지 **유니코드 상의 문자를 위한 방식이다.**
> 이미지, 동영상 파일의 경우 문자 스트림 방식을 사용하면 안된다.
> **_1byte 단위로 데이터가 구성된 파일을 2byte 단위로 읽어들여_** 파일이 깨지기 때문에 바이트 스트림 방식을 사용해야한다.
