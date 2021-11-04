---
title: "Session Clustering for OAuth 2.0 Applications"
date: 2021-07-07
description: "Learn how sessions are used with OAuth 2.0 and build an example with HAproxy, Redis, and Spring Boot."
type: post
author: bdemers
reading_time: "111"
layout: remotepost
remote_url: https://developer.okta.com/blog/2021/09/30/oauth-sessions-with-java
featuredabsurl: https://developer.okta.com/assets-jekyll/blog/oauth-sessions-with-java/social-c93a21db4c9c38a979bc210005d447e16bf8a90a503d79a0ad2e7806eeae4583.png
categories:
- spring-session
- spring
- microservices
- java
- spring-boot
- haproxy
- oauth2
- oidc
- session
---

A common OAuth 2.0 question we get: "How do I deal with OAuth in a load-balanced application?" The short answer: There's nothing specific about session clustering for OAuth. The longer answer is—you likely still need to worry about cluster session management. This post will discuss how an OAuth login relates to your application's session. And we'll build a simple, secure, load-balanced application to demonstrate.
