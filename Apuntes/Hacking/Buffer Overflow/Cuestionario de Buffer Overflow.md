****
¿Cuál de los siguientes lenguajes de programación es más susceptible a los buffer overflow?

- [ ] Python
- [ ] Java
- [ ] Ruby
- [x] C/C++

Note: (**Los lenguajes de programación C y C++ son más susceptibles a los Buffer Overflows debido a que ambos lenguajes permiten el acceso directo a la memoria y los punteros.**)

¿Cuál de las siguientes funciones es más segura que la función gets() en C?

- [ ] strcpy()
- [ ] scanf()
- [x] fgets()
- [ ] sprintf()

Note: (**La función fgets() es más segura que la función gets() en C, ya que fgets() incluye un parámetro adicional que especifica el tamaño máximo del buffer de destino.**)

¿Qué son los Badchars?
- [x] Caracteres que pueden causar problemas en la ejecución del Shellcode
- [ ] Caracteres que ayudan a mejorar el rendimiento de una aplicación
- [ ] Caracteres que se utilizan para comprimir datos
- [ ] Caracteres que protegen aplicaciones de ataques

Note:(**Cuando se está desarrollando un exploit, es importante identificar y evitar los Badchars en el código del Shellcode, ya que su presencia podría provocar que la ejecución del código falle o que el programa objetivo se comporte de forma inesperada.**)

¿Qué función de C/C++ es especialmente vulnerable a ataques de buffer overflow debido a su incapacidad para comprobar el tamaño del buffer de destino?

- [ ] fgets()
- [ ] memcpy()
- [x] sprintf()
- [ ] strncpy()

Note:(**La función sprintf() es especialmente vulnerable a los ataques de Buffer Overflow debido a su incapacidad para comprobar el tamaño del buffer de destino.**)

¿Qué objetivo tiene el proceso de Fuzzing en el ámbito de Buffer Overflow?

- [ ] Mejorar el rendimiento de aplicaciones
- [x] Enviar datos aleatorios a una aplicación para encontrar vulnerabilidades
- [ ] Comprimir y descomprimir datos en aplicaciones
- [ ] Proteger aplicaciones de ataques

Note:(**En el ámbito del Buffer Overflow, el objetivo del proceso de Fuzzing es encontrar vulnerabilidades en una aplicación mediante el envío de datos aleatorios que puedan desencadenar comportamientos inesperados.**)

¿Qué es un ataque “return-to-libc” en el contexto de buffer overflow?

- [ ] Un ataque que explota la corrupción de punteros en la biblioteca libc
- [ ] Un ataque que inyecta código en la biblioteca libc
- [x] Un ataque que evita la protección de la pila no ejecutable llamando a funciones de la biblioteca libc
- [ ] Un ataque que explota vulnerabilidades en la implementación de la biblioteca libc

Note:(**Este tipo de ataque es común en sistemas operativos que utilizan la protección de pila no ejecutable (como DEP o NX) para prevenir la ejecución de código malicioso en áreas de memoria de la pila.**)

¿Qué es un OpCode?

- [ ] Un comando que se utiliza para proteger aplicaciones
- [x] Un código de operación en lenguaje ensamblador
- [ ] Un método de compresión de datos
- [ ] Un tipo de error en aplicaciones

Note:(**Los OpCodes se utilizan para representar las operaciones elementales que un procesador puede ejecutar, como operaciones aritméticas, lógicas o de transferencia de datos.**)

¿Qué es un shellcode?

- [ ] Un lenguaje de programación de alto nivel
- [x] Una secuencia de instrucciones utilizadas en un ataque de buffer overflow
- [ ] Una técnica de protección de memoria
- [ ] Un algoritmo de cifrado

Note:(**Un Shellcode se suele diseñar para aprovechar una vulnerabilidad de Buffer Overflow y se inserta en un buffer que se desborda con el fin de sobrescribir la memoria y ejecutar el Shellcode.**)

¿Para qué se utiliza el registro EIP?

- [x] Para almacenar el puntero a la siguiente instrucción a ejecutar
- [ ] Para guardar el puntero de la pila actual
- [ ] Para llevar un registro de los datos en caché
- [ ] Para almacenar el tamaño del archivo ejecutable

Note:(**El registro EIP se utiliza en arquitecturas x86 para almacenar la dirección de memoria de la siguiente instrucción a ejecutar en un programa. Durante la ejecución, el procesador carga en el registro EIP la dirección de la siguiente instrucción a ejecutar, lo que permite al procesador seguir ejecutando el código de manera secuencial.**)

¿Qué técnica se utiliza para evitar el desbordamiento de memoria en la función strcpy()?

- [x] strncpy()
- [ ] memcpy()
- [ ] strcat()
- [ ] sprintf()

Note:(**Para evitar el desbordamiento de memoria en la función strcpy(), se puede utilizar la función strncpy(), la cual es similar a strcpy() pero incluye un parámetro adicional que especifica el tamaño máximo del buffer de destino.**)

¿Qué es un NOP sled?

- [ ] Una técnica para evadir la detección de malware
- [x] Una secuencia de instrucciones sin operación
- [ ] Una técnica de protección de memoria
- [ ] Una secuencia de instrucciones utilizada para deshabilitar la seguridad del sistema

Note:(**Un NOP sled (también conocido como "deslizador NOP") es una secuencia de instrucciones sin operación que se utiliza en un ataque de Buffer Overflow para facilitar la ejecución de un código malicioso**)

¿Qué tipo de vulnerabilidad es explotada en un ataque de buffer overflow?

- [ ] Errores de lógica en el programa
- [ ] Errores de configuración del sistema
- [x] Errores en el manejo de la memoria
- [ ] Errores en la autenticación de usuarios

Note:(**Un atacante puede aprovechar esta vulnerabilidad para sobrescribir áreas de memoria específicas con código malicioso que puede permitirle tomar el control del sistema afectado.**)

¿Cuál de los siguientes términos describe el proceso de encontrar un buffer overflow en una aplicación?

- [x] Fuzzing
- [ ] Hardening
- [ ] Decompiling
- [ ] Reverse engineering

Note:(**A través de esta técnica, se prueba a enviar datos aleatorios en alguna sección de la aplicación con el objetivo de intentar provocar errores o fallos de seguridad en la misma.**)

¿Cuál es el principal objetivo de un ataque de buffer overflow?
- [ ] Robar información confidencial
- [x] Ejecutar código malicioso
- [ ] Causar una denegación de servicio
- [ ] Deshabilitar la seguridad del sistema

Note:(**Al aprovechar una vulnerabilidad de Buffer Overflow, un atacante puede sobrescribir áreas de memoria específicas para insertar código malicioso que se ejecutará en el sistema afectado.**)

¿Qué función tiene Immunity Debugger en un laboratorio de pruebas?

- [ ] Realizar pruebas de rendimiento en aplicaciones
- [ ] Proteger aplicaciones de vulnerabilidades
- [x] Analizar y depurar aplicaciones en busca de fallos de seguridad
- [ ] Comprimir y descomprimir datos en aplicaciones

Note:(**Immunity Debugger se utiliza en laboratorios de pruebas para analizar y depurar aplicaciones con el objetivo de encontrar vulnerabilidades de seguridad.**)

¿Qué hace ASLR en un sistema operativo?

- [ ] Protege los datos confidenciales del usuario
- [ ] Protege el sistema operativo contra los ataques de fuerza bruta
- [x] Aleatoriza la ubicación en memoria de los módulos cargados del sistema y de las aplicaciones
- [ ] Cifra los datos en el disco duro para protegerlos de los ataques

Note:(**ASLR funciona aleatorizando la ubicación en la memoria de los módulos cargados del sistema y de las aplicaciones, lo que hace que sea más difícil para un atacante predecir la ubicación de las áreas de memoria vulnerables.**)

 ¿Cuál de las siguientes instrucciones en ensamblador x86 es comúnmente utilizada para saltar a una dirección específica en un ataque de buffer overflow?

- [ ] MOV
- [ ] PUSH
- [x] JMP
- [ ] ADD

Note:(**Esta instrucción permite modificar el flujo de ejecución del programa para que salte a una dirección de memoria controlada por el atacante, lo que permite ejecutar el código malicioso en el sistema afectado.**)

¿Qué es un Buffer Overflow?

- [ ] Una técnica para proteger aplicaciones de ataques
- [x] Un tipo de error de programación que permite la sobreescritura de memoria
- [ ] Un método de compresión de datos
- [ ] Una forma de almacenar datos en caché para mejorar el rendimiento

Note:(**Un Buffer Overflow ocurre cuando un programa intenta almacenar más información en un buffer de lo que puede soportar, lo que provoca que la información sobrante sobrescriba otras áreas de memoria, pudiendo causar errores o vulnerabilidades de seguridad.**)