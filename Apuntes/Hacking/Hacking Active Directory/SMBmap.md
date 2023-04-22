Smbmap es una herramienta de línea de comandos que se utiliza para enumerar y explorar recursos compartidos en una red SMB.
## Enumerar recursos compartidos en un servidor SMB
```python
smbmap -H <IP address or hostname>
```
Por ejemplo, para enumerar los recursos compartidos en un servidor con la dirección IP 192.168.1.100, puede ejecutar el siguiente comando, el cual mostrará una lista de los recursos compartidos en el servidor, junto con información sobre los permisos de acceso.
```python
smbmap -H 192.168.1.100
```
### Enumerar archivos y directorios en un recurso compartido
Para enumerar los archivos y directorios en un recurso compartido específico, puede utilizar el siguiente comando:
```python
smbmap -H <IP address or hostname> -u <username> -p <password> -s <sharename> -R
```
Por ejemplo, para enumerar los archivos y directorios en el recurso compartido "compartido1" en un servidor con la dirección IP 192.168.1.100, puede ejecutar el siguiente comando, el cual mostrará una lista de los archivos y directorios en el recurso compartido "compartido1", junto con información sobre los permisos de acceso.
```python
smbmap -H 192.168.1.100 -u usuario -p contrasena -s compartido1 -R
```
--- 
## EJEMPLO FUNCIONAMIENTO SMBMAP

Así sería el funcionamiento de smbmap
![[Pasted image 20230213104857.png]]