---
title: "Response"
excerpt: "Response Code 관리 방법"

categories:
  - Project
  tags:
  - [tag1, tag2]

permalink: /project/projectIssue2/

toc: true
toc_sticky: true

date: 2023-08-20
last_modified_at: 2023-08-20
---

## 🔎 본문

### Response를 깔끔하게 정리하여 관리하는 방식 적용
- 공통 응답 코드 BaseResponse 클래스에서 관리
- 일관된 응답 형식을 위한 응답 스펙 클래스 정의
- 클래스 내 필드는 code(응답 코드) / msg(응답 메세지) / result(응답 결과) / timestamp(응답 시간)를 포함
