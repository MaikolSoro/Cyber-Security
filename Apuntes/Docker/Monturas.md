----
- Tags: #docker #dockerFile #contenedor 
----

# Definición

---
> Las monturas, por otro lado, nos permiten compartir un directorio o archivo entre el sistema host y el contenedor. Esto nos permitirá persistir la información entre ejecuciones de contenedores y compartir datos entre diferentes contenedores.

Para utilizar las monturas, se utiliza la opción **“-v” o “–volume”** en el comando **“docker run“.** Esta opción se utiliza para especificar la montura y se puede utilizar de varias maneras.

Por ejemplo, si se desea montar el directorio **“/home/usuario/datos”** del host en el directorio **“/datos”** del contenedor, se puede utilizar la siguiente sintaxis:

```bash
 docker run -v /home/usuario/datos:/datos mi_imagen
```

Esto montará el directorio **“/home/usuario/datos”** del host en el directorio “/datos” del contenedor

----
Si se desea especificar una opción adicional, como la de montar el directorio en modo de solo lectura, se puede utilizar la opción **“-v”** con un formato diferente. Por ejemplo, si se desea montar el directorio en modo de solo lectura, se puede utilizar la siguiente sintaxis:

```bash
docker run -v /home/usuario/datos:/datos:ro mi_imagen
```
