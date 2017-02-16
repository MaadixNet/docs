# Cómo crear y editar usuarios de sistema

MaadiX permite crear fácilmente, a través de tu Cpanel, usuarios de sistema con acceso SFTP/SSH a tu servidor. Estos usuarios de sistema tienen su propio espacio en tu servidor con ruta */home/sftpusers/usuario/*. Dentro de este espacio podrán crear y modificar archivos y carpteas. También ahí encontrarán el acceso directo a las carpetas de los dominios de los que sean Webmaster.

A diferencia del Superusuario, este tipo de usuario nunca podrá ver, acceder ni modificar el resto de carpetas y archivos del servidor más allá de su carpeta personal */home/usuario/* y de las carpetas de dominio de las que sea Webmaster.

## Crear un usuario nuevo

Haz click en la pestaña **Usuarios** de tu Cpanel. En este apartado puedes ver listados todos los usuarios de sistema actuales. Puedes ver cuales de ellos tienen acceso SFTP a su */home/sftpusers/usuario/* en tu servidor, si tienen activado el servicio VPN y tus dominios propios de los que son Webmaster. El primer usuario de esta lista es siempre el SuperUsuario de sistema.

![Screenshot](img/lista-usuarios.png)

Haz click en le botón **Añadir Usuario** encima de la lista para desplegar el formulario. Los campos marcados con (\*) son obligatorios. Elige el nombre y contraseña para el nuevo usuario. Asígnale un correo electrónico, puedes elegir entre una de las cuentas de correo que hayas creado en con MaadiX o una cuenta de correo externa.

### Acceso SFTP

Marcando la casilla **Acceso SFTP** se creará una carpeta para el nuevo usuario dentro de tu servidor en la ruta */home/sftpusers/usuario/* a la cual tendrá acceso por SFTP con los creedenciales:

* **Servidor**: tu *subdomino.maadix.org*
* **Protocolo**: SFTP  
* **Modo de acceso**: Normal  
* **Usuario**: El nombre del usuario (sensible a mayúsculas/minúsculas)
* **Contraseña**: La contraseña que has establecido para este usuario

a través de un cliente SFTP como por ejemplo [Filezilla](https://filezilla-project.org/). Si quieres compartir estos credenciales de acceso deberás buscar un canal seguro para comunicarlos tú ya que por razones de seguridad MaadiX no las envirá.

### Cuenta VPN

Marcando la casilla **Cuenta VPN** darás acceso al nuevo usuario a utilizar la VPN de tu servidor. Esto le permitirá conectarse a su espacio en el servidor utilizando una conexión cifrada y segura. Además de ello, podrá visitar cualquier dirección de Internet pasando primero a través de la VPN. Esto le permite navergar de manera más segura si, por ejemplo, está conectado a una red WiFi pública.

La VPN de MaddiX funciona con OpenVPN. Es necesario instalar en los dispositivos que vayan a utilizarla el software de OpenVPN y añadir ciertas configuraciones. Aquí puedes encontrar un tutorial sencillo para diferentes sistemas operativos (Linux / MacOX / Windows) y para PC o móvil: [Instrucciones para crear VPN](vpn)

Por defecto al crear la cuenta VPN para el nuevo usuario se le enviará un mail con estas instrucciones y los archivos de configuración preparados. Sin embargo, nuevamente la contraseña no se enviará por razones de seguridad y deberás hacersela llegar por otro canal. El usuario/contraseña es el mismo que el del acceso SFTP.

![Screenshot](img/add-usuario.png)


## Editar un usuario

Puedes ver y editar tus usuarios entrando en la sección **Usuarios** del menú y dentro de la lista de usuarios haciendo click en el botón *editar* del usuario que quieras modificar.

En la pantalla de edición puedes, en cualquier momento, activar o desactivar el acceso SFTP del usuario. Ahí está también apuntada la ruta a su directorio personal que siempre es    /home/sftpusers/usuario    .

Puedes crear o borrar la cuenta VPN del usuario desde aquí, además de mandarle nuevamente las instrucciones para uso y archivos de configuración

Desde la edición de usario puedes cambiar su nombre/apellido y su correo electrónico asociado. Sin embargo, una vez creado, no puedes cambiar el nombre de usuario de sistema. Por ejemplo en el caso anterior, puedes modificar *Ana* pero no puedes modificar *user3*.

Puedes también aquí modificar la contraseña del usuario de sistema. Esta es la contraseña con la que accede al servidor por SFTP y también la contraseña de su cuenta VPN. Por razones de seguridad, MaadiX no notifica al usuario el cambio de contraseña cambios en las credenciales de acceso. Si necesitas comunicar de estos cambios al usuario deberás hacerlo por otro canal.


## Eliminar usuario

Los usuarios de sistema se eliminan también desde la sección **Usuarios** de tu Cpanel.
