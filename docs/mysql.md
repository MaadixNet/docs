# Servidor Mysql 

Cada máquina virtual dispone de un servidor Mysql propio.     
En el mail de activación del servicio se envian las credenciales para el usuario root de mysql, y se recomienda cambiarlas cuando se accede al servidor.  
Si no se ha elegido instalar la aplicación PhpMyAdmin, solo se podrán administrar las bases de datos y sus usuarios a través de la consola de comandos (terminal). En caso contrario se puede utilizar la aplicación para la gestión de las bases de datos y de susu usuarios.  


# PhpMyAdmin

Se trata de una aplicación externa al Panel de Control que permite administrar bases de datos e usuarios mysql desde una interfaz gráfica.  

Por razones de seguridad esta aplicación está protegida con doble contraseña. Solo los usuarios que tengan activado el  'Acceso Aplicación PhpMyAdmin' podrán acceder a ella.
Puedes activar este acceso en el momento de crear nuevos usuarios, o editando el perfil de usuarios ya existentes.  

![Screenshot](img/apache-access.png)  

## Primera contraseña  

Cuando se accede a la aplicación PhpMyAdmin, se muestra la primera autentificación con una ventana emergente. En este primer formulario se tienen que insertar las credenciales user/password de un usuario que tenga activado el servicio 'Acceso Aplicación PhpMyAdmin' (ojo, no se trata del user/password de un usuario mysql para una base datos o el usuario root de mysql, ese es el siguiente paso).  

![Phpmyadmin private area](img/private-area-phpmyadmin.png)

## Segunda contraseña  
Una vez efectuada satisfactoriamente esta autentificación, se muestra la interfaz de la aplicación PhpMyAdmin, que solicitará un usuario Mysql. Por defecto exite un usuario Mysql cuyo nombre es root y cuya contraseña está incluida en el correo electrónico que se envia en el momento de activar el servidor, junto con las otras contraseñas y que puedes utilizar para acceder a la aplicación.  

![Phpmyadmin](img/phpmyadmin.png)

Es muy recomendable cambiar la contraseña del usuario root. Puedes hacerlo desde la misma aplicación :

![Phpmyadmin change password ](img/phpmyadmin-chpswd.png)   


Además es buena práctica crear un usuario Mysql diferente por cada base de datos y otorgarle permisos solo sobre una y no todas las bases de datos que tengas creadas.

Tanto las bases de datos como los usuarios mysql y sus contraseñas se pueden crear e administrar desde PhpMyadmin.  
Por defecto solo el usuario root de Mysql tiene los privilegios necesarios para crear nuevas bases de datos, nuevos usuarios, y otorgar permisos a cada uno de ellos.  

Puedes encontrar aquí la documentación oficial para el uso de la aplicación  

[https://www.phpmyadmin.net/docs/](https://www.phpmyadmin.net/docs/)
