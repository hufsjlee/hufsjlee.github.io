---
title: "Interceptor"
excerpt: "프로젝트에 Interceptor 적용"

categories:
  - Project
tags:
  - [tag1, tag2]

permalink: /project/projectIssue9/

toc: true
toc_sticky: true

date: 2023-08-30
last_modified_at: 2023-08-30
---

## 🔎 본문

### Interceptor 사용 이유?
- 컨트롤러(Controller)에 접근하는 과정에서 권한 관련 로직을 제어하기 위해 사용.

### HandlerInterceptor
- HandlerInterceptor 인터페이스를 구현할 클래스를 생성
- preHandle()은 무엇인가?
  - 컨트롤러(Controller) 접근하기 전 수행되도록 preHandle() 메서드를 구현

### WebMvcConfigurer
- WebMvcConfigurer 인터페이스 구현함으로써 인터셉터 적용
  - logFilter()
    - 필터를 등록할 때 **@Bean**으로 등록
    - setFilter() -> 직접 구현한 클래스(MyFilter) 등록
    - setOrder() -> 필터 체인(chain) 순서 등록
    - addUrlPatterns() -> 필터가 수행될 URL을 정의
  - addInterceptors()
    - 애플리케이션 내에 인터셉터를 등록
      - addPathPatterns() -> 인터셉터를 호출하는 주소와 경로 추가