# Etherpad   

Etherpad-lite es una aplicación externa al Panel de Control que permite la edición colaborativa de documentos online (Pads) en tiempo real y entre múltiples usuarios. 
Los servidores creados con MaadiX incluyen por defecto, junto con esta aplicación, una extensión que permite habilitar áreas de trabajo privadas. De esta manera se puede elegir si los documentos creados son accesibles al público en general o solo a los usuarios que tengan una cuenta activada.  


# Etherpad admin

La aplicación Etherpad-lite incluye un panel propio de administración que permite:

* Editar preferencias  
* Instalar/desinstalar plugins  
* Reinicar la aplicación  

El área de administración de la aplicación está disponible en la dirección:
    https://*minombreenmaddix*.maadix.org/etherpad/admin/

o si tienes un dominio porpio activado en el servidor:  
    https//*midominio*.com/etherpad/admin/  

Para poder acceder a esta área tendrás que insertar el nombre de administrador y la contraseña de la aplicación (estos datos están incluidos en el mail de activación del servidor, junto con las otras contraseñas). 

El usuario admin solo puede acceder a esta área en la que tiene accesso a todos los grupos y usuarios creados en el sistema.  Su contraseña no es válida para operar desde el front-end.

## Cambiar contraseña de administardor  

Una vez dentro del área de administrador, es recomendable que cambies la contraseña.  Para ello, haz click en la pestaña 'Settings' del menú de la izquiera.  
Se abrirá un archivo en texto plano que contiene todos los parámetros de tu instalación.  
Haz scroll hasta el final de este archivo, donde encontrarás unas líneas parecidas a las siguientes:

      "users": {
        "admin": {
        "password": "**yourpasswordhere**",
        "is_admin": true
        }
      }

1 - Cambia el valor del password por tu nueva contraseña, teniendo cuidado de ponerlo entre las comillas    
2 - Haz click en 'Save Settings'  
3 - Haz Click en 'Restart Etherpad'  
 
![Change etherpad password] (img/ch-paswd.png)  


# Etherpad Área Privada 

MaadiX ha desarrollado un plugin de etherpad-lite que permite crear espacios privados de trabajo, y que por defecto se instala junto con la aplicación.  
Desde el área de administración de etherpad-lite se pueden establecer preferencias de configuración para la instalación.  
Haciendo click en la pestaña 'Users and groups' de la columna izquierda aparecerán las siguientes opciones:  


* Allow users to recover lost password - Activar esta opción permitirá a los usuarios recuperar su contraseña. En general es aconsejable dejarla activada, ya que esto permite a los usuario restablecer por sí mismos su contraseña si la pierden, evitando tener que enviarla por email u otro canal.   

* Allow users to register - Si esta opción está activada cualquier persona podrá crearse una cuenta sin necesidad de recibir una invitación. De lo contrario solo los usuarios con una invitación válida podrán acceder a la aplicación.  
  
* Allow public pads - Pemite crear pads públicos sin necesidad de tener un usuario activado, ni pertenecer a ningún grupo. Los grupos y pads privados siguen estando disponibles aunque esta opción esté activada. Si se quiere evitar que cualquier persona pueda crear nuevos pads en la instalación se puede desactivar.    



## Crear usuarios  
 
Desde el área de administrador puedes crear grupos e invitar usuarios. Si has elegido no permitir que los usuarios se registren sin invitación tendrás que crear almenos una cuenta. El susuario así creado podrá empezar a administrar grupos desde el front-end de la aplicación.  Recuerda que las credenciales del usuario administrador no son válidas para operar desde el front-end.   

Para crear grupos e invitar usuarios desde el área de administrador haz click en las pestañas 'Manage Groups' o 'Manage User' que encuentras en la cabecera de la sección 'Users and groups' de la columna izquierda (página principal del plugin).

## Etherpad front-end

Los usuarios que tengan una cuenta activada pueden administrar grupos, invitar otros usuarios, crear y editar documentos (pads) desde el front-end. 

El front-end de la aplicación está disponible en la dirección:
    https://*minombreenmaddix*.maadix.org/etherpad/

o si tienes un dominio porpio activado en el servidor:
    https://*midominio*.com/etherpad/

Para acceder a el área privada hay que indentificarse haciendo click en 'Login' En la parte superior derecha de la página.

### Grupos  

Los pads privados y los usuarios deben estar asociados a un grupo.  
Un mismo usuario puede pertenecer a uno o más grupos además de poder crear uno propio.  
Si un usuario no pertenece a ningún grupo tendrá que crear uno antes de poder crear documentos o invitar nuevos usuarios.   

 Se pueden consultar los grupos a los que se tiene acceso o crear nuevos haciendo click en 'My groups', una vez entrados en la aplicación (Login).  

#### ¿Cómo crear un grupo privado?  

En "Create a new Private Group" (Crear un nuevo grupo privado) inserta un nombre de grupo (este nombre no debe existir aún en el sistema) y haz clic en el botón "Create" (Crear). El nuevo grupo aparecerá en la misma página. Hecho esto, podrás empezar a invitar otros usuarios o crear nuevos documentos.  

### Invitar Usuarios  

Para agregar / invitar  usuarios a un grupo, haz clic en "View / Add Users" (Ver / Agregar usuarios) desde la tabla de la página "My groups". En el campo "Invite user to this group" (Invitar usuario a este grupo) inserta una dirección de correo electrónico válida del usuario que quieras crear. Si  la dirección insertada no está registrada todavía en el sistema, se enviará un correo electrónico de confirmación al nuevo usuario con las instrucciones para activar la cuenta. También deberás elegir el rol que deseas asignar al nuevo usuario para este grupo.  

### Roles

El rol asignado a un usuario sólo se aplica al grupo actual. Un usuario puede tener acceso a varios grupos con diferentes roles en cada uno de ellos. Si un usuario crea un nuevo grupo, su rol para dicho grupo será 'Admin'.

Un usuario nunca puede asignar un rol más alto que su propio rol dentro del grupo actual.

Los roles disponibles son:

    **Usuario**: Puede crear y editar Pads
    **Editor**: Puede crear / editar / borrar Pads e invitar / quitar Usuarios
    **Admin**: Puede crear / editar / borrar Pads, invitar / eliminar Usuarios y borrar todo el grupo

El nuevo usuario invitado aparecerá en la tabla de abajo. El rol asignado al usuario se puede modificar y editar más tarde.  

### ¿Cómo crear un pad privado?  

Los Pads se deben crear desde la página de la lista de Pads de un grupo específico, ya que cada pad solo puede pertenecer a un grupo determinado. Para crear un nuevo pad haz click en "View/Add Pads" (Ver / Agregar Pads) en la tabla de la página "My groups".  En la nueva página que se abre inserta el nombre del pad que quieres crear en el campo "Add a Private Pad to this Group" (Crear Pad Privado para este grupo) y haz clic en el botón "Create" (Crear). El nuevo pad aparecerá en la tabla de abajo.  

El nombre del pad debe ser único para cada grupo.  

### Visitar Pads existentes  

Para abrir un pad ya creado haz click en "View/Add Pads" (Ver / Agregar Pads)  en la tabla de la página "My groups" en la línea correspondiente al grupo en el que el documento fue creado. Encontrarás un listado de todos los pads ordenados por fecha de última edición del grupo seleccionado.  
Puedes invertir este orden para que se muestren las ediciones más antiguas primero, o reordenar el listado por orden alfabético utilizando las flechas de las columnas correspondientes.  

Puedes encontrar aquí la documentación oficial de la aplicación Etherpad-Lite 

[https://github.com/ether/etherpad-lite/wiki](https://github.com/ether/etherpad-lite/wiki)
