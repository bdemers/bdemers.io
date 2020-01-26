---
title: 'Secure Server-to-Server Communication with Spring Boot and OAuth 2.0'
type: post
date: 2018-04-02
author: bdemers
layout: remotepost
remote_url: https://developer.okta.com/blog/2018/04/02/client-creds-with-spring-boot
featuredabsurl: https://raw.githubusercontent.com/oktadeveloper/okta-blog/master/_source/_assets/img/blog/featured/okta-java-bottle-headphones.jpg
categories:
- OAuth 2.0
- Java
- Spring Boot
- Spring Security
- Client Credentials
---

Most OAuth 2.0 guides are focused around the context of a user, i.e., login to an application using Google, Github, Okta, etc., then do something on behalf of that user. While useful, these guides ignore server-to-server communication where there is no user and you only have one service connecting to another one.