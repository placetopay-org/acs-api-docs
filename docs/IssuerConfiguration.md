<!--
type: tab
title: Detalles del emisor
-->

# Emisores en ACS

<br>

## ¿Qué es un emisor?

Un emisor o banco emisor, es la institución financiera responsable de emitir los medios de pago, como tarjetas de débito o de crédito. Estas tarjetas de pago se emiten con la marca de la asociación. También pueden existir emisores de tarjetas de pago propias y no franquiciadas.

Entre las funciones de un emisor están:

- El emisor tiene la responsabilidad de autorizar o denegar una transacción cuando recibe los datos de la compra. 

- El emisor se encarga de transferir el dinero de una compra hecha por el consumidor, al adquiriente, que a su vez es quien paga al comercio y mantiene relación con este. 

- El emisor debe dar el mantenimiento requerido a cuentas y tarjetas.

- El emisor es responsable de resolver cargos disputados a su favor, por motivos de fraudes o riesgos.

- El emisor se encarga de activar, suspender y bloquear una tarjeta de pago cuando se requiera.


## ¿Cómo acceder a la gestión de emisores de ACS?

Para acceder al listado de emisores de la aplicación siga los siguientes pasos:

**1.** Remítase al menú lateral izquierdo dónde visualizará tres opciones, "Dashboard", "Sistema" y "Seguridad", seleccione "Sistema" y luego "Emisores":

  ![](https://wiki.placetopay.com/images/3/34/Emisor-menu.png)

**2.** Visualizará una pantalla similar a la siguiente:

  ![](https://wiki.placetopay.com/images/8/83/Indice-emisores.png)

## ¿Cómo crear un emisor en ACS?

Para crear un emisor, haga clic en el botón **Crear**, ubicado en la parte lateral derecha del índice de emisores.

Visualizará un formulario similar al siguiente:

![](https://wiki.placetopay.com/images/6/62/Issuer-create-form.png)

Para diligenciarlo tenga en cuenta los siguientes datos:

- **Nombre:** Ingrese en este campo el nombre del banco emisor que va a crear.

- **País:** Seleccione de la lista desplegable el país dónde opera el banco emisor.

- **Moneda:** Seleccione de la lista desplegable la moneda con la cual procesa las transacciones el banco emisor.

- **Slug:** Ingrese una cadena clave para el emisor. Esta cadena se agregará a las URL donde se gestionen configuraciones y servicios del emisor.

- **Logo:** Aquí puede cargar una imagen con el logo del emisor. Para hacerlo haga clic en la opción *Seleccionar archivo* y busque la imagen correspondiente al logo en su equipo. La imagen debe tener unas dimensiones máximas de 1000x1000.

### Validación de datos:

Para el formulario de creación de un emisor en ACS, y para todos los formularios en general de la aplicación, se dispone de la funcionalidad de validación de los datos ingresados, lo cual permite asegurar la integridad y validez de los datos ingresados en los formularios.

De esta forma, al diligenciar el formulario puede encontrar dos tipos de validaciones:

**1. Validaciones de lado del cliente:**

  Estas validaciones se realizan cuando un dato no cumple las reglas mínimas de aceptación y no hay necesidad de enviar la respuesta al servidor, sí se ha validado previamente que está errónea la información. Se visualizan con mensajes en rojo para el campo erróneo y le ofrece al usuario una ayuda de cómo debe diligenciar el campo en cuestión para ser aceptado. Si hay errores en estas validaciones, la aplicación no permite el envío del formulario.

  La siguiente imagen ilustra errores en validaciones del lado del cliente:

  ![](https://wiki.placetopay.com/images/3/30/Issuer-pre-validations.png)

**2. Validaciones de lado del servidor:**

  Estas validaciones se aplican cuando se envía un formulario o una información al servidor y ésta no cumple con las validaciones requeridas, por lo cual se genera un error, deniega la solicitud y muestra al usuario el error encontrado. Estas validaciones se ejecutan cuando no se han registrado como validaciones del lado del cliente, o son complicadas de validar del lado del cliente o el usuario logra por algún medio pasar el primer filtro de validaciones del cliente con la información errónea, sin embargo, este filtro de validaciones detiene una solicitud con datos inválidos.

  La siguiente imagen ilustra errores en validaciones del lado del servidor, en la cual se logró enviar el formulario pero al momento de recibirlo se encontraron errores en los datos de la solicitud, por lo cual no pudo ser procesada correctamente:

  ![](https://wiki.placetopay.com/images/9/91/Image-issuer-error.png)    


## ¿Cuáles son los requerimientos para crear un emisor en ACS?

Para crear y configurar un emisor en ACS, este debe haber emitido tarjetas de pago con las marcas que ya hayan sido certificadas para funcionar en ACS.

Se requiere que el país y el idioma con el cual se vaya a crear el emisor, estén disponibles para ACS.

Se requiere que exista una relación entre emisor, adquiriente y comercio y que estos estén registrados en las aplicaciones de ACS y de MPI de PlacetoPay Evertec, para lograr un proceso de autenticación exitosa. 

Importante tener en cuenta habilitar todos los campos de configuración del menú *Campos de configuración* de la aplicación, antes de crear el emisor, ya que todos estos campos son requeridos para el funcionamiento básico de un emisor.

> En este punto es importante recordar que la aplicación de **MPI** también implementa y pertenece al flujo propuesto por el protocolo 3-D Secure para autenticar un tarjetahabiente. Pertenece al dominio el adquiriente y entre sus funciones principales están:
  >> - Recibir y responder la petición de autenticación enviada por el comercio o pasarela de pagos.
  >> - Solicitar al emisor la autorización del pago.
  >> - Responder al comercio o pasarela de pagos el estado final de la autenticación.


## Índice de emisores

En esta sección se visualiza el listado o índice de emisores, la información se presenta en una tabla donde se muestran los datos principales de cada emisor, tales como: Nombre, País y Estado. 

![](https://wiki.placetopay.com/images/4/4a/Issuer-actions.png)

### Acciones disponibles para los emisores:

En el título "Acciones" ubicado en la parte lateral derecha del índice de emisores, se encuentra un menú desplegable, haga clic en este menú y despliegue las acciones o funcionalidades disponibles para cada emisor. En el menú se encuentran las siguientes acciones:

- **Ver:** Seleccione esta opción para visualizar los detalles del emisor, sus configuraciones y componentes.

  Visualizará una vista similar a la siguiente:

  ![](https://wiki.placetopay.com/images/8/8f/Detalles-emisor.png)

- **Editar:** Seleccione esta opción para actualizar o corregir los datos con los cuales se creó el emisor. 

  Visualizará un formulario similar al de creación del emisor. Todos los datos son editables.

  ![](https://wiki.placetopay.com/images/3/3c/Edit-issuer.png)

- **Habilitar o Deshabilitar:** Deslice el botón tipo switch para habilitar el emisor si se encuentra deshabilitado o para deshabilitarlo cuando se encuentre habilitado. 

  ![](https://wiki.placetopay.com/images/8/81/Issuer-actions-toggle.png)

  Al habilitar o deshabilitar, la aplicación le entregará un mensaje de confirmación similar al siguiente e inmediatamente cambiará el estado del emisor editado.

  ![](https://wiki.placetopay.com/images/c/ca/Issuer-toggle.png)

### ¿Cómo habilitar un emisor?

**1. Active los campos de configuración requeridos:** En el menú *Campos de configuración* de la aplicación, habilite todos los campos de configuración (debe habilitarlos antes de crear el emisor), ya que estos son requeridos para la habilitación del emisor. Para obtener más información de los campos de configuración, vaya al título **Campos de configuración** del presente documento.

  La siguiente imagen muestra un índice de los campos de configuración donde todos los campos visibles están habilitados, así deben estar para comenzar a configurar correctamente el emisor.

  ![](https://wiki.placetopay.com/images/f/f3/Campos-configuracion-indice.png)

  > Si algún campo se encuentra deshabilitado, despliegue el menú de la parte lateral derecha y seleccione la opción *Habilitar*.

**2. Habilitar estrategias del emisor:** En los detalles del emisor, en la pestaña *Configuraciones*, y luego en la pestaña *Servicios*, encontrará las estrategias disponibles para el emisor (esta funcionalidad se explica más adelante), debe habilitar tres estrategias (cardholderStrategy, otpStrategy y authStrategy).

  Un ejemplo del menú *Servicios* es el siguiente:

   ![](https://wiki.placetopay.com/images/3/3c/Estrategias.png)
    
  Nótese que en la imagen anterior, las estrategias se encuentran habilitadas. Si se intentara habilitar el emisor con una o todas las estrategias deshabilitadas, arrojaría un error como el siguiente y no permitiría ejecutar la habilitación del emisor.

  ![](https://wiki.placetopay.com/images/8/88/Error-habilitacion.png)


**3. Suscribir marca al emisor:** En la pestaña **Operaciones -> Marcas suscritas** del detalle del emisor,  seleccione una marca del listado, sino hay marcas disponibles, debe ir al menú *Marcas* de la aplicación y crear una nueva marca para el emisor, para esto guíese de la sección *Configuración de marcas* de la presente documentación.
    
**4. Configurar rangos de tarjeta para el emisor:** En la pestaña **Operaciones -> Gestionar rangos de tarjetas** del detalle del emisor, haga clic en el botón *Crear* y cree rangos de tarjeta manuales o por importación, para ello guíese de la sección *Gestión de rangos de tarjetas* del presente documento.
    
**5. Crear certificado tipo Cliente para las marcas del emisor:** Para habilitar un emisor debe crear un certificado tipo *CLIENT*, en el menú de *Certificados*, y seleccionar el emisor correspondiente y una marca suscrita para el mismo emisor. Luego debe firmar el certificado con la entidad certificadora y en el índice de certificados, este debe registrar en el campo *Certificado* con el estado *Encontrado*, que indica que fue validado correctamente. 

  Para crear el certificado, guíese de la sección **Otras configuraciones**, pestaña **Certificados SSL**.

  Un ejemplo de la primera vista del formulario de creación de un certificado es el siguiente:

  ![](https://wiki.placetopay.com/images/4/4a/Formulario-cert.png)

## Detalles de un emisor

### Información principal del emisor:

Para ir a los detalles de un emisor, haga clic en la acción *Ver* del menú desplegable del emisor, ubicado en el índice de emisores. 

En la siguiente imagen se visualiza un ejemplo de la parte superior de la vista de *Detalles de un emisor*. En la vista se encuentra la información con la cual se creó el emisor, el estado en que se encuentra el emisor (está habilitado o no), las fechas de creación del emisor y de actualización y los usuarios que hicieron la creación y/o la actualización.

Además, en la parte lateral derecha, hay un botón para acceder al formulario de edición en caso de requerirlo.

![](https://wiki.placetopay.com/images/8/8f/Detalles-emisor.png)

<!--
type: tab
title: Gestión de suscripciones por marcas
-->

# Suscripción por marcas

Para acceder a esta funcionalidad, haga clic en el menú **Operaciones -> Marcas suscritas**, que actualmente se ubica al lado derecho del menú *Detalles del emisor*. 

Luego visualizará una vista similar a la siguiente:

![](https://wiki.placetopay.com/images/5/5f/Marcas-emisor.png)

En ella encontrará el listado de marcas registradas para el emisor y un formulario para agregar nuevas marcas.

> Para las marcas están disponibles las funciones de *Editar* y *Eliminar*, las cuales se encuentran dando clic en el menú desplegable ubicado al final del registro de cada marca.

### ¿Cómo suscribir una nueva marca?:

Para suscribir una nueva marca a su emisor, haga clic en el botón **Crear**, ubicado en la parte lateral derecha de la lista de marcas. Luego seleccione la marca de la lista disponible, la versión del protocolo y el certificado SSL correspondiente.

> Si la aplicación le arroja este mensaje *"No se ha encontrado certificados disponibles para hacer la suscripción a esta marca."*, entonces debe crear un certificado SSL para continuar con el proceso de suscripción de la marca.


<!--
type: tab
title: Gestión de rangos de tarjetas
-->

# Rangos de tarjetas

<br>

## ¿Cómo acceder a este menú?

Para acceder a este menú, haga clic en el menú **Operaciones -> Gestionar rangos de tarjetas**, ubicado en la parte superior de la vista.

Visualizará un índice similar al siguiente:

![](https://wiki.placetopay.com/images/a/a2/Rangos-emisor.png)

En esta sección se importan y crean los rangos de tarjetas aceptadas para un emisor específico. Puede ver la información principal de cada rango organizada en una tabla,entre los datos están: BIN del rango, rango inicial, rango final, marca, clase, si acepta desafía desacoplado y las respectivas acciones que tienen cada uno de los rangos.

## Acciones de los rangos de tarjetas

Las acciones disponibles para los rangos de tarjetas se encuentran ubicadas en el menú desplegable ubicado al final de cada rango. Las acciones son las siguientes:

- **Ver:** Seleccione esta opción para visualizar los detalles del rango y las fechas de creación y actualización y los datos de los usuarios que ejecutaron las acciones.

  Visualizará una vista similar a la siguiente:

  ![](https://wiki.placetopay.com/images/a/ae/Detalle-rango.png)

- **Editar:** Seleccione esta opción para actualizar o corregir los datos con los cuales creó el rango.  Visualizará un formulario similar al de creación de un rango de tarjeta. Todos los datos son editables.

- **Eliminar:** Seleccione esta opción para eliminar un rango de tarjetas del emisor. Si elimina un rango, tenga en cuenta que las solicitudes de autenticación que lleguen con un número de tarjeta que esté en este rango, no podrán ser procesadas.


## ¿Cómo crear un rango de tarjetas?

Al dar clic en el botón **Crear**, se desplegarán dos opciones para crear rangos:

  ![](https://wiki.placetopay.com/images/1/18/Create-button-card.png)

**1. Crear un rango de tarjetas,** este permite crear un rango de forma manual.

  Si selecciona esta opción, obtendrá un formulario similar al siguiente:

  ![](https://wiki.placetopay.com/images/f/f3/Crear-rango-form.png)

  Para diligenciar el formulario tenga en cuenta:

   - **Marca:** Seleccione el nombre de la marca a la cual se le va a registrar el rango.

   - **Clase:** Ingrese el nombre de la clase del rango de tarjetas. Por ejemplo Gold, Platinium...

   - **Rango inicial:** Ingrese los primeros números del BIN y adicione otros números que indiquen el inicio del rango. El valor debe tener mínimo 13 dígitos.

  - **Rango final:** Ingrese los primeros números del BIN y adicione otros números que indiquen el final del rango y que sean mayores al rango inicial. El valor debe tener mínimo 13 dígitos.

  - **Desafío desacoplado:** Marque o desmarque la casilla según el criterio del rango, ¿se puede procesar desafío desacoplado o no para este rango?

**2. Crear importación,** con esta opción puede importar rangos de tarjetas que tenga en un archivo CSV.

Para crear una importación visualizará un formulario similar al siguiente:

![](https://wiki.placetopay.com/images/b/ba/Acs-create-import-ranges.png)

Debe seleccionar la franquicia para la cual se van a cargar los rangos y un archivo de tipo CSV (archivo de valores separados por comas), que contenga la información de los rangos. Un ejemplo del archivo es este:

![](https://wiki.placetopay.com/images/8/8f/Acs-file-import-example.png)

El archivo debe contener cuatro títulos separados por comas en minúscula:

**1. start_range**: Indica el valor inicial para el rango de tarjetas.

**2. end_range**: Indica el valor final para el rango de tarjetas.

**3. class**: Hace referencia a la clase o tipo de tarjeta utilizada, por ejemplo si es Gold, Platinum.

**4. action**: Debe indicar qué acción se debe ejecutar para el rango indicado, las acciones posibles y sus indicadores son los siguientes:

 - **I**: Indicador para acción de insertar rango.

 - **U**: Indicador para acción de actualizar rango .

 - **D**: Indicador para acción de eliminar rango.


Estos títulos deben seguirse de sus respectivos valores en filas hacia abajo, igualmente separados por comas, sin espacios.

> Para visualizar el formato de un archivo CSV de ejemplo, haga clic en la opción *Descargar* que aparece en el lado izquierdo del formulario.


<!--
type: tab
title: Gestión de control de fraude
-->

# Motor de Control de Fraude

La principal funcionalidad de ACS es el motor de control antifraude, este permite validar la información que se recibe en la petición de autenticación, a través de un conjunto de reglas que validan las autenticaciones de cada emisor registrado.

Esta funcionalidad se gestiona desde la sección de Emisores de la aplicación.

## Listas de control de fraude

Las listas de control de fraude son el primer filtro que por el cual pasan las solicitudes de autenticación de ACS. 

> Las listas de control antifraude se ejecutan antes de los grupos de control antifraude y según los resultados que obtenga de sus validaciones, puede evitar que una autenticación tenga que pasar por las validaciones de los grupos de reglas.

### Índice de las listas de reglas:

Para acceder al índice de listas de reglas, diríjase al menú **Gestionar control de fraude -> Gestionar listas de control de fraude**, en las pestañas ubicadas en la parte superior del detalle de un emisor.

Al dar clic en el menú, visualizará el índice de listas de reglas, similar al de la siguiente imagen:

![](https://wiki.placetopay.com/images/3/35/Listas-antifraude.png)


### Acciones de las listas de reglas:

Las acciones disponibles para las listas de reglas se encuentran ubicadas en el menú desplegable ubicado al final de cada lista. Las acciones son las siguientes:

- **Ver:** Seleccione esta opción para visualizar los detalles de la lista. Visualizará una vista similar a la siguiente:

  ![](https://wiki.placetopay.com/images/4/48/List-detail.png)

- **Editar:** Seleccione esta opción para actualizar o corregir los datos con los cuales creó la lista. Visualizará un formulario similar al de creación de una lista. Todos los datos son editables.

- **Eliminar:** Seleccione esta opción para eliminar la lista.

### Filtros para las listas de reglas:

ACS provee para este módulo la funcionalidad de filtrar listas, esta permite hacer la búsqueda más flexible y específica cuando tiene muchos datos. 

Para acceder a los filtros, diríjase a la parte lateral derecha del índice de listas, al lado izquierdo del botón *Crear*, encontrará la opción **Filtrar**, haga clic en esta y se desplegará una vista como la siguiente:

![](https://wiki.placetopay.com/images/1/11/Filter-lists.png)

Puede filtrar únicamente por el tipo de lista que desea buscar, seleccione la requerida y haga clic en el botón *Buscar* o en el botón *Limpiar filtros* cuando necesite hacer una nueva búsqueda.


### Tipos de listas de reglas:

Estas listas son temporales, es decir, tienen una duración específica que usted le asigna al crearla, y se dividen en dos clases:

- **Permisivas:** Estas listas van a crear un filtro que va a permitir que las autenticaciones que cumplan con los valores registrados en estas, puedan eximirse de la ejecución de los grupos de reglas, y continuar así con el proceso de autenticación.

  > En esta lista se pueden agregar valores de clientes con historiales seguros y confiables, ya que al ser permisiva, será más flexible al momento de hacer la validación de la autenticación.

- **Restrictivas:** Por el contrario, este tipo de listas, al evaluar que los datos de la autenticación coinciden con los datos de la lista, enviará las autenticaciones directamente a ejecutar los grupos de reglas.

  > En esta lista se pueden agregar valores de clientes con historiales de riesgo. Al ser restrictiva la lista, permitirá ejercer mayor control de los filtros de validación. 

### ¿Cómo crear una lista de control de fraude?

Al dar clic en el botón *Crear*, ubicado en la parte lateral derecha del índice de listas, se desplegarán dos opciones para crear listas:

  ![](https://wiki.placetopay.com/images/4/43/Button-create-list.png)


**1. Crear una lista de control de fraude:** Esta opción le permite crear una lista de forma manual e individual. 

  Si escoge esta opción se direccionará a un formulario como este:

  ![](https://wiki.placetopay.com/images/5/53/Acs-create-fraud-list.png)

Se solicitará:

- **Fecha de inicio:** Fecha en la que la lista va a comenzar a funcionar y hacer las validaciones.

- **Fecha de finalización:** Fecha en la que la lista dejará de funcionar y validar reglas.

- **Tipo de lista:** ACS dispone de dos tipos de listas (PERMISSIVE y RESTRICTIVE), escoja una según el tipo de validaciones a ejecutar.

- **Tipo de valor:** Aquí se selecciona el parámetro por el cual se van a hacer los filtros de las autenticaciones. 

    Los siguientes son los tipos de valores disponibles:

   - **IP:**  Internet Protocol. Es la dirección pública que identifica un dispositivo conectado a una red que utiliza el protocolo.

   - **PAN:** Primary Account Number. Es el número de tarjeta que aparece en el anverso de una tarjeta de pago.

   - **EMAIL:** Correo electrónico del comprador.

   - **MERCHANT_ID:** Número identificador del comercio.

   - **MCC:** Merchant Category Code. Hace referencia al código de categoría del comercio.

  Los visualizará en la lista desplegable del campo *Tipo de valor* así:

    ![](https://wiki.placetopay.com/images/e/e8/Value-type-list.png)

- **Valor:** Corresponde al valor del tipo de parámetro seleccionado en el campo anterior. Con este valor se procede a hacer las validaciones y a verificar la coincidencia del dato con los recibidos en la autenticación.

**2. Crear importación de listas de control de fraude:** Con esta opción podrá crear listas de reglas de forma masiva a partir de un archivo que contenga las reglas.

> El archivo a cargar debe estar en formato .CSV, .TSV o .TXT.

Si escoge esta opción, se cargará un formulario como el siguiente:

  ![](https://wiki.placetopay.com/images/e/ed/List-import-create.png)

  En el formulario, haga clic en la opción *Seleccionar archivo* y busque en su equipo el archivo que desea cargar. Luego haga clic en el botón *Guardar*.

> Para visualizar un ejemplo del formato de una importación, haga clic en el link *Descargar*, ubicado en la parte lateral izquierda, en el título *Información básica*.

## Reglas de control de fraude

Las reglas permiten hacer las validaciones de los datos recibidos en las solicitudes de autenticación. Estas reglas evalúan la coincidencia de las condiciones contenidas en la regla y de los datos obtenidos en la solicitud de autenticación.

> Al crear un emisor en ACS, se agregarán automáticamente una serie de reglas por defecto al emisor. Estas se encontrarán en esta sección y puede habilitarlas, editarlas o deshabilitarlas, según su necesidad.

### Índice de reglas:

Para acceder al índice de reglas de control de fraude, diríjase al menú **Gestionar control de fraude -> Reglas de control de fraude**, ubicado en las pestañas de la parte superior del detalle de un emisor.

Visualizará una pantalla similar a la siguiente:

![](https://wiki.placetopay.com/images/1/18/Indice-reglas-antifraude.png)

### Funciones de las reglas:

Las reglas tienen dos funciones a las cuales puede acceder haciendo clic en el menú desplegable ubicado al final de cada regla:

- **Ver:** Seleccione esta opción para visualizar más detalles de la regla. Haga clic en el botón con la leyenda *Ver*, ubicado al final de cada regla.

  Encontrará una vista similar a la siguiente, en la cual está el estado de la regla, el nombre, el tipo de regla y el valor que le asignó, así mismo, las fechas y usuarios que crearon y actualizaron la regla:

  ![](https://wiki.placetopay.com/images/3/36/Rule-detail.png)

- **Activar/Inactivar:** Deslice este botón tipo switch para activar o inactivar una regla.

  > Si deshabilita una regla, no podrá validar la autenticación con los parámetros de la regla. Además, siempre debe tener reglas habilitadas para poder hacer un proceso de autenticación exitoso y confiable.

### ¿Cómo puedo cambiar el orden de ejecución de las reglas?

Las reglas se ejecutan y validan en el orden dado en el índice de reglas. Las nuevas reglas que cree, se ubicarán automáticamente debajo de la última creada y se ejecutarán en ese mismo orden (solo se ejecutan las que reglas que tengan estado *Activo*).

Para cambiar el orden de las reglas, mantenga presionada la regla que desea cambiar de lugar y deslícela al lugar donde desea ubicarla. Posteriormente aparecerá un mensaje que dice lo siguiente: *"Existen cambios sin guardar, si abandona esta página puede perderlos!"*

Y en la parte inferior del índice obtendrá dos botones, presione **Guardar cambios** para confirmar el cambio de lugar de la regla o **Restablecer cambios** para volver al estado anterior de ordenamiento de las reglas.


### Solicitudes de reglas:

Haga clic en la pestaña *Solicitudes de reglas*, ubicada en la parte superior derecha del índice de reglas. Allí se pueden visualizar las peticiones de creación, actualización o eliminación de reglas, las cuales se encuentran pendientes por aprobar o denegar.

- **Aprobar:** Para aprobar una solicitud, haga clic en el botón con check verde para aprobar o en el botón con equis en rojo para denegar la solicitud. Luego se desplegará una ventana para confirmar la aprobación y el despliegue de la regla al entorno productivo, dé clic en *Confirmar* para aceptar la acción o en *Cancelar* para volver a las solicitudes.

- **Denegar:** Para denegar una solicitud, haga clic en el botón con equis en rojo. Luego se desplegará una ventana para confirmar la eliminación, dé clic en *Confirmar* para aceptar la acción o en *Cancelar* para volver a las solicitudes.

### ¿Cómo crear solicitudes de reglas?

Para crear una petición de regla, diríjase a la pestaña **Solicitudes de reglas** y haga clic en el botón **Crear petición de regla**, ubicado en la parte lateral derecha.

![](https://wiki.placetopay.com/images/5/59/Acs-rule-create.png)

Luego visualizará una ventana como esta, dónde le solicitan la acción que desea hacer con la regla.

![](https://wiki.placetopay.com/images/c/c2/Acs-rule-create-actions.png)

#### Acciones disponibles:

- **Crear:** Permite crear una petición para crear una nueva regla.

- **Actualizar:** Permite crear una petición para editar una regla existente. Si selecciona esta opción, luego se desplegará una lista con las reglas disponibles para editar, seleccione una y haga clic en el botón *Siguiente* y lo redirigirá a un formulario como el de creación de regla.

  ![](https://wiki.placetopay.com/images/8/89/Edit-rule.png)

- **Eliminar:** Permite crear una petición para eliminar una regla existente, si selecciona esta opción también se desplegará una lista con las reglas que puede eliminar, luego haga clic en el botón *Enviar solicitud*.

![](https://wiki.placetopay.com/images/f/f5/Delete-rule.png)

### ¿Cómo crear nuevas reglas?

Para crear una nueva regla, debe seleccionar la opción *Crear* de la lista de peticiones y se desplegará un formulario como el siguiente:

![](https://wiki.placetopay.com/images/f/f0/Acs-conditions-rule.png)

Los datos requeridos son:

- **Nombre:** ¿Cómo desea nombrar la regla que va a crear?

- **Acción:** Se refiere a la función que va a cumplir la regla en el proceso de autenticación. Estas acciones se describen detalladamente en el título *Acciones de las reglas*, de la presente documentación.

- **Tipo de regla:** Hace referencia al tipo de regla que desea crear, por ejemplo es una regla que valida un número de tarjeta de crédito, o valida un rango de tarjetas, un email, un rangos de bines...

- **Valor:** Es el valor que requiere una regla para validar y comparar los datos de la regla y de la solicitud de autenticación.

#### Reglas con múltiples condiciones:

Puede además agregar otras condiciones para una misma regla,haciendo clic en el botón inferior del formulario **Agregar condición**, y se desplegarán nuevos campos para ingresar otro tipo de regla y su valor correspondiente.

> Para habilitar este botón debe haber diligenciado ya una condición completa con su tipo de regla y valor.

Al hacer clic en el botón se presentará un formulario como el siguiente:

![](https://wiki.placetopay.com/images/d/dc/Add-condition-rule.png)

También hay otros tipos de reglas que ofrecen más posibilidades. En la siguiente imagen puede visualizar una regla donde puede escoger el operador con el cual va a comparar los valores la regla, por ejemplo, que el valor dado tenga un rango específico, un valor mínimo o máximo.

![](https://wiki.placetopay.com/images/1/19/Acs-others-rule-conditions.png)

Luego de enviar la solicitud de regla, esta se agregará al listado de *Solicitudes de regla*, allí tiene la opción de *Aceptar* o *Denegar*, con los botones de la parte lateral derecha.

![](https://wiki.placetopay.com/images/a/aa/Acs-accept-deny.png)

> Hasta que no acepte la solicitud de regla, esta no podrá visualizarse ni utilizarse en producción. Luego de aceptarla recuerde habilitarla.

### Acciones de las reglas: 

Al crear una regla se le define un tipo de acción específica que va a ejecutar. Estas acciones permiten definir el transStatus (estado de autenticación de la transacción). 

Estas acciones se encuentran en el formulario de creación de regla, en el campo *Acción*:

![](https://wiki.placetopay.com/images/d/db/Rule-actions.png)

Las acciones permitidas son las siguientes:

- **Autenticar:** Las reglas que contengan esta acción, permitirán validar la solicitud de autenticación y aprobarla automáticamente si la validación de los datos pasa de forma exitosa, generando un estatus Y (autenticación satisfactoria). Por ejemplo una regla de tipo *Rango de bines* va a contener un rango mínimo y máximo de BIN, las autenticaciones con tarjetas cuyo BIN entren en este rango, se validarán exitosamente y autenticará inmediatamente la solicitud.

- **Realizar desafío:** Las reglas cuya acción es realizar desafío, al validarse generarán el estatus C (requiere desafío), con este estatus el tarjetahabiente será direccionado a una interfaz de usuario en la cual se le pedirá aceptar un desafío para validar su identidad. 

- **Desafío desacoplado:** Las reglas que contengan esta acción, al validarse generarán un estatus D (desafío desacoplado)y la petición de autenticación se pondrá en pausa y el emisor se encargará de realizar el desafío manualmente con el tarjetahabiente.
 
- **No autenticar:** Las reglas con acción de no autenticar, al cumplirse la validación, lanzarán automáticamente un estado N (autenticación fallida). Los datos incluídos en estas reglas suelen ser riesgosos.

- **Ejecutar grupo de reglas:** Las reglas creadas con esta acción, pueden ejecutar todas las reglas contenidas en un grupo de reglas específico del emisor. Para escoger esta opción debes tener grupos de reglas habilitados para el emisor.

  Si escoges esta opción, el formulario se visualizará como el siguiente:

  ![](https://wiki.placetopay.com/images/5/5c/Rule-to-execute-group.png)

  En el apartado *Grupos de control de fraude*, se presentará una lista de los grupos disponibles, escoja uno y continúe con el diligenciamiento de las condiciones para la regla.

- **Ninguno:** Las reglas con esta acción, tomarán la acción por defecto y generarán un estatus N (No autenticado.

> La función de ejecutar un grupo de reglas permite crear reglas que abarquen más validaciones y también permite utilizar reglas creadas anteriormente para hacer otras validaciones o complementarlas con otras condiciones, y de esta forma agrupar funcionalidades y disminuir reglas repetidas.

### Tipos de reglas: 

Al crear una regla se asigna un tipo específico. Las opciones disponibles se visualizan en el formulario de creación de la regla, en el campo *Tipo de regla*.

Visualizará una lista similar a esta con la lista de reglas disponibles:

![](https://wiki.placetopay.com/images/f/fe/Rule-types.png)

Los tipos de reglas disponibles actualmente son:

#### Regla de rango de número de tarjeta: 
Esta regla permite validar que la tarjeta que llegue en la petición de autenticación, esté en el rango especificado. Acepta dos valores, el rango inicial que debe tener mínimo 13 dígitos y el rango final que debe ser mayor al inicial y tener máximo 19 dígitos dígitos.

  ![](https://wiki.placetopay.com/images/6/64/Regla-rango-tarjeta.png)

#### Regla de rango de bines: 
Esta regla permite validar que la tarjeta que llegue en la petición de autenticación, esté en el rango especificado. Acepta dos valores, el rango inicial que debe ser un BIN de 6 o de 8 dígitos y el rango final que debe tener los mismos dígitos.

  ![](https://wiki.placetopay.com/images/9/96/Bin-range-rule.png)

#### Regla de número de tarjeta de transacción: 
Esta regla permite validar que el número de tarjeta que registre en el valor, sea igual al número de tarjeta de la petición de autenticación. Esta regla recibe mínimo 13 dígitos y máximo 19, y debe coincidir con el algoritmo de Luhn, el cual comprueba mediante una secuencia de dígitos, si un número de tarjeta es válido.

  ![](https://wiki.placetopay.com/images/7/7f/Card-number-rule.png)

#### Regla de monto de compra:
Esta regla permite validar el monto de la transacción a autenticar. Acepta un valor numérico que indique un monto de pago.

  ![](https://wiki.placetopay.com/images/1/14/Rule-total.png)

#### Regla de datos de autenticación:
 Esta regla valida los campos que se envían en el mensaje AReq, siendo este un tipo de mensaje del Protocolo 3-D Secure, con el cual se da inicio al proceso de autenticación. Esta regla recibe los siguientes parámetros:

  - **Campo**, hace referencia al campo contenido en el mensaje AReq. Se presenta una lista con todos los campos disponibles para validar. Seleccione uno.

  - **Condiciones**, en este campo se selecciona el operador con el cual se va a hacer la comparación de valores a validar. Según el campo seleccionado se despliegan unos operadores específicos.

  - **Valores**, aquí se ingresa el valor con el cual se va a hacer la comparación que permite validar o no la regla.

Un ejemplo de regla para datos de autenticación es el siguiente:

  ![](https://wiki.placetopay.com/images/d/d4/Areq-rule.png)
   
##### Campos de autenticación disponibles para la regla de datos de autenticación:

- **Identificador de la cuenta del titular:** Identificador de cuenta del titular de la tarjeta: Esta regla valida la solicitud de autenticación a partir de la puntuación que tenga el emisor que procesa la transacción. La regla permite asignar el operador de comparación con el valor final que le va a asignar.   

- **Indicador de edad de la cuenta del titular:** Tiempo que el titular de la tarjeta ha tenido la cuenta con el solicitante 3DS, los valores recibidos son de 2 caracteres, y son de tipo numéricos.

    Los valores recibidos son:
    -   01 = Sin cuenta 
    -   02 = Creado durante esta transacción
    -   03 = Menos de 30 días
    -   04 = 30 – 60 días
    -   05 = Mas de 60 días

- **Fecha de la cuenta del titular de la tarjeta:** Fecha en que el titular de la tarjeta abrió la cuenta con el solicitante 3DS, los valores recibidos son de 8 caracteres, con un formato de fecha AAAAMMDD

- **Indicador de cambio de cuenta del titular de la tarjeta:** Indicador del tiempo transcurrido desde que se modificó por última vez la información de la cuenta del titular de la tarjeta con el solicitante 3DS, incluída la dirección de facturación o envío, una nueva cuenta de pago o nuevos usuarios agregados. Los valores recibidos son de 2 caracteres, y son de tipo numérico.
    
    Los valores recibidos son:
    -   01 = Sin cambios
    -   02 = Modificado durante esta transacción
    -   03 = Menos de 30 días
    -   04 = 30 – 60 días
    -   05 = Mas de 60 días

- **Cambio de cuenta del titular de la tarjeta:** Fecha en la que se modificó por última vez la cuenta del titular de la tarjeta con el solicitante de 3DS, incluída la dirección de facturación o envío, la nueva cuenta de pago o los nuevos usuarios agregados. El tipo de dato que se recibe es en el formato AAAAMMDD.

- **Indicador de cambio de contraseña de la cuenta del titular de la tarjeta:** Indica el tiempo transcurrido desde que se cambió la contraseña o se restableció la cuenta del titular de la tarjeta con el solicitante 3DS, los valores recibidos son de 2 caracteres, y son de tipo numérico.
    
    Los valores recibidos son:
    -   01 = sin cambios
    -   02 = Modificado durante esta transacción
    -   03 = Menos de 30 días
    -   04 = 30 – 60 días
    -   05 = Mas de 60 días

- **Cambio de contraseña de la cuenta del titular de la tarjeta:** Fecha en que se cambió la contraseña o se restableció la cuenta del titular de la tarjeta con 3DS Requestor, el tipo de dato que se recibe es en el formato AAAAMMDD.

- **Indicador de uso de la dirección de envío:** Indica cuando se utilizó por primera vez la dirección de envío para la transacción con 3DS Requestor, los valores recibidos son de 2 caracteres, y son de tipo numérico.

    Los valores recibidos son:
    -   01 = Esta transacción 
    -   02 = Menos de 30 días
    -   03 = 30 – 60 días
    -   04 = Mas de 60 días

- **Uso de la dirección de envío**: Fecha en la que se utilizó por primera vez la dirección de envío para la transacción con el solicitante 3DS. El tipo de dato que se recibe es en el formato AAAAMMDD.

- **Número de transacciones por día**: Número de transacciones (exitosas y abandonadas) para esta cuenta del titular de tarjeta con 3DS Requestor, en todas las cuentas de pago en las 24 horas anteriores.

- **Número de transacciones por año**: Número de transacciones (exitosas y abandonadas) para esta cuenta de titular de tarjeta con 3DS Requestor, en todas las cuentas de pago en el año anterior.

- **Número de intentos de aprovisionamiento por día**: Número de intentos de agregar una tarjeta en las últimas 24 horas.

- **Recuento de compras de la cuenta del titular de la tarjeta**: Número de compras realizadas con esta cuenta del titular de tarjeta, durante los seis meses anteriores.

- **Actividad de cuenta sospechosa**: Indica si el solicitante de 3DS ha experimentado una actividad sospechosa (incluído un fraude anterior) en la cuenta del titular de la tarjeta.

- **Indicador de nombre de envío**: Indica si el nombre del titular de la tarjeta en la cuenta es idéntico al nombre de envío utilizado para esta transacción. 

- **Indicador de antigüedad de la cuenta de pago**: Indica el periodo de tiempo que la cuenta de pago estuvo inscrita en la cuenta del titular de la tarjeta con el solicitante de 3DS, los valores recibidos son de 2 caracteres, y son de tipo numérico.

    Los valores recibidos son:
    -   01 = sin cambios
    -   02 = Modificado durante esta transacción
    -   03 = 30 – 60 días
    -   04 = Mas de 60 días

- **Antigüedad de la cuenta de pago**: Fecha en que la cuenta de pago se inscribió en la cuenta del titular de la tarjeta con el solicitante de 3DS, el tipo de dato que se recibe es en el formato AAAAMMDD.

- **Tipo de cuenta**: Indica el tipo de cuenta. Por ejemplo, para una tarjeta con varias cuentas. Los valores recibidos son de 2 caracteres, y son de tipo numérico.                                                                           
    Los valores recibidos son:
    -   01 = No aplicable
    -   02 = Credito 
    -   03 = Debito
    -   04 - 79 = Reservado para valores a futuro EMVCo 
    -   80 - 99 = DS o pagos de sistemas especificos

- **BIN del adquirente**: Código de identificación de la institución según lo asignado por el DS que recibe el mensaje AReq. Este valor se correlaciona con el BIN del comprador según lo definido por cada sistema de pago o DS.
    
- **ID de comerciante del adquirente**: Identificador del comerciante asignado por el adquirente. Este puede ser el mismo valor que se utiliza en las solicitudes de autorización enviadas en nombre del solicitante 3DS y está representado en los requisitos de formato ISO 8583.
    
    El valor aceptado:
    Los servidores de directorio individuales pueden imponer requisitos específicos de formato y carácter en el contenido de este campo. Tiene una longitud de 35 caracteres. 

- **Indicador de coincidencia de direcciones**: Indica si la dirección de envío del titular de la tarjeta y la dirección de facturación del titular de la tarjeta son iguales.
    
    Los valores recibidos son:
    -   Y = La dirección de envío coincide con la facturación
    -   N = La dirección de envío no coincide con la dirección de facturación
    
- **Ciudad de la dirección de facturación del titular de la tarjeta**: La ciudad de la dirección de facturación del titular de la tarjeta asociada con la tarjeta utilizada para esta compra. Los valores a recibir son de un tamaño máximo 50 caracteres. 

- **País de la dirección de facturación del titular de la tarjeta**: Es el país de la dirección de facturación del titular de la tarjeta asociada con la tarjeta utilizada para esta compra. El valor aceptado es el código de país numérico de tres dígitos según el ISO 3166-1.

- **Línea 1 de la dirección de facturación del titular de la tarjeta**: Primera línea de la dirección postal o parte local equivalente de la dirección de facturación del titular de la tarjeta asociada con la tarjeta utilizada para esta compra. El valor aceptado es de un tamaño máximo de 50 caracteres.
    
- **Dirección de facturación del titular de la tarjeta, línea 2**: Segunda línea de la dirección postal o parte local equivalente de la dirección de facturación del titular de la tarjeta asociada con la tarjeta utilizada para esta compra. El valor aceptado es de un tamaño máximo de 50 caracteres.

- **Dirección de facturación del titular de la tarjeta, línea 3**: Tercera línea de la dirección postal o parte local equivalente de la dirección de facturación del titular de la tarjeta asociada con la tarjeta utilizada para esta compra. El valor aceptado es de un tamaño máximo de 50 caracteres.

- **Dirección de facturación del titular de la tarjeta - código postal**: ZIP u otro código postal de la dirección de facturación del titular de la tarjeta asociada con la tarjeta utilizada para esta compra. El valor aceptado es de un tamaño maximo de 16 caracteres.

- **Estado de la dirección de facturación del titular de la tarjeta**: El estado o provincia de la dirección de facturación del titular de la tarjeta asociada con la tarjeta utilizada para esta compra. El valor aceptado debe ser el código de subdivisión del país definido en ISO 3166-2, conformado por 3 caracteres.

- **Canal de dispositivo**: Indica el tipo de interfaz de canal que se utiliza para iniciar la transacción.
    
    Los valores recibidos son:
    
    -   01 = Basado en aplicaciones (APP)
    -   02 = Navegador (BRW)
    -   03 = Solicitante de 3DS Iniciado (3RI)
    -   04–79 = Reservado para uso futuro de EMVCo (valores no válidos hasta que los defina EMVCo)
    -   80–99 = Reservado para uso de DS
    
- **Dirección de correo electrónico del titular de la tarjeta**: La dirección de correo electrónico asociada con la cuenta que ingresó el titular de la tarjeta o que está archivada con el Solicitante de 3DS. El valor aceptado deberá cumplir con los requisitos de la Sección 3.4 de IETF RFC 5322.
    
- **Código del país del número de teléfono de la casa del titular de la tarjeta**: El codigo del teléfono residencial proporcionado por el titular de la tarjeta. El valor recibido es de 1 a 3 caracteres.
    
- **Número de teléfono de la casa del titular de la tarjeta**: El número de teléfono residencial proporcionado por el titular de la tarjeta. El valor recibido es de máximo 15 caracteres. 
    
- **Código de categoría de comerciante**: Código específico de DS que describe el tipo de negocio, producto o servicio del comerciante. Este valor se correlaciona con el código de categoría de comerciante según lo definido por cada sistema de pago o DS.
    
- **Código de país del comerciante**: Este valor se correlaciona con el código de país del comerciante según lo definido por cada cistema de pago o DS. El valor recibido es de 3 caracteres. 
    
- **Nombre del comerciante**: Nombre del comerciante asignado por el adquiriente o sistema de Pago. El valor a recibir es mayor a 40 caracteres. 
    
- **Indicador de envío**: Indica el método de envío elegido para la transacción. Los comerciantes deben elegir el código del indicador de envío que describa con mayor precisión la transacción específica del titular de la tarjeta, no su negocio general. Si uno o más artículos están incluidos en la venta, use el código de indicador de envío para los bienes físicos, o si todos son bienes digitales, use el código de indicador de envío que describe el artículo más caro.
    
    Los valores recibidos son:
    
    -    01 = Enviar a la dirección de facturación del titular de la tarjeta
    -    02 = Enviar a otra dirección verificada registrada con comerciante
    -    03 = Dirección de envío que es diferente a la dirección de facturación del titular de la tarjeta
    -    04 = "Enviar a la tienda" / Recoger en la tienda local (la dirección de la tienda se completará en los campos de dirección de envío)
    -    05 = Productos digitales (incluye servicios en línea, tarjetas de regalo electrónicas y códigos de canje)
    -    06 = Boletos de viaje y eventos, no enviados
    -    07 = Otro (por ejemplo, juegos, servicios digitales no enviados, suscripciones a emedia, etc.)
    
- **Plazo de entrega**: Indica el plazo de entrega de la mercancía.

    Los valores recibidos son:
    
    -    01 = Entrega electrónica
    -    02 = Envío el mismo día
    -    03 = Envío al día siguiente
    -    04 = Envío en dos días o más
    
- **Dirección de correo electrónico de entrega**: Para entrega electrónica, la dirección de correo electrónico a la que se entregó la mercancía. El valor máximo es de 254 caracteres. 
    
- **Indicador de reordenar artículos**: Indica si el titular de la tarjeta está reordenando mercancía comprada anteriormente.
    
    Los valores recibidos son:
    
    -   01 = Pedido por primera vez
    -   02 = Reordenado
    
- **Indicador de compra anticipada**: Indica si el Titular de la tarjeta está realizando un pedido de mercancía con una disponibilidad futura o una fecha de lanzamiento.
    
    Los valores recibidos son:
    
    - 01 = Mercancía disponible
    - 02 = Disponibilidad futura
    
- **Fecha de reserva**: Para una compra pre-ordenada, la fecha esperada en que la mercancía estará disponible, el tipo de dato que se recibe es en el formato AAAAMMDD.
    
- **Monto de la tarjeta de regalo**: El monto de la tarjeta de regalo.
    
- **Moneda de la tarjeta de regalo**: La moneda de uso en la compra de la tarjeta de regalo. 
    
- **Recuento de tarjetas de regalo**: Cantidad de tarjetas de regalo. 

- **Categoría de mensaje**: Identifica la categoría del mensaje para un caso de uso específico.
    
    Los valores recibidos son:
    
    - 01 = PA
    - 02 = NPA
    - 03–79 = Reservado para uso futuro de EMVCo (valores no válidos hasta que los defina EMVCo)
    - 80–99 = Reservado para uso de DS
    
- **Código del país del número de teléfono móvil del titular de la tarjeta**: El código del teléfono móvil proporcionado por el titular de la tarjeta. El valor recibido es de 1 a 3 caracteres.

- **Número de teléfono móvil del titular de la tarjeta**: El número de teléfono móvil proporcionado por el titular de la tarjeta. El valor recibido es de maximo 15 caracteres. 

- **Moneda de compra**: Moneda en la que se expresa el monto de la compra. El valor a recibir es el código de moneda de tres dígitos según el ISO 4217.

- **Fecha de compra**: Fecha y hora de la compra expresada en UTC.

- **Datos de pago a plazos**: Indica el número máximo de autorizaciones permitidas para pagos a plazos.
    
- **Caducidad recurrente**: Fecha a partir de la cual no se realizarán más autorizaciones.
    
- **Frecuencia recurrente**: Indica el número mínimo de días entre autorizaciones.

- **Ciudad de la dirección de envío del titular de la tarjeta**: Parte de la ciudad de la dirección de envío solicitada por el titular de la tarjeta. El valor recibido es de maximo 50 caracteres. 

- **País de la dirección de envío del titular de la tarjeta**: País de la dirección de envío solicitada por el Titular de la Tarjeta. El valor aceptado es el código de país de tres dígitos ISO 3166-1.
    
- **Dirección de envío del titular de la tarjeta 1**: Primera línea de la dirección postal o parte local equivalente de la dirección de envío solicitada por el titular de la tarjeta. El valor recibido es de máximo 50 caracteres. 
                                                                   
- **Dirección de envío del titular de la tarjeta 2**: Segunda línea de la dirección postal o parte local equivalente de la dirección de envío solicitada por el titular de la tarjeta. El valor recibido es de maximo 50 caracteres. 
    
- **Dirección de envío del titular de la tarjeta 3**: Tercera línea de la dirección postal o parte local equivalente de la dirección de envío solicitada por el titular de la tarjeta. El valor recibido es de maximo 50 caracteres. 
   
- **Código postal de la dirección de envío del titular de la tarjeta**: El ZIP u otro código postal de la dirección de envío solicitada por el titular de la tarjeta. El valor recibido es de maximo 16 caracteres.
    
- **Estado de la dirección de envío del titular de la tarjeta**: El estado o provincia de la dirección de envío asociada con la tarjeta que se utiliza para esta compra. El valor aceptado debe ser el código de subdivisión del país definido en ISO 3166-2.

- **Indicador de desafío del solicitante de 3DS**: El código del desafío del solicitante que entrega 3DS.
    
- **Datos de autenticación de transacciones previas del solicitante 3DS**:  Datos que documentan y respaldan un proceso de autenticación específico. En la versión actual de la especificación, este elemento de datos no está definido en detalle, sin embargo, la intención es que para cada método de autenticación de solicitante 3DS, este campo contenga datos que el ACS pueda usar para verificar el proceso de autenticación. En versiones futuras de la especificación, se espera que se incluyan estos detalles. El valor recibido es de maximo 2048 caracteres.             

- **Método de autenticación de transacción previa del solicitante 3DS**: Mecanismo utilizado por el titular de la tarjeta para autenticarse previamente ante el Solicitante 3DS.
    
    Los valores recibidos son:
    
    - 01 = Autenticación sin fricciones realizada por ACS
    - 02 = Desafío del titular de la tarjeta ocurrido por ACS
    - 03 = AVS verificado
    - 04 = Otros métodos de emisor
    - 05–79 = Reservado para uso futuro de EMVCo (valores no válidos hasta que los defina EMVCo)
    - 80–99 = Reservado para uso de DS
    
- **Marca de tiempo de autenticación de transacción previa del solicitante 3DS**: Fecha y hora en UTC de la autenticación del titular de la tarjeta anterior.
    
- **Referencia de transacción previa del solicitante 3DS**: Este elemento de datos proporciona información adicional al ACS para determinar el mejor enfoque para entregar una solicitud.

- **ID de operador del servidor 3DS**: Identificador del operador que entrega el servidor de 3DS.
    
- **Indicador 3RI**: Indica el tipo de solicitud 3RI.
  Este elemento de datos proporciona información adicional al ACS para determinar el mejor enfoque para entregar una solicitud de tipo 3RI.
    
    Los valores recibidos son:
    
    - 01 = Transacción recurrente
    - 02 = Transacción a plazos
    - 03 = Agregar tarjeta
    - 04 = Mantener tarjeta información
    - 05 = Verificación de la cuenta
    - 06 = Envío dividido / retrasado
    - 07 = T op-up
    - 08 = Pedido por correo
    - 09 = Pedido de teléfono
    - 10 = Verificación del estado de la lista blanca
    - 11 = Otro pago
    - 12–79 = Reservado para uso futuro de EMVCo (valores no válidos hasta que los defina EMVCo)
    - 80–99 = Reservado para uso de DS
    
- **Tipo de transacción**: Identifica el tipo de transacción que se autentica.
    
    Los valores recibidos son:
    
    - 01 = Compra de bienes / servicios
    - 03 = Aceptación de cheques
    - 10 = Financiamiento de la cuenta
    - 11 = Cuasi efectivo transacción
    - 28 = Activación y carga prepago
    *Nota: Valores derivados de la norma ISO 8583.*
    
- **Estado de la lista blanca**: Permite la comunicación del estado de la lista blanca para los beneficiarios de confianza entre ACS, DS y 3DS Requestor.
    
    Los valores recibidos son:
    
    - Y = 3DS Requestor está incluido en la lista blanca por titular de la tarjeta
    - N = El solicitante de 3DS no está incluido en la lista blanca por parte del titular de la tarjeta
    - E = No elegible según lo determinado por el emisor
    - P = Pendiente de confirmación por titular de la tarjeta
    - R = Tarjetahabiente rechazada
    - U = Estado de la lista blanca desconocido, no disponible o no se aplica
    
    *Nota: Los valores válidos en el mensaje AReq son Y o N*
    
- **Fuente de estado de la lista blanca**: Este elemento de datos se completará con la configuración del sistema de estado de la lista blanca.
    
    Los valores recibidos son:
    
    - 01 = Servidor 3DS
    - 02 = DS
    - 03 = ACS
    - 04-79 = Reservado para uso futuro de EMVCo (valores no válidos hasta que los defina EMVCo)
    - 80-99 = Reservado para uso de DS
    
- **Código del país del número de teléfono del trabajo del titular de la tarjeta**: El código del teléfono del trabajo proporcionado por el titular de la tarjeta. El valor recibido tiene de 1 a 3 caracteres.

- **Número de teléfono del trabajo del titular de la tarjeta**: El número de teléfono del trabajo proporcionado por el titular de la tarjeta. El valor recibido es de maximo 15 caracteres. 

### Reglas de puntuación:

<br>

#### Regla de puntuación del emisor:
Esta regla valida la solicitud de autenticación a partir de la puntuación que tenga el emisor que procesa la transacción. La regla permite asignar el operador de comparación con el valor final que le va a asignar.

#### Regla de puntuación histórica:
Esta regla valida la solicitud de autenticación a partir de la puntuación que tenga el tarjetahabiente históricamente. Se evalúa a partir de transacciones anteriores. La regla permite asignar el operador de comparación con el valor final que le va a asignar.

#### Regla de puntuación RBA Master Card:
Esta regla valida la solicitud de autenticación a partir de la puntuación de riesgo evaluada para MasterCard. La regla permite asignar el operador de comparación con el valor final que le va a asignar.

 Los operadores disponibles para las reglas de puntuación son:
  - **Entre**, acepta un valor mínimo y uno máximo. El dato en la autenticación debe estar en el rango para pasar la validación.

  - **Menor que**, acepta un valor y valida que el dato de la autenticación sea menor al valor dado en la regla.

  - **Menor o igual que**, acepta un valor y valida que el dato de la autenticación sea menor o igual al valor dado en la regla.

  - **Mayor que**, acepta un valor y valida que el dato de la autenticación sea mayor al valor dado en la regla.

  - **Mayor o igual que**, acepta un valor y valida que el dato de la autenticación sea mayor o igual al valor dado en la regla.

  - **Igual a**, acepta un valor y valida que el dato de la autenticación sea igual al valor dado en la regla.

*Un ejemplo de una regla de puntuación es el siguiente:*

  ![](https://wiki.placetopay.com/images/8/8d/Score-rule.png)

### Reglas de coincidencia o match:

<br>

#### Regla de coincidencia para correo electrónico: 
Esta regla permite validar si el correo electrónico del tarjetahabiente que llega en los datos de autenticación, coincide con el correo electrónico guardado para el mismo tarjetahabiente en transacciones anteriores. 

Acepta uno de los siguientes dos valores: hacer match (encontrar coincidencia) o no hacer match (No encontrar coincidencia).

#### Regla de coincidencia para teléfono móvil:
Esta regla permite validar si el teléfono móvil del tarjetahabiente que llega en los datos de autenticación, coincide con el número de teléfono móvil guardado para el mismo tarjetahabiente en transacciones anteriores. 

Acepta uno de los siguientes dos valores: hacer match (Encontrar coincidencia) o no hacer match (No encontrar coincidencia).

#### Regla de coincidencia para teléfono fijo:
Esta regla permite validar si el teléfono fijo del tarjetahabiente que llega en los datos de autenticación, coincide con el número de teléfono fijo guardado para el mismo tarjetahabiente en transacciones anteriores. 

Acepta uno de los siguientes dos valores: hacer match (Encontrar coincidencia) o no hacer match (No encontrar coincidencia).

#### Regla de coincidencia para teléfono del trabajo:
Esta regla permite validar si el teléfono del trabajo del tarjetahabiente que llega en los datos de autenticación, coincide con el número de teléfono del trabajo guardado para el mismo tarjetahabiente en transacciones anteriores. 

Acepta uno de los siguientes dos valores: hacer match (Encontrar coincidencia) o no hacer match (No encontrar coincidencia).

#### Regla de coincidencia para el dispositivo:
Esta regla permite validar si el fingerprint o huella digital del tarjetahabiente que se crea en la transacción, coincide con algún fingerprint guardado para el mismo tarjetahabiente en transacciones exitosas anteriores. El fingerprint es un método que registra automáticamente un identificador de un usuario, a partir de la información captada con el dispositivo usado al realizar una transacción o un movimiento digital.

Acepta uno de los siguientes dos valores: hacer match (Encontrar coincidencia) o no hacer match (No encontrar coincidencia).

*Un ejemplo de una regla tipo match es el siguiente:*

![](https://wiki.placetopay.com/images/3/33/Match-mobile-phone-rule.png)

Encontrará en el campo *Valor*, una lista con dos opciones, hacer match (Encontrar coincidencia) o no hacer match (No encontrar coincidencia) con el dato guardado en ACS.


## Grupos de control de fraude

Los grupos de control de fraude permiten clasificar y agrupar reglas para hacer validaciones con fines específicos. 

Por ejemplo, puede crear dos grupos, uno llamado *Lista blanca*, donde se podrían incluir números de tarjetas y datos de clientes con bajo riesgo de fraude y las acciones de las reglas podrían ser en su mayoría *Autenticar*. El otro grupo se llama *Lista negra*, aquí se podrían agregar los números de tarjeta e información personal asociada a clientes con historiales o reportes riesgosos y la acción de las reglas podría ser *No autenticar*.

### Índice de grupos de control de fraude:

Para acceder al índice de grupos de reglas, diríjase al menú **Gestionar control de fraude -> Grupos de control de fraude**, ubicado en las pestañas de la parte superior del detalle de un emisor.

En la siguiente imagen se muestra un listado de grupos de control de fraude de un emisor. La información se encuentra organizada en una tabla y muestra los datos principales de los grupos tales como: Nombre, fecha, reglas y estado.

![](https://wiki.placetopay.com/images/7/7b/Group-index.png)

### ¿Cómo crear un nuevo grupo de reglas?

Para crear un grupo, haga clic el botón **Crear** ubicado en la parte lateral derecha del índice de grupos. Se desplegará un formulario similar al siguiente:

![](https://wiki.placetopay.com/images/0/08/Create-group.png)

En el formulario solo debe ingresar el nombre que desea que tenga el grupo, luego haga clic en el botón *Guardar*.

> Un grupo de reglas solo se ejecuta cuando al crear una nueva regla, se escoge la opción *Ejecutar grupo de reglas*, se selecciona el grupo específico, y posteriormente, se habilita la regla.

### Detalles de un grupo:

Para visualizar los detalles de un grupo, haga clic en el botón **Ver**, ubicado en la parte lateral derecha de la tabla, al frente de cada grupo.

Visualizará una vista como la siguiente:

![](https://wiki.placetopay.com/images/6/68/Detalle-grupo-antifraude.png)

#### Habilitar y deshabilitar un grupo:
Para habilitar o deshabilitar un grupo, haga clic en el menú lateral derecho, en el detalle del grupo y deslice el botón tipo switch para habilitar o deshabilitar según corresponda.

#### Reglas de un grupo:
En la parte inferior del detalle de un emisor, encontrará el listado de reglas en producción del grupo, listadas en una tabla que muestra el estado de la regla, el nombre y la acción que ejecutan al validar. 
Puede habilitarlas o deshabilitarlas, haciendo clic en el menú desplegable ubicado al final de cada regla. También, puede visualizar los detalles de cada regla presionar el botón con la leyenda *Ver*.

#### Solicitudes de reglas:
Esta funcionalidad se comporta igual a la sección de solicitudes de las *Reglas de control antifraude*, con la diferencia que las solicitudes de reglas que se hagan para crear, actualizar o eliminar reglas, se guardarán exclusivamente para el grupo escogido.

> Luego de crear una solicitud de regla, recuerde aprobarla y posteriormente, habilitarla en el menú de *Reglas en producción*.

<!--
type: tab
title: Gestión de configuraciones
-->

# Configuraciones del emisor

<br>

## ¿Cómo acceder a este menú?

Para acceder a este menú, haga clic en el menú **Configuraciones**, del detalle del emisor. 

Luego visualizará una vista similar a la siguiente:

![](https://wiki.placetopay.com/images/f/fd/Config-general.png)

En la parte inferior de la vista, encontrará tres pestañas que contienen los campos de configuración de los emisores, agrupados en tres secciones: **General, Vistas de Desafíos y Servicios**.

Ingresando a cada una de las pestañas, podrá ver la información de los campos del emisor organizada en tablas, en las cuales se muestra el nombre, el valor inicial del campo, el estado del mismo y las acciones disponibles.

## Categorías de los campos de configuración: 

  - **General:** Los campos registrados en esta categoría permiten configurar comportamientos generales de la aplicación.

 - **Vistas de desafíos:** Los campos registrados en esta categoría permiten configurar las interfaces de usuario para los diferentes tipos de OTP (código de un solo uso, OTP con única y múltiple opción de selección y OTP fuera de banda).

  - **Servicios:** Los campos registrados en esta categoría validan las estrategias a utilizar para implementar servicios del ACS como el OTP, el servicio de información del tarjetahabiente o los servicios de acceso y autorización a la aplicación. Así como los valores particulares para configurar cada una de estas estrategias.

> Para una mejor comprensión del funcionamiento de los campos de configuración y de las categorías, remítase a la sección *Otras configuraciones*, pestaña *Campos de configuración* de la presente documentación.


## Acciones para las configuraciones del emisor:

Para visualizar las acciones disponibles para los campos de configuración, haga clic en el menú desplegable ubicado al final de cada campo.

Las acciones disponibles son:

- **Ver:** Seleccione para visualizar los detalles de configuración del campo.

- **Editar:** Seleccione para editar algún valor de la configuración con la cual se creó inicialmente el campo.

    > Edite los campos de configuración teniendo en cuenta la lógica de negocio y el funcionamiento del emisor específico.

- **Habilitar / Deshabilitar:** Deslice el botón tipo switch para habilitar o deshabitar el campo según corresponda con el estado actual.

  > Tenga en cuenta que si deshabilita un campo de los que están por defecto, el emisor no podrá ser habilitado.


<!--
type: tab
title: Gestión de servicios del emisor
-->

# Servicios del emisor

<br>

## ¿Cómo acceder a este menú?

En la pestaña **Servicios** de las configuraciones, se encuentran las estrategias disponibles para ejecutar servicios de ACS para el emisor. Estas son:

## cardholderStrategy

Esta estrategia permite definir cómo se va a implementar el servicio de información del tarjetabiente. Para ello en el valor del campo, se ingresa la estrategia correspondiente. 

  En el momento se dispone de las siguientes estregias:

  - **Standard Strategy:** Permite autenticar las solicitudes que lleguen al ACS con la estrategia estandar, mediante la cual se toma la decisión de autenticar o no, conforme a la información del tarjetahabiente recibida.

  - **Standard No Auth Strategy:** Permite no autenticar las solicitudes que lleguen al ACS con la estrategia estandar.

  - **No Service Strategy:** No valida la información del tarjetahabiente y pasa a ejecutar las reglas de validación correspondientes para aprobar o denegar la autenticación.

  - **SisCard Strategy:** Permite autenticar las solicitudes que lleguen al ACS mediante el servicio de SisCard.

  Para la estrategia seleccionada debe configurar los siguientes valores:

  - **cardholderInfoURL:** Ingrese una URL válida para conectar con el servicio externo para obtener la información del tarjetahabiente.

  - **cardholderInfoUser:** Ingrese el usuario provisto por el servicio de cardholder con el cual se va a conectar y el cual le permitirá autenticarse.

  - **cardholderInfoPassword:** Ingrese la contraseña provista por el servicio de cardholder para completar la autenticación.

## otpStrategy

Esta estrategia permite definir cómo se va a implementar el servicio del OTP (Autenticación con contraseña de un solo uso), para el emisor específico.  Para ello en el valor del campo, se ingresa la estrategia correspondiente. 

  En el momento se dispone de las siguientes estregias:

  - **Standard Strategy:** Para enviar y validar el OTP se utiliza un servicio propio de PlacetoPay.

  - **Diners Strategy:** Para enviar y validar el OTP se utiliza un servicio propio de Diners.

  Para la estrategia seleccionada debe configurar los siguientes valores:

  - **otpURL:** Ingrese una URL válida para consumir el servicio externo para el envío del OTP.

  - **otpSize:** Ingrese un número que indique el número de dígitos que debe tener el OTP.

  - **otpRuleRegex:** Ingrese la expresión regular que permitirá validar el OTP ingresado.
  
  - **otpAuthMethod:** Seleccione el indicador para el método de autenticación con el servicio de OTP.


## authStrategy

Esta estrategia permite definir cómo se va a implementar el servicio de autorización a ACS. Este servicio se utilizará cuando ACS requiera consumir un servicio externo que a su vez necesite algún tipo de autenticación o autorización mediante token. Para ello en el valor del campo, se ingresa la estrategia de autenticación OAuth correspondiente. 

  En el momento se dispone solo de un tipo de estrategia:

- **Standard OAuth Strategy:** Permite autorizar el acceso a un servicio consumido por ACS con una estrategia estándar, mediante la utilización de un Bearer token.

 También debe configurar los siguientes valores para la estrategia:

  - **authURL:** Ingrese una URL válida para consumir el servicio externo de autorización OAuth.

  - **authUsername:** Ingrese el usuario provisto por el servicio de autorización OAuth con el cual se va a conectar y el cual le permitirá autenticarse.

  - **cardholderInfoPassword:** Ingrese la contraseña provista por el servicio de autorización OAuth para completar la autenticación.
  

> Estas estrategias deben estar tener sus valores particulares de configuración diligenciados, para poder habilitarse posteriormente.

<!-- type: tab-end -->