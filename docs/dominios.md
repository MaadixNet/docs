# Configuración de dominios en MaadiX

## Consigue tu dominio

Toda web o aplicación necesita un buen dominio. Si tienes un dominio propio, MaadiX te permite fácilmente activarlo y configurarlo para usarlo en tus aplicaciones.

Si aún no dispones de dominio propio, aquí te dejamos un par de proveedores de ejemplo donde puedes registrarlo (hay muchísimos más [1]):

* [gandi.net](https://www.gandi.net/)
* [namecheap.com](https://www.namecheap.com/domains/registration.aspx)

Elegir un buen nombre no siempre es fácil. Mientras decides cual va a ser tu domino, puedes seguir usando MaadiX y la mayoría de sus aplicaciones usando tu *subdominio.maadix.org*, donde 'subdominio' coincide con el nombre que elegiste al adquirir tu servidor MaadiX (*no obstante, solo podrás configurar y usar el servidor de correo electrónico y las listas de correo si dispones de dominio propio activado*).

Si ya dispones de dominio propio sigue las instrucciones a continuación para activarlo.

## Activa tu dominio

Desde tu Cpanel entra en la pestaña '**Dominios**' y haz click en '**Añadir dominios**'. 

Se desplegará un formulario con los siguientes campos:

* **Nombre de dominio**:  introduce el nombre de tu dominio (o subdominio) completo (por ejemplo: example.com o docs.example.com)

Para cada dominio o subdominio que actives se creará una carpeta en tu servidor del tipo`/var/www/html/example.com/`. Debes subir tu web o aplicación a esta carpeta para que sea accesible desde el navegador visitando *example.com*

* **Activar servidor de correo para este dominio**: Si quieres usar el servidor de correo interno para el dominio que estás creando esta opción tiene que estar activada. Si de lo contrario quieres que el correo electrónico sea gestionado por otro servidor esterno dejala desactivada. 
Podrás cambiar esta opción en cualquier momento desde la página de edición del dominio

* **Webmaster**: A cada dominio o subdominio que actives en MaadiX puedes asignarle un (Webmaster) (Administrador Web).  
  
El Webmaster tendrá permisos para crear, borrar o modificar archivos dentro de la carpeta `/var/www/html/example.com/`, donde podrá crear la aplicación web. Este usuario tendrá acceso por SFTP a esta carpeta y a su home, pero no podrá acceder ni ver el resto archivos y carpetas en tu servidor.

Si no asignas ningún usuario como Webmaster, se establecerá por defecto como Webmaster el SuperUsuario del sistema.

Recomendamos encarecidamente que crees un usuario Webmaster, sobretodo si quieres compartir con alguien el acceso para que trabaje sobre la web, aplicación o contenidos de la carpeta `/var/www/html/example.com/`, y que nunca compartas el acceso como SuperUsuario, cuyos privilegios son ilimitados.


![Screenshot](img/add-domain.png) 



## Configura los DNS de tu dominio para que apunten a tu servidor

Ya has configurado tu servidor para que trabaje con tu dominio propio *example.com*. Sin embargo, para que todo funcione necesitas, por otro lado, decirle a tu dominio propio que apunte a tu servidor en MaadiX :) 

Tu servidor incluye un sistema que comprueba automáticamente si tu dominio está apuntando correctamente a tu servidor. En caso afirmativo el mismo stema procederá con la creación de todas las configuraciones necesarias. En caso contrario volverá periódicamente a hacer la misma comprobación hasta conseguir una respuesta afirmativa. Para saber si el proceso de activación y configuración del dominio ha terminado con éxito consulta en la sección **Ver Dominios** la columna "Activado". 
![Screenshot](img/dominio-pendiente.png) 

Para apuntar tu dominio hacia tu servidor debes modificar sus DNS. Los servidores DNS (Systema de Nombre de Dominios) son los que transforman los nombres de dominio, amigables para comprensión huma, en números que corresponden a las direcciones IP de las diferentes máquinas conectadas y accesibles públicamente en Internet.

Haciendo click en "Ver" en la columna DNS de tu dominio (ver captura de pantalla anterior), encontrarás las configuraciones requeridas para que tu dominio funcione tanto para tu aplicación web (Registro A) como para tu servidor de correo (Registro MX). 

![Screenshot](img/configuracion-requerida-dominio.png) 

Debes introducir estos datos en la sección correspondiente a la configuración de DNS dentro del **área de cliente de tu proveedor de dominio** (este paso es fuera de tu servidor MaadiX). Seguramente habrá un enlace o pestaña, quizás en el menú, que diga algo como *DNS* , *Editar registros DNS* o *Editar zona DNS*.

Una vez hechos los cambios, vuelve a consultar la ṕagina de configuración de DNS en el Panel de Control de tu servidor Maadix (Haciendo click en "Ver" en la columna DNS).  
Recuerda que el proceso de propagación de los nuevos DNS puede tardar hasta 48 horas , por lo que es normal que durante un tiempo la configuración siga resultando incorrecta.  

## HTTPS

Todos los dominios que actives a través del panel de control tendrán activado un certificado SSL y serán accesibles a través de la dirección  

https://tudominio.com

La creación y configuración de los certifcados está automatizada y se completa junto con todo el proceso de activación y configuración de dominios en tu sistema utilizando [Let`s Encrypt](https://letsencrypt.org).  

No  necesitas aplicar ninguna configuración adicional para activar https para tu dominio.  



## Subir tu web o aplicación al dominio propio

Una vez aparezca el check verde en la columna "Activado" ya puedes subir los archivos de tu aplicación web a la recién creada carpeta `/var/www/html/example.com/`. Puedes hacerlo muy fácilmente con un cliente SFTP (por ejemplo [Filezilla](https://filezilla-project.org/)). Una vez estén ahí, podrás visitarlos desde el navegador en tu dominio *example.com*.

**Nota**: Si has estado trabajando en una web o aplicación dentro de la carpeta en tu servidor `/var/www/html/subdominio.maadix.org/`, que visitas a través de tu *subdominio.maadix.org* y ahora te gustaría trasladarla a tu dominio propio recién activado, debes mover el contenido de esta carpeta a la nueva carpeta nueva `/var/www/html/example.com/`. Hecho esto, podrás visitar tu web o aplicación desde el navegador a través de tu dominio propio *example.com* (es posible que haya que cambiar también alguna configuración de tu web o app).

Puedes encontrar más indicaciones aquí: [Crea tu web o aplicación](create-web)


## Empieza a usar tu servidor de correo

Si has activado la casilla 'Activar servidor de correo para este dominio',  puedes empezar a usar tu servidor de correo electrónico. Entra en el apartado *Email -> Cuentas mail* para abrir nuevas cuentas de correo *usuario@ejemplo.com*.  
Recuerda que los registros MX tienen que estar correctamente configurados para que apuntien a tu servidor

Puedes encontrar más indicaciones aquí: [Crea y gestiona cuentas de correo](email)


----

[1] Listado completo de las empresas registradoras de dominios acreditadas por el ICANN: [Ver listado](https://www.icann.org/registrar-reports/accredited-list.html)
