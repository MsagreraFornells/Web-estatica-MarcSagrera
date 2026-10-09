---
title: "Auditoria de permisos a Linux"
date: 2026-10-08
author: "Marc Sagrera"
tags: ["linux", "seguretat"]
---

Una auditoria periòdica de permisos evita problemes de seguretat.

![Permisos rwx i el seu valor numèric](permisos.svg)

## Què buscar

- Fitxers amb permisos d'escriptura per a **tothom**.
- Fitxers amb el bit **SUID**.
- Fitxers sense propietari vàlid.

```bash
find / -type f -perm -0002 2>/dev/null     # escriptura per a tothom
find / -type f -perm -4000 2>/dev/null     # fitxers SUID
find / -nouser 2>/dev/null                 # sense propietari
```

Documenta cada excepció i corregeix amb `chmod` o `chown`.
