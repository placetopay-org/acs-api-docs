<!--
type: tab
title: Roles
-->

# Roles

Para acceder a este módulo, dírijase al menú ubicado en la parte lateral izquierda, y despliegue la opción de *Seguridad*, luego seleccione el título *Roles*.

![](https://wiki.placetopay.com/images/b/b6/Acs-security-menu.png)

## Índice de roles:

En este módulo se gestionan los roles de usuario de la aplicación. Inicialmente se tiene una vista con la lista de roles creados, los cuales se pueden ver, editar y eliminar haciendo clic en las opciones del menú desplegable ubicado en la parte lateral derecha. 

![](https://wiki.placetopay.com/images/2/21/Acs-roles-index.png)

## ¿Cómo crear un nuevo rol?

Además, se pueden crear nuevos roles mediante el botón *Crear*, ubicado en la parte lateral derecha. Se debe diligenciar un nombre y opcionalmente una descripción para el mismo.

![](https://wiki.placetopay.com/images/9/92/Acs-create-role.png)

## Funcionalidades para los roles:

En la parte inferior de los detalles de un rol se puede visualizar una sección con tres pestañas que direccionan a tres funcionalidades diferentes:

### 1. Permisos:

Al dar clic en la opción *Ver* de un rol, se presentarán los detalles del rol seleccionado y en la parte inferior de la pantalla encontrará un menú como el siguiente:

![](https://wiki.placetopay.com/images/c/c5/Acs-permissions.png)

Aquí se pueden buscar permisos referentes a diversas funcionalidades de ACS, seleccionarlos, denegarlos y concederlos. Estos permisos determinan las funcionalidades y acciones a las cuales tiene acceso el rol.
Además, se pueden conceder y denegar otros roles al actual.

### 2. Roles ancestros:

Aquí registran los roles que están utilizando el rol actual. Esto puede darse cuando se le concede un rol a otro rol en el menú de *Permisos*. 

> Al crear roles hijos, se permite extender funcionalidades y permisos de un rol padre sin necesidad de volver a asignar una lista de permisos.

### 3. Usado por:

En esta sección se listan los usuarios que usan el rol que seleccionó.

<!--
type: tab
title: Perfiles
-->

# Perfiles

Para acceder a este módulo, dírijase al menú ubicado en la parte lateral izquierda, y despliegue la opción de *Seguridad*, luego seleccione el título *Perfiles*.

![](https://wiki.placetopay.com/images/b/b6/Acs-security-menu.png)

## Índice de perfiles:

Los roles se asocian con los perfiles. El siguiente es un ejemplo de un índice de perfiles.

Para acceder a este módulo, el usuario con los permisos necesarios para crear los perfiles, ingresa a través del menú despegable ubicado en la izquierda del panel, en la pestaña de seguridad.

Al ingresar al módulo, la plataforma muestra una tabla con los campos del nombre, descripción, rol y fechas de creación y actualización del perfil.

![](https://wiki.placetopay.com/images/c/c2/Acs-profiles-index.png)

## Acciones para los perfiles:

Cada perfil cuenta con unas opciones para ser gestionado como son la opción de ver, editar o deshabilitar.

![](https://wiki.placetopay.com/images/9/95/Acs-options-profile.png)

- **Opción *Ver*:** Permite visualizar una información más detallada del perfil como son el nombre, si es un perfil compartido o no, la fecha de creación, actualización, y el usuario que lo creó, al igual que los permisos que el perfil tiene a disposición o los que desea agregar. 

Un ejemplo de una vista de detalle de un perfil es el siguiente:

![](https://wiki.placetopay.com/images/1/1a/Acs-detail-profile.png)

- **Opción *Editar*:** Permite actualizar el nombre, descripción, rol y la opción de compartido.

> Es importante tener en cuenta que un perfil no se puede eliminar, ya que existen actividades que se hanrealizado en nombre de ese perfil y si se pudiera eliminar, se puede producir un error. Por esta razón, la aplicación tiene la opción de deshabilitar el perfil para denegar el acceso.


## ¿Cómo crear un nuevo perfil?

Para crear un nuevo perfil se solicitará:

- Nombre para el perfil.
- Descripción (opcional).
- Rol, debe seleccionar el rol que se asociará al perfil.
- Compartido, puede habilitar o deshabilitar esta opción. Un perfil compartido se da cuando el perfil está siendo utilizado por otros roles.

![](https://wiki.placetopay.com/images/5/5a/Acs-profile-create.png)


### ¿Qué es el ACL?

El ACL (Access Control List), es un módulo de gestión de permisos y reglas desarrollado en PlacetoPay y utilizado por ACS. Este se encarga de gestionar los permisos y accesos de los diferentes roles y perfiles creados en ACS. 

Estos permisos y reglas de acceso, se diferencian de los permisos básicos registrados en los roles, en que estos son más específicos y ofrecen una capa de seguridad extra a los datos manejados en la aplicación, ya que estos permisos permiten que se visualice la información que corresponde solo a un cliente en específico y que no se filtre otra información que pertenece a otros clientes u organizaciones.

La lista de reglas se puede visualizar en el detalle de un perfil, en una vista similar a la siguiente:

![](https://wiki.placetopay.com/images/c/c4/Acs-acl-list.png)

### ¿Cómo crear reglas ACL?

Para crear una regla ACL, haga clic en el botón *Crear*, se presentará un formulario como el siguiente:

![](https://wiki.placetopay.com/images/c/cf/Acs-acl-create.png)

#### Información general:

Las reglas tienen dos opciones disponibles:
- Permitir accesos
- Denegar accesos

En el campo entidad, debe seleccionar el la entidad que gestional el módulo al cual quiere aplicarle las condiciones que va a crear.

#### Condicionales:

- Atributo: Seleccione el campo correspondiente a la entidad seleccionada previamente y al cual desea validar.

- Operador: Permite hacer las comparaciones de los datos.

- Valor: Ingrese uno o varios valores que debería contener el atributo seleccionado.

<!--
type: tab
title: Logs
-->

# Logs de Seguridad

Para acceder a este módulo, dírijase al menú ubicado en la parte lateral izquierda, y despliegue la opción de *Seguridad*, luego seleccione el título *Logs*.

![](https://wiki.placetopay.com/images/b/b6/Acs-security-menu.png)

## Índice de logs:

En esta sección se registran los movimientos y actualizaciones que se realizan en la aplicación de ACS. Los logs permiten tener un control de los cambios y de lo que sucede en la aplicación. 
En la sección de logs se encuentra un listado de los mismos,con una descripción, la fecha y hora en que fue registrado el movimiento. 

Un ejemplo de un índice de logs es el siguiente:

![](https://wiki.placetopay.com/images/3/3d/Acs-logs-index.png)

### Acciones para los logs:

Para visualizar las acciones disponibles para el listado de los logs, haga clic en el menú ubicado en la parte superior lateral derecha y se desplegarán las siguientes acciones:

- **Eliminar:** Esta opción eliminará toda la lista de logs registrados. 

- **Reportes:** Redirecciona al listado de reportes de logs que se han exportado.

- **Exportar:** Exportará un documento en el cual registran todos los logs listados.

![](https://wiki.placetopay.com/images/1/10/Acs-logs-actions.png)

### Detalles de un log:

Puede visualizar los detalles de cada log haciendo clic en el botón *Ver*, ubicado al final de cada registro. Allí puede visualizar el usuario que realizó el movimiento, la dirección IP, el sistema operativo y un detalle del cambio con un antes y después.

![](https://wiki.placetopay.com/images/9/91/Acs-logs-detail.png)

### Filtros:

Para hacer búsquedas de los logs registrados utilice la sección de filtros. Haga clic en el botón *Filtros*, ubicado en la parte lateral izquierda, se desplegará un módulo para filtrar por rango de fechas y por el correo electrónico del usuario que realizó el cambio o movimiento:

![](https://wiki.placetopay.com/images/b/bb/Acs-logs-filters.png)


<!-- type: tab-end -->