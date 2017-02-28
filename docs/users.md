# Admistración de cuentas de usuario

Existen diferentes tipos de usuarios que puedes activar o administrar en tu sistema. Cada uno de ellos tiene privilegios y funciones distintas. Esta página te ayuda a entender cómo utilizar cada uno de ellos.  


* **Administrador del Panel de Control**: Es el único usuario con ilimitados privilegios para la administración de los datos a través del panel de control. Este usuario se crea automáticamente en el mismo momento en el que se crea el servidor y no se puede eliminar.    
* **SuperUsuario**: Este usuario no tiene acceso a través del panel de control sin embargo es más poderoso que el anterior ya que tiene ilimitados privilegios sobre todo el sistema (usuario root de Linux). 
* **Usuarios ordinarios**: Usuarios que el el administrador puede crear a través del panel de control y a los que puede otorgar permisos para utlizar o acceder a los servicios.    
* **Usuario Postmaster**: Por cada dominio activado en el panel de control se crea una cuenta postmaster. Este tipo de usuario tendrá la posbilidad de crear y administrar cuentas de correo electrónico asociadas al mismo dominio. 
* **Cuentas email**: Los titulares de una cuenta de correo electrónico tendrán acceso al panel de control con el único privilegio de ver o editar sus propios datos (contraseña, nombre, reenvío autómatico).  

## Administrador

El administrador del panel de control es probablemente el usuario que más utilizarás, ya que es el que tiene todos los privilegios en el panel de control. Esto significa que este usuario puede crear, configurar y eliminar a todos los demás usuarios, los dominios, las cuentas de correo electrónico y cualquier otro dato administrable desde el panel de control.  

Este usuario se crea automáticamente  y no se puede eliminar. De lo contarío perderías el acceso al panel de control.  
Cuando desde Maadix construimos el servidor instalando las aplicaciones que has elejido, también creamos este usuario asignándole una contraseña aleatoria que por razones de seguridad estás forzado a cambiar la primera vez que accedes al panel de control.  

Todos los parámetros, menos el nombre de usuario, se pueden editar en cualquier momento desde la página de perfil del panel de control. Puedes acceder a ella a través del menú que se despliega en la esquina superior derecha.  

![admin](../img/usuarios/admin.png)

Es muy importante que la cuenta de correo electrónico asociada a este usuario sea una cuenta válida a la que tengas acceso, ya que es la que el sistema utiliza para ciertas notificaciones o funcionalidades como la recuperación de la contraseña.


  
## SuperUsuario

Este usuario no puede operar desde el panel de control, ni siquiera tiene un acceso válido al mismo. Sin embargo es el usuario más poderoso del sistema . En otros términos es tu usuario ´root´.  
Tener acceso ´root´ a un sistema significa tener el control total sobre el mismo, poder implementar cualquier tipo de cambio, acceder a cualquier carpeta, instalar cualquier aplicación.  

 
Por razones de seguridad es aconsejable evitar el uso de este usuario, y crear en su lugar cuentas de usuarios ordinarios siempre que sea posible. En este mismo documento encontrarás detalles sobre como crear y utilizar este tipo de usuario.  

 
Al igual que el administrador, el SuperUsuario se crea automáticamente en el proceso de creación del servidor y hasta que no cambies su contraseña durante el proceso de activación del panel de dontrol, será un usuario sin ningún tipo de acceso.  

Una vez activado, este usuario podrá acceder al servidor a través de una conexión sftp o SSH. Como decíamos sus privilegios en el sistema son ilimitados, y le permitirán efectuar cualquiera de las siguientes acciones:

* Aceder a todas las carpetas del sitema a través una conexión (STFP/SSH)
* Leer, modificar, eliminar o ejecutar cualquier archivo del sistema incluso si no es propietario (SSH)
* Modificar, instalar o eliminar cualquier aplicación (SSH)
* Crear otros usuarios `root`  
* Apagar o reiniciar el servidor
* Todo lo demás....

Estas operaciones no son permitidas desde el panel de control.  


## Usuarios genéricos

Son usuarios creados por el administrador y a los que se pueden asignar diferentes permisos y accesos.

* Acceso sftp: podrán acceder al servidor por sftp y estarán confinados en su propia carpeta personal. No pueden acceder al resto del sistema ni tienen acceso ssh.
* Webmaster: pueden ser nombrados webmaster de una aplicación web. En este caso se crea un acceso directo en su carpeta personal a la carpeta de la aplicación web. Se convierte en el propietario de dicha carpeta y de todos los archivos que pueda contener adquiriendo  así todos los privilegios sobre estos archivos. Los usuarios webmaster necesitarán tener activado el acceso SFTP para poder editar los archivos.   
* Cuenta VPN: Se le puede activar una cuenta VPN para que su conexión con el servidor sea directa y segura. El usuario podrá utilizar esta conexión también para conectar a cualquier otra dirección en internet.

## Usuarios postmaster

Este usuario tiene la única facultad de administrar las cuentas de correo electrónico asociadas a su dominio. Podrá crear, modificar y borrar las direcciones email a través del panel de controli. Es muy útil para poder permitir estas tareas sin necesidad de otrogar a otro colaborador todos los privilegios.  

Los usuarios postmaster se crean por defecto por cada dominio que se habilita en el panel de control. Tienes un listado completo de estos usuarios en la página Usuarios -> Postmasters

![Postmasters](../img/usuarios/postmasters.png)

Desde esta misma página puedes asignar o resetear la sus contraseñas haciendo click en editar.


Para operar desde el panel de controlel postmaster tendrá que identificarse utilizando el nombre de usuario postmaster@sudominio.com y la contraseña que se le ha asgnado.  

![Postmaster log in](../img/usuarios/postmaster-login.png)

  
Una vez entrado en el panel de control este usuario tendrá una interfaz un poco diferente a la del administrador, en la que solo tendrá habilitado el acceso a las funcionalidades que tiene permitidas.

![Postmaster logged in](../img/usuarios/postmaster-logged.png)


## Cuentas email

Las cuentas de correo electrónico creadas en el panel de control pueden ser administradas directamente por su titular.  
El usuario que tenga un email activado podrá entrar en el panel de control insertando su cuenta de correo como nombre de usuario y la contraseña asignada a la misma.     

![Email log in](../img/usuarios/email-login.png)  

Sus privilegios de edición están limitados a su propia cuenta de correo electrónico. Podrá cambiar su contraseña, su nombre y apillodo y establecer o desactivar el renvío automático.
También puede aceeder para consultar los datos para la configuración de su cuenta en un cliente de correo electrónico en su ordenador (Thunderbird, Outlook, etc).   

![Email logged in](../img/usuarios/email-logged.png)  


