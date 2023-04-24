https://github.com/swisskyrepo/PayloadsAllTheThings

### OWASP TOP 10 y vulnerabilidades web

# Cuestionario de vulnerabilidades

¿Qué es la enumeración del sistema en términos de seguridad informática?
- [x] Identificar información sobre el sistema objetivo para ayudar a la explotación

¿El ataque de Type Juggling ocurre en lenguajes de programación como PHP, donde un atacante puede manipular la comparación entre dos variables mediante la explotación de la conversión automática de 
**tipos** de datos.

¿Qué es la explotación de vulnerabilidades en términos de seguridad informática?
 - [x] Aprovechar fallos en el software para tomar control del sistema
 - [ ] Descubrir y reportar errores en el software
 - [ ] Realizar pruebas de penetración en sistemas operativos
 - [ ]  Ninguna de las anteriores
 
¿Qué componente de un sistema operativo UNIX se explota en un ataque ShellShock?
- [x] Bash
- [ ] Cron
- [ ] Sudo
- [ ] Chroot
 

¿Qué función de PHP puede ser explotada en un ataque LFI?
- [ ] fopen()
- [x] include() 
- [ ] strpos()
- [ ] array_merge()

¿Qué método HTTP se utiliza para enviar datos de formulario?
- [ ] GET
- [x] POST
- [ ] HEAD
- [ ]  OPTIONS

¿Cuál es el puerto por defecto utilizado por el servicio FTP?
- [x] 21
- [ ] 23
- [ ] 25
- [ ] 80

¿En un ataque XXE, ¿qué componente de un documento XML se explota?
- [x] Entidades externas
- [ ] Atributos
- [ ] Espacios de nombres

En un ataque RFI, ¿qué protocolo suele ser utilizado para incluir archivos remotos?
- [ ] FTP
- [ ] SMTP
- [x] HTTP
- [ ] SSH

### Rellena el espacio con la palabra correcta

Los ataques de Client-Side Template Injection (CSTI) ocurren cuando un atacante inyecta datos maliciosos en una plantilla del lado del cliente, lo que lleva a la ejecución de código  ___javascript___  malicioso en el navegador del usuario.

### Rellena el espacio con la palabra correcta

Un ataque de inyección LDAP permite a un atacante manipular una consulta LDAP a través de la inyección de caracteres especiales en la entrada del usuario, lo que puede llevar a la divulgación de información confidencial almacenada en un  __directorio___ LDAP.

¿En qué lenguaje de programación es común el ataque de Prototype Pollution?
- [x] JavaScript
- [ ] Python
- [ ] Java
- [ ] Ruby

¿Qué protocolo se explota en un ataque de transferencia de zona (AXFR – Full Zone Transfer)?
- [ ] HTTP
- [ ] FTP
- [x] DNS
- [ ] SMTP

¿Cuál es el principal objetivo de un ataque XSS?
- [ ]  Eliminar la base de datos
- [ ]  Enviar spam a otros usuarios
- [x] Ejecutar código JavaScript en el navegador de la víctima 
- [ ] Deshabilitar el servidor web

### Rellena el espacio con la palabra correcta

Un ataque de Remote File Inclusion (RFI) ocurre cuando un atacante incluye un archivo remoto en una página web mediante la manipulación de la 
__URL___ .

¿Cuál de los siguientes es un vector común para ataques de Log Poisoning?
- [ ] Entrada del usuario en formularios web
- [x] Encabezados HTTP maliciosos
- [ ] Cookies manipuladas
- [ ] Archivos adjuntos maliciosos

Introduce palabras clave relacionadas con la temática ‘XSS’, cuando la palabra sea correcta, automáticamente se rellenará en los cuadros inferiores (pueden ser una o un conjunto de palabras)

Palabra clave #1  Palabra clave #2  #3 #4

### Rellena el espacio con la palabra correcta

La inyección SQL es una técnica de ataque en la que un atacante introduce comandos 
__sql__ maliciosos en una consulta para obtener acceso no autorizado a una base de datos.

¿Qué característica de GraphQL puede ser explotada para obtener información sobre la estructura de un esquema GraphQL?
 - [ ] Mutaciones
 - [ ] Suscripciones
 - [ ] Fragmentos
 - [x] Introspección

Un ataque CSRF engaña a la víctima para que envíe solicitudes HTTP no autorizadas a un sitio web mientras la víctima mantiene una sesión activa, explotando la confianza del sitio en las **cookies** del navegador.

¿Qué protocolo de red utiliza el servicio SSH?
- **TCP**  
- ARP
- UDP
- ICMP

¿Qué tipo de ataque se produce cuando un atacante utiliza un archivo remoto para incluir contenido malicioso en un sitio web?
- SQLI
- XSS
- RFI sdsdsdsdsdsdsd
- LFI

¿Qué puerto por defecto utiliza un SQUID Proxy?
- 8080
- 1080
- 1080
- 3128 ssdsdsdsd
¿Qué encabezado HTTP se utiliza para permitir el acceso a recursos entre dominios en CORS?
- Content-Type
- Access-Control-Allow-Origin sdsdsdsdsd
- X-Content-Type-Options
- X-Frame-Options

¿Qué tipo de ataque XSS se ejecuta en tiempo real y no se almacena en el servidor?

- Persistente
- Reflejado dsdsds
- DOM-based
- Local

¿Cuál es el principal objetivo de un ataque XXE?
- Ejecutar comandos en el servidor
- Modificar el contenido de un sitio web
- Leer archivos locales y acceder a servicios internos en el servidor sdsd corrr
- Enviar spam a otros usuarios

¿Qué componente criptográfico se explota en un ataque de oráculo de relleno (Padding Oracle)?
- Generación de claves
- Funciones hash
- Validación de relleno en el descifrado simétrico sdsdsd
- Algoritmos de cifrado asimétrico

¿Cuál es el principal objetivo de un ataque de inyección SQL?
 - Modificar el contenido de un sitio web
 - Obtener información confidencial almacenada en una base de datos correcta
 - Ejecutar comandos en el servidor
 - Obtener acceso no autorizado a cuentas de usuario

En un ataque XSS, ¿qué elemento de seguridad del navegador suele ser eludido?

- Prevención de la ejecución de datos
- Control de acceso basado en roles
- Política de mismo origen  sdsdsdsdsdsdsdsdsdd
- Autenticación multifactor

¿Qué tipo de ataque XSS ocurre cuando el atacante explota una vulnerabilidad en el almacenamiento de datos en el servidor?

- Reflejado
- Persistente (**El tipo de ataque XSS en el que el atacante explota una vulnerabilidad en el almacenamiento de datos en el servidor se conoce como ataque XSS persistente. En este tipo de ataque, el código malicioso se almacena permanentemente en la base de datos del sitio web y se entrega a los usuarios cada vez que acceden a la página web comprometida.**)
- DOM-based
- Local

¿Cuál es el archivo de configuración principal de WordPress?

- wp-config.php (**El archivo de configuración principal de WordPress es wp-config.php. Este archivo contiene información importante como las credenciales de la base de datos y las claves de seguridad utilizadas para cifrar datos sensibles en WordPress.**)
- index.html
- config.ini
- settings.xml

¿Qué lenguaje de plantillas es vulnerable a la inyección de plantillas en el lado del servidor (SSTI)?

- CSS
- Jinja2 (**Jinja2 es un motor de plantillas utilizado en el framework de aplicaciones web Flask y otros frameworks similares de Python.**)
- JavaScript
- HTML

### Rellena el espacio con la palabra correcta

Un ataque SSRF permite a un atacante realizar solicitudes HTTP desde un servidor vulnerable a otros sistemas, posiblemente exponiendo información confidencial o recursos internos a través de la explotación de la funcionalidad del  ___servidor___  .

¿Cuál es el nombre del protocolo de red utilizado por el servicio SMB?
- Transmission Control Protocol
- Simple Mail Transfer Protocol
- Server Message Block  (**El servicio SMB (Server Message Block) utiliza el protocolo de red del mismo nombre, SMB, para proporcionar acceso compartido a archivos, impresoras y otros recursos en una red. SMB se ejecuta sobre TCP/IP y se utiliza principalmente en sistemas Windows.**)
- Hypertext Transfer Protocol

### Rellena el espacio con la palabra correcta

En un ataque de Log Poisoning, los atacantes pueden inyectar código malicioso en los archivos de registro a través de campos manipulados como el **User-Agent** , lo que permite la ejecución remota de código.

¿Qué medida de seguridad puede ayudar a prevenir ataques de condiciones de carrera?
- Implementar bloqueos y mecanismos de sincronización (**Para prevenir los ataques de condiciones de carrera, los desarrolladores pueden utilizar bloqueos y mecanismos de sincronización para garantizar que los procesos o hilos de ejecución no accedan simultáneamente a los recursos compartidos.**)
- Limitar la tasa de solicitudes
- Utilizar HTTPS
- Implementar controles de acceso basados en roles

¿Qué es un payload Stageless?
 - Un payload que requiere múltiples pasos para la ejecución
- Un payload que se ejecuta en un solo paso (**Un payload Stageless es un tipo de carga útil que se ejecuta en un solo paso sin requerir una comunicación adicional con el atacante.**)
- Un payload que se ejecuta en una máquina diferente a la que se está atacando
- Un payload que no requiere privilegios de administrador para su ejecución

¿Cuál es el principal objetivo de un ataque RFI?
- Ejecutar código JavaScript en el navegador de la víctima
- Eliminar la base de datos
- Incluir y ejecutar archivos remotos en el servidor (**Este tipo de ataque se lleva a cabo mediante la explotación de una vulnerabilidad en una aplicación web que permite a los atacantes incluir archivos remotos en una solicitud HTTP.**)
- Enviar spam a otros usuarios

### Rellena el espacio con la palabra correcta

Un ataque XXE explota las entidades externas en documentos 
  **xml** 
para ejecutar operaciones no autorizadas, como la lectura de archivos locales o la realización de solicitudes HTTP a servicios internos.

¿Qué componente de GraphQL puede ser utilizado para modificar datos en un servidor GraphQL?
- Consultas
- Suscripciones
- Mutaciones (**En GraphQL, las mutaciones permiten a los clientes enviar datos de cambios al servidor GraphQL, que luego se utilizan para actualizar los datos en el servidor.**)
- Fragmentos

¿Qué función de Python puede ser explotada en un ataque de deserialización Pickle (DES-Pickle)?
- json.loads()
- base64.b64decode()
- zlib.decompress()
- pickle.loads()  (**En un ataque de deserialización Pickle, un atacante puede enviar datos maliciosos que son procesados por la función pickle.loads(), lo que puede permitir la ejecución de código malicioso en el sistema.**)

¿Cuál es el principal objetivo de un ataque SSRF?
- Ejecutar comandos en el servidor
- Modificar el contenido de un sitio web
- Enviar spam a otros usuarios
- Realizar solicitudes desde el servidor a sistemas internos o externos  (**Este tipo de ataque se lleva a cabo mediante la explotación de una vulnerabilidad en una aplicación web que permite al atacante enviar solicitudes HTTP desde el servidor a sistemas internos o externos.**)

¿Qué comando LaTeX puede ser explotado para ejecutar código arbitrario en un ataque de inyección LaTeX?
- \input correcta (**En un ataque de inyección LaTeX, el atacante utiliza el comando input{} para incluir comandos maliciosos en un archivo LaTeX, que son ejecutados en el sistema cuando el archivo es compilado.**)
- \section
- \emph
- \textbf

¿Cuál es el principal objetivo de un ataque de Log Poisoning?
- Modificar el contenido de un sitio web
- Obtener información confidencial almacenada en una base de datos
- Ejecutar comandos en el servidor mediante la explotación de registros maliciosos    correcta -> 
###### NOTA Este tipo de ataque se lleva a cabo mediante la inserción de comandos maliciosos en los registros de la aplicación, lo que permite al atacante ejecutar código en el servidor
- Obtener acceso no autorizado a cuentas de usuario

En un ataque CSRF, ¿qué tipo de solicitud HTTP es más susceptible?
- POST
- PUT
- GET   (**Esto se debe a que las solicitudes HTTP GET son más fáciles de manipular y pueden ser incluidas en un enlace malicioso o una imagen.**)
- DELETE

¿Qué tipo de gestor de contenido (CMS) es Magento?
- Blog
- Red Social
- Wiki
- Comercio electrónico  (**Magento es un CMS de comercio electrónico que se utiliza para crear tiendas en línea y gestionar el contenido relacionado con el comercio electrónico, como la gestión de pedidos, los productos y los clientes.**)

¿Cuál de los siguientes es un ejemplo de un operador lógico en SQL?
- OR correcta 
- XOR
- AND  (**Los operadores lógicos en SQL incluyen AND, OR y NOT, que se utilizan para combinar o filtrar los resultados de una consulta. En este caso, el operador AND se utiliza para obtener resultados que cumplan con dos o más condiciones.**)
- NOT correcta

¿Cuál es el principal objetivo de un ataque CSRF?
- Hacer que un usuario autenticado realice acciones no deseadas en una aplicación web (**Este tipo de ataque se lleva a cabo mediante la explotación de la confianza entre el usuario y la aplicación web. El atacante consigue que la víctima envíe una solicitud maliciosa a la aplicación web, que parece ser legítima, pero en realidad contiene una petición para realizar una acción maliciosa.**)
- Eliminar la base de datos
- Ejecutar código JavaScript en el navegador de la víctima
- Leer archivos locales y acceder a servicios internos del servidor

### Rellena el espacio con la palabra correcta

En un ataque de Server-Side Template Injection (SSTI), un atacante puede ejecutar código arbitrario en el servidor al inyectar entrada maliciosa en una **plantilla**  de servidor.

¿Cuál es la diferencia entre una Reverse Shell y una Bind Shell?

- En las Reverse Shell, la conexión se realiza desde la máquina víctima hacia el atacante, mientras que en las Bind Shells, la conexión se realiza desde la máquina del atacante hacia la víctima (**En una Reverse Shell, la víctima ejecuta un código malicioso que establece una conexión de red con el atacante, mientras que en una Bind Shell, el atacante abre un puerto en la máquina víctima para realizar una conexión externa hacia este.**)

- En las Reverse Shell, la conexión se realiza desde la máquina atacante hacia la víctima, mientras que en las Bind Shells, la conexión se realiza desde la máquina víctima hacia el atacante

- En las Reverse Shell, se requiere que el atacante se autentique hacia la máquina víctima, mientras que una Bind Shell no

- Ninguna de las anteriores

¿Qué tipo de ataque XSS ocurre cuando el atacante explota una vulnerabilidad en la construcción del DOM por el navegador?
- Reflejado
- Persistente
- DOM-based (**El tipo de ataque XSS en el que el atacante explota una vulnerabilidad en la construcción del DOM por el navegador se conoce como ataque XSS basado en DOM (Dom-based XSS). En este tipo de ataque, el código malicioso se ejecuta en el navegador de la víctima utilizando JavaScript y se basa en la modificación de la estructura del documento HTML.**)
- Local

¿Qué biblioteca JavaScript es vulnerable a la inyección de plantillas en el lado del cliente (CSTI)?
- AngularJS (**La biblioteca JavaScript que es vulnerable a la inyección de plantillas en el lado del cliente (CSTI) es AngularJS. AngularJS es un framework de aplicaciones web utilizado para construir aplicaciones web dinámicas y de una sola página.**)
- jQuery
- React
- Vue.js

¿Cuál es el principal objetivo de un ataque LFI?
- Ejecutar código JavaScript en el navegador de la víctima
- Eliminar la base de datos
- Incluir y ejecutar archivos locales en el servidor (**Este tipo de ataque se lleva a cabo mediante la explotación de una vulnerabilidad en una aplicación web que permite a los atacantes incluir archivos locales en una solicitud HTTP.**)
- Enviar spam a otros usuarios

¿Qué es una inyección SQL basada en tiempo (a ciegas)?
- Una técnica de inyección SQL que se basa en el uso de comandos para obtener datos confidenciales
- Una técnica de inyección SQL que se basa en la inserción de sentencias para obtener información confidencial
- Una técnica de inyección SQL que se basa en la introducción de retrasos en las consultas aplicadas para extraer información sensible
(**Una inyección SQL basada en tiempo (a ciegas) es una técnica de ataque de inyección SQL en la que el atacante no puede obtener los resultados de inmediato, y en su lugar, introduce retrasos en la base de datos para detectar si la vulnerabilidad existe o no.**)
- Ninguna de las anteriores

¿En qué lenguaje de programación es común el ataque de Type Juggling?
- Python
- Java
- Ruby
- PHP (**En un ataque de Type Juggling, el atacante utiliza la conversión de tipos de datos de PHP para engañar a la aplicación web y realizar acciones maliciosas.**)
