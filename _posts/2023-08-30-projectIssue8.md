---
title: "Filter"
excerpt: "프로젝트 내 Filter 적용"

categories:
  - Project
tags:
  - [tag1, tag2]

permalink: /project/projectIssue8/

toc: true
toc_sticky: true

date: 2023-08-30
last_modified_at: 2023-08-30
---

## 🔎 본문

### Filter를 적용한 이유?
- servlet 실행 전과 후에 요정(request)과 응답(response)에 대한 필터링을 하기위해 Filter를 적용

### Filter의 동작 과정
- Filter는 1)초기화 -> 2)필터링 -> 3)소멸 의 단계를 거친다.
- Filter 인터페이스를 구현할 클래스(MyFilter) 생성한 후 메서드를 구현
  - init()
  - doFilter() -> 서비스의 request와 response에 대한 필터링 로직 작성
  - destroy()
- @Component
  - Filter를 적용하기 위해서 스프링빈(Spring Bean) 으로 등록하여 사용

