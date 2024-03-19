---
title: "시간복잡도와 공간복잡도"
excerpt: "시간복잡도와 공간복잡도에 대해 알아보자!"

categories:
  - OS
tags:
  - [tag1, tag2]

permalink: /os/complexity/

toc: true
toc_sticky: true

date: 2024-03-19
last_modified_at: 2024-03-19
---

## 🔎 본문

## 시간 복잡도와 공간 복잡도
시간 복잡도와 공간 복잡도의 개념을 알아야 하는 이유가 있다. 이 두 가지의 개념이 가장 중요한 이유는 코드의 효율성을 수치화하여 가장 잘 나타낼 수 있는 지표이기 때문이다.

**1) 시간 복잡도(Time complexity):** 프로그램이 실행되고, 완료되는데 걸리는 시간(이론적으로 계산할 수 있는)

**2) 공간 복잡도(Space complexity):** 프로그램이 실행되고, 완료되는데 필요한 메모리

실행 시간과 메모리 사용량은 프로그래밍이 있어서 한정적 자원(computing resource)입니다.(물론 하드웨어의 발전으로 인해 옛날 보다는 한정적이지 않긴 합니다.) 때문에 이를 효율적으로 활용해야합니다.

### 시간 복잡도(Time Complexity)
시간 복잡도는 컴파일타임(Compile Time)과 러닝타임(Excution&Running)으로 나뉩니다. 실행시간은 컴퓨터 사양과 네트워크 환경 등에 따라 변수가 너무 많기 때문에, 컴파일 시간의 복잡도만 계산하면 됩니다.

예를 들어, for문으로 구구단을 1단부터 9단까지 나오게끔 코드를 짜면, 코드가 9 x 9 = 81번, 즉 9의 2승 만큼 실행이 됩니다. 그럼 N단이 나오는 코드를 짜면 어떤 값이 나올까요? N^2의 값이 나올 겁니다. 이렇게 사용하는 데이터 개수(N)에 의해서 시간복잡도가 정해집니다.

### 공간 복잡도(Space Complexity)
공간 복잡도는 코드의 효율성을 수치화할 수 있는 지표입니다. 프로그램을 실행하면, 데이터들이 RAM이라는 메모리에 올라가게 되는데, 이때 메모리의 크기는 고정되어 있습니다. 즉, 메모리를 최대한 덜 잡아먹게끔 코드를 설계해야 합니다.

설계한 코드의 공간복잡도를 계산하는 방법은 고정공간 요구량과 가변공간 요구량의 덧셈으로 구할 수 있습니다.

**1) 고정 공간 요구량(Fixed space requirements):** 자료구조가 사용하는 고정된 메모리 공간을 의미합니다. 고정된 크기를 갖는 변수(int, double)가 여기에 포함되며, 크기가 정해진 배열의 경우에도 고정 공간 요구량에 속합니다.

**2) 가변 공간 요구량(Variable space requirements):** 필요에 따라 동적으로 할당, 해제되는 메모리의 공간을 의미합니다. 특정 instance에 따라서 사이즈가 달라지는 변수들이 여기에 속합니다.

출처: [https://coduking.com/entry/자료구조란-feat-시간복잡도-공간복잡도](https://coduking.com/entry/%EC%9E%90%EB%A3%8C%EA%B5%AC%EC%A1%B0%EB%9E%80-feat-%EC%8B%9C%EA%B0%84%EB%B3%B5%EC%9E%A1%EB%8F%84-%EA%B3%B5%EA%B0%84%EB%B3%B5%EC%9E%A1%EB%8F%84) [코딩에듀킹:티스토리]


