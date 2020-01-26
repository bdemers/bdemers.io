---
title: "Watch GraalVM Turn Your Java Into Binaries"
description: "Tutorial: Learn how to build native binaries from a Java application with GraalVM's native-image tool."
type: post
date: 2019-11-27
author: bdemers
layout: remotepost
remote_url: https://developer.okta.com/blog/2019/11/27/graalvm-java-binaries
featuredabsurl: https://raw.githubusercontent.com/oktadeveloper/okta-blog/master/_source/_assets/img/blog/graalvm-java-binaries/native-image-header.png
categories:
- Java
- CI
- Builds
- Security
---

There has been much buzz about GraalVM and what it means for the Java world. GraalVM is a Java distribution from Oracle that adds a bunch of features, most notably a new JIT compiler, polyglot capabilities, an LLVM runtime... and the ability to turn your Java application into a native binary.

This last one offers the potential to distribute Java applications as a single binary, and a few frameworks like Quarkus, Helidon, and Micronaut already take advantage of this feature. Native images also open up the possibility to distribute Java applications as CLI applications, which has recently been the near-exclusive domain of Go and Node. This tutorial will show you how!
