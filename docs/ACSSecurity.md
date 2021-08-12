<!--
type: tab
title: Usuarios
-->

# Usuarios

Para acceder al módulo de usuarios, diríjase al menú lateral izquierdo, despliegue la opción *Seguridad* y busque la sección de *Usuarios* en los títulos.

![](https://wiki.placetopay.com/images/c/c8/Users-menu-2.png)

## Listado de usuarios:

En este módulo se puede visualizar el listado de usuarios con acceso a ACS. El listado contiene el nombre y el correo electrónico asociado al usuario.

> Es importante recordar que los usuarios se crean a través del módulo invitaciones y solo aparece en este módulo, cuando haya aceptado la invitación para unirse a ACS, creado el usuario y haya iniciado sesión sin conflicto alguno.

El siguiente es un ejemplo de un índice de usuarios.

![](https://wiki.placetopay.com/images/4/48/Users-index-2.png)

<!-- theme: warning -->

> Los usuarios no se pueden eliminar ni editar. Para hacer ediciones del correo electrónico de un usuario o la contraseña, se deben realizar en la aplicación de *Accounts*, que es quien gestiona los usuarios y accesos para ACS.


<!--
type: tab
title: Cuenta de usuario
-->

## Página de inicio 

La siguiente imagen muestra un ejemplo de una pantalla inicial, a esta vista se redirecciona el usuario cuando se loguea exitosamente en ACS. 

![](https://wiki.placetopay.com/images/9/9a/Home.png)

En esta vista encontrará:
 - Fecha y hora del último inicio de sesión.
 - Dirección IP, navegador y sistema operativo del dispositivo utilizado para la sesión.
 - Gráfica con datos del flujo transaccional del año anterior y el año actual.


# Gestión de cuenta

Para acceder al módulo de gestión de la cuenta de usuario,
haga clic en el menú desplegable que se encuentra al lado derecho del avatar de usuario con sus iniciales, ubicado en la parte superior derecha de la aplicación.

Visualizará un menú como el siguiente:

![](https://wiki.placetopay.com/images/6/6e/Account-menu.png)

El menú puede contener las siguientes secciones:

## Cuenta:

En esta parte registra el nombre de usuario y el correo electrónico, si se hace clic en esta sección, le llevará a una vista con los datos de su cuenta como la siguiente:

![](https://wiki.placetopay.com/images/3/33/Account-info-2.png)

- Para actualizar datos de la cuenta, haga clic en la opción *Administra tu cuenta*, ubicado en la parte inferior del avatar de usuario.

- Para visualizar los datos del perfil de la cuenta, haga clic en el nombre del perfil ubicado en la parte lateral derecha de la vista. 

## Perfiles:

Si tiene varios perfiles, al desplegar el menú se listarán todos y al hacer clic en un perfil específico, podrá cambiar el perfil con el que inició sesión previamente, por el perfil seleccionado.

## Sesión:

En esta sección encontrará el botón *Cerrar sesión*, para cuando desee salir de la aplicación.


<!--
type: tab
title: Invitaciones
-->

# Invitaciones de usuarios

Para acceder al módulo de invitaciones, diríjase al menú lateral izquierdo, despliegue la opción *Seguridad* y busque la sección de *Invitaciones* en los títulos.

![](https://wiki.placetopay.com/images/d/d6/Invitations-menu-2.png)

En este módulo se gestionan las invitaciones que realiza un usuario registrado en ACS a otro usuario u otro grupo de usuarios que desean utilizar la aplicación.

## Listado de invitaciones:

En este módulo se puede visualizar el listado de invitaciones creadas. El listado contiene el nombre de la invitación, el estado y las fechas de creación y actualización.

El siguiente es un ejemplo de un índice de invitaciones, con una invitación en estado *Aceptada*.

![](https://wiki.placetopay.com/images/f/fb/Invitations-index-2.png)

### Estados de las invitaciones:

Las invitaciones poseen dos estados:

- **Aceptada:** Una invitación adquiere este estado, cuando un usuario o el grupo de usuarios a los cuales se les envió, aceptaron la misma.

- **Pendiente:** Una invitación adquiere este estado, cuando un usuario o el grupo de usuarios a los cuales se les envió, no han aceptado la misma.

> Cuando la invitación fue enviada a varios usuarios, el estado se muestra con un indicador similar al siguiente, el cual muestra cuantas de las invitaciones enviadas, están en el estado específico.

![](https://wiki.placetopay.com/images/0/05/Invitation-state.png)


## Invitaciones para crear nuevos usuarios de ACS:

Es a través de una invitación que se pueden crear nuevos usuarios. Una invitación se envía a uno o varios correos electrónicos y allí redirecciona al usuario a la aplicación de Accounts de PlacetoPay. En esta redirección, el usuario podrá registrar sus datos personales y contraseña para acceder posteriormente a ACS.

> Los datos que registre deben ser los mismos que se utilizaron para enviar la invitación.

## ¿Cómo crear una invitación o un grupo de invitaciones?

Para crear una invitación, haga clic en el botón *Crear* del módulo de invitaciones. Visualizará un formulario como el siguiente:

![](https://wiki.placetopay.com/images/8/8e/Invitation-create-2.png)

Datos a diligenciar:

- **Nombre de la invitación:** Corresponde al nombre con el cual se va a identificar la invitación.

- **Correo electrónico:** Debe ingresar un correo válido porque allí es dónde se enviará la invitación. Puede ingresar uno o varios para conformar una invitación grupal.

- **Copiar datos de un usuario existente:** Con este botón deslizable, puede activar o desactivar la opción de copiar la información (permisos), que posee un usuario existente actualmente en ACS, a el usuario o usuarios nuevos que desea crear. 

- **Perfiles:** Si activó la opción "Copiar datos de un usuario existente", debe seleccionar uno o varios perfiles existente a partir del cual desea crear el nuevo usuario.

- **Roles:** Si desactivó la opción "Copiar datos de un usuario existente", debe seleccionar uno o varios roles existente a partir del cual desea crear el nuevo usuario.

Luego de diligenciar el formulario, haga clic en el botón *Siguiente*, visualizará una vista similar a la siguiente:

![](https://wiki.placetopay.com/images/b/b8/Invitation-detail-add-acl.png)

En esta vista se encuentra el paso siguiente para crear una invitación. 

#### Información básica de la invitación:

En esta vista, en la parte superior se muestra el o los correos a los cuales se va a enviar la invitación y el rol copiado si se seleccionó.

#### Permisos ACL creados para la invitación:

En la parte inferior de la vista se encuentran los permisos de tipo ACL, que permitirán personalizar los permisos de la aplicación, denegando o permitiendo accesos a diferentes secciones.

Los permisos se encuentran organizados en una tabla con el modelo para el cual se creó el permiso, la descripción de la regla y el botón para eliminar el permiso.

### Crear nueva regla ACL:

Desde las invitaciones puede crear nuevas reglas ACL para adjuntar a la invitación específica de los usuarios que desea crear.

Para crear una nueva regla, haga clic en el botón *Agregar regla acl*, ubicado en la parte lateral derecha de la vista. Se desplegará un formulario, diligencie los datos a partir de la siguiente información:

#### Acción:

Seleccione una opción para la regla ACL:

- **Permitir:** La regla permitirá acceder a un módulo y una acción específica.

- **Denegar:** La regla denegará el acceso a un módulo y una acción específica.

![](https://wiki.placetopay.com/images/e/ec/Invitations-form-action.png)

#### Modelo:

Seleccione de la lista, para el módulo al cual desea crear una regla que dé o deniegue un acceso.

![](https://wiki.placetopay.com/images/4/44/Invitations-form-model.png)

#### Atributo:

Seleccione de la lista, el atributo o campo del módulo, para el cual desea crear la regla.

![](https://wiki.placetopay.com/images/0/08/Invitations-form-attributte.png)

#### Operador:

Seleccione de la lista, el operador para generar la lógica de la regla, por ejemplo:

- Para comparar un valor (eq).
- Para encontrar un valor en una lista (in).

![](https://wiki.placetopay.com/images/c/c4/Invitations-form-operator.png)


#### Valor:

Seleccione de la lista, el valor que va a asignar para completar la regla:

![](https://wiki.placetopay.com/images/4/42/Invitations-form-value.png)

### Condicionales:

Para agregar y guardar la regla, haga clic en el botón *Agregar condicional*, posteriormente, visualizará la condición o regla ACL creada, en la parte inferior de la vista, similar a la siguiente vista:

![](https://wiki.placetopay.com/images/c/c2/Invitations-conditional-added.png)


<!--
type: tab
title: Roles
-->

# Roles

Para acceder a este módulo, dírijase al menú ubicado en la parte lateral izquierda, y despliegue la opción de *Seguridad*, luego seleccione el título *Roles*.

![](https://wiki.placetopay.com/images/b/b4/Roles-menu-2.png)

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

![](https://wiki.placetopay.com/images/f/f8/Profiles-menu-2.png)

## Índice de perfiles:

Los roles se asocian con los perfiles, ya que varios perfiles pueden estar asociados a un mismo rol. El siguiente es un ejemplo de un índice de perfiles.

Para acceder a este módulo, el usuario con los permisos necesarios para crear los perfiles, ingresa a través del menú despegable ubicado en la izquierda del panel, en la pestaña de seguridad.

Al ingresar al módulo, la plataforma muestra una tabla con los campos del nombre, descripción, usuario y fechas de creación y actualización del perfil. 

Además, esta sección posee un buscador de perfiles en la parte superior izquierda.


![](https://wiki.placetopay.com/images/d/d1/Profiles-index-2.png)

## Acciones para los perfiles:

Cada perfil cuenta con unas opciones para ser gestionado como son la opción de ver, editar o deshabilitar.

![](https://wiki.placetopay.com/images/9/95/Acs-options-profile.png)

**Ver:** Permite visualizar una información más detallada del perfil como son el nombre, la fecha de creación, actualización, y el usuario que lo creó, al igual que los permisos que el perfil tiene a disposición o los que desea agregar. 

  Un ejemplo de una vista de detalle de un perfil es el siguiente:

  ![](https://wiki.placetopay.com/images/2/2e/Profile-detail.png)

  En el detalle de un perfil se encuentran tres secciones:

  - **Información del perfil:** En esta sección se visualiza el estado del perfil, el nombre, si es el perfil actual o no (el perfil con el cual inició sesión es el mismo que está visualizando en el detalle) y si está habilitado, también, las fechas de creación y actualización y los usuarios que realizaron los movimientos.

  - **Roles:** Lista los roles asociados al perfil, su nombre, descripción y la opción de ver el detalle del rol.

  - **Acl:** Lista los permisos ACL creados para el perfil, el modelo o entidad de cada permiso, la descripción de la regla y el número de excepciones si las posee.

  > Las excepciones a una regla ACL, permiten que una regla con acción *Denegar*, permita que el perfil actual pueda visualizar solo aquellos registros que se hayan creado con ese mismo perfil.


**Editar:** Permite actualizar el nombre y la descripción del perfil.

  Un ejemplo del formulario de edición es el siguiente.

  ![](https://wiki.placetopay.com/images/7/73/Profile-edit-2.png)

> Es importante tener en cuenta que un perfil no se puede eliminar, ya que existen actividades que se han realizado en nombre de ese perfil y si se pudiera eliminar, se puede producir un error. Por esta razón, la aplicación tiene la opción de deshabilitar el perfil para denegar el acceso.


## ¿Cómo crear un nuevo perfil?

Para crear un nuevo perfil debe hacerlo a través de una invitación.

### ¿Qué es el ACL?

El ACL (Access Control List), es un módulo de gestión de permisos y reglas desarrollado en PlacetoPay y utilizado por ACS. Este se encarga de gestionar los permisos y accesos de los diferentes roles y perfiles creados en ACS. 

Estos permisos y reglas de acceso, se diferencian de los permisos básicos registrados en los roles, en que estos son más específicos y ofrecen una capa de seguridad extra a los datos manejados en la aplicación, ya que permiten que se visualice la información que corresponde solo a un cliente en específico y que no se filtre otra información que pertenece a otros clientes u organizaciones.

La lista de reglas se puede visualizar en el detalle de un perfil, en una vista similar a la siguiente:

![](https://wiki.placetopay.com/images/e/e1/Acl-rules.png)

### ¿Cómo crear reglas ACL?

Para crear una regla ACL, haga clic en el botón *Crear*, se presentará un formulario como el siguiente:

![](https://wiki.placetopay.com/images/c/cf/Acs-acl-create.png)

#### Información general:

Las reglas tienen dos opciones disponibles:
- Permitir accesos
- Denegar accesos

En el campo entidad, debe seleccionar la entidad que gestiona el módulo al cual quiere aplicarle las condiciones que va a crear.

#### Condicionales:

- Atributo: Seleccione el campo correspondiente a la entidad seleccionada previamente y al cual desea validar.

- Operador: Permite hacer las comparaciones de los datos.

- Valor: Ingrese uno o varios valores que debería contener el atributo seleccionado.

Al finalizar el diligenciamiento del formulario, haga clic en el botón *Guardar*.

<!--
type: tab
title: Logs
-->

# Logs de Seguridad

Para acceder a este módulo, dírijase al menú ubicado en la parte lateral izquierda, y despliegue la opción de *Seguridad*, luego seleccione el título *Logs*.

![](https://wiki.placetopay.com/images/3/3a/Logs-menu-2.png)

## Índice de logs:

En esta sección se registran los movimientos y actualizaciones que se realizan en la aplicación de ACS. Los logs permiten tener un control de los cambios y de lo que sucede en la aplicación. 
En la sección de logs se encuentra un listado de los mismos, con una descripción, la fecha y hora en que fue registrado el movimiento. 

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