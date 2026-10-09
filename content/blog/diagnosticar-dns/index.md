---
title: "Diagnosticar problemes de DNS"
date: 2026-10-07
author: "Marc Sagrera"
tags: ["dns", "xarxes"]
---

Quan «no va internet», sovint el problema és el **DNS**. Aquest és un mètode ràpid per descobrir-ho.

![Resolució DNS d'un domini](dns.svg)

## Mètode

1. Comprova la connectivitat per IP: `ping 8.8.8.8`.
2. Comprova la resolució de noms: `ping exemple.com`.
3. Si el pas 1 va i el 2 no, el problema és el DNS.

```bash
dig exemple.com +short
dig @8.8.8.8 exemple.com +short   # provar un altre servidor DNS
```

Si amb `8.8.8.8` funciona, revisa els servidors a `/etc/resolv.conf`.
