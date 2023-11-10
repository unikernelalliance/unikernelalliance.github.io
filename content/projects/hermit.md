---
title: "Hermit"
description: ""
summary: ""
date: 2023-11-10T16:04:48+02:00
lastmod: 2023-11-10T16:04:48+02:00
draft: false
menu:
  docs:
    parent: ""
    identifier: "hermit-6a1a6be4373e933280d78ea53de6158e"
weight: 810
toc: true
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---

Hermit is Rust-based, lightweight unikernel.
It targets a scalable and predictable runtime for high-performance and cloud computing.

The ownership model of Rust guarantees memory/thread-safety and enables us to eliminate many classes of bugs at compile-time.
Consequently, the use of Rust for kernel development promises fewer vulnerabilities in comparison to common programming languages.

The kernel is able to run Rust applications, as well as C/C++/Go/Fortran applications.

- Website: [http://hermit-os.org/](http://hermit-os.org/)
- Code: [https://github.com/hermit-os](https://github.com/hermit-os)
- Contact: [https://hermit.zulipchat.com/](https://hermit.zulipchat.com/)
