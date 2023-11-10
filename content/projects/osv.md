---
title: "OSv"
description: ""
summary: ""
date: 2023-11-10T16:04:48+02:00
lastmod: 2023-11-10T16:04:48+02:00
draft: false
menu:
  docs:
    parent: ""
    identifier: "osv-6a1a6be4373e933280d78ea53de6158e"
weight: 810
toc: true
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---

OSv is an open-source unikernel designed to run a single unmodified Linux application securely as microVM on top of a hypervisor.
This is contrast to traditional operating systems which were designed for a vast range of physical machines.
OSv can execute precompiled Linux dynamically-linked binaries that use glibc, dynamically-linked binaries which use system calls directly instead of glibc (e.g., golang) as well as glibc functions, and finally statically linked and dynamically linked executables with full Linux glibc instead of built-in OSv’ glibc.
OSv guests can run on QEMU/KVM, Firecracker, Cloud Hypervisor, VMWare, VirtualBox, HyperKit and XEN (AWS Nitro support is coming soon).

- Website: [https://osv.io/](https://osv.io/)
- Code: [https://github.com/cloudius-systems/osv](https://github.com/cloudius-systems/osv)
- Contact: [https://groups.google.com/g/osv-dev](https://groups.google.com/g/osv-dev)
