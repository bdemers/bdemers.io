---
title: 'OpenID Connect Logout Options with Spring Boot'
description: 'This tutorial demonstrates the logout options you have when developing Spring applications and helps you pick the right one for you!'
type: post
date: 2020-03-27
author: bdemers
reading_time: 111
layout: remotepost
remote_url: https://developer.okta.com/blog/2020/03/27/spring-oidc-logout-options
featuredabsurl: https://developer.okta.com/assets-jekyll/blog/spring-oidc-logout-options/spring-boot-logout-options-e22539993afc9c640a1fe1b7b7fdc386751c2a539a281e4d56010736ef863346.png
categories:
- OAuth 2.0
- OIDC
- Java
- Spring Boot
- Tutorials
---

On the Okta blog, we spend much of our time talking about logging in. That is because once you configure your application to log in, the log out just works. But there are a few things you should consider when you’re thinking about your app’s logout configuration. In this post, I’ll walk through examples of the two logout options you have with Spring Security: the "default" session clearing logout, and relying party initiated logout.