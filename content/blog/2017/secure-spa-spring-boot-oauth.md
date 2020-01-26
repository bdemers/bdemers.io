---
title: 'Secure your SPA with Spring Boot and OAuth'
type: post
date: 2017-07-13
author: bdemers
layout: remotepost
remote_url: https://developer.okta.com/blog/2017/10/27/secure-spa-spring-boot-oauth
featuredabsurl:  https://raw.githubusercontent.com/oktadeveloper/okta-blog/master/_source/_assets/img/blog/featured/okta-java-bottle-headphones.jpg
categories:
- OAuth 2.0
- Java
- Spring Boot
- Spring Security
---

If you have a JavaScript single-page application (SPA) that needs to securely access resources from a Spring Boot application, you likely want to use the OAuth 2.0 implicit flow! With this flow your client will send a bearer token with each request and your server side application will verify the token with an Identity Provider (IdP). This allows your resource server to trust that your client is authorized to make the request. In OAuth terms your SPA is the client and your Spring Boot application is the Resource Server. For a more detailed explanation on the various OAuth flows take a look at our [What the Heck is OAuth](/blog/2017/06/21/what-the-heck-is-oauth) post.