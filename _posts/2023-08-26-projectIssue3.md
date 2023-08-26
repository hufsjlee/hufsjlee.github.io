---
title: "예외처리"
excerpt: "예외를 공통으로 처리하기"

categories:
- Project
  tags:
- [tag1, tag2]

permalink: /project/projectIssue3/

toc: true
toc_sticky: true

date: 2023-08-20
last_modified_at: 2023-08-20
---

## 🔎 본문

### 발생하는 예외를 공통으로 처리하기 위해 적용한 방식
- @ExceptionHandler 적용
  - 각 클래스에서 발생하는 예외를 처리할 수 있는 Exception Handler 사용
  

- @RestControllerAdvice
  - GlobalExceptionHandler 클래스를 만들고, 클래스 내 적절한 예외를 처리하기 위해 만든 Custom Exception을 공통으로 처리
