---
title: "SSH"
date: 2026-10-03
author: "Marc Sagrera"
---

**SSH** permet accedir de manera segura a una màquina remota pel port **22**.

```bash
sudo apt install openssh-server
sudo systemctl enable --now ssh
ssh usuari@192.168.1.10
```

## Fitxer de configuració

`/etc/ssh/sshd_config`:

```text
PermitRootLogin no
PasswordAuthentication no
Port 22
```

Després de canviar-lo: `sudo systemctl restart ssh`.
