# Configuración de dominios en MaadiX

## Consigue tu dominio

Toda web o aplicación necesita un buen dominio. Si tienes un dominio propio, MaadiX te permite fácilmente activarlo y configurarlo para usarlo en tus aplicaciones.

Si aún no dispones de dominio propio, aquí te dejamos un par de proveedores de ejemplo donde puedes registrarlo (hay muchísimos más [1]):

* [gandi.net](https://www.gandi.net/)
* [namecheap.com](https://www.namecheap.com/domains/registration.aspx)

Elegir un buen nombre no siempre es fácil. Mientras decides cual va a ser tu domino, puedes seguir usando MaadiX y la mayoría de sus aplicaciones usando tu *subdominio.maadix.org*, donde 'subdominio' coincide con el nombre que elegiste al adquirir tu servidor MaadiX (*no obstante, solo podrás configurar y usar el servidor de correo electrónico y las listas de correo si dispones de dominio propio activado*).

Si ya dispones de dominio propio sigue las instrucciones a continuación para activarlo en MaadiX.

## Activa tu dominio en MaadiX

Desde tu Cpanel entra en la pestaña '**Dominios**' y haz click en '**Añadir dominios**'. 

Se desplegará un formulario con los siguientes campos:

* **Nombre de dominio**:  introduce el nombre de tu dominio (o subdominio) completo (por ejemplo: example.com o docs.example.com)

Para cada dominio o subdominio que actives en MaadiX se creará una carpeta */var/www/html/example.com/*. Debes subir tu web o aplicación a esta carpeta para que sea accesible desde el navegador visitando *example.com*

* **Webmaster**: A cada dominio o subdominio que actives en MaadiX puedes asignarle un (Webmaster) (Administrador Web).  
  
El Webmaster tendrá permisos para crear, borrar o modificar archivos dentro de la carpeta */var/www/html/example.com/*, donde podrá crear la aplicación web. Este usuario tendrá acceso por SFTP o SSH a esta carpeta y a su home, pero no podrá acceder ni ver el resto archivos y carpetas en tu servidor.

Si no asignas ningún usuario como Webmaster, se establecerá por defecto como Webmaster el SuperUsuario del sistema.

Recomendamos encarecidamente que crees un usuario Webmaster, sobretodo si quieres compartir con alguien el acceso para que trabaje sobre la web, aplicación o contenidos de la carpeta */var/www/html/example.com/*, y que nunca compartas el acceso como SuperUsuario, cuyos privilegios son mucho mayores.


![Screenshot](img/activar-dominio.png) 



## Configura los DNS de tu dominio para que apunten a tu servidor MaadiX

Ya has configurado tu servidor MaadiX para que trabaje con tu dominio propio *example.com*. Sin embargo, para que todo funcione necesitas, por otro lado, decirle a tu dominio propio que apunte a tu servidor en MaadiX :) 

Para ello debes modificar los DNS de tu dominio. Los DNS (Domain Name Servers) son los que transforman los nombres de dominio, amigables para comprensión huma, en números que corresponden a las direcciones IP de las diferentes máquinas conectadas y accesibles públicamente en Internet.

Para configurar los DNS de tu dominio debes entrar en la sección correspondiente dentro del **área de cliente de tu proveedor de dominio** (este paso es fuera de MaadiX).

Una vez dentro introduce las configuraciones requeridas que encontrarás en tu Cpanel de Maadix dentro de la pestaña **Ver Dominios**.

Una vez introducidos los cambios, refresca la sección **Ver Dominios** en MaadiX para que compruebe otra vea que la configuración de los DNS de tu dominio es correcta.

======
Screenshot de configuración requerida

![Screenshot](img/statusok.png)  

======


### Subir tu web o aplicación al dominio propio

Ahora ya puedes subir los archivos de tu web o aplicación web a la recién creada carpeta */var/www/html/example.com/*. Puedes hacerlo muy fácilmente con un cliente SFTP (por ejemplo [Filezilla](https://filezilla-project.org/)) o por SSH. Una vez estén ahí, podrás visitarlos desde el navegador en tu dominio *example.com*.

**Nota**: Si has estado trabajando en una web o aplicación dentro de la carpeta en tu servidor */var/www/html/subdominio.maadix.org/*, que visitas a través de tu *subdominio.maadix.org* y ahora te gustaría trasladarla a tu dominio propio recién activado, debes mover el contenido de esta carpeta a la nueva carpeta nueva */var/www/html/example.com/*. Hecho esto, podrás visitar tu web o aplicación desde el navegador a través de tu dominio propio *example.com* (es posible que haya que cambiar también alguna configuración de tu web o app).

Puedes encontrar más indicaciones aquí: [Crea tu web o aplicación](create-web)


----

[1] Listado completo de las empresas registradoras de dominios acreditadas por el ICANN: [Ver listado](https://www.icann.org/registrar-reports/accredited-list.html)
