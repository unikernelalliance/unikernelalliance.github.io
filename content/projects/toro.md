---
title: "Toro Kernel"
description: ""
summary: ""
date: 2023-11-10T16:04:48+02:00
lastmod: 2023-11-10T16:04:48+02:00
draft: false
menu:
  docs:
    parent: ""
    identifier: "toro-6a1a6be4373e933280d78ea53de6158e"
weight: 810
toc: true
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---

Toro is a simple kernel that provides a dedicated API to develop microservices.
We propose two kinds of sockets to build microservices: blocking and non-blocking.
Blocking sockets are good for intensive-IO microservices whereas non-blocking sockets are good for microservices that can serve a request without blocking.
When a microservice executes in Toro, it runs alone in the system thus leveraging on the VM's resources.

Toro is a set of libraries that compile within the user application, i.e., the microservice.
The user can choose which components are included, .e.g, drivers, filesystems, networking, etc.
This results in a binary that can run on top of modern hypervisors like KVM, Xen or VirtualBox.
Once the kernel has been initialized, the microservice starts to execute. The microservice runs free from interference from other applications and without the need of users, password or remote login.

- Website: [https://torokernel.io/](https://torokernel.io/)
- Code: [https://github.com/torokernel](https://github.com/torokernel)
- Contact: [https://groups.google.com/g/torokernel](https://groups.google.com/g/torokernel)
