---
title: Spring Boot
description: This is a note for  Spring Boot
slug: spring-boot
date: 2020-01-01
categories:
  - Development
tags:
  - Spring Boot
---

# Issues

---

org.springframework.dao.InvalidDataAccessApiUsageException: No EntityManager with actual transaction available for current thread - cannot reliably process 'remove' call; nested exception is javax.persistence.TransactionRequiredException: No EntityManager with actual transaction available for current thread - cannot reliably process 'remove' call

**_Solution:_**

- Add @Transactional to deleteByXXXIn()

- OnDelete(action = OnDeleteAction.CASCADE)
  Put on child property to enable removing parent cascade to current

- Delete clause should be after find clause to make entity managed by transaction.

---

org.springframework.dao.InvalidDataAccessApiUsageException: org.hibernate.loader.MultipleBagFetchException: cannot simultaneously fetch multiple bags: [model.project.FProjectRequest.languageInfoList, model.project.FProjectRequest.certificateInfoList]; nested exception is java.lang.IllegalArgumentException: org.hibernate.loader.MultipleBagFetchException: cannot simultaneously fetch multiple bags: [model.project.FProjectRequest.languageInfoList, model.project.FProjectRequest.certificateInfoList]

**_Solution:_**
Use @OrderColumn on List properties
