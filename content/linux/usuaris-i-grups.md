---
title: "Usuaris i grups"
date: 2026-10-01
author: "Marc Sagrera"
---

A Linux cada usuari té un **UID** i pertany a un o més **grups** (GID). La informació es guarda en fitxers de text.

## Fitxers importants

| Fitxer | Contingut |
|---|---|
| `/etc/passwd` | Llista d'usuaris |
| `/etc/shadow` | Contrasenyes xifrades |
| `/etc/group` | Llista de grups |

## Comandes habituals

```bash
sudo useradd -m -s /bin/bash anna     # crear usuari amb home
sudo passwd anna                      # assignar contrasenya
sudo groupadd informatica             # crear grup
sudo usermod -aG informatica anna     # afegir usuari al grup
id anna                               # veure UID i grups
```

> *Important:* sense l'opció `-a`, `usermod -G` **substitueix** els grups de l'usuari.

Més informació: [manual de useradd](https://man7.org/linux/man-pages/man8/useradd.8.html).
