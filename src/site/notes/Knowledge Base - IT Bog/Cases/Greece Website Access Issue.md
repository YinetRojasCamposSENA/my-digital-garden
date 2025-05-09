---
{"dg-publish":true,"permalink":"/knowledge-base-it-bog/cases/greece-website-access-issue/","tags":["gardenEntry"]}
---


## 📌 Descripción del Problema  

- Usuaria en **Colombia** no puede acceder a un sitio web alojado en **Grecia**.  
- Síntomas: Timeout, error "Acceso denegado".  

## 🔍 Pasos para Diagnosticar  

1. Verificar si el sitio estaba caído globalmente:  
	- Herramienta: [DownForEveryoneOrJustMe](https://downforeveryoneorjustme.com)
2. Test de conectividad desde Colombia:  
   - `ping dominio.com` → ¿Timeouts?  
   - `tracert dominio.com` → ¿Bloqueos en saltos intermedios?  
3. Revisar configuración regional:  
   - ¿El sitio restringe acceso por geolocalización? (usar VPN para probar desde Grecia).  

## 🛠️ Solución Aplicada  
- Causa raíz: **Bloqueo por IP regional** (el sitio solo permitía conexiones desde Grecia).  
- Solución:  
  - Configurar excepción en el firewall del sitio **o**  
  - Usar VPN con IP griega (recomendado: [[Urban VPN: https://www.urban-vpn.com/es/\|Urban VPN: https://www.urban-vpn.com/es/]]).  

## 💡 Lecciones Aprendidas  
- Siempre verificar **restricciones geográficas** en sitios internacionales.  
- Herramientas clave: `ping`, `tracert`, VPN.  