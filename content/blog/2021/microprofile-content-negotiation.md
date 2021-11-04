---
title: "Developers Guide to GPG and YubiKey"
date: 2021-08-04
description: "Tutorial: API clients have different capabilities and needs! Learn how to make your server select the correct languages, media types, and compression!"
type: post
author: bdemers
reading_time: "111"
layout: remotepost
remote_url: https://developer.okta.com/blog/2021/08/04/microprofile-content-negotiation
featuredabsurl: https://developer.okta.com/assets-jekyll/blog/microprofile-content-negotiation/social-5fe6b3d9441cde6dd3e967e7d21d3a2bc37e6d9f8ed19c3a412c77e944ac05fa.png
categories:
- content-negotiation
- microservices
- java
- quarkus
- jaxrs
---

Content negotiation allows for an HTTP server to respond to different types of clients. Many modern clients expect a JSON response, but there may be a need to format responses differently, maybe XML for older clients or a binary format for newer ones. Content negotiation is the mechanism used to solve that problem and others, such as dealing with multiple languages and even compressing HTTP requests.

In this post, I'll walk through building a simple Java MicroProfile application and explain how content negotiation works.
