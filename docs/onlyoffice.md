# Only Office   

Only Office es una aplicación que, como Libre Office Online, proporciona la posibilidad de editar de forma colaborativa y en tiempo real, documentos en un navegador.

Constituye una alternativa a Google Docs, y permite editar documentos de texto enriquecido, hojas de cálculo y presentaciones. Por defecto utiliza el formato .docx, pero se pueden habilitar otros formatos para archivos creados fuera de la aplicación y subidos a nuestra instalación (.odt, .doc, .docx, .ods, xls, .xlsx, .odp,.ppt, .pptx...).  


Para utilizarla se necesita también una instalación de Nextcloud/Owncloud, que será el interfaz que permitirá acceder a la edición de los documentos.  
Con Only Office, los documentos almacenados en Nextcloud/Owncloud, se abrirán en el navegador para su lectura/edición, en lugar de mostrarse por defecto la opción de descarga.  


## Instalación  

Antes de proceder con la instalación es necesario decidir bajo qué dominio o subdominio se quiere alojar la aplicación. Usaremos como ejemplo el subdominio onlyoffice.maydomain.com.  

Tendremos que crear una entrada DNS de tipo A, que apunte a la IP del servidor.

 `onlyoffice.maydomain.com A IP.DE.TU.SERVIDOR`  

Según el proveedor de dominio que tengas, la propagación de los DNS puede tardar entré pocos minutos y unas horas. Una vez los DNS estén propagados podrás proceder a la instalación desde el panel de control.  

Al hacer clic en Only Office, desde la página 'Instalar aplicaciones', se abrirá una ventana emergente, en la que tendrás que insertar el nombre del dominio/subdominio que quieras utilizar para instalar la aplicación. En el caso de nuestro ejemplo será onlyoffice.maydomain.com

![Screenshot](img/onlyoffice/install-oo.png)


## Conectar Nextcloud / Owncloud

Una vez terminado el proceso de instalación de Only Office, es necesario instalar y configurar la extensión Only Office desde Nextcloud. Para activarla, visita la sección Apps -> Office & Text, como administrador de Nextcloud.

![Screenshot](img/onlyoffice/install-oo-nc.png)

Una  vez activada tendrás que ir a Configuración -> Only Office e insertar dos valores:

- La url de instalación de la aplicación con 'https://'. En el caso de nuestro ejemplo 'https://onlyoffice.maydomain.com'.  
- La clave secreta que autorizará tu instalación de Nextcloud a conectar con el servidor Only Office. Esta clave está incluida en el correo electrónico que tu servidor ha enviado a la cuenta de administrador del panel de control, una vez terminada la instalación.


En esta misma página podrás también establecer otras preferencias, como habilitar otros formatos para la edición de documentos.

![Screenshot](img/onlyoffice/onlyoffice-configure.png)

A partir de ahora, cada vez que accedas a un documento desde la sección Files/Archivos, se abrirá en el navegador para su edición.

