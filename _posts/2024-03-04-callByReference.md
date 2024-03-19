---
title: "Call by reference"
excerpt: "Call by reference란 무엇이고 보통 어떻게 쓰일까?"

categories:
  - CS
tags:
  - [tag1, tag2]

permalink: /cs/reference/

toc: true
toc_sticky: true

date: 2024-03-04
last_modified_at: 2024-03-04
---

## 🔎 본문

### Call By Reference란?

Call by reference는 함수에 매개변수를 전달할 때, 해당 매개변수의 메모리 주소를 전달하는 방식입니다. 이는 함수 내에서 매개변수의 값을 변경할 때, 실제로 메모리에 있는 데이터를 직접 조작할 수 있게 해줍니다.

보통 프로그래밍 언어에서는 Call by reference를 사용할 때, 포인터 또는 레퍼런스를 이용합니다. 자바에서는 Call by reference를 직접적으로 지원하지 않습니다. 그 대신, 객체를 통한 참조 전달이 발생합니다.

### 예제 코드
```java
class Number {
    int value;

    Number(int value) {
        this.value = value;
    }
}

public class CallByReferenceExample {
    // 객체를 통한 참조 전달
    static void square(Number num) {
        num.value = num.value * num.value;
    }

    public static void main(String[] args) {
        Number number = new Number(5);

        System.out.println("square 함수 호출 전: " + number.value);

        // 객체를 통해 참조 전달
        square(number);

        System.out.println("square 함수 호출 후: " + number.value);
    }
}
```
```java
square 함수 호출 전: 5
square 함수 호출 후: 25
```
- 위와 같은 방식으로 자바에서는 객체를 이용하여 참조를 전달함으로써 Call by reference와 유사한 효과를 얻을 수 있습니다.

