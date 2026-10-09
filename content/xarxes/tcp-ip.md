---
title: "TCP/IP"
date: 2026-10-02
author: "Marc Sagrera"
---

El model **TCP/IP** organitza la comunicació en capes.

| Capa | Exemples |
|---|---|
| Aplicació | HTTP, DNS, SSH |
| Transport | TCP, UDP |
| Internet | IP, ICMP |
| Accés a xarxa | Ethernet, Wi-Fi |

## Diagnòstic bàsic

```bash
ip a                  # adreces IP de la màquina
ip route              # taula d'encaminament
ping -c 4 8.8.8.8     # comprovar connectivitat
ss -tuln              # ports en escolta
```

**TCP** és *fiable* i orientat a connexió; **UDP** és més ràpid però no garanteix l'entrega.
