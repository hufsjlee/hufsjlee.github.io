---
title: "JPA N+1"
excerpt: "JPA N+1 문제 이슈"

categories:
  - Project
tags:
  - [tag1, tag2]

permalink: /project/projectIssue1/

toc: true
toc_sticky: true

date: 2023-08-20
last_modified_at: 2023-08-20
---

## 🔎 본문

### JPA N+1 문제을 위한 해결 방법
- ‘fetchType = Eager’ → ‘fetchType = Lazy’로 변경하였습니다.
-  FetchJoin을 활용하여 문제를 개선하였습니다.
