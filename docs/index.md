# Tutoriales y documentación 

Documentación completa sobre el uso de MaadiX.

[Web oficial de MaadiX](https://maadix.net/)  

En esta página encontrarás la documentación completa sobre el uso de MaadiX, que comprende indicaciones, tutoriales detallados de cada herramienta y soluciones a problemas que se suelen plantear.

# ¿Qué es MaadiX?

MaadiX es una herramienta que te permite habilitar con un clic aplicaciones de código abierto en un servidor propio. Además, las puedes administrar a través de una interfaz gráfica sin necesidad de **conocimientos técnicos** o **grandes inversiones**.

# ¿Cómo funciona?

MaadiX integra una serie de configuraciones de sistema estandarizadas, que permiten a los usuarios administrar servidores virtuales propios y aplicaciones desde una interfaz gráfica fácil e intuitiva. Permite instalar aplicaciones avanzadas como OpenVPN, Etherpad, servidor de correo, Mailman, Let's Encrypt u Owncloud entre otras, todo en un simple clic. Con MaadiX, podrás disponer de una nube propia independiente, privada y segura.

# Panel de Control

El panel de control es la interfaz que permite ejecutar distintas tareas de administración y mantenimiento sin necesidad de ejecutar comandos en la terminal. Las tareas que se pueden llevar a cabo a través del panel de control son tareas avanzadas, que normalmente requerirían altos privilegios en el sistema. Sin embargo, por cuestiones de seguridad, el panel de control no dispone de estos privilegios. [Saber más](https://docs.maadix.net/panel-de-control/).

# Los datos

Todos los servidores tienen instalado un directorio donde se almacenarán los datos de usuarios, dominios, cuentas de correo electrónico y aplicaciones (técnicamente hablando, se trata de un directorio LDAP).
El panel de control es la interfaz gráfica para administrar este directorio, y el sistema sacará del mismo la información necesaria para su configuración. De esta forma, el panel de control no necesita los privilegios necesarios para escribir directamente esta información en el sistema.

