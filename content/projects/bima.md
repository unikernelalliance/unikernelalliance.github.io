---
title: "bima"
description: ""
summary: ""
date: 2023-11-10T16:04:48+02:00
lastmod: 2023-11-10T16:04:48+02:00
draft: false
menu:
  docs:
    parent: ""
    identifier: "bima-6a1a6be4373e933280d78ea53de6158e"
weight: 810
toc: true
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---

How can we package unikernels in the OCI image format? 

To address this challenge, we created `bima`, a tool specifically designed for this purpose. `bima` follows a simplistic approach by creating a pseudo rootfs and storing the unikernel blob in a designated location, along with any additional files required for running the unikernel (such as a configuration file). Custom OCI annotations, intentionally extensible, are utilized by `bima` to furnish the runtime with crucial information on how to execute the unikernel. This information includes the storage location of the unikernel within the rootfs, the desired hypervisor type, the necessary command line parameters, and the location of any extra required files.



- Code: [https://github.com/nubificus/bima](https://github.com/nubificus/bima)
- Contact: [gntouts](mailto:gntouts@nubificus.co.uk), [cmainas](mailto:cmainas@nubificus.co.uk), [ananos](mailto:ananos@nubificus.co.uk)

