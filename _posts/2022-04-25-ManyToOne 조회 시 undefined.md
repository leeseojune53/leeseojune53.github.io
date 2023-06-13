---
layout: post
title: ManyToOne 조회 시 undefined
date: '2022-04-25'
description: 'ManyToOne 조회 시 undefined'
categories: ['Backend', 'NestJS', 'Tips']
tags: ['Backend', 'NestJS', 'Tips']
---
# ManyToOne 조회 시 undefined

### 🐛 문제 상황

TypeORM의 EntityRepository를 이용해서 entity를 find하였는데, relation이 맺어져있는 필드를 가져오지 않아서 undefined가 나옴.

### 🏴‍☠️ 원인

TypeORM Entity에서 관계 설정을 할 때 Lazy 또는 Eager를 설정하지 않으면 로드되지 않는다.

### ♻️ 해결법

따로 설정하지 않는다면 find할 때 옵션을 아래와 같이 주면 된다.

```typescript
repository.find({
  ...
  relations: ['필드 명'],
});
```

Lazy로 설정한다면 필드를 가져오고, 아래와 같이 Promise를 풀어야한다.

```typescript
const result = repository.find({...});
console.log(await result.user);
```

필드를 find할 때 즉시 가져오고 싶다면 fetch type을 Eager를 주면 된다.