---
title: "카카오 로컬 API 사용_(with Retrofit)"
excerpt: "외부 서비스와의 통신을 위한 Retrofit 사용 사례"

categories:
  - Project
tags:
  - [tag1, tag2]

permalink: /project/projectIssue11/

toc: true
toc_sticky: true

date: 2023-08-30
last_modified_at: 2023-08-30
---

## 🔎 본문

### 외부 서비스와 통신을 위해서 어떤 라이브러리를 사용할 수 있을까?
- 주소 검색 기능을 추가하고 싶어서 외부 서비스(외부 API)와 통신하고 싶었다. 여러가지를 검색해보니 WebFlux와 WebClient도 있었지만
내 프로젝트에서는 retrofit을 사용했다.
- 그래서, 카카오 로컬 API를 적용하기 위해서 server와 client 간 HTTP 통신을 위해 retrofit 사용

### Retrofit을 선택한 이유는?
- **간편한** API 정의가 가능하고 **가독성**이 좋다는 측면에서 선택
- Okhttp 라이브러리 사용으로 인터페이스를 통해 **편리**하고 **간결하다**는 점이 장점으로 다가옴

### Retrofit을 사용해서 외부 API를 처음 사용해보고 느낀점
- server와 client 통신을 위해 라이브러리 사용은 처음해보았는데, Okhttp 라이브러리를 인터페이스를 통해서 생각보다 간편하게
사용할 수 있었다.



