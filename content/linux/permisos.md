---
title: "Permisos"
date: 2026-10-01
author: "Marc Sagrera"
---

Cada fitxer té permisos per al **propietari**, el **grup** i **altres**: lectura (`r`), escriptura (`w`) i execució (`x`).

```text
-rwxr-xr--  1 anna informatica 120 oct 1 10:00 script.sh
```

## Valors numèrics

| Permís | Valor |
|---|---|
| `r` | 4 |
| `w` | 2 |
| `x` | 1 |

Per exemple, `755` vol dir `rwxr-xr-x`.

## Comandes

```bash
chmod 755 script.sh          # canviar permisos
chmod u+x script.sh          # afegir execució al propietari
chown anna:informatica f.txt # canviar propietari i grup
ls -l                        # veure permisos
```

- Evita `chmod 777`: dóna accés total a tothom.
- Aplica el **principi de mínim privilegi**.
