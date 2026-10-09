---
title: "Securitzar SSH amb claus"
date: 2026-10-06
author: "Marc Sagrera"
tags: ["ssh", "seguretat"]
---

Les contrasenyes es poden endevinar. Les **claus SSH** són una alternativa molt més segura.

![Esquema d'autenticació amb claus SSH](ssh.svg)

## Passos

1. Generar el parell de claus al client.
2. Copiar la clau pública al servidor.
3. Desactivar l'accés per contrasenya.

```bash
ssh-keygen -t ed25519 -C "marc@novasys"
ssh-copy-id usuari@192.168.1.10
```

Després, a `/etc/ssh/sshd_config`, posa `PasswordAuthentication no` i reinicia el servei.

*Conclusió:* amb claus, un atacant necessita la clau privada, no només una contrasenya.
