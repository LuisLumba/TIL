# Extend (상속)

### 다른 클래스와 중복되는 메소드를 상위 클래스,하위 클래스로 나누어 상속으로 호출 하여 사용한다.
1. 상속 관계의 객체를 생성하면 그 내부의 부모,자식 모두 생성된다.하위클래스에서 메서드를 먼저 호출하고 없으면 상위인 부모 클래스에서 찾는다.
2. 그래도 없을경우 계속해서 상위 부모클래스에서 찾는다.
3. 만약 없다면 컴파일 오류가 발생


## Overriding (오버라이딩) = 재정의
### 상속받는 부모클래스의 기능을 그대로 쓰지 않고 자식 클래스에서 같은 이름으로 기능만 따로 수정하여 메서드를 사용한다.
- 이때 메모리는 부모클라스까지 갈 필요 없이 **자식에서 찾아서 바로 호출**한다.
- **@Override** 라고 위에 **annotation**을 해주고 이 annotation은 혹시나 오버라이드 할 메서드가 잘못되을때 알려주기 위함이다. 잘 되었을땐 오버라이딩 했음을 알려줄 수도 있다.


## 메서드 오버라이딩 조건
- **이름, 파라미터(매개변수),반환 타입**이 같아야함
- **접근제어자**가 상위 클래스보다 제한적이어서는 안된다.
ex. 상위클래스가 **protected**면 하위에선 **public** 또는 *protected* 여야 한다.
private,default 면 오버라이드 할 수 없다.  
- **static,final,private**가 붙은건 오버라이딩을 할 수 없다.
- **생성자**는 오버라이딩을 할 수 없다.

## Super 
### 부모와 자식의 필드명이 같거나 오버라이딩이 되어 있으면, 자식에서 부모의 필드나 메서드를 호출할 수 없다. 이때 super 키워드를 사용하면 부모를 참조할 수 있다.
### 예를들어 부모와 자식의 필드명이 둘다 value 로 똑같을때 자식클래스에서 부모클래스의 value 를 사용하려면 `super.value` 를 입력하면 부모의 value 를 호출하게 된다.

## 생성자에는 반드시 부모 클래스의 생성자를 호출해야 한다.
### 생성자 첫줄에는 먼저 `super` 또는 `this` 를 사용해야 한다.


## 