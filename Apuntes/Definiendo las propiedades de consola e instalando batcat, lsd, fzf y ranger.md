Por aquí os comparto mi archivo de configuración de la ZSH ‘**.zshrc**‘:

-   [https://hack4u.io/wp-content/uploads/2022/09/zshrc.txt](https://hack4u.io/wp-content/uploads/2022/09/zshrc.txt)

Recordad que es el mismo para el usuario ‘**root**‘, ya que contamos con un enlace simbólico.

Este archivo de configuración cuenta con algunas configuraciones adicionales, como por ejemplo la siguiente:

![](https://hack4u.io/wp-content/uploads/2022/09/bindkeys-266x89.png)

Estos bindkeys lo que hacen es que te funcionen las teclas ‘**Inicio**‘ y ‘**Fin**‘ para los desplazamientos rápidos entre líneas y ‘**Supr**‘ o ‘**Backspace**‘ para los borrados de caracteres.

Por otro lado, tenemos también contemplado en las primeras líneas del archivo la siguiente configuración:

![](https://hack4u.io/wp-content/uploads/2022/09/java_problem-288x52.png)

Esta línea nos permitirá evitar problemas con Java a la hora de abrir la interfaz gráfica de ciertos programas como Burpsuite, entre otros. Cabe destacar que si incorporas estas primeras líneas en el archivo, es aconsejable que contemples la siguiente línea en tu archivo ‘**bspwmrc**‘:

![](https://hack4u.io/wp-content/uploads/2022/09/java_problem_bspwmrc.png)