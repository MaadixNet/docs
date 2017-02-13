# VPN

Una red privada virtual o VPN ([Virtual Private Network - Wikipedia](https://es.wikipedia.org/wiki/Red_privada_virtual) ), es una tecnología de red que permite una extensión segura de tu red privada de área local (LAN) a travs de una red pública sobre la que no tienes control como Internet. 

La VPN de MaadiX te permite conectarte a tu servidor y gestionarlo utilizando una conexión cifrada y segura. Además de ello, puedes visitar cualquier dirección de Internet pasando primero a través de tu VPN. Esto te permite una connexión segura si, por ejemplo, estás navegando a través de una red WiFi pública. 
  
Para activar una conexión VPN con tu servidor necesitas crear el usuario en el Cpanel y tener instalado un programa  'cliente' en los dispositivo que se van a conectar.  

# Crear cuentas 

1- Desde el Cpanel entra en la pestaña 'Usuarios'. Puedes editar un usuario existente o crear uno nuevo.  
2- Entre los atributos disponibles verás 'Cuenta VPN'. Activa la casilla.  
3- Si quieres enviar indicaciones al usuario para configurar su conexión, activa la casilla 'Enviar email con instrucciones al usuario'  


# Instalar y configurar cliente  

## Windows

1- Descargar e instalar la aplicación OpenVpn  

https://openvpn.net/index.php/open-source/downloads.html  

![Screenshot](img/windows-vpn/01-vpn-download.png)


2- Tomar nota de la ubicación de la aplicación y acabada la instalación copiar en la carpeta \config los dos archivos  
a) vpn.ovpn    
b) ca.crt  

![Screenshot](img/windows-vpn/02-vpn-location.png)

NOTA: La ubicación por defecto es C:\Program Files\OpenVPN, así que tendrás que copiar ambos archivos en C:\Program Files\OpenVPN\config a menos que durante la instalación hayas ubicado la aplicación en otra carpeta 

Cuando se activa una cuenta VPN desde el Cpanel, hay la opción de enviar un email al nuevo usuario con  las instrucciones para configurar el cliente. En este mismo mail están adjuntos los archivos que tienes que copiar. Si no has recibido ningún mail solicita estos datos a la persona que tenga acceso de administrador al panel de control  

3- Abre la aplicación OpenVPN GUI   

4- Introduce el usuario y contraseña que te han proporcionado para la conexión  

![Screenshot](img/windows-vpn/03-insert-user.png)

 Espera unos segundos hasta que se establezca la conexión. Para comprobar que la conexión se ha efectuado con éxito visita la web [http://cualesmiip.com/](http://cualesmiip.com/) activando y desactivando la VPN.  El resultado que te ofrece como 'Tu IP real' debería ser distinto.


## Linux

1- Instala el cliente openVpn si no lo tienes instalado todavía (muchas distribuciones de linux lo incluyen por defecto)     

Por consola:  

    sudo apt-get install netwotk-manager-openvpn

Con Synaptic
Aplicaciones > Herramientas de Sistema > Gestor de paquetes Synaptic busca y selecciona netwotk-manager-openvpn  
Una vez seleccionado el paquete haz click en 'Aplicar', en la bandeja superir de la interfaz

![Screenshot](img/linux-vpn/01-install.png)

2- Haz click en 'Configuración de Red' desde el panel de Network Manager  

![Screenshot](img/linux-vpn/ubuntu-edit.conn.png)

3- Busca el botón 'Añadir' o '+' para  añadir la configuración y elige VPN  

![Screenshot](img/linux-vpn/03-add-vpn.png)

4- Escoge la opción 'Importar desde un archivo'  

![Screenshot](img/linux-vpn/03-import-profile.png)

5- Selecciona el archivo vpn.conf que te han proporcionado  

![Screenshot](img/linux-vpn/04-select-file.png)

Cuando se activa una cuenta VPN desde el Cpanel, hay la opción de enviar un email al nuevo usuario con  las instrucciones para configurar el cliente. En este mismo mail están adjuntos los archivos que tienes que guardar para una fácil configuración. Ambos archivos (vpn.conf y ca.crt) tienen que estar en la misma carpeta por lo que no los muevas. Simplemente importa el archio vpn.conf.   


6- Inserta un nombre para tu conexión el usuario que recibiste .Por razones de seguridad la contraseña no se envia por email. El administrador de sistema se encargará de hacertela llegar por el medio que considere más seguro. Elije el método de gestión de la contraseña (es aconsejable la opción 'Preguntar siempre')    

![Screenshot](img/linux-vpn/04-select-file.png) 

7- Vuelve al panel del Network Manager y activa la conexión recién creada
![Screenshot](img/linux-vpn/07-connected-vpn.png) 

En unos segundos se crea la conexión. Para comprobar que la conexión se ha efectuado con éxito visita la web [http://cualesmiip.com/](http://cualesmiip.com/) activando y desactivando la VPN.  El resultado que te ofrece como 'Tu IP real' debería ser distinto.  

## Android

1- Descarga el cliente OpenVpn Connect para Android  

[Descargar OpenVpn Connect](https://play.google.com/store/apps/details?id=net.openvpn.openvpn&hl=es)

2- Lanza la aplicación y desde el menú escoge 'Import'  

![Screenshot](img/android-vpn/01-import.png)

3- Selecciona 'Import profile from SD card'  

![Screenshot](img/android-vpn/02-profile.jpeg)

4- Selecciona el archivo de configuración android-client.ovpn que  has previamente recibido y guardado en tu dispositivo    

![Screenshot](img/android-vpn/03-choosefile.jpeg)

Cuando se activa una cuenta VPN desde el Cpanel, hay la opción de enviar un email al nuevo usuario con  las instrucciones para configurar el cliente. En este mismo mail están adjuntos los archivos que tienes que guardar. Ambos archivos (android-client.ovpn y ca.crt) tienen que estar en la misma carpeta. Si no has recibido ningún mail solicita estos datos a la persona que tenga acceso de administrador al panel de control

5- Inserta el nombre de usuario y la contraseña  

![Screenshot](img/android-vpn/04-user-password.jpeg)

6- Espera unos segundos hasta que se establezca la conexión  

![Screenshot](img/android-vpn/05-connect.jpeg)

 Espera unos segundos hasta que se establezca la conexión. Para comprobar que la conexión se ha efectuado con éxito visita la web [http://cualesmiip.com/](http://cualesmiip.com/) activando y desactivando la VPN.  El resultado que te ofrece como 'Tu IP real' debería ser distinto.

