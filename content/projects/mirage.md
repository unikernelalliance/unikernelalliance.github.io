---
title: "MirageOS"
description: ""
summary: ""
date: 2023-11-10T16:04:48+02:00
lastmod: 2023-11-10T16:04:48+02:00
draft: false
menu:
  docs:
    parent: ""
    identifier: "mirage-6a1a6be4373e933280d78ea53de6158e"
weight: 810
toc: true
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---

MirageOS is a library operating system that constructs unikernels for secure, high-performance network applications across a variety of cloud computing and mobile platforms.
Code can be developed on a normal OS such as Linux or macOS, and then compiled into a fully-standalone, specialised unikernel that runs under a Xen or KVM hypervisor.
This lets your services run more efficiently, securely and with finer control than with a full conventional software stack.

MirageOS applications take a few milliseconds to start-up instead of the few minutes that traditional OSes take.
Binaries are self-contained: they do not need an additional OS to execute.
Even then, the size of MirageOS binary is usually a few megabytes.

MirageOS applications are written in OCaml, an industrial strength programming language supporting functional, imperative and object-oriented styles.

- Website: [https://mirage.io/](https://mirage.io/)
- Code: [https://github.com/mirage](https://github.com/mirage)
- Contact: [https://lists.xenproject.org/cgi-bin/mailman/listinfo/mirageos-devel](https://lists.xenproject.org/cgi-bin/mailman/listinfo/mirageos-devel)
