---
title: "HTTP"
date: 2026-10-03
author: "Marc Sagrera"
---

**HTTP** és el protocol de la web (port **80**; HTTPS usa el **443**).

## Instal·lar Nginx

```bash
sudo apt install nginx
sudo systemctl status nginx
curl -I http://localhost
```

## Codis de resposta

| Codi | Significat |
|---|---|
| 200 | OK |
| 301 | Redirecció permanent |
| 403 | Accés prohibit |
| 404 | No trobat |
| 500 | Error del servidor |

Els fitxers de la web es troben a `/var/www/html`.
