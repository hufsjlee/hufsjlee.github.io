---
title: "Fallback 이란?"
excerpt: "서비스에 적용한 외부 API 가 동작하지 않는 이슈가 발생한다면?"

categories:
  - Project
tags:
  - [tag1, tag2]

permalink: /project/projectIssue12/

toc: true
toc_sticky: true

date: 2023-08-30
last_modified_at: 2023-08-30
---

## 🔎 본문

### 외부 API 가 갑자기 동작하지 않는다면..?
- 프로젝트 내에 **주소검색** 기능을 위해 카카오 로컬 API 를 적용했는데, 만약 카카오 API가 먹통이 된다면 어떻게 이를 처리할 수 있을까?
- 이에 대해 궁금해서 이것 저것 검색해보던 중 **Fallback**에 대해서 알게 되었다

## 해결 방안
- 행정안전부 API 등 다른 외부 API를 추가하고 카카오 로컬 API가 동작하지 않을 때에는 행정안전부 API로 대체될 수 있도록 로직을 작성해야 할 것으로 보인다!




