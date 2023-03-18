---
layout: post
title: @SuperBuilder에 필요한 생성자
date: '2022-07-18'
description: '@SuperBuilder에 필요한 생성자'
categories: ['Backend', 'ㅣLombok', 'Tips']
tags: ['Backend', 'Lombok', 'Tips']
---
# @SuperBuilder에 필요한 생성자



### 📌 정의

SuperBuilder는 자신의 부모클래스의 Field까지 Builder패턴으로 사용할 수 있는 어노테이션이다.

SuperBuilder을 사용할 때 @AllArgsConstructor를 같이 사용하는 예시를 많이 볼 수 있다. 하지만, 실제 SuperBuilder를 이용한 클래스가 build된 .class 파일을 보면 @AllArgsConstructor를 사용하지 않아도 생성자가 생성되어있다. 그래서 어디에서 생성자를 만들어주는지 알아보고자 이 글을 작성한다.

우선 handle이라는 거대한 method의 중간에

![SuperBuilder](https://github.com/leeseojune53/yatudy/blob/main/images/SuperBuilder.png)

이 부분이 존재한다.

@SuperBuilder가 붙어있는 Class에 **생성자가 존재하는지 체크**하고, 없다면 **생성자를 만들**어주는 코드이다.