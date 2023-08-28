---
title: "RDBMS N:M"
excerpt: "테이블 설계 단계에서의 N:M 관계 이슈"

categories:
  - Project
  tags:
  - [tag1, tag2]

permalink: /project/projectIssue4/

toc: true
toc_sticky: true

date: 2023-08-28
last_modified_at: 2023-08-28
---

## 🔎 본문

### 관계형 데이터베이스 N:M 문제 해결 방식 
- 관계형 데이터베이스의 사용으로 N:M 관계에 있던 두 테이블을 N:1 / 1:N 으로 해결하길 원함.


- 문제 해결을 위해 N:M 관계에 있는 두 테이블 사이에 중간 테이블을 하나 두어 Entity로 만들고,
 Entity의 필드에 @OneToMany, @ManyToOne 어노테이션(annotation)을 사용하여 N:M 관계를 풀어냄
