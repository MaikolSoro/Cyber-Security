Por aquí te comparto mi archivo de configuración ‘**current.ini**‘:

-   [https://hack4u.io/wp-content/uploads/2022/09/current.ini_.txt](https://hack4u.io/wp-content/uploads/2022/09/current.ini_.txt)

Te comparto también mi archivo ‘**launch.sh**‘ para la Polybar:

-   [https://hack4u.io/wp-content/uploads/2022/09/launch.sh_.txt](https://hack4u.io/wp-content/uploads/2022/09/launch.sh_.txt)

Asimismo, os compartimos los scripts correspondientes a los 2 módulos creados para representar la dirección IP de la interfaz ‘**ens33**‘ y la ‘**tun0**‘ correspondiente a la VPN:

-   [https://pastebin.com/HcKxU3tD](https://pastebin.com/HcKxU3tD) [**ethernet_status.sh**]
-   [https://pastebin.com/Bx6X6cg3](https://pastebin.com/Bx6X6cg3) [**hackthebox_status.sh**]

Recomendamos no cargar directamente los archivos ‘**current.ini**‘ y ‘**launch.sh**‘ que os estamos compartiendo. A ser preferible, usadlos sólo como referencia, dado que tenemos definidos nuevos módulos que por ahora no hemos creado y los cuales estaremos tocando en la siguiente clase.

# Creando nuevos módulos en la Polybar

Por aquí te comparto el script ‘**target_to_hack.sh**‘:

-   [https://pastebin.com/BC6cUHFL](https://pastebin.com/BC6cUHFL)

Asimismo, te comparto las funciones ‘**settarget**‘ y ‘**cleartarget**‘ las cuales debes incorporar en tu archivo ‘**.zshrc**‘:

-   [https://pastebin.com/z0Hy7PUB](https://pastebin.com/z0Hy7PUB) [**settarget**]
-   [https://pastebin.com/JnHSrq3Y](https://pastebin.com/JnHSrq3Y) [**cleartarget**]

Recuerda que por defecto estas definiciones vienen con la ruta ‘**s4vitar**‘ contemplada, en tu caso tendrás que cambiarlo a tu usuario correspondiente.