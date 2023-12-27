# Constructor (생성자)

### 생성자는 객체를 생성하고 변수에 초기값을 설정하는데 그때 반복되는 초기값을 생성자를 이용하여 간단하게 만들 수 있다.

### 기초 객체 생성 후 초기화 ex.
```java
public class MemberInit {
 String name;
 int age;
 int grade;
}

public static void main(String[] args) {
 MemberInit member1 = new MemberInit();
 member1.name = "user1";
 member1.age = 15;
 member1.grade = 90;

 MemberInit member2 = new MemberInit();
 member2.name = "user2";
 member2.age = 16;
 member2.grade = 80;
```


### 이것을 생성자를 이용하여 짧게 만들어 보자.

## 생성자
### 인텔리제이에서는 Alt+Insert 버튼으로 쉽게 생성자를 만들 수 있다.



```java
public class MemberInit {
 String name; // 변수 생성
 int age;
 int grade;

 MemberConstruct(String name, int age, int grade) { // 생성자 
        System.out.println("이름:" + name + " 나이:" + age + " 성적: " + grade); //생성자에 바로 출력하는 메서드 생성
        this.name = name;
        this.age = age;
        this.grade = grade;
    }

// 메인 영역
        public static void main(String[] args) {
        MemberConstruct member1 = new MemberConstruct("한사장", 30, 90);

        MemberConstruct member2 = new MemberConstruct("한국인", 25, 95);
        }
} // 이런식으로 한줄로 객체와 초기화,출력까지 한번에 할 수 있게되며 빠르고 가독성도 좋게 만들 수 있다. 

```

### 비교해 볼 수 있도록 메서드도 확인해 보자.
## 메서드
```java
public class MemberMethod {
  String name;
    int age;
    int grade;


    void members(String name, int age, int grade) {
        this.name = name;
        this.age = age;
        this.grade = grade;
    }

public static void main(String[] args) {
        MemberInit member1 = new MemberInit(); // 메서드
        member1.members("한우종", 31, 90);
        MemberInit member2 = new MemberInit();
        member2.members("김보미", 31, 100);
    }
    MemberInit[] members = {member1, member2}; // 배열에 넣고 
    
        for (MemberInit member : members) {//foreach를 통하여 출력
            System.out.println("이름:" + member.name + " 나이:" + member.age + " 성적: " + member.grade);
        }
}

```

### 이런식으로 2명의 맴버를 만들고 출력하는데도 생성자를 이용하면 복잡함과 길이를 많이 줄여줄 수 있다.

