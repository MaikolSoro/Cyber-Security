----
- Tags: #web #wordpress #reconocimiento #herramientas
---
>Con ** Wpscan ** [^1], podemos realizar una enumeración completa del sitio web y obtener información detallada sobre la instalación de WordPress, como la versión utilizada, los plugins y temas instalados y los usuarios registrados en el sitio. También nos permite realizar pruebas de fuerza bruta para descubrir contraseñas débiles y vulnerabilidades conocidas en plugins y temas.

>Wpscan es una herramienta muy útil para los administradores de sitios web que desean mejorar la seguridad de su sitio WordPress, ya que permite identificar y corregir vulnerabilidades antes de que sean explotadas por atacantes malintencionados. Además, es una herramienta fácil de usar y muy efectiva para identificar posibles debilidades de seguridad en nuestro sitio web.

El uso de esta herramienta es bastante sencillo, a continuación se indica la sintaxis básica :

``` bash
wpscan --url https://example.com
```

Si deseas enumerar usuarios o plugins vulnerables en WordPress utilizando la herramienta wpscan, puedes añadir los siguientes parámetros a la línea de comandos:

```bash
wpscan --url https://example.com --enumerate u
```

En caso de querer enumerar plugins existentes los cuales sean vulnerables, puedes añadir el siguiente parámetro a la línea de comandos:
```bash
wpscan --url https://example.com --enumerate vp
```

Otra de las utilidades de esta herramienta es que es capaz de aplicar fuerza bruta para descubrir credenciales válidas en los paneles de autheticación:
```bash
wpscan --url https://example.com -U lotus -P /usr/share/wordlists/rockyou.txt
```

Cabe destacar que este procedimiento, también puede aplicarse de forma manual [^2], abusando del archivo **xmlrpc.php** siendo necesario crear para ello un script por ejemplo en Bash o Python.

-------
## Referencias

[^1]: Enlace al proyecto en Github: [Enlace](https://github.com/wpscanteam/wpscan)
[^2]: Procedimiento Manual abusando del XMLRPC: [[XMLRPC]]
