----
- Tags: #docker #dockerFile #scripting #herramientas 
---

# Definicion
---
>Un archivo **Dockerfile** se compone de varias secciones, cada una de las cuales comienza con una palabra clave en mayúsculas, seguida de uno o más argumentos.

Algunas de las secciones más comunes en un archivo **Dockerfile** son:

**FROM**: Se utiliza para especificar la imagen base desde la cual se construirá la nueva imagen.
**RUN**: Se utiliza para ejecutar comandos en el interior del contenedor, como la instalación de paquetes o la configuración del entorno.
**COPY**: Se utiliza para copiar archivos desde el sistema host al interior del contenedor.
**CMD**: Se utiliza para especificar el comando que se ejecutará cuando se arranque el contenedor.

Además de estas secciones, también se pueden incluir otras instrucciones para configurar el entorno, instalar paquetes adicionales, exponer puertos de red y más.

----

Para crear una imagen de [[Docker]], es necesario tener un archivo Dockerfile que defina la configuración de la imagen. Una vez que se tiene el Dockerfile, se puede utilizar el comando **“docker build”** para construir la imagen. Este comando buscará el archivo **‘Dockerfile’** en el directorio actual y utilizará las instrucciones definidas en el mismo para construir la imagen.

Algunas de las instrucciones:

**docker build**: Es el comando que se utiliza para construir una imagen de Docker a partir de un [[Dockerfile]].

La sintaxis básica es la siguiente:

```bash
docker build [opciones] ruta_al_Dockerfile
```

El parámetro **“-t”** se utiliza para etiquetar la imagen con un nombre y una etiqueta. Por ejemplo, si se desea etiquetar la imagen con el nombre **“mi_imagen” y la etiqueta** **“v1“**, se puede usar la siguiente sintaxis:
```bash
docker build -t mi_imagen:v1 ruta_al_Dockerfile
```

El punto (“.“) al final de la ruta al **Dockerfile** se utiliza para indicar al comando que busque el Dockerfile en el directorio actual. Si el Dockerfile no se encuentra en el directorio actual, se puede especificar la ruta completa al Dockerfile en su lugar. Por ejemplo, si el Dockerfile se encuentra en **“/home/usuario/proyecto/“,** se puede usar la siguiente sintaxis:
```bash
docker build -t mi_imagen:v1 /home/usuario/proyecto/
```

**docker pull**: es el comando que se utiliza para descargar una imagen de Docker desde un registro de imágenes.
La sintaxis básica es la siguiente:
```bash
docker pull nombre_de_la_imagen:etiqueta
```

Por ejemplo, si se desea descargar la imagen **“ubuntu”** con la etiqueta **“latest”,** se puede usar la siguiente sintaxis:
```bash
 docker pull ubuntu:latest
```

**docker images**: es el comando que se utiliza para listar las imágenes de Docker que están disponibles en el sistema.
La sintaxis básica es la siguiente:
```bash
docker images [opciones]
```

Durante la construcción de la imagen, [[Docker]] descargará y almacenará en caché las capas de la imagen que se han construido previamente, lo que hace que las compilaciones posteriores sean más rápidas.

----

El comando **“docker run”** se utiliza para crear y arrancar un contenedor a partir de una imagen. 
Algunas de las opciones más comunes para el comando **“docker run”** son:

**“-d” o “–detach“**: Se utiliza para arrancar el contenedor en segundo plano, en lugar de en primer plano.
**“-i” o “–interactive“**: Se utiliza para permitir la entrada interactiva al contenedor.
**“-t” o “–tty“**: Se utiliza para asignar un seudoterminal al contenedor.
**“–name“**: Se utiliza para asignar un nombre al contenedor.

Para arrancar un contenedor a partir de una imagen, se utiliza el siguiente comando:

```bash
docker run [opciones] nombre_de_la_imagen
```

Por ejemplo, si se desea arrancar un contenedor a partir de la imagen  **“mi_imagen“,** en segundo plano y con un seudoterminal asignado, se puede utilizar la siguiente sintaxis:
```bash
 docker run -dit mi_imagen
```

Una vez que el contenedor está en ejecución, se puede utilizar el comando “docker ps” para listar los contenedores que están en ejecución en el sistema. Algunas de las opciones más comunes son:

**“-a” o “–all“** : se utiliza para listar todos los contenedores, incluyendo los contenedores detenidos.
**“-q” o “–quiet“**: se utiliza para mostrar sólo los identificadores numéricos de los contenedores.

Por ejemplo, si se desea listar todos los contenedores que están en ejecución en el sistema, se puede utilizar la siguiente sintaxis:

```bash
docker ps -a
```

Para ejecutar comandos en un contenedor que ya está en ejecución, se utiliza el comando “docker exec” con diferentes opciones. Algunas de las opciones más comunes son:

**“-i” o “–interactive“**: se utiliza para permitir la entrada interactiva al contenedor.
**“-t” o “–tty“**: se utiliza para asignar un seudoterminal al contenedor.
Por ejemplo, si se desea ejecutar el comando “bash” en el contenedor con el identificador “123456789“, se puede utilizar la siguiente sintaxis:

```bash
docker exec -it 123456789 bash
```