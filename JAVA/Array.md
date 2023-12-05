# 배열 ( Array )

## 배열 선언,출력 방법

### 1차 배열

```java
public class Array {
    public static void main(String[] args) {

//        배열 선언 1
        int[] students = new int[5];
        
        students[0] = 90;
        students[1] = 80;
        students[2] = 70;
        students[3] = 60;
        students[4] = 50;


//        배열 선언 2 (생략+초기화)
        int[] students1 = {90, 80, 70, 60, 50}; // new int[] 생략 가능

//        출력 방법
for (int i = 0; i < 6; i++) {
            System.out.println("학생 " + (i + 1) + "번 점수 : " + students[i]);
        }

//       길이를 이용한 방법 
for (int i = 0; i < students1.length; i++) {
            System.out.println("학생 " + (i + 1) + "번 점수 : " + students1[i]);
        }
```

### 2차 배열
```java
//        배열 선언1
int[][] arrayD = new int[2][3];
        arrayD[0][0] = 1;
        arrayD[0][1] = 2;
        arrayD[0][2] = 3;
        arrayD[1][0] = 4;
        arrayD[1][1] = 5;
        arrayD[1][2] = 6;

//        배열 선언2 (생략+초기화)
int[][] arrayD1 = {
                {1, 2, 3},
                {4, 5, 6}
        };


//        출력 방법

for (int row = 0; row < 2; row++) {
            for (int column = 0; column < 3; column++) {
                System.out.print(arrayD[row][column] + " ");
        }
    }
//        길이를 이용한 출력
for (int i = 0; i < arrayD1.length; i++) {
            for (int column = 0; column < arrayD1[i].length; column++) {
                System.out.print(arrayD[i][column] + " ");
            }
        }
```
 **2차원 자리의 출력에서는 `arrayD1[(첫번째 for문의 int) i]` 넣어준다.**

 ### for문을 이용해 배열에 순서대로 1씩 증가하는 값 입력
 ```java
 int[][] arrayD2 = new int[3][5];
 int i = 1;
 for (int row = 0; row < arrayD2.length; row++){
    for(int column = 0; column < arrayD2[row].length; column++){
        arrayD2[row][column] = i++;
        System.out.print(arrayD2[row][column]+" ");
    }
    System.out.println();
 }
 ```

### 일차원 배열에서 순서대로 꺼낼때는 for-each 를 사용하면 좋다.
for (int 변수 : 배열변수){
    System.out.println(변수);
}

```java
for (int i : numbers){
System.out.print(i);
}
```
**Tip** : 인텔리제이에서 iter를 입력하면 자동으로 for-each를 만들어준다.
foreach를 직접 치는것보다 더 빠르고 편리하다.

**But**
for-each 를 사용할 수 없는 경우가 있다.
증가하는 index 값이 필요할때 이다.
```java
for (int i = 0; i < numbers.length; i++) {
    System.out.println("배열[" + i + "]번의 결과 : " + numbers[i]);
        }
```

이 때 index i값이 계속 증가해야 할 땐 일반for문 사용하는게 좋다.

