---
{"dg-publish":true,"permalink":"/knowledge-base-it-bog/commands/power-shell-commands-list/"}
---

## Limpiar imagen

```powershell

dism /online /cleanup-image /restorehealth

```

## Limpiar archivos corruptos

```powershell

sfc /scannow
```

## Actualizar apps

```powershell

winget upgrade --all
```

