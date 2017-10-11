# Categorías de usuarios

En MaadiX existen diferentes categorías de usuarios que puedes activar o administrar en tu sistema. Cada uno de ellos cuenta con distintos privilegios y funciones, que en esta página te ayudaremos a entender para saber mejor cómo utilizarlos.


* **Administrador del panel de control**: Se trata del único usuario con privilegios ilimitados para la administración de los datos a través del panel de control. Este usuario se crea automáticamente en el mismo momento en el que se crea el servidor y no se puede eliminar.
* **Superusuario**: Aunque este usuario no tenga acceso a través del panel de control, es jerárquicamente más importante que el anterior, dado que tiene unos privilegios ilimitados sobre la totalidad del sistema ("usuario root" de Linux). No se puede eliminar, de modo que no llegues a perder nunca el acceso root al sistema.
* **Usuarios ordinarios**: Usuarios que el administrador puede crear a través del panel de control, a los cuales puede otorgar permisos para utilizar o acceder a los distintos servicios.    
* **Usuario postmaster**: Por cada dominio activado en el panel de control, se crea una cuenta postmaster. Este tipo de usuario tendrá la posibilidad de crear y administrar cuentas de correo electrónico asociadas al mismo dominio. 
* **Cuentas de correo**: Los titulares de una cuenta de correo electrónico tendrán acceso al panel de control con el único privilegio de ver o editar sus propios datos (contraseña, nombre, reenvío autómatico...).  

## Administrador

El administrador del panel de control es probablemente el usuario que más utilizarás, ya que es el que tiene todos los privilegios dentro del panel de control. Esto significa que este usuario puede crear, configurar y eliminar a todos los demás usuarios, los dominios, las cuentas de correo electrónico y cualquier otro dato administrable desde el panel de control.

Este usuario se crea automáticamente y no es posible eliminarlo. De lo contrario, perderías el acceso al panel de control.  
Cuando desde MaadiX construimos el servidor, también creamos este usuario asignándole, una contraseña aleatoria que por razones de seguridad estás obligado a cambiar la primera vez que accedes al panel de control.

Todos los parámetros, excepto el nombre de usuario, se pueden editar en cualquier momento desde la página de 'Perfil' del panel de control. Puedes acceder a ella a través del menú que se despliega en la esquina superior derecha.  

![admin](../img/usuarios/admin.png)

Es muy importante que la cuenta de correo electrónico asociada a este usuario sea una cuenta válida a la que tengas acceso, puesto que es la que el sistema utiliza para enviar ciertas notificaciones o funcionalidades importantes, tales como la recuperación de la contraseña.


  
## Superusuario

Este usuario no puede operar desde el panel de control (de hecho, ni siquiera tiene un acceso válido al mismo). Aún así, es el usuario más poderoso del sistema. Técnicamente hablando, es el usuario ´root´.  
Tener acceso ´root´ a un sistema significa tener el control total sobre el mismo, poder implementar cualquier tipo de cambio, acceder a cualquier carpeta e instalar cualquier aplicación.  

 
Por razones de seguridad, es aconsejable evitar el uso de este usuario, creando en su lugar cuentas de usuarios ordinarios siempre que esto sea posible. En este mismo documento encontrarás más detalles sobre cómo crear y utilizar este tipo de usuario.  

 
Al igual que el administrador, el Superusuario se crea automáticamente en el proceso de creación del servidor, y hasta que no cambies su contraseña durante el proceso de activación del panel de dontrol, será un usuario sin ningún tipo de acceso.  

Una vez activado, este usuario podrá acceder al servidor a través de una conexión SFTP o SSH. Sus privilegios en el sistema son ilimitados, de forma que le permiten efectuar cualquiera de las siguientes operaciones, que no están permitidas desde el panel de control:

* Acceder a todas las carpetas del sistema a través una conexión (STFP/SSH).
* Leer, modificar, eliminar o ejecutar cualquier archivo del sistema incluso si no es propietario (SSH).
* Modificar, instalar o eliminar cualquier aplicación (SSH).
* Crear otros usuarios `root`.
* Apagar o reiniciar el servidor.


## Usuarios ordinarios

Son usuarios creados por el administrador y a los que se pueden asignar diferentes grados de permisos y accesos.

* Acceso SFTP: Podrán acceder al servidor por SFTP y estarán confinados en su propia carpeta personal. No pueden acceder al resto del sistema ni tienen acceso SSH.
* Webmaster: Pueden ser nombrados webmasters de una determinada aplicación web. En este caso, se crea un acceso directo en su carpeta personal a la carpeta de la aplicación web. Se convierte en el propietario de dicha carpeta y de todos los archivos que pueda contener, adquiriendo así todos los privilegios sobre estos archivos. Ten presente que los usuarios tipo webmaster necesitarán tener activado el acceso SFTP para poder editar los archivos.   
* Cuenta VPN: Se les puede activar una cuenta VPN para que su conexión con el servidor sea directa y segura. Asimismo, el usuario también podrá utilizar esta conexión para conectarse a cualquier otra dirección de Internet.
* Acceso aplicación phpMyAdmin: Se les puede activar el permiso para acceder a esta aplicación, en caso de que estuviera instalada. Por razones de seguridad, esta aplicación está protegida por una doble contraseña y es necesario tener habilitado el acceso a la interfaz con tal de poder acceder.

## Usuarios postmaster

Este usuario solamente tiene la facultad de administrar las cuentas de correo electrónico asociadas a su dominio. Podrá crear, modificar y borrar las direcciones de correo a través del panel de control. Este tipo de usuario es sumamente útil para poder permitir estas tareas sin necesidad de otorgar a otro colaborador todos los privilegios.  

Los usuarios postmaster se crean por defecto por cada dominio que se habilita en el panel de control.


Para operar desde el panel de control, el postmaster tendrá que identificarse utilizando el nombre de usuario postmaster@sudominio.com y la contraseña que se le ha asignado.  

![Postmaster log in](../img/usuarios/postmaster-login.png)

  
Una vez dentro del panel de control, este usuario tendrá una interfaz ligeramente distinta a la del administrador, en la que sólo tendrá habilitado el acceso a las funcionalidades que tiene permitidas.

![Postmaster logged in](../img/usuarios/postmaster-logged.png)


## Cuentas de correo

Las cuentas de correo electrónico creadas en el panel de control pueden ser administradas directamente por su titular.  
El usuario que tenga un correo electrónico activado, podrá entrar en el panel de control insertando su cuenta de correo como nombre de usuario y la contraseña asignada a la misma.     

![Email log in](../img/usuarios/email-login.png)  

Sus privilegios de edición están limitados a su propia cuenta de correo electrónico. Podrá cambiar la contraseña, su nombre y apellido, aparte de establecer o desactivar el reenvío automático.
También puede acceder para consultar los datos para la configuración de su cuenta en un cliente de correo electrónico en su dispositivo (Thunderbird, Outlook...).   

![Email logged in](../img/usuarios/email-logged.png)  


