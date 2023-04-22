----
- Tags: #web #reconocimiento #herramientas #joomla
---

# Definición
---
>**Joomscan**[^1] es una herramienta de línea de comandos diseñada específicamente para escanear sitios web que utilizan Joomla y buscar posibles vulnerabilidades y debilidades de seguridad.

> **Joomscan**[^1] utiliza una variedad de técnicas de enumeración para identificar información sobre el sitio web de Joomla, como la versión de Joomla utilizada, los plugins y módulos instalados y los usuarios registrados en el sitio. También utiliza una base de datos de vulnerabilidades conocidas para buscar posibles vulnerabilidades en la instalación de Joomla.

---


Podemos utilizar la siguiente sintaxis básica para escanear un sitio web de Joomla:
```bash
 perl joomscan.pl -u <URL>
```

Donde **URL**,  es la URL del sitio web que deseamos escanear. **Joomscan** escaneará el sitio web y nos proporcionará una lista detallada de posibles vulnerabilidades y debilidades de seguridad.
Es importante tener en cuenta que **joomscan** no es una herramienta infalible y puede generar falsos positivos o falsos negativos. Por lo tanto, es importante utilizar joomscan junto con otras herramientas y técnicas de seguridad para tener una imagen completa de la seguridad del sitio web de [[Joomla]] que estemos auditando.

---

Para utilizar Joomscan, primero debemos descargar la herramienta desde su sitio web oficial. A continuación se le proporciona el enlace al proyecto:
## Referencia
[^1]: Enlace al proyecto en Github: [Enlace](https://github.com/OWASP/joomscan)