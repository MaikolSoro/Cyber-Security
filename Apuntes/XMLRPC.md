----
-  Tags: #web #scripting #bash #herramientas #wordpress 
----
>Este archivo es una característica de [[WordPress]] que permite la comunicación entre el sitio web y aplicaciones externas utilizando el protocolo XML-RPC.
  El archivo **xmlrpc.php** es utilizado por muchos plugins y aplicaciones móviles de WordPress para interactuar con el sitio web y realizar diversas tareas, como publicar contenido, actualizar el sitio y obtener información.

>Sin embargo, este archivo también puede ser abusado por atacantes malintencionados para aplicar fuerza bruta y descubrir credenciales válidas de los usuarios del sitio. Esto se debe a que **xmlrpc.php** permite a los atacantes realizar un número ilimitado de solicitudes de inicio de sesión sin ser bloqueados, lo que hace que la ejecución de un ataque de fuerza bruta sea relativamente sencilla.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<methodCall> 
<methodName>wp.getUsersBlogs</methodName> 
<params> 
<param><value>\{\{your username\}\}</value></param> 
<param><value>\{\{your password\}\}</value></param> 
</params> 
</methodCall>
```
