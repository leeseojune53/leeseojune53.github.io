---
layout: post
title: Request Wrapper를 만드는 이유
date: '2021-11-18'
description: 'Request Wrapper를 만드는 이유'
categories: ['Backend', 'SpringBoot', 'Tips']
tags: ['Backend', 'SpringBoot', 'Servlet', 'Tips']
---
# Request Wrapper를 만드는 이유

### ❓ 왜 만들까?

HttpServletRequest를 여러 번 읽고 싶을 때 Request Wrapper를 만드는데, 그 이유는 HttpServletRequest는 단 한 번 읽을 수 있기때문이다.

한 번 읽을 수 있는 이유는 Tomcat을 개발할 때 getInputStream을 한 번만 사용할 수 있게 제약한 것인데, 상세 내용은 아직 찾지 못했다😭