---
title: "JWT vs Opaque Access Tokens: Use Both With Spring Boot"
date: 2020-08-07
description: "Tutorial: Learn how to use JWT and opaque access with Spring Boot."
type: post
author: bdemers
reading_time: "111"
layout: remotepost
remote_url: https://developer.okta.com/blog/2020/08/07/spring-boot-remote-vs-local-tokens
featuredabsurl: https://developer.okta.com/assets-jekyll/blog/spring-boot-remote-vs-local-tokens/spring-jwt-and-opaque-8832789d48707952cca320bdbd18cb188eef66c6b3cc63aa9e53af47564ecea1.png
categories:
- java
- spring
- spring-boot
- security
- oauth
- jwt
---

The topic of validating an OAuth 2.0 access tokens comes up frequently on this blog. Often we talk about how to validate JSON Web Token (JWT) based access tokens; however, this is NOT part of the OAuth 2.0 specification. JWTs are so commonly used that Spring Security supported them before adding support for remotely validating tokens (which is part of the OAuth 2.0 specification.)

In this post, you will build a simple application that takes advantage of both types of validation.

