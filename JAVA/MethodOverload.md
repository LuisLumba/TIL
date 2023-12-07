# Method Overload

1. 같은 이름의 메소드명 생성 할 수 있다.
2. 매개변수의 타입,갯수 등 달라야한다.
3. return 값이 있던 없던 상관없다.

Ex. 가능
```java
add(int a, int b) 
add(int a, int b, int c) // 갯수가 다름
add(double a, double b) // 타입이 다름
add(int a, double b) // 타입이 다름
add(double a, int b) 타입 순서가 다름
```

Ex. 불가능
```java
int add(int a, int b)
int add(int c, int d) // 매개변수 타입이 같음
double add(int a, int b) // 메소드 타입이 달라도 이름과 매개변수가 같으면 불가능

 public static int add(int a, int b) {
        int sum = a + b;
        return sum;
    }
    public static double add(int a, int b) {
        double sum = a + b;
        return sum;
    }  = 이름과 매개변수 같아서 불 가 능

// -------------------------------------------

    public static void add(int a, int b) {
        int sum = a + b;
        Systen.out.println(sum);
    }
    public static double add(int a, int b) {
        double sum = a + b;
        return sum;
    }  = return 값이 있던 없던 이름과 매개변수 같아서 불 가 능
```