---
title: "Nexus Tips: Disable Redeployment in Nexus"
type: post
date: 2011-11-02
author: bdemers
layout: remotepost
remote_url: https://blog.sonatype.com/2009/11/nexus-tips-disable-redeployment-in-nexus/
categories:
- nexus
- tutorial
---

It's a fundamental tenet of Maven that release artifacts never change once they are released. This is enforced in Maven by the fact that once a release artifact or POM is located in the local repository, Maven will never check for an updated artifact in a remote repository. Once an artifact is released, it is considered a static, unchanging artifact. If you release an artifact and then subsequently change it (intentionally or otherwise), you're in for some fun as people will have different versions based on when they first retrieved it... that's a situation not exactly conducive to a repeatable, standard build. This blog post discusses a feature in Nexus 1.4 which can enforce this rule and help you avoid problems caused by the redeployment of release artifacts.