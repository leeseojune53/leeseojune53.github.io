---
layout: post
title: setup-java
date: '2022-03-24'
description: 'Setup-java'
categories: [CI, Github]
tags: [CI, Github]
---
# Setup-java

#### 📌 정의

Github Actions workflow에서 **자바를 세팅**하는 Github Action

### 사용법

```yaml
steps:
- uses: actions/setup-java@v2
  with:
    distribution: '구현체 종류'
    java-version: '버전'
```

구현체 종류는 `temurin`, `zulu`, `adopt`, `adopt-openj9`, `liberica`, `microsoft`가 있다.

버전은 major만 보면 `8`, `11`, `16`, `17`이 있다.