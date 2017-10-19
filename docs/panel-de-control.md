# Alta del servidor


Cuando el proceso de creación de una máquina virtual en MaadiX termina, el mismo servidor recién creado envía un correo de notificación a la cuenta de correo electrónico que se ha designado como administrador.  

El correo contiene instrucciones sobre cómo acceder al servidor, incluyendo las contraseñas. Dichas contraseñas son generadas localmente por el servidor, de modo que nadie más que él las conoce.  
Sin embargo (al menos por el momento), el proceso de envío de contraseñas mediante correo se efectúa en texto plano, lo que hace absolutamente indispensable que se proceda inmediatamente a cambiarlas por cuestiones de seguridad. Es por eso que MaadiX fuerza al nuevo administrador a que cambie las contraseñas a través de un proceso de activación, que solamente se tendrá que hacer una vez.

# Activación 

La primera vez que se accede al panel de control solamente se mostrará la página de activación. En esta página se tendrá que proceder al cambio de la contraseña de los dos diferentes usuarios del sistema:  

* El administrador del panel de control  
* El usuario root del sistema (Superusuario)    

Hasta que no se complete este proceso, las otras secciones del panel de control no serán accesibles y el usuario root no podrá acceder al sistema ni por SSH ni por SFTP. 

Esta es una importante medida de seguridad, que también tiene que ser aplicada para cualquier otra aplicación que se haya instalado y que requiera un nombre de usuario y contraseña. 

Es sumamente importante que el correo electrónico asociado al administrador del panel de control sea válido y que tengas acceso al mismo, ya que el servidor enviará a esta cuenta todas las notificaciones, indicaciones e instrucciones para recuperar la clave de acceso del panel de control en caso de que la olvidaras.

# Detalles

La ventana de inicio del panel de control muestra información estadística interna acerca del uso de recursos en el sistema. Si quieres volver a consultarla en cualquier otro momento, tienes que remitirte a la pestaña 'Detalles' del margen izquierdo del panel.

![Screenshot](img/cpanel-stats.png)
