---
title: Protecting JAX-RS Resources with RBAC and Apache Shiro
type: post
date: 2017-01-18
author: bdemers
layout: remotepost
remote_url: https://stormpath.com/blog/protecting-jax-rs-resources-rbac-apache-shiro
featuredabsurl: http://stormpath.com/wp-content/uploads/2016/04/trooper-conga.jpg
categories:
- Java
- Apache Shiro
- Security
---

Security is probably the most important thing for your application, but it doesn’t have to be the hardest thing. Today I’ll show you how to use Shiro’s wildcard permissions to enable fine grained Role-Based Access Control (RBAC) which makes granting user permissions trivial (a single line). This will also make your application’s security policy more flexible, so when your business rules change (and you know they will) your code does not have to. You can read more about RBAC and Roles vs Permissions here.