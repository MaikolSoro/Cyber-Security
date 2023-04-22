----
- Tags: #docker #herramientas 
---

# Definición
---
> **El port forwarding**, también conocido como reenvío de puertos, nos permite redirigir el tráfico de red desde un puerto específico en el host a un puerto específico en el contenedor. Esto nos permitirá acceder a los servicios que se ejecutan dentro del contenedor desde el exterior.

Para utilizar el **port forwarding**, se utiliza la opción **“-p” o “–publish”** en el comando **“docker run“.** Esta opción se utiliza para especificar la redirección de puertos y se puede utilizar de varias maneras. Por ejemplo, si se desea redirigir el puerto 80 del host al puerto 8080 del contenedor, se puede utilizar la siguiente sintaxis:
```bash
docker run -p 80:8080 mi_imagen
```

Esto redirigirá cualquier tráfico entrante en el puerto 80 del host al **puerto 8080** del contenedor. Si se desea especificar un protocolo diferente al protocolo TCP predeterminado, se puede utilizar la opción **“-p”** con un formato diferente. Por ejemplo, si se desea redirigir el puerto 53 del host al puerto 53 del contenedor utilizando el protocolo UDP, se puede utilizar la siguiente sintaxis:

```bash
 docker run -p 53:53/udp mi_imagen
```
