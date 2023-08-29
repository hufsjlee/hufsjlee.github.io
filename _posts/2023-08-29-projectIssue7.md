---
title: "외부 API 사용"
excerpt: "외부 API 사용시 했던 고민"

categories:
  - Project
tags:
  - [tag1, tag2]

permalink: /project/projectIssue7/

toc: true
toc_sticky: true

date: 2023-08-29
last_modified_at: 2023-08-29
---

## 🔎 본문

### 의존성 문제
- 외부 API와 관련된 필드를 가지고 있는 ConversionCoordinatesSystem 클래스를 어떤 패키지에 위치시켜야 할까?
- 위의 고민 끝에 domain 패키지에 위치시키기로 결정. 이유는?
  - 지금까지 진행했던 패키지 구조상, 외부 API 관련된 필드를 가지고 있는 ConversionCoordinatesSystem 클래스를 Infrastructure 패키지에 위치시키게되면
    domain -> infrastructure 형식의 의존성 방향을 나타내는데, 이렇게 되면 infrastructure가 DB 통신과 외부 통신 등의 세부 구현 기술이 변경될 때 domain 패키지도 변경이 일어나기 때문
