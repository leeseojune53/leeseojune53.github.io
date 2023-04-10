---
layout: post
title: PVC(Persistent Volume Claim)
date: '2022-05-03'
description: 'PVC(Persistent Volume Claim)란?'
categories: ['DevOps', 'K8S', 'Storage']
tags: ['DevOps', 'K8S', 'Storage']
---
# PVC(Persistent Volume Claim)란?

### 📌 정의

사용자(파드)의 스토리지에 대한 **요청**이다.

PV를 참조(요청)하는 것

### ⚙️ Spec

- 클래스 : storageClassName 속성에 작성
  - 요청된 클래스의 PV만 바인딩 될 수 있다.
  - 반드시 Class로 요청할 필요는 없다. 값이 ""로 설정된 PVC는 is-default-class가 true로 되어있으면 기본값 PV에만 바인딩되고, 설정되어있지 않으면 클래스가 없는 PV에만 바인딩할 수 있다.