---
title: "테스트 코드 작성"
excerpt: "테스트 코드 작성 중 발생한 이슈"

categories:
  - Project
tags:
  - [tag1, tag2]

permalink: /project/projectIssue15/

toc: true
toc_sticky: true

date: 2023-09-14
last_modified_at: 2023-09-14
---

## 🔎 본문

### stadium 테이블
- stadium 테이블의 stadium_id 가 1인 구장의 '참여 가능한 최대 인원(maximumPersonnel)'은 18명으로 설정되어 있다.
  (reservable_stadium 테이블에는 stadium_id를 외래키(FK)로 가지고 있다.)
  <img src="https://github.com/HUFSjlee/stadiumManager-backend/assets/67497759/f22c5a97-0007-48ae-baf6-f9b0ba96fdd4/">
  <img src="https://github.com/HUFSjlee/stadiumManager-backend/assets/67497759/9b2f4561-2d8e-400f-aeb9-79d8df7d85e7/">

### 테스트 진행 과정 및 이슈
- 1. stadium_id가 1인 구장에 30명이 동시에 예약 신청을 시도한 상황이라고 가정하고 테스트를 진행해보려한다.
  2. 위 1번을 진행할 때, Lock을 걸었을 때와 Lock을 걸지 않았을 때의 결과값의 차이를 알아보고자 한다.
  3. 우선 현재 프로젝트의 reservationService 내에 있는 reserve 메서드에 Lock을 설정해둔 상태이고, Lock을 걸었을 때의 기댓값을(예측값)을 18로 예측했는데 엉뚱항 결과값이 나오는 문제가 발생
  4. Member 엔티티에서 JPA 쿼리 메서드를 만들어서 사용할 수도 있었지만 첫 테스트이기 때문에 stadium_id가 1인 구장에 예약이 가능한 조건을 충족하는 member를 테스트 코드 내에 하드코딩 해두었다.
  <img src="https://github.com/HUFSjlee/stadiumManager-backend/assets/67497759/fb50e40c-af73-4686-9c22-52ed7919809c/">