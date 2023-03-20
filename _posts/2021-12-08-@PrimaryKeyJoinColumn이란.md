---
layout: post
title: \@PrimaryKeyJoinColumn이란
date: '2021-12-08'
description: '@PrimaryKeyJoinColumn이란?'
categories: ['Backend', 'SpringBoot', 'JPA', 'Tips']
tags: ['Backend', 'SpringBoot', 'JPA', 'Tips']
---
# @PrimaryKeyJoinColumn이란?

### 📌 정의

JPA 1.0에서는 **OneToOne관계 또는 ManyToOne관계**에서 Id를 사용할 수 없었으므로 사용했던 것이 `@PrimaryKeyJoinColumn`이다.

`@Id` + `@JoinColumn`과 `@PrimaryKeyJoinColumn`은 **유사**하다. 하지만, 앞에서 쓴 방식(`Id + JoinColumn`)이 더 명확해서 추천한다.

현재 `@PrimaryKeyJoinColumn`은 **상속관계 매핑**(JOINED)에서 사용되고있다.