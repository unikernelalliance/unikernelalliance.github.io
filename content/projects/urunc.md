---
title: "urunc"
description: ""
summary: ""
date: 2023-11-10T16:04:48+02:00
lastmod: 2023-11-10T16:04:48+02:00
draft: false
menu:
  docs:
    parent: ""
    identifier: "urunc-6a1a6be4373e933280d78ea53de6158e"
weight: 810
toc: true
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---

To bridge the gap between unikernels and traditional containerized environments, enabling seamless integration with cloud-native architectures, we introduce `urunc`.
Designed to fully leverage the container semantics and benefit from the OCI tools and methodology, `urunc` aims to become "runc for unikernels", while offering compatibility with the Container Runtime Interface (CRI).
By relying on underlying hypervisors, urunc launches unikernels provided by OCI-compatible images, allowing developers and administrators to package, deliver, deploy, and manage unikernels using familiar cloud-native practices.

- Code: [https://github.com/nubificus/urunc](https://github.com/nubificus/urunc)
- Contact: [gntouts](mailto:gntouts@nubificus.co.uk), [cmainas](mailto:cmainas@nubificus.co.uk), [ananos](mailto:ananos@nubificus.co.uk)
