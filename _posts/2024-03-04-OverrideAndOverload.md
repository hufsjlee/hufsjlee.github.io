---
title: "Override 와 Overload"
excerpt: "Override 와 Overload 는 무엇이며, 어떤 차이가 있을까?"

categories:
  - CS
tags:
  - [tag1, tag2]

permalink: /cs/process/

toc: true
toc_sticky: true

date: 2024-03-04
last_modified_at: 2024-03-04
---

## 🔎 본문

### Overload(오버로딩)
* 오버로딩은 같은 메서드 이름을 가지면서 매개변수의 타입, 개수, 또는 순서가 다른 여러 메서드를 정의하는 것입니다. 즉, 동일한 메서드 이름으로 다양한 매개변수를 받아들일 수 있게 하는 것입니다.

```java
public class OverloadExample {
    // 정수형 매개변수를 받는 메서드
    public int add(int a, int b) {
        return a + b;
    }

    // 실수형 매개변수를 받는 메서드 (오버로딩)
    public double add(double a, double b) {
        return a + b;
    }

    // 문자열 매개변수를 받는 메서드 (오버로딩)
    public String add(String a, String b) {
        return a + b;
    }

    public static void main(String[] args) {
        OverloadExample example = new OverloadExample();

        System.out.println("정수형 덧셈: " + example.add(2, 3));
        System.out.println("실수형 덧셈: " + example.add(2.5, 3.5));
        System.out.println("문자열 이어붙이기: " + example.add("Hello", " World"));
    }
}
```
* 위 코드에서 add 메서드는 세 번 오버로딩되었습니다. 각각 정수형, 실수형, 문자열을 매개변수로 받아서 다른 연산을 수행하고 있습니다.

### Override(오버라이딩)
* 오버라이딩은 부모 클래스에서 정의된 메서드를 자식 클래스에서 동일한 시그니처(메서드 이름, 매개변수 타입 및 개수)로 다시 정의하는 것입니다. 이는 자식 클래스에서 부모 클래스의 메서드를 재정의하여 새로운 구현을 제공하는 것을 의미합니다.

```java
class Animal {
    void makeSound() {
        System.out.println("Some generic sound");
    }
}

class Dog extends Animal {
    // 부모 클래스의 makeSound 메서드를 오버라이딩
    @Override
    void makeSound() {
        System.out.println("Bark! Bark!");
    }
}

public class OverrideExample {
    public static void main(String[] args) {
        Animal animal = new Dog(); // 다형성을 이용한 객체 생성

        // Dog 클래스에서 오버라이딩한 makeSound 메서드가 호출됨
        animal.makeSound();
    }
}
```
* 코드를 보면 Dog 클래스는 Animal 클래스의 makeSound 메서드를 오버라이딩합니다. 부모 클래스의 메서드를 자식 클래스에서 새로운 구현으로 대체하므로, Dog 객체에서 makeSound를 호출하면 자식 클래스의 메서드가 실행됩니다.



