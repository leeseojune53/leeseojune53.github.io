---
layout: post
title: ! 'static 변수에 @Value 사용하기'
date: '2021-09-21'
description: 'static 변수에 @Value 사용하기'
categories: ['Backend', 'SpringBoot', 'Tips']
tags: ['Backend', 'SpringBoot', 'Tips']
---
# static 변수에 @Value 사용하기

### 🐛 문제 상황

static 변수에 @Value를 사용하였는데 null값이 들어가있음.

### 🏴‍☠️ 원인

Spring에서 static 변수에 값 주입을 허용하지 않기 때문이다.

### ♻ 해결법

해당 static field의 Setter를 만들어서 해당 메소드 위에 @Value("${~~}")를 붙인다.