1. 기본 생성자 필수

```
자바 언어에서 상속을 받으면 자식 클래스의 생성자를 호출할 때
자식 클래스의 생성자에서 부모 클래스의 생성자도 호출해야 한다. (이 부분이 생략되어 있다면 자식
클래스의 생성자 첫줄에 부모 클래스의 기본 생성자를 호출하는 super() 가 자동으로 들어간다.) 이
부분은 자바 문법 규약이다.

(기본 생성자는 파라미터가 하나도 없는 생성자를 뜻한다. 생성자가 하나도 없으면
자동으로 만들어진다.)
```
