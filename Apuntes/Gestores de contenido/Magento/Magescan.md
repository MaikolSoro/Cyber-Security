----
- Tags: #web #reconocimiento #magento #herramientas 
----

# Definición
----
> **Magescan** [^1], puede detectar vulnerabilidades comunes en [[Magento]], incluyendo problemas con permisos de archivos, errores de configuración y vulnerabilidades conocidas en extensiones populares de Magento.

---
Su sintaxis y modo de uso es bastante sencillo, a continuación se comparte un ejemplo:
```bash
php magescan.phar scan:all https://example.com
```

Donde **“magescan.phar”** es el archivo ejecutable de la herramienta **“Magescan“,**  **“scan:all”** es el comando específico de Magescan que indica que se realizará un escaneo exhaustivo de todas las vulnerabilidades conocidas en el sitio web objetivo y **“https://example.com”** es la URL del sitio web objetivo que se escaneará en busca de vulnerabilidades.

## Referencia
---
 [^1]: Enlace al proyecto en Github: [Enlace](https://github.com/steverobbins/magescan)