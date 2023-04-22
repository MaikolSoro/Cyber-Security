-----
- Tags: #contenedor #docker #dockerFile #comandos
----

**docker rm $(docker ps -a -q) –force**: Este comando se utiliza para eliminar todos los contenedores en el sistema, incluyendo los contenedores detenidos. La opción “-q” se utiliza para mostrar sólo los identificadores numéricos de los contenedores, y la opción **“–force”** se utiliza para forzar la eliminación de los contenedores que están en ejecución. 
Es importante tener en cuenta que la eliminación de todos los contenedores en el sistema puede ser peligrosa, ya que puede borrar accidentalmente contenedores importantes o datos importantes. Por lo tanto, se recomienda tener precaución al utilizar este comando.

----


**docker rm id_contenedor**: Este comando se utiliza para eliminar un contenedor específico a partir de su identificador.
Es importante tener en cuenta que la eliminación de un contenedor eliminará también cualquier cambio que se haya realizado dentro del contenedor, como la instalación de paquetes o la modificación de archivos.

----

**docker rmi $(docker images -q)**: Este comando se utiliza para eliminar todas las imágenes de Docker en el sistema. La opción **“-q”** se utiliza para mostrar sólo los identificadores numéricos de las imágenes.

Es importante tener en cuenta que la eliminación de todas las imágenes de Docker en el sistema puede ser peligrosa, ya que puede borrar accidentalmente imágenes importantes o datos importantes. Por lo tanto, se recomienda tener precaución al utilizar este comando.

----

**docker rmi id_imagen**: este comando se utiliza para eliminar una imagen específica a partir de su identificador. Es importante tener en cuenta que la eliminación de una imagen eliminará también cualquier contenedor que se haya creado a partir de esa imagen. Si se desea eliminar una imagen que tiene contenedores en ejecución, se deben detener primero los contenedores y luego eliminar la imagen.

----
