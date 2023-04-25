¿Cómo puede el atacante hacer que el sistema cargue la versión maliciosa de la biblioteca compartida?
- [ ] El sistema operativo busca la biblioteca compartida y carga la función requerida en memoria
- [ ] El programador incluye todas las funciones requeridas en el código del programa
- [ ] El programador enlaza estáticamente la función requerida antes de la ejecución del programa
- [x] El sistema operativo busca la biblioteca compartida y enlaza dinámicamente la función requerida en memoria

Note: (**Esto permite que el programa utilice la función requerida sin tener que tener todo el código de la biblioteca compartida incluido en el programa en sí.**)

¿Qué usuario adquiere los mismos privilegios que el propietario de un archivo binario con permiso SUID?

- [ ] El usuario root
- [ ] El usuario que creó el archivo
- [x] El usuario que ejecuta el archivo
- [ ] Ninguna de las anteriores

Note: (**Esto significa que el programa se ejecutará con los mismos permisos que el propietario del archivo, incluso si el usuario que lo ejecuta no tiene esos permisos normalmente.**)

¿Cómo puede el atacante hacer que el sistema cargue la versión maliciosa de la biblioteca compartida?

- [x] Colocando la biblioteca maliciosa en un directorio donde el sistema la buscará
- [ ] Cambiando el nombre de la biblioteca legítima en el código del programa víctima
- [ ] Modificando el código del programa víctima para buscar la biblioteca maliciosa
- [ ] Accediendo remotamente al sistema operativo para forzar la carga de la biblioteca maliciosa

Note: (**Si la biblioteca maliciosa se encuentra en una ruta que figura en 'LD_LIBRARY_PATH' o en una de las rutas estándar donde se buscan bibliotecas compartidas, entonces el sistema cargará la versión maliciosa de la biblioteca compartida cuando sea requerida por una aplicación.**)

¿Cómo se lleva a cabo un Python Library Hijacking?

- [ ] Reemplazando una librería utilizada por el script por una versión legítima en una ruta accesible después de que la librería maliciosa haya sido encontrada
- [x] Reemplazando una librería utilizada por el script por una versión maliciosa en una ruta accesible antes de que la librería legítima sea encontrada
- [ ] Creando una librería utilizada por el script en una ruta inaccesible
- [ ] Creando una librería utilizada por el script en una ruta accesible después de que la librería legítima haya sido encontrada

Note: (**El atacante secuestra una librería utilizada por un script de Python creando su propia librería con el mismo nombre en el directorio actual de trabajo o en alguna de las rutas que figuran en 'sys.path' antes de que se llegue a la librería legítima**)

¿Qué es un archivo crontab?
- [ ] Un archivo que se ejecuta automáticamente al inicio de un sistema Unix/Linux
- [x] Un archivo de configuración que especifica qué comandos deben ejecutarse y cuándo deben ejecutarse
- [ ] Un archivo de configuración que especifica qué comandos deben ejecutarse y cómo deben ejecutarse
- [ ] Un archivo que contiene instrucciones para la ejecución de tareas en segundo plano

Note: (**Cada usuario tiene su propio archivo crontab, que contiene una lista de tareas programadas y su frecuencia de ejecución. El archivo crontab se utiliza para automatizar tareas de mantenimiento, realizar copias de seguridad, generar informes periódicos, entre otras tareas.**)

¿Cuál es el puerto correspondiente al protocolo de gestión remota de Docker (Docker Remote API)?

- [ ] 2378
- [ ] 2379
- [ ] 2374
- [x] 2375

Note:(**Este puerto es utilizado por aplicaciones cliente para conectarse a un daemon de Docker y enviar comandos para crear, modificar o eliminar contenedores Docker, así como para gestionar imágenes de Docker y otras tareas relacionadas con Docker.**)

¿Qué es una tarea cron?
- [ ] Una tarea programada en sistemas Windows que se ejecuta en un momento determinado
- [x] Una tarea programada en sistemas Unix/Linux que se ejecuta en un momento determinado o en intervalos regulares de tiempo
- [ ] Una tarea programada que solo se ejecuta una vez en sistemas Unix/Linux
- [ ] Una tarea programada que solo se ejecuta una vez en sistemas Windows

Note:(**Estas tareas son programadas utilizando el programa 'cron', que es un demonio del sistema que se ejecuta en segundo plano y que está diseñado para ejecutar comandos de forma periódica.**)

¿Qué es PATH Hijacking?

- [ ] El proceso de explotar una vulnerabilidad en el sistema de archivos para obtener privilegios elevados
- [ ] El proceso de robar contraseñas almacenadas en el archivo /etc/shadow
- [x] El proceso de cambiar la variable PATH para secuestrar comandos y causar ejecuciones alternativas
- [ ] El proceso de secuestrar una conexión de red para redirigir el tráfico a un destino malicioso

Note:(**PATH hijacking es un tipo de ataque informático en el que se modifica la variable PATH del sistema para que un comando legítimo apunte a una ubicación malintencionada.**)

¿Qué comando se utiliza para buscar archivos SUID?
- [ ] locate
- [ ] grep
- [ ] chmod
- [x] find

Note:(**El comando find es una herramienta de línea de comandos en sistemas Unix y Linux que se utiliza para buscar archivos y directorios en un sistema de archivos.**)

¿Qué archivo en Linux contiene la lista de tareas programadas para el sistema?
- [x] /etc/cron.d
- [ ] /etc/cron.conf
- [ ] /etc/crontab.d
- [ ] /etc/cron.daily

Note:(**Este directorio contiene archivos que especifican las tareas programadas en el sistema y su frecuencia de ejecución, utilizando el formato de configuración cron.**)

¿Qué es el archivo /etc/sudoers y para qué se utiliza en sistemas Linux?

- [ ] Es un archivo de configuración que se utiliza para instalar nuevos paquetes en el sistema
- [x] Es un archivo de configuración que se utiliza para controlar el acceso de todos los usuarios a las diferentes acciones que pueden realizar en el sistema
- [ ] Es un archivo de configuración que se utiliza para conectar el sistema a una red
- [ ] Ninguna de las anteriores

Note:(**Este archivo contiene reglas que especifican qué usuarios pueden ejecutar comandos con privilegios elevados utilizando el comando sudo. Esto permite a los usuarios realizar tareas que normalmente requerirían permisos de superusuario sin tener que iniciar sesión como superusuario u otros usuarios.**)

¿Qué es el PATH en sistemas Unix/Linux?

- [x] Una variable de entorno que define las rutas de búsqueda para los archivos ejecutables en el sistema
- [ ] Un comando que muestra el contenido de un archivo en el sistema
- [ ] Una herramienta de línea de comandos para la manipulación de archivos en el sistema
- [ ] Una técnica utilizada por los atacantes para secuestrar comandos de un sistema Unix/Linux

 Note:(**Cuando se ejecuta un comando en una terminal de Unix o Linux, el sistema busca el archivo ejecutable correspondiente en las rutas especificadas en el PATH.**)

¿Por qué el atacante también puede crear su propia librería en el directorio actual de trabajo de cara a un Python Library Hijacking?
- [ ] Porque la librería legítima se encuentra en el directorio actual de trabajo
- [ ] Porque es más fácil modificar la librería legítima en este directorio
- [ ] Porque es menos probable que Python detecte la librería maliciosa en este directorio
- [x] Porque Python comienza la búsqueda en este directorio por defecto

 Note:(**Si el atacante coloca una versión maliciosa de la biblioteca en el directorio actual de trabajo, Python cargará esa versión antes de buscar en otras rutas.**)

¿Qué puede hacer un atacante si logra manipular el PATH y crear un nuevo archivo con el mismo nombre de uno de los comandos definidos internamente en un binario?
- [ ] Puede hacer que el binario ejecute el comando legítimo
- [ ] No puede hacer nada porque el sistema verificará la integridad del archivo
- [x] Puede hacer que el binario interprete la versión maliciosa del nuevo comando creado en lugar de la versión legítima
- [ ] Puede hacer que el binario ejecute ambos comandos al mismo tiempo


Note:(**Si un atacante logra manipular el PATH y crea un nuevo archivo con el mismo nombre de uno de los comandos definidos internamente en un binario, puede hacer que el binario ejecute la versión maliciosa del comando en lugar de la versión legítima.**)

¿Qué es Python Library Hijacking?

- [x] Una técnica de ataque que busca secuestrar librerías con el objetivo de inyectar código malicioso en un script de Python
- [ ] Una técnica de ataque que busca y modifica archivos en un script de Python
- [ ] Una técnica de ataque que busca y roba información de un script de Python
- [ ] Una técnica de ataque que busca y elimina archivos de un script de Python

Note:(**Python Library Hijacking es una técnica de ataque en la que un atacante reemplaza bibliotecas utilizadas por un script de Python con versiones maliciosas que contienen código malicioso.**)

¿Qué es un archivo SUID (Set User ID)?

- [x] Un archivo que se ejecuta con el permiso de su propietario en lugar del usuario que lo ejecuta
- [ ] Un archivo que se ejecuta solo en el directorio de inicio del usuario
- [ ] Un archivo que rastrea los ID de usuario en el sistema
- [ ] Un archivo que controla la conexión de red de los usuarios

Note:(**Un archivo SUID (Set User ID) es un tipo especial de archivo en sistemas Unix y Linux que permite que un programa se ejecute con los permisos del propietario del archivo en lugar de los permisos del usuario que lo ejecuta.**)

¿De qué forma un atacante se podría aprovechar de un contenedor desplegado con los parámetros ‘–pid=host’ y ‘–privileged’?

- [x] Dado que los procesos están compartidos, se podría inyectar un shellcode en un proceso privilegiado de la máquina host visible desde el contenedor para conseguir escapar de este y ejecutar comandos privilegiados
- [ ] Dado que los procesos no están compartidos, se podría inyectar un shellcode directamente en la máquina host, consiguiendo escapar del contenedor y ejecutando comandos de forma privilegiada
- [ ] Dado que los procesos están compartidos, se podría inyectar un comando directamente en un proceso privilegiado de la máquina host visible desde el contenedor para conseguir escapar de este
- [ ] No habría forma de aprovecharse de esto, dado que el parámetro '--privileged' limitaría la ejecución de ciertas instrucciones privilegiadas

Note:(**Esto crea un riesgo de seguridad ya que si un atacante obtiene acceso al contenedor, puede inyectar código malicioso en un proceso privilegiado del sistema host que es visible desde el contenedor.**)

¿Para qué sirve el comando “sudo -l” en sistemas Linux?

- [x] Listar los permisos de sudo de un usuario en particular
- [ ] Listar los usuarios que tienen acceso al sistema
- [ ] Listar los paquetes instalados en el sistema
- [ ] Listar los procesos en ejecución en el sistema

Note:(**Al ejecutar el comando 'sudo -l', el sistema verificará los permisos del usuario y mostrará una lista de comandos que el usuario puede ejecutar con 'sudo'.**)

¿Qué es una ruta relativa en sistemas Unix/Linux?

- [ ] Una ruta que especifica la ubicación exacta de un archivo ejecutable en el sistema
- [ ] Una ruta que especifica la ubicación aproximada de un archivo ejecutable en el sistema
- [ ] Una ruta que depende del tiempo en el que se está ejecutando el comando
- [x] Una ruta que depende de la posición actual del usuario en el sistema de archivos

Note:(**Las rutas relativas se especifican utilizando una ruta que comienza desde el directorio actual, en lugar de una ruta que comienza desde la raíz del sistema de archivos.**)

¿Cuál de los siguientes archivos configura quiénes tienen acceso a sudo?

- [ ] /etc/passwd
- [ ] /etc/shadow
- [x] /etc/sudoers
- [ ] /etc/groups

Note:(**Este archivo es utilizado por el sistema operativo Unix y Linux para definir las políticas de seguridad y permisos del programa sudo, que permite a los usuarios realizar tareas con privilegios de superusuario.**)

¿Qué son las bibliotecas compartidas?

- [ ] Archivos que contienen datos irrelevantes utilizados por múltiples programas
- [ ] Archivos que contienen información confidencial utilizada por múltiples programas
- [x] Archivos que contienen funciones y recursos utilizados por múltiples programas
- [ ] Archivos que contienen código malicioso utilizado por múltiples programas

Note:(**Las bibliotecas compartidas son cargadas en memoria cuando se ejecuta un programa que las utiliza, y varias aplicaciones pueden utilizar la misma biblioteca compartida al mismo tiempo, lo que ayuda a reducir la cantidad de memoria utilizada en el sistema.**)

¿Qué son las Capabilities en Linux?
- [ ] Un conjunto de permisos básicos que se pueden asignar a un proceso
- [ ] Un conjunto de permisos de usuario que se pueden asignar a un proceso
- [x] Un conjunto de permisos avanzados que se pueden asignar a un proceso
- [ ] Ninguna de las anteriores

Note:(**Con Capabilities, los procesos pueden tener permisos limitados y específicos que les permiten realizar tareas que de otra manera requerirían privilegios de superusuario.**)

