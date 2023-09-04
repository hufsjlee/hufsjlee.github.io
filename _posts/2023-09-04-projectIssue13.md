---
title: "동시성 이슈"
excerpt: "동시성 이슈란 무엇이고, 해결 방법은 뭐가 있을까?"

categories:
  - Project
tags:
  - [tag1, tag2]

permalink: /project/projectIssue13/

toc: true
toc_sticky: true

date: 2023-09-04
last_modified_at: 2023-09-04
---

## 🔎 본문

### 동시성 이슈란?
- 여러 프로세스 및 스레드가 동시에 동일한 데이터 **(공유 데이터)** 를 조작할 때 타이밍이나 접근 순서에 따라 예상했던 결과가 달라질 수 있는 상황을 의미

## Redis로 동시성 이슈 해결하기
### Redis 라이브러리
  1) **Lettuce**  
    - Lettuce 는 Setnx 명령어를 활용하여 **분산락** 을 구현하고, 기존 값이 없을 때에만 Set을 하는 명령어이다.  
    - Setnx 는 Spin Lock 방식으로 retry 로직을 개발자가 작성.  
    - **Spin Lock**이란 Lock을 획득하려는 스레드가 Lock을 획득할 수 있는지 확인하면서 반복적으로 시도하는 방법.
  

   2) **Redisson**  
    - Pub-sub 기반으로 Lock 구현을 제공  
    - Pub-sub 방식이란, 락을 점유중인 스레드가 락을 해제했음을 대기중인 스레드에게 알려주면 대기중인 스레드가 락 점유를 시도하는 방식  
    - Lettuce와는 다르게 별도의 Retry 방식을 작성하지 않아도 된다.

## Lettuce 와 Redisson 장단점
### Lettuce
- 구현이 간단함
- Spring data redis을 이용하면 Lettuce가 기본이기 때문에 별도의 라이브러리를 사용하지 않아도 된다.
- Spin Lock 방식이기 때문에 동시에 많은 스레드가 lock 획득 대기 상태라면 Redis에 부하가 갈 수 있다.

### Redisson
- 락 획득 재시도를 기본으로 제공한다.
- pub-sub 방식으로 구현이 되어있기 때문에 Lettuce와 비교했을 때 Redis에 **부하**가 덜 간다.
- 별도의 라이브러리를 사용 해야 한다.
- Lock 라이브러리 차원에서 제공해주기 때문에 사용법을 공부해야 한다.

