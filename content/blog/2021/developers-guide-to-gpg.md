---
title: "Developers Guide to GPG and YubiKey"
date: 2021-07-07
description: "Tutorial: Set up a YubiKey for GPG and SSH!"
type: post
author: bdemers
reading_time: "111"
layout: remotepost
remote_url: https://developer.okta.com/blog/2021/07/07/developers-guide-to-gpg
featuredabsurl: https://developer.okta.com/assets-jekyll/blog/developers-guide-to-gpg/developers-guide-to-gpg-540fbc298126b5cfcc660b5095f6f8aef591798787f408e51c3b3eeaf15bbb2c.png
categories:
- yubikey
- user-authentication
- github
- gpg
---

Setting up a new YubiKey as a second factor is easy—your browser walks you through the entire process. However, setting up a YubiKey to sign your Git commits and Secure Shell (SSH) authentication is a very different experience. In this post, I'll walk through configuring a YubiKey and highlight some of the things I've learned along the way.

