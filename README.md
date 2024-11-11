#Práctica 1

#Configuración del Ubuntu Server.

Con este comando se cambia el nombre de ubuntu a server05
![aa](/home/isard/Escritorio/captura1.png "")

Configura tu tarjeta de red usando la dirección 192.168.X.1/24.

![aa](/home/isard/Escritorio/captura2.png "")
![aa](/home/isard/Escritorio/captura3.png "")

Con este comando guardamos los cambios

![aa](/home/isard/Escritorio/captura22.png "")

Aquí podemos ver como se ha actualizado

![aa](/home/isard/Escritorio/captura4.png "")

#Configuración del Cliente Ubuntu

Busca el diálogo de configuración y cambia el nombre del equipo a ubuntuXX

![aa](/home/isard/Escritorio/captura5.png "")

sudo nano /etc/hosts

![aa](/home/isard/Escritorio/captura6.png "")

Busca el diálogo de configuración (windows + red) y cambia la configuración de red usando la dirección 192.168.X.2/24

![aa](/home/isard/Escritorio/captura7.png "")

Comprueba que la IP se ha actualizado con el comando ip a

![aa](/home/isard/Escritorio/captura8.png "")
![aa](/home/isard/Escritorio/captura9.png "")

#Configuración del Cliente Windows 10

Busca el diálogo de configuración y cambia el nombre del equipo a windowsXX

Para cambiarlo tienes que entrar en configuración-sistema-acerca de-cambiar nombre del equipo

![aa](/home/isard/Escritorio/captura10.png "")

Busca el diálogo de configuración (windows + conexiones) y cambia la configuración de red usando la dirección 192.168.X.2/24

Para cambiar la configuración tienes que ir a configuración-red e internet-ethernet-cambiar opciones del adaptador de red. Entramos en la red que se está utilizando y le damos a propiedades. Ahí vamos a Protocolo de internet versión 4 y a su propiedades y ponemos nuestra ip.

![aa](/home/isard/Escritorio/captura11.png "")

Comprueba que la IP se ha actualizado con el comando ipconfig. Para cambiar el nombre en Windows: botón derecho sobre icono de equipo.

![aa](/home/isard/Escritorio/captura12.png "")

#Configuración DHCP en Ubuntu Server

Añade una tarjeta de red a tus 3 máquinas asociadas a la red Personal 1 (Hecho por el profesor). En las máquinas línux se etiquetará como enp4s0.
Vas a utilizar la dirección de red: 192.168.1XX.0/24, donde XX debes sustituirlo por tu número de alumno

![aa](/home/isard/Escritorio/captura13.png "")

sudo nano /etc/default/isc-dhcp-server

![aa](/home/isard/Escritorio/captura14.png "")
![aa](/home/isard/Escritorio/captura15.png "") 
![aa](/home/isard/Escritorio/captura16.png "")

Configura el servidor DHCP. Debes definir un rango desde la IP 192.168.XX.100 hasta la 192.168.XX.200.

![aa](/home/isard/Escritorio/captura17.png "")

Comprueba la dirección obtenida y la conexión mediante ping.

![aa](/home/isard/Escritorio/captura18.png "")

Verifica las leases o préstamos del servidor (dhcp-lease-list y /var/lib/dhcp/dhcpd.leases_)

![aa](/home/isard/Escritorio/captura19.png "")

Configura una reserva de IP fija en el servidor DHCP. Por ejemplo la dirección 50.

![aa](/home/isard/Escritorio/captura20.png "")

Reinicia el servicio, y renueva la IP en windows. Verifica que la nueva configuración toma efecto.

![aa](/home/isard/Escritorio/captura21.png "")
