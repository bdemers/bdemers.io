---
title: "SBOMs Are Not Enough"
date: 2025-05-13
description: "Software Bill of Materials (SBOMs) have emerged as a critical component of software supply chain security, promising transparency about the dependencies in our applications. But are they delivering on that promise?"
type: presentation
author: bdemers
layout: single
event_name: JCON
event_link: https://jcon.one/
featured: social.jpeg
featuredpath: /img/2025/sboms-are-not-enough-jcon
notist: bdemers/9jfpju
links:
- name: SBOM / Software supply chain
  url: https://en.wikipedia.org/wiki/Software_supply_chain
- name: World's greatest pancake recipe (use real maple syrup)
  url: https://www.google.com/search?q=world%27s+greatest+pancake+recipe
- name: CycloneDX
  url: https://cyclonedx.org/
- name: SPDX
  url: https://spdx.dev/
- name: xkcd - standards
  url: https://xkcd.com/927/
- name: syft
  url: https://github.com/anchore/syft
- name: SLSA
  url: https://slsa.dev/
- name: paketo - build packs - SBOM
  url: https://paketo.io/docs/concepts/sbom/
- name: XZ Utils Backdoor
  url: https://www.wired.com/story/xz-backdoor-everything-you-need-to-know/
- name: SpotBugs token leak
  url: https://www.securityweek.com/compromised-spotbugs-token-led-to-github-actions-supply-chain-hack/
- name: in-toto (attestations)
  url: https://in-toto.io/
- name: JReleaser attestations example
  url: https://github.com/jreleaser/jreleaser/attestations
- name: Dice Parser (Java & Kotlin)
  url: https://github.com/diceroll-dev
- name: Free Build Scan Service
  url: https://scans.gradle.com
- name: The Developer Productivity Engineering (DPE) Handbook
  url: https://gradle.com/developer-productivity-engineering/handbook/
- name: Gradle is Hiring
  url: https://gradle.com/careers/
categories:
- maven
- security
- development
- builds
- sbom
---

Software Bill of Materials (SBOMs) have emerged as a critical component of software supply chain security, promising transparency about the dependencies in our applications. But are they delivering on that promise? While SBOMs provide a snapshot of the components included in software, they often fail to address a vital piece of the puzzle: the tools, libraries, and configurations actually used to build it.

In this talk, we’ll explore the varying degrees of SBOM quality and expose the gaps that can undermine their utility. By understanding what SBOMs are—and what they aren’t—we’ll uncover the risks of relying on incomplete or inaccurate data and discuss complementary strategies for achieving a truly transparent and secure build process. Attendees will leave with a deeper appreciation of how SBOMs fit into the broader supply chain security landscape and actionable insights for bridging the gaps.

Who should attend: Developers, security professionals, and DevOps practitioners looking to enhance software supply chain security beyond the baseline provided by SBOMs.