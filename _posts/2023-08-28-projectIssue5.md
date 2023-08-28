---
title: "Swagger 오류 문제"
excerpt: "Failed to start bean 'documentationPluginsBootstrapper'; nested exception is java.lang.NullPointerException"

categories:
- Project
  tags:
- [tag1, tag2]

permalink: /project/projectIssue5/

toc: true
toc_sticky: true

date: 2023-08-28
last_modified_at: 2023-08-28
---

## 🔎 본문

### 갑자기 마주친 에러 로그!
- 프로젝트 내 예약 기능에 동시성 처리를 위해 redis 의존성을 추가했더니 예상치 못한 오류 로그를 만났다.
- 우선 동시성 처리가 중요하기 때문에 테스트 코드를 작성하고 테스트를 통과하는지 확인 후에 다시 Swagger를 필요로 할 때 이 오류를 해결해 봐야겠다.
