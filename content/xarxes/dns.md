---
title: "DNS"
date: 2026-10-02
author: "Marc Sagrera"
---

El **DNS** tradueix noms de domini (`exemple.com`) en adreces IP.

## Registres habituals

| Registre | Funció |
|---|---|
| A | Nom → IPv4 |
| AAAA | Nom → IPv6 |
| CNAME | Àlies d'un altre nom |
| MX | Servidor de correu |
| NS | Servidors de noms |

## Consultes

```bash
dig exemple.com A
dig exemple.com MX +short
nslookup exemple.com
cat /etc/resolv.conf     # servidors DNS configurats
```

Documentació oficial: [ISC BIND](https://www.isc.org/bind/).
