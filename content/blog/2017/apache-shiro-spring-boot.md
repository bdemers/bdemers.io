---
title: 'Protecting a Spring Boot App with Apache Shiro'
type: post
date: 2017-07-13
author: bdemers
layout: remotepost
remote_url: https://developer.okta.com/blog/2017/07/13/apache-shiro-spring-boot
featuredabsurl: https://raw.githubusercontent.com/oktadeveloper/okta-blog/master/_source/_assets/img/blog/featured/okta-java-bottle-headphones.jpg
categories:
- Java
- Authentication
- Apache Shiro
---

My favorite thing about Apache Shiro is how easy it makes handling authorization. You can use a role-based access control (RBAC) model of assigning roles to users and then permissions to roles. This makes dealing with the inevitable requirements change simple. Your code does not change, just the permissions associated with the roles. In this post I want to demonstrate just how simple it is, using a Spring Boot application and walking through how I'd handle the following scenario: