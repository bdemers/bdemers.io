---
title: 'Make Java Tests Groovy With Hamcrest'
description: 'A tutorial on testing Java code with Groovy.'
type: post
date: 2019-08-21
author: bdemers
layout: remotepost
remote_url: https://developer.okta.com/blog/2019/08/21/make-java-tests-groovy
featuredabsurl: https://raw.githubusercontent.com/oktadeveloper/okta-blog/master/_source/_assets/img/blog/featured/okta-java-short-skew.jpg
categories:
- Java
- Spring Boot
- Testing
- Hamcrest
- Groovy
---

My favorite way to test Java code is with Groovy.  Specifically, writing tests in Groovy with Hamcrest.  In this post, I'll walk through how to test a simple Spring Boot application with these tools.

Groovy is an optionally typed dynamic language for the JVM, and can be compiled statically.  That is a mouthful and I'll explain this as we go, but for now think of Groovy as Java with lots of sugar.
