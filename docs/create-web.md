# Crea tu web o aplicación

## Elige tu dominio

Para poder crear un sito web accesible desde cualquier navegador necesitarás un dominio o subdominio. 

Si tienes un dominio propio, MaadiX te permite fácilmente activarlo y configurarlo para usarlo en tu página web y aplicaciones. Si todavía no has activado tu dominio en MaadiX, puedes encontrar las instrucciones sobre como proceder aquí: [Activar mi Dominio](dominios.md)

Alternativamente, si no dispones de dominio propio, puedes usar tu *subdominio.maadix.org*, donde 'subdominio' coincide con el nombre que elegiste al adquirir tu servidor MaadiX. Deberás crear tu web o aplicación dentro de la carpeta */var/www/html/subdominio.maadix.org* y visitarlo desde en el navegador con tu *subdominio.maadix.org*.

En el siguiente tutorial se describe el proceso en caso de utilizar un dominio propio. Sin embargo, el proceso es el mismo para un *subdominio.maadix.org* si se tiene en cuenta el párrafo anterior.

## Subir contenidos

Una vez tengas [activado el dominio](dominios.md) para tu nuevo sito web, tendrás que subir los archivos de tu aplicación a la carpeta que se encuentra en */var/www/html/midominio.com*.   

Puedes acceder a esta ubicación y subir los archivos fácilmente utilizando un cliente SFTP (Secure File Transfer Protocol). Si no tienes ningún cliente SFTP instalado y no sabes cual escoger, [Filezilla](https://filezilla-project.org/) es uno de los más usados y sencillos.

El cliente SFTP te pedirá una serie de credenciales para conectar con el servidor:

#### Como usuario Webmaster  

Si al activar tu dominio le has asignado un usuario Webmaster específico (lo cual recomendamos), éste será el propietario de la carpeta */var/www/html/midominio.com* y solo él podrá modificar los archivos en ella.

Las credenciales para la conexión con el usuario Webmaster son:

* **Servidor**: tu *subdomino.maadix.org*
* **Protocolo**: SFT/SSH  
* **Modo de acceso**: Normal  
* **Usuario**: El nombre del usuario Webmaster
* **Contraseña**: La contraseña que has establecido para este usuario

![Screenshot](img/sftp-anna.png)

Cuando se establezca la conexión el usuario Webmaster verá na carpeta con su nombre. En ella encontrará una carpeta que le da acceso a */var/www/html/midominio.com*, o varias si es Webmaster de otros dominios a parte de este.

También puede tener ahí otros archivos propios que haya subido o creado anteriormente. Los usuarios Webmaster solo tienen acceso a esta zona y no a todos los archivos del sistema como tiene el Superusuario. 

<a id="domain-folder"></a>
#### Dentro de la carpeta */var/www/html/midominio.com* 

Dentro de la carpeta */var/www/html/midominio.com* hay dos elementos: Una carpeta con nombre .well-known y un archivo index.html.  

La carpeta .well-known es necesaria para la conexión segura a la web (https) y no debes tocarla (*si no puedes ver la carpeta .well-known, no te preocupes. El punto delante del nombre significa que es un archivo oculto, está ahí pero Filezilla, o tu cliente SFTP, está configurado para no mostrar los archivos ocultos*).  

![Screenshot](img/sftp-midominio.png)

El archivo index.html es un archivo tipo *placeholder* que se crea en el proceso de activación del dominio y sirve para comprobar que la activación del dominio se ha completado con éxito. Si vistas desde un navegador tu dominio antes de haber subido tus propios archivos, encontrarás la página de bienvenida de este archivo index.html.  

[Screenshot de la bienvenida]

Así pues, puedes ahora borrar (o sobrescribir) este archivo index.html existente y **subir aquí los archivos de tu web o aplicación**. 

# Como Superusuario de sistema 

Si no has creado ningún usuario webmaster para tu nuevo dominio, el propietario de la carpeta web en */var/www/html/midominio.com* será tu Superusuario de sistema.

Puedes establecer connexión por SFTP como tu Superusuario con las credenciales:

* **Servidor**: tu *subdomino.maadix.org*
* **Protocolo**: SFT/SSH  
* **Modo de acceso**: Normal  
* **Usuario**: El nombre del Superusuario
* **Contraseña**: La contraseña del Superusuario

Si no recuerdas tus datos de Superusuario, puedes consultarlos en la pestaña **usuarios** de tu Cpanel. Es el primero que aparece en la lista. También puedes ahí restablecer su contraseña en caso de que la hayas olvidado.

El Superusuario tiene altos  privilegios y acceso a todo el sistema. Cuando estableces la conexión SFTP al servidor como Superusuario, la ubicación en la que te encuentras al inicio de sesión es la carpeta personal en */home/nombre_del_superusuario/*.

Deberás navegar a través de las carpetas hasta llegar a */var/www/html/midominio.com*, que es donde tendrás que subir o crear los archivos de tu nueva web o aplicación. Otra opción más rápida es escribir la ruta */var/www/html/midominio.com* en el campo "Sitio remoto".


Una vez ahí puedes seguir los mismos pasos descritos para usuario [Webmaster](#domain-folder)

![Screenshot](img/sftp-midominio.png)

