# Registra tu dominio

Toda web o aplicación necesita un buen dominio. Si tienes un dominio propio, MaadiX te permite fácilmente activarlo y configurarlo para usarlo en tus aplicaciones además del *subdominio.maadix.org* que hayas elegido para tu servidor.

Si aún no dispones de dominio propio, aquí te dejamos un par de proveedores de ejemplo donde puedes registrarlo (hay muchísimos más\*):

* [gandi.net](https://www.gandi.net/)
* [namecheap.com](https://www.namecheap.com/domains/registration.aspx)

Elegir un buen nombre no siempre es fácil. Mientras decides cual va a ser tu domino, puedes seguir usando MaadiX y la mayora de sus aplicaciones a través de tu *subdomio.maadix.org*. No obstante, necesitarás tener un dominio propio para poder configurar y usar el servidor de correo electrónico y las listas de correo.

Si ya dispones de dominio propio sigue las instrucciones a continuación para activarlo en MaadiX.

## Activa tu dominio en MaadiX

Desde tu Cpanel entra en la pestaña '**Dominios**' y haz click en '**Añadir dominios**'. 

Se desplegará un formulario con los siguientes campos:

* **Nombre de dominio**:  introduce el nombre de tu dominio (o subdominio) completo (por ejemplo: example.com o docs.example.com)

Para cada dominio o subdominio que actives en MaadiX se creará una carpeta */var/www/html/example.com/*. Debes subir tu web o aplicación a esta carpeta para que sea accesible desde el navegador visitando *example.com*

* **Webmaster** (Administrador sito Web): A cada dominio o subdominio que actives en MaadiX puedes asignarle un Administrador Web (Webmaster).  
  
El Administrador Web tendrá permisos para crear, borrar o modificar archivos dentro de la carpeta */var/www/html/example.com/*, donde podrá crear la aplicación web. Este usuario tendrá acceso por SFTP o SSH a esta carpeta, pero no podrá acceder ni ver el resto archivos y carpetas en tu servidor.

Si no asignas ningún usuario como Administrador Web, se establecerá por defecto como Webmaster el SuperUsuario del sistema.

Si quieres compartir con alguien el acceso para que trabaje sobre la web, aplicación o contenidos de la carpeta */var/www/html/example.com/*, te recomendamos encarecidamente que crees un usuario Webmaster para ello y que nunca compartas el acceso como SuperUsuario, cuyos privilegios son mucho mayores y resulta peligroso.

### Subir o migrar tu web o applicación al dominio propio

Ahora ya puedes subir los archivos de tu web o aplicación web a la recién creada carpeta */var/www/html/example.com/*. Puedes hacerlo muy fácilmente con un cliente SFTP (por ejemplo [Filezilla](https://filezilla-project.org/) o por SSH. Una vez estén ahí, podrás visitarlos desde el navegador en tu dominio *example.com*.

**Nota**: Si has estado trabajando en una web o aplicación dentro de la carpeta en tu servidor */var/www/html/subdominio.maadix.org/*, que visitas a través de tu *subdominio.maadix.org* y ahora te gustaría trasladarla a tu dominio propio reción activado, debes mover el contenido de esta carpeta a la nueva carpeta nueva */var/www/html/example.com/*. Hecho esto, podrás visitar tu web o aplicación desde el navegador a través de tu dominio propio *example.com* (es posible que haya que cambiar también alguna configuración de tu web o app).

Puedes econtrar más indicaciones aquí:  
[Crear Web](create-web)

======
Necesitamos screenshots nuevos!

![Screenshot](img/activar-dominio.png) 

El sistema puede tardar hasta 5 minutos en completar la nueva configuración. Para saber si el proceso ha terminado refresca la página 'Dominios' y averigua que la columna 'Status' tenga el check verde

![Screenshot](img/statusok.png)  
======


## Configura los DNS de tu dominio para que apunten a tu servidor en MaadiX

Ya has configurado tu servidor MaadiX para que trabaje con tu dominio propio *example.com*. Sin embargo, para que todo funcione necesitas, por otro lado, decirle a tu dominio propio que apunte a tu servidor en MaadiX :) 

Para ello debes modificar los DNS de tu dominio. Los DNS (Domain Name Servers) son los que transfomarman los nombres de dominio, amigables para comprensión huma, en números que corresponden a las direcciones IP de las diferentes máquinas conectadas y accesibles públicamente en internet.

Para configurar los DNS de tu dominio debes entrar en la sección correspondiente dentro del **área de cliente de tu proveedor de dominio** (este paso es fuera de MaadiX).

Una vez dentro introduce las configuraciones requeridas que encontrarás en tu Cpanel de Maadix dentro de la pestaña **Ver Dominios**.

Una vez introducidos los cambios, refresca la sección **Ver Dominios** en MaadiX para que compruebe otra vea que la configuración de los DNS de tu dominio es correctaa.

----

\* Listado completo de las empresas registradoras de dominios acreditadas por el ICANN: [Ver listado](https://www.icann.org/registrar-reports/accredited-list.html)
