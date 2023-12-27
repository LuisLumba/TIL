# Access Modifier (접근제어자)

## 접근제어자는 객체지향프로그램의 캡슐화의 특징이다.

### 접근제어자는 4가지가 있으며 각각에 역할에 맞게 호출할 수 있는 권한을 나누어 준다.



## 접근제어자 종류
1. default : 같은 패키지 안에서만 호출을 허용한다. (생략가능 하며 제어자를 쓰지 않으면 자동으로 default가 된다.)
2. public : 모든 외부에서 호출할 수 있다.
3. private : 모든 외부 호출을 막으며 숨겨야할 속성(데이터)에 사용한다.
4. protected : 같은 패키지 안에서 호출 가능하고 추가로 상속관계의 호출도 가능하다.


## 접근제어자 사용 위치
- 필드
- 메서드
- 생성자
- 클래스 는 public과 default만 사용할 수 있다.

```java
public class Speaker { //클래스 레벨
 
 private int volume; //필드
 
 public void volumeUp() {} //메서드
 public void volumeDown() {}
 public void showVolume() {}

 public Speaker(int volume) {} //생성자
}
```