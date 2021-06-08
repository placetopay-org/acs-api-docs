<!--
type: tab
title: Generalidades del emisor
-->

# Emisores en ACS

## ¿Qué es un emisor?

Un emisor o banco emisor, es la institución financiera responsable de emitir los medios de pago, como tarjetas de débito o de crédito. Estas tarjetas de pago se emiten con la marca de la asociación de tarjetas o franquicia. También pueden existir emisores de tarjetas de pago propias y no franquiciadas.

Entre las funciones de un emisor están:

- El emisor tiene la responsabilidad de autorizar o denegar una transacción cuando recibe los datos de la compra. 

- El emisor se encarga de transferir el dinero de una compra hecha por el consumidor, al adquiriente, que a su vez es quien paga al comercio y mantiene relación con este. 

- El emisor debe dar el mantenimiento requerido a cuentas y tarjetas.

- El emisor es responsable de resolver cargos disputados a su favor, por motivos de fraudes o riesgos.

- El emisor se encarga de activar, suspender y bloquear una tarjeta de pago cuando se requiera.


## ¿Cómo acceder a la gestión de emisores de ACS?

Para acceder al listado de emisores de la aplicación siga los siguientes pasos:

1. Remítase al menú lateral izquierdo dónde visualizará tres opciones, "Dashboard", "Sistema" y "Seguridad", como muestra la siguiente imagen:

![](https://wiki.placetopay.com/images/a/ac/Lateral-menu.png)

2. Haga clic en el menú "Sistema", se desplegará un listado de opciones, haga clic en la opción "Emisores".

3. Visualizará una pantalla similar a la siguiente:

![](https://wiki.placetopay.com/images/4/4e/Issuer-index.png)

## ¿Cómo crear un emisor en ACS?

Para crear un emisor, haga clic en el botón Crear ubicado en la parte lateral derecha del índice de emisores.

Visualizará un formulario similar al siguiente:

![](https://wiki.placetopay.com/images/3/35/Create-issuer.png)

Para diligenciarlo tenga en cuenta los siguientes datos:

- **Nombre:** Ingrese en este campo el nombre del banco emisor que va a crear.

- **Idioma:** Seleccione de la lista desplegable el idioma principal con el cual desea que se procesen las autenticaciones para los usuarios.

- **País:** Seleccione de la lista desplegable el país dónde opera el banco emisor.

- **Slug:** Ingrese una cadena clave para el emisor. Esta cadena se agregará a las URL donde se gestionen configuraciones y servicios del emisor.

- **Logo:** Aquí puede cargar una imagen con el logo del emisor. Para hacerlo haga clic en la opción *Seleccionar archivo* y busque la imagen correspondiente al logo en su equipo. La imagen debe tener unas dimensiones máximas de 1000x1000.

### Validación de datos:

Para el formulario de creación de un emisor en ACS, y para todos los formularios en general de la aplicación, se dispone de la funcionalidad de validación de los datos ingresados, lo cual permite asegurar la integridad y funcionalidad de los datos.

De esta forma, al diligencia el formulario puede encontrar dos tipos de validaciones:

1. **Validaciones de lado del cliente:**

    Estas validaciones se realizan cuando un dato no cumple las reglas mínimas de aceptación y no hay necesidad de enviar la respuesta al servidor si se ha validado previamente que está errónea la información. Se visualizan con mensajes en rojo para el campo erróneo y le ofrece al usuario una ayuda de cómo debe diligenciar el campo en cuestión para ser aceptado. Si hay errores en estas validaciones, la aplicación no permite el envío del formulario.

    La siguiente imagen ilustra errores en validaciones del lado del cliente:


    ![](https://wiki.placetopay.com/images/3/30/Issuer-pre-validations.png)

1. **Validaciones de lado del servidor:**

    Estas validaciones se aplican cuando se envía un formulario o una data al servidor y esta no cumple con las validaciones requeridas, por lo cual se genera un error, deniega la solicitud y muestra al usuario el error encontrado. Estas validaciones se ejecutan cuando no se han registrado como validaciones del lado del cliente, o son complicadas de validar del lado del cliente o el usuario logra por algún medio pasar el primer filtro de validaciones del cliente con la información errónea, sin embargo, este filtro de validaciones detiene una solicitud con datos inválidos.

    La siguiente imagen ilustra errores en validaciones del lado del servidor, en la cual se logró enviar el formulario pero al momento de recibirlo se encontraron errores en los datos de la solicitud, por lo cual no pudo ser procesada correctamente:


    ![](https://wiki.placetopay.com/images/9/91/Image-issuer-error.png)    

## ¿Cuáles son los requerimientos para crear un emisor en ACS?

Para crear y configurar un emisor en ACS, este debe haber emitido tarjetas de pago con las franquicias que ya hayan sido certificadas para funcionar en ACS.

Se requiere que el país y el idioma con el cual se vaya a crear el emisor, estén disponibles para ACS.

Se requiere que exista una relación entre emisor, adquiriente y comercio y que estos estén registrados en las aplicaciones de ACS y de MPI de PlacetoPay Evertec, para lograr un proceso de autenticación exitosa. 

Importante tener en cuenta habilitar todos los campos de configuración del menú *Campos de configuración* de la aplicación, antes de crear el emisor, ya que todos estos campos son requeridos para el funcionamiento básico de un emisor.

> En este punto es importante recordar que la aplicación de **MPI** también implementa y pertenece al flujo propuesto por el protocolo 3-D Secure para autenticar un tarjetahabiente.
Pertenece al dominio el adquiriente y entre sus funciones principales están:
  >> - Recibir y responder la petición de autenticación enviada por el comercio o pasarela de pagos.
  >> - Solicitar al emisor la autorización del pago.
  >> - Responder al comercio o pasarela de pagos el estado final de la autenticación.


## Índice de emisores

En esta sección se visualiza el listado o índice de emisores, la información se presenta en una tabla donde se muestran los datos principales de cada emisor, tales como: Nombre, País y Estado. 

![](https://wiki.placetopay.com/images/4/4a/Issuer-actions.png)

### Acciones disponibles para los emisores:

En el título "Acciones" ubicado en la parte lateral derecha del índice de emisores, se encuentra un menú con tres puntos,haga clic en este menú y despliegue las acciones o funcionalidades disponibles para cada emisor. En el menú se encuentran las siguientes acciones:

- **Ver:** Seleccione esta opción para visualizar los detalles del emisor, sus configuraciones y componentes.

  Visualizará una vista similar a la siguiente:

![](https://wiki.placetopay.com/images/f/f6/Issuer-detail.png)

- **Editar:** Seleccione esta opción para actualizar o corregir los datos con los cuales creó el emisor. 

  Visualizará un formulario similar al de creación del emisor. Todos los datos son editables.

![](https://wiki.placetopay.com/images/3/3c/Edit-issuer.png)

- **Habilitar o Deshabilitar:** Deslice el botón tipo switch para habilitar el emisor si se encuentra deshabilitado o para deshabilitarlo cuando se encuentre habilitado. 

![](https://wiki.placetopay.com/images/8/81/Issuer-actions-toggle.png)

Al habilitar o deshabilitar, la aplicación le entregará un mensaje de confirmación similar al siguiente e inmediatamente cambiará el estado del emisor editado.

![](https://wiki.placetopay.com/images/c/ca/Issuer-toggle.png)

### ¿Cómo habilitar un emisor?

1. **Active los campos de configuración requeridos:** En el menú *Campos de configuración* de la aplicación, habilite todos los campos de configuración (debe habilitarlos antes de crear el emisor), ya que estos son requeridos para la habilitación del emisor. Para obtener más información de los campos de configuración, vaya al título *Campos de configuración* del presente documento.

    La siguiente imagen muestra un índice de los campos de configuración donde todos los campos visibles están habilitados, así deben estar para comenzar a configurar correctamente el emisor.

    ![](https://wiki.placetopay.com/images/3/31/Configuration-fields.png)

2. **Habilitar estrategias del emisor:** En los detalles del emisor, en la parte inferior y la última pestaña encontrará un menú con el nombre de *SERVICES*, donde encontrará las estrategias disponibles para el emisor (esta funcionalidad se explica más adelante), debe habilitar ambas estrategias.

    Un ejemplo del menú *Services* es el siguiente:

   ![](https://wiki.placetopay.com/images/5/5b/Strategies.png)

    
    Nótese que en la imagen anterior, la estrategia con
    nombre *cardholderStrategy*, se encuentra deshabilitada. Si se intentara habilitar el emisor con esta o ambas estrategias deshabilitadas, arrojaría un error como el siguiente y no permitiría ejecutar la habilitación del emisor.

    ![](https://wiki.placetopay.com/images/0/07/Error-enable-issuer.png)


3. **Suscribir franquicia al emisor:** En la pestaña *Franquicias suscritas* del detalle del emisor, seleccione una franquicia del listado, sino hay franquicias disponibles, debe ir al menú *Franquicias* de la aplicación y crear una nueva franquicia para el emisor, para esto guíese de la sección *Configuración de franquicias* de la presente documentación.

    > La franquicia seleccionada debe ser diferente a franquicias previamente suscritas a otros emisores. 
    
4. **Configurar rangos de tarjeta para el emisor:** En la pestaña *Gestionar rangos de tarjetas* del detalle del emisor, haga clic en el botón *Crear* y cree rangos de tarjeta manuales o por importación, para ello guíese de la sección *Gestión de rangos de tarjetas* del presente documento.
    
5. **Crear certificado tipo Cliente para las franquicias del emisor:** Para habilitar un emisor debe crear un certificado tipo *CLIENT*, en el menú de *Certificados*, y seleccionar el emisor correspondiente y una franquicia suscrita para el mismo emisor. Luego debe firmar el certificado con la entidad certificadora y en el índice de certificados, este debe registrar en el campo *Certificado* con el estado *Encontrado*, que indica que fue validado correctamente. 

    Para crear el certificado, guíese de la sección *Otras configuraciones* pestaña *Certificados SSL*.

    Un ejemplo de la primera vista del formulario de creación de un certificado es el siguiente:

    ![](https://wiki.placetopay.com/images/8/8a/Client-certificate.png)

## Detalles de un emisor

### Información principal del emisor:

Para ir a los detalles de un emisor, haga clic en la acción *Ver* del menú desplegable del emisor, ubicado en el índice de emisores. 

En la siguiente imagen se visualiza un ejemplo de la parte superior de la vista de *Detalles de un emisor*. En la vista se encuentra la información con la cual se creó el emisor, el estado en que se encuentra el emisor (está habilitado o no),las fechas de creación del emisor y de actualización y los usuarios que hicieron la creación y/o la actualización.

En la parte lateral derecha hay un recuadro en el cual se debe mostrar el logo del emisor, para este ejemplo no se cargó una imagen, por lo cual se muestra en negro.

Además, en la parte lateral derecha, hay un botón para acceder al formulario de edición en caso de requerirlo.

En la parte superior derecha de la vista actual, se encuentran pestañas que permiten acceder a otros menús de configuración de un emisor, los cuales se revisarán más adelante.

![](https://wiki.placetopay.com/images/6/63/Issuer-detail-basic-info.png)

### Configuraciones del emisor:

En la parte inferior de la vista del detalle de un emisor, se encuentra la sección correspondiente a la gestión de configuración de campos del emisor.

Ingresando a cada una de las pestañas (GENERAL, UI_OTP, SINGLE_SELECT, UI_MULTI_SELECT, UI_OOB), podrá ver la información de los campos del emisor organizada en tablas, en las cuales se muestra el nombre, el valor inicial del campo y el estado del mismo.

La siguiente imagen muestra una vista de configuraciones de un emisor.

![](https://wiki.placetopay.com/images/6/6b/Acs-issuers-configurations.png)

Los títulos de las pestañas de la sección esta *Configuraciones*, hacen referencia a las categorías en las cuales se ubican los campos de configuración del emisor.

#### Categorías de los campos de configuración: 

  - **GENERAL:** Los campos registrados en esta categoría aplican para todos los tipos de interfaces de usuario utilizadas en autenticaciones con desafío.

  - **UI_OTP:** Los campos registrados en esta categoría  validan el desafío con una interfaz de usuario para OTP (código de un solo uso).

  - **UI_SINGLE_SELECT:** Los campos registrados en esta categoría validan el desafío con una interfaz de usuario diseñada para que se seleccione una única opción para el desafío.

  - **UI_MULTI_SELECT:** Los campos registrados en esta categoría validan el desafío con una interfaz de usuario diseñada para seleccionar múltiples opciones en un desafío. 

  - **UI_OOB:** Los campos registrados en esta categoría  validan el desafío con una interfaz de usuario fuera de banda (OOB), la cual permite a los emisores utilizar otros métodos de autenticación como por ejemplo la aplicación móvil de un emisor.

  - **SERVICES:** Los campos registrados en esta categoría validan las estrategias a utilizar para implementar servicios del ACS como el OTP o el servicio de información del tarjetahabiente.


> Para una mejor comprensión del funcionamiento de los campos de configuración y de las categorías, remítase a la sección *Otras configuraciones*, pestaña *Campos de configuración* de la presente documentación.


#### Acciones para las configuraciones del emisor:

Para visualizar las acciones disponibles para los campos de configuración, haga clic en el menú desplegable con tres puntos, ubicado al final de cada campo, obtendrá un menú como el de la siguiente imagen:

![](https://wiki.placetopay.com/images/3/38/Setting-field-actions.png)

Las acciones disponibles son:

- **Ver:** Seleccione para visualizar los detalles de configuración del campo.

- **Editar:** Seleccione para editar algún valor de la configuración con la cual se creó inicialmente el campo.

    > Edite los campos de configuración teniendo en cuenta la lógica de negocio y el funcionamiento del emisor específico.

- **Habilitar / Deshabilitar:** Deslice el botón tipo switch para habilitar o deshabitar el campo según corresponda con el estado actual.

  > Tenga en cuenta que si deshabilita un campo de los que están por default, el emisor no podrá ser habilitado.


## Estrategias del emisor:

También, en la sección *Configuraciones* del emisor, en la pestaña *SERVICES*, se encuentran las estrategias disponibles para ejecutar servicios de ACS para el emisor.

![](https://wiki.placetopay.com/images/5/5b/Strategies.png)

### otpStrategy

Esta estrategia permite definir a través de un indicador, cómo se va a implementar el servicio del OTP (Autenticación con contraseña de un solo uso), para el emisor específico.  Para ello en el valor del campo, se ingresa la estrategia correspondiente. 

  En el momento se dispone de las siguientes estregias:

  - **PlacetoPayStrategy:** Para enviar y validar el OTP se utiliza un servicio propio de PlacetoPay.

  - **DinersStrategy:** Para enviar y validar el OTP se utiliza un servicio propio de Diners.

### cardholderStrategy

Esta estrategia permite definir a través de un indicador, cómo se va a implementar el servicio de información del tarjetabiente. Para ello en el valor del campo, se ingresa la estrategia correspondiente. 

  En el momento se dispone de las siguientes estregias:

  - **StandardStrategy:** Permite autenticar las solicitudes que lleguen al ACS con la estrategia estandar, mediante la cual se toma la decisión de autenticar o no, conforme a la información del tarjetahabiente recibida.

  - **StandardNoAuthStrategyStandard:** Permite no autenticar las solicitudes que lleguen al ACS con la estrategia estandar.

  - **NoServiceStrategy:** No valida la información del tarjetahabiente y pasa a ejecutar las reglas de validación correspondientes para aprobar o denegar la autenticación.

> Estas estrategias deben estar en estado habilitado para que el emisor pueda ser habilitado al crearse.

## Gestión de franquicias:

Para acceder a este menú, haga clic en el menú *Franquicias suscritas*, que actualmente se ubica al lado derecho del menú *Detalles del emisor*. 

Luego visualizará una vista similar a la siguiente:

![](https://wiki.placetopay.com/images/6/62/Issuer-franchises.png)

En ella encontrará el listado de franquicias agregadas para el emisor y un formulario para agregar nuevas franquicias.

> Para las franquicias solo está disponible la función de *Eliminar*, la cual se ejecuta dando clic en el botón con el mismo nombre ubicado al frente de cada franquicia.

### Agregar una nueva franquicia:

Para suscribir una nueva franquicia a su emisor, dírijase a la primera sección de la vista actual, al apartado *Franquicia* y despliegue la lista de franquicias disponibles haciendo clic en la flecha hacia abajo. Seleccione una franquicia y haga clic en el botón *Agregar*.

![](https://wiki.placetopay.com/images/1/1f/Add-franchise.png)

## Gestión de rangos de tarjetas:

Para acceder a este menú, haga clic en el menú *Gestionar rangos de tarjetas*, ubicado en la parte superior de la vista.

Visualizará un índice similar al siguiente:

![](https://wiki.placetopay.com/images/2/22/Acs-card-ranges-index.png)

En esta sección se importan y crean los rangos de tarjetas aceptadas para un emisor específico. Puede ver la información principal de cada rango organizada en una tabla, entre los datos están: BIN del rango, Rango inicial, Rango final, Franquicia, Clase y las respectivas acciones que tienen cada uno de los rangos.

### Acciones de los rangos de tarjetas:

Las acciones disponibles para los rangos de tarjetas se encuentran ubicadas en el menú desplegable ubicado al final de cada rango. Las acciones son las siguientes:

- **Ver:** Seleccione esta opción para visualizar los detalles del rango y las fechas de creación y actualización y los datos de los usuarios que ejecutaron las acciones.

  Visualizará una vista similar a la siguiente:

![](https://wiki.placetopay.com/images/6/6b/Card-range-detail.png)

- **Editar:** Seleccione esta opción para actualizar o corregir los datos con los cuales creó el emisor. 

  Visualizará un formulario similar al de creación de un rango de tarjeta. Todos los datos son editables.

- **Eliminar:** Seleccione esta opción para eliminar un rango de tarjetas del emisor. Si elimina un rango tenga en cuenta que las solicitudes de autenticación que lleguen con un número de tarjeta que entre en este rango, no podrán ser procesadas.


### ¿Cómo crear un rango de tarjetas?

Al dar clic en el botón *Crear*, se desplegarán dos opciones para crear rangos:

  ![](https://wiki.placetopay.com/images/1/18/Create-button-card.png)

1. **Crear un rango de tarjetas,** este permite crear un rango de forma manual.

  Si selecciona esta opción, obtendrá un formulario similar al siguiente:

  ![](https://wiki.placetopay.com/images/c/c3/Create-card-range.png)

  Para diligenciar el formulario tenga en cuenta:

   -  **Bin del rango:** Ingrese el bin del rango de la tarjeta a crear, este debe ser de 8 dígitos.

   - **Franquicia:** Seleccione el nombre de la franquicia a la cual se le va a registrar el rango.

   - **Clase:** Ingrese el nombre de la clase del rango de tarjetas. Por ejemplo Gold, Platinium...

   - **Rango inicial:** Ingrese los primeros números del BIN y adicione otros números que indiquen el inicio del rango. El valor debe tener 19 dígitos.

  - **Rango final:** Ingrese los primeros números del BIN y adicione otros números que indiquen el final del rango y que sean mayores al rango inicial. El valor debe tener 19 dígitos.


2. **Crear importación,** con esta opción puede importar rangos de tarjetas que tenga en un archivo.

Para crear una importación visualizará un formulario similar al siguiente:

![](https://wiki.placetopay.com/images/b/ba/Acs-create-import-ranges.png)

Debe seleccionar la franquicia para la cual se van a cargar los rangos y un archivo de tipo CSV (archivo de valores separados por comas) que contenga la información de los rangos. Un ejemplo del archivo es este:

![](https://wiki.placetopay.com/images/8/8f/Acs-file-import-example.png)

El archivo debe contener cuatro títulos separados por comas en minúscula:

1. **start_range**: Indica el valor inicial para el rango de tarjetas.

2. **end_range**: Indica el valor final para el rango de tarjetas.

3. **class**: Hace referencia a la clase o tipo de tarjeta utilizada, por ejemplo si es Gold, Platinum.

4. **action**: Debe indicar qué acción se debe ejecutar para el rango indicado, las acciones posibles y sus indicadores son los siguientes:

    **I**: Indicador para acción de insertar rango.

    **U**: Indicador para acción de actualizar rango .

    **D**: Indicador para acción de eliminar rango.


Estos títulos deben seguirse de sus respectivos valores en filas hacia abajo, igualmente separados por comas, sin espacios.

> Para visualizar el formato de un archivo CSV de ejemplo, haga clic en la opción *Descargar* que aparece en el lado izquierdo del formulario.

## Gestión del control de fraude:
Estas funcionalidades están descritas detalladamente en la sección de *Motor Antifraude*. Aquí se hace la gestión de las reglas y de las lostas y grupos donde están contenidas. Las reglas permiten validar los datos que llegan al ACS y garantizar la seguridad de la información, lo cual permitirá aceptar las solicitudes de autenticación que sean realmente válidas y tener filtros que permitan optimizar este proceso de validación.


<!--
type: tab
title: Motor Antifraude
-->

# Motor de Control de Fraude

La principal funcionalidad de ACS es el motor de control antifraude, este permite validar la información que se recibe en la petición de autenticación, a través de un conjunto de reglas que validan las autenticaciones de cada emisor registrado.

Esta funcionalidad se gestiona desde la sección de Emisores de la aplicación.

## Gestionar listas de control de fraude:

Las listas de control de fraude son el primer filtro que por el cual pasan las solicitudes de autenticación de ACS. 

> Las listas de control antifraude se ejecutan antes de los grupos de control antifraude y según los resultados que obtenga de sus validaciones, puede evitar que una autenticación tenga que pasar por las validaciones de los grupos de reglas.

### Índice y acciones de las listas de reglas:

Para acceder al índice de reglas, busque el título *Gestionar listas de control de fraude* en las pestañas ubicadas en la parte superior del detalle de un emisor. Actualmente se ubica a la derecha del menú *Gestionar rangos de tarjetas*.

Al dar clic en el menú, visualizará el índice de listas de reglas, similar al de la siguiente imagen:

![](https://wiki.placetopay.com/images/f/f9/Acs-fraud-list-index.png)


#### Acciones de la reglas:

Las acciones disponibles para las listas de reglas se encuentran ubicadas en el menú desplegable ubicado al final de cada rango en el título *Acciones* de la tabla. Las acciones son las siguientes:

- **Ver:** Seleccione esta opción para visualizar los detalles de la lista.

  Visualizará una vista similar a la siguiente:

![](https://wiki.placetopay.com/images/4/48/List-detail.png)

- **Editar:** Seleccione esta opción para actualizar o corregir los datos con los cuales creó la lista. 

  Visualizará un formulario similar al de creación de un rango de tarjeta. Todos los datos son editables.

- **Eliminar:** Seleccione esta opción para eliminar la lista.

### Filtros para las listas de reglas:

ACS provee para este módulo la funcionalidad de filtrar listas, esta permite hacer la búsqueda más flexible y específica cuando tiene muchos datos. 

Para acceder a los filtros diríjase a la parte lateral derecha del índice de listas, al lado izquierdo del botón *Crear*, encontrará la opción llamada *Filtrar*, haga clic y se desplegará una vista como la siguiente:

![](https://wiki.placetopay.com/images/1/11/Filter-lists.png)

Puede filtrar únicamente por el tipo de lista que desea buscar, seleccione la requerida y haga clic en el botón *Buscar* o en el botón *Limpiar filtros* cuando necesite hacer una nueva búsqueda.


### Tipos de listas de reglas:

Estas listas son temporales, es decir, tienen una duración específica que usted le asigna al crearla, y se dividen en dos clases:

- **Permisivas:** Estas listas van a crear un filtro que va a permitir que las autenticaciones que cumplan con los valores registrados en estas, puedan eximirse de la ejecución de los grupos de reglas, y continuar así con el proceso de autenticación.

> En esta lista puedes agregar valores de clientes con historiales seguros y confiables, ya que al ser permisiva, será más flexible al momento de hacer la validación de la autenticación.

- **Restrictivas:** Por el contrario, este tipo de listas, al evaluar que los datos de la autenticación coinciden con los datos de la lista, enviará las autenticaciones directamente a ejecutar los grupos de reglas.

> En esta lista puedes agregar valores de clientes con historiales de riesgo. Al ser restrictiva la lista, permitirá ejercer mayor control de los filtros de validación. 

### ¿Cómo crear una lista de control de fraude?

Al dar clic en el botón *Crear*, ubicado en la parte lateral derecha del índice de listas, se desplegarán dos opciones para crear listas:

  ![](https://wiki.placetopay.com/images/4/43/Button-create-list.png)


1. **Crear una lista de control de fraude:**, Esta opción le permite crear una lista de forma manual e individual. 

    Si escoge esta opción se direccionará a un formulario como este:

    ![](https://wiki.placetopay.com/images/5/53/Acs-create-fraud-list.png)

Se solicitará:

- **Fecha de inicio:** Fecha en la que la lista va a comenzar a funcionar y hacer las validaciones.

- **Fecha de finalización:** Fecha en la que se va a finalizar el funcionamiento y validación de la lista de reglas.

- **Tipo de lista:** ACS dispone de dos tipos de listas:
    - PERMISSIVE
    - RESTRICTIVE

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

2. **Crear importación:** Con esta opción podrá crear listas de reglas de forma masiva a partir de un archivo que contenga las reglas.

> El archivo a cargar debe estar en formato .CSV, .TSV o .TXT.

Si escoge esta opción, se cargará un formulario como el siguiente:

  ![](https://wiki.placetopay.com/images/e/ed/List-import-create.png)

  En el formulario, haga clic en la opción *Seleccionar archivo* y busque en su equipo el archivo que desea cargar. Luego haga clic en el botón *Guardar*.

> Para visualizar un ejemplo del formato de una importación, haga clic en el link *Descargar*, ubicado en la parte lateral izquierda, en el título *Información básica*.

## Reglas de control de fraude:

Las reglas permiten hacer las validaciones de los datos recibidos en las solicitudes de autenticación. Estas reglas evalúan la coincidencia de las condiciones contenidas en la regla y de los datos obtenidos en la solicitud de autenticación.

> Al crear un emisor en ACS, se agregarán automáticamente una serie de reglas por defecto al emisor. Estas se encontrarán en esta sección y puede habilitarlas, editarlas o deshabilitarlas, según su necesidad.

### Índice de reglas:

Para acceder al índice y gestión de reglas, diríjase al menú superior del detalle del emisor y haga clic en la pestaña con nombre *Reglas de control de fraude*.

Visualizará una pantalla similar a la siguiente:

![](https://wiki.placetopay.com/images/5/5e/Index-rules.png)

#### Funciones de las reglas:

Las reglas tienen dos funciones a las cuales puede acceder haciendo clic en el menú con tres puntos ubicado al final de cada regla:

- **Ver:** Seleccione esta opción para visualizar más detalles de la regla. Haga clic en el botón con ícono de ojo ubicado al final de cada regla.

  Encontrará una vista similar a la siguiente, en la cual encontrará el estado de la regla, el nombre, el tipo de regla y el valor que le asignó, así mismo, las fechas y usuarios que crearon y actualizaron la regla:

  ![](https://wiki.placetopay.com/images/3/36/Rule-detail.png)

- **Activar/Inactivar:** Deslice este botón tipo switch para activar o inactivar una regla.

  > Si deshabilita una regla, no podrá validar la autenticación con los parámetros de la regla. Además, siempre debe tener reglas habilitadas para poder hacer un proceso de autenticación exitoso y confiable.

### ¿Cómo puedo cambiar el orden de ejecución de las reglas?

Las reglas se ejecutan y validan en el orden dado en el índice de reglas. Las nuevas reglas que cree, se ubicarán automáticamente debajo de la última creada y se ejecutará en ese mismo orden (solo se ejecutan las que reglas que tengan estado activo).

Para cambiar el orden de las reglas, mantenga presionada la regla que desea cambiar de lugar y deslícela al lugar donde desea ubicarla. Posteriormente aparecerá un mensaje que dice lo siguiente:

"Existen cambios sin guardar, si abandona esta página puede perderlos!"

Y en la parte inferior del índice obtendrá dos botones, presione *Guardar* para confirmar el cambio de lugar de la regla o *Cancelar* para volver al estado de orden anterior.


### Solicitudes de reglas:

Haga clic en la pestaña *Solicitudes de reglas*, ubicada en la parte superior derecha del índice de reglas. Allí se pueden visualizar las peticiones de creación, actualización o eliminación de reglas, las cuales se encuentran pendientes por aprobar o denegar.

- **Aprobar:** Para aprobar una solicitud, haga clic en el botón con check verde para aprobar o en el botón con equis rojo para denegar la solicitud. Luego se desplegará una ventana para confirmar la aprobación y el despliegue de la regla al entorno productivo, dé clic en *Confirmar* para aceptar la acción o en *Cancelar* para volver a las solicitudes.

- **Denegar:** Para denegar una solicitud, haga clic en el botón con equis rojo. Luego se desplegará una ventana para confirmar la eliminación, dé clic en *Confirmar* para aceptar la acción o en *Cancelar* para volver a las solicitudes.

### ¿Cómo crear solicitudes de reglas?

Para crear una petición de regla, haga clic en el botón *Crear petición de regla*, ubicado en la parte lateral derecha en la pestaña *Solicitudes de reglas*.

![](https://wiki.placetopay.com/images/5/59/Acs-rule-create.png)

Luego visualizará una ventana como esta, dónde le solicitan la acción que desea hacer con la regla.

![](https://wiki.placetopay.com/images/c/c2/Acs-rule-create-actions.png)

#### Acciones disponibles:

- **Crear:** Permite crear una petición para crear una nueva regla.

- **Actualizar:** Permite crear una petición para editar una regla existente. Si selecciona esta opción, luego se desplegará una lista con las reglas disponibles para editar, seleccione una y haga clic en el botón *Siguiente*, lo redirigirá a un formalario como el de creación de regla.

![](https://wiki.placetopay.com/images/8/89/Edit-rule.png)

- **Eliminar:** Permite crear una petición para eliminar una regla existente, si selecciona esta opción también se desplegará una lista con las reglas que puede eliminar, luedo haga clic en el botón *Enviar solicitud*.

![](https://wiki.placetopay.com/images/f/f5/Delete-rule.png)

### ¿Cómo crear nuevas reglas?

Para una nueva regla, debe seleccionar la opción *Crear* de la lista de peticiones y se desplegará un formulario como el siguiente:

![](https://wiki.placetopay.com/images/f/f0/Acs-conditions-rule.png)

Los datos requeridos son:

- **Nombre:** ¿Cómo desea nombrar la regla que va a crear?

- **Acción:** Se refiere a la función que va a cumplir la regla en el proceso de autenticación. Estas acciones se describen detalladamente en el siguiente título.

  *Construcción de la condición de la regla:*

- **Tipo de regla:** Hace referencia al tipo de regla que desea crear, por ejemplo es una regla que valida números de tarjeta de crédito, o valida emails, o rangos de bines...

- **Valor:** Es el valor que requiere una regla para validar y comparar los datos de la regla y de la solicitud de autenticación.

#### Reglas con múltiples condiciones:

Puede además agregar otras condiciones para una misma regla,haciendo clic en el botón inferior del formulario *Agregar condición*, y se desplegarán nuevos campos para ingresar otro tipo de regla y su valor correspondiente.

> Para habilitar este botón debe haber diligenciado ya una condición completa con su tipo de regla y valor.

Al hacer clic en el botón se presentará un formulario como el siguiente:

![](https://wiki.placetopay.com/images/d/dc/Add-condition-rule.png)

También hay otros tipos de reglas que ofrecen más posibilidades, en la siguiente imagen puede visualizar una regla donde puede escoger el operador con el cual va a comparar los valores la regla, por ejemplo, que el valor dado tenga un rango específico, un valor mínimo o máximo.

![](https://wiki.placetopay.com/images/1/19/Acs-others-rule-conditions.png)

Luego de enviar la solicitud de regla, esta se agregará al listado de *Solicitudes de regla*, allí tiene la opción de *Aceptar* o *Denegar*, con los botones de la parte lateral derecha.

![](https://wiki.placetopay.com/images/a/aa/Acs-accept-deny.png)

> Hasta que no acepte la solicitud de regla, esta no podrá visualizarse ni utilizarse en producción. Luego de aceptarla recuerde habilitarla.

### Acciones de las reglas: 

Al crear una regla se le define un tipo de acción específica que va a ejecutar. Estas acciones permiten definir el transStatus (estado de autenticación de la transacción). 

Estas acciones se encuentran en el formulario de creación de regla, en el campo *Acción*:

![](https://wiki.placetopay.com/images/d/db/Rule-actions.png)

Las acciones permitidas son las siguientes:

- **Autenticar:** Las reglas que contengan esta acción, permitirán validar la solicitud de autenticación y aprobarla automáticamente si la validación de los datos pasa exitosamente, generando un estatus Y (autenticación satisfactoria). Por ejemplo una regla de tipo *BinRange* va a contener un rango mínimo y máximo de BIN, las tarjetas cuyo BIN entren en este rango, se validará exitosamente y autenticará la solicitud.

- **Realizar desafío:** Las reglas cuya acción es realizar desafío, al validarse generarán el estatus C (requiere desafío), con este estatus el tarjetahabiente será direccionado a una interfaz de usuario en la cual se le pedirá aceptar un desafío para validar su identidad. 

- **Desafío desacoplado:** Las reglas que contengan esta acción, al validarse generarán un estatus D y la petición de autenticación se pondrá en pausa y el emisor se encargará de realizar el desafío manualmente con el tarjetahabiente.
 
- **No autenticar:** Las reglas con acción de no autenticar, al cumplirse la validación, lanzarán automáticamente un estado *N* (Autenticación fallida). Los datos incluídos en estas reglas suelen ser riesgosos.

- **Ejecutar grupo de reglas:** Las reglas creadas con esta acción, pueden ejecutar todas las reglas contenidas en un grupo de reglas específico del emisor. Para escoger esta opción debes tener grupos de reglas habilitados para el emisor.

  Si escoges esta opción, el formulario se visualizará como el siguiente:

  ![](https://wiki.placetopay.com/images/5/5c/Rule-to-execute-group.png)

  En el apartado *Grupos de control de fraude*, se presentará una lista de los grupos disponibles, escoja uno y continúe con el diligenciamiento de las condiciones para la regla.

- **Ninguno:** Las reglas con esta acción, tomarán la acción por defecto y generarán un estatus N (No autenticado).

> La función de ejecutar un grupo de reglas permite crear reglas que abarquen más validaciones y también permite utilizar reglas creadas anteriormente para hacer otras validaciones o complementarlas con otras condiciones, y de esta forma agrupar funcionalidades y disminuir reglas repetidas.

### Tipos de reglas: 

Al crear una regla se asigna un tipo específico. Las opciones disponibles se visualizan en el formulario de creación de la regla, en el campo *Tipo de regla*.

Visualizará una lista similar a esta con la lista de reglas disponibles:

![](https://wiki.placetopay.com/images/f/fe/Rule-types.png)

Los tipos de reglas disponibles actualmente son:

#### Rango de bines: 
Esta regla permite validar que la tarjeta que llegue en la petición de autenticación, esté en el rango especificado. Acepta dos valores, el rango inicial que debe ser un BIN de 6 o de 8 dígitos y el rango final que debe tener los mismos dígitos.

  ![](https://wiki.placetopay.com/images/9/96/Bin-range-rule.png)

#### Número de tarjeta de transacción: 
Esta regla permite validar que el número de tarjeta que registre en el valor, sea igual al número de tarjeta de la petición de autenticación. Esta regla recibe mínimo 13 dígitos y debe coincidir con el algoritmo de Luhn, el cual comprueba mediante una secuencia de dígitos, si un número de tarjeta es válido.

  ![](https://wiki.placetopay.com/images/7/7f/Card-number-rule.png)

#### Monto de compra:
Esta regla permite validar el monto de la transacción a autenticar. Acepta un valor numérico que indique un monto de pago.

  ![](https://wiki.placetopay.com/images/1/14/Rule-total.png)

#### Datos de autenticación:
 Esta regla valida los campos que se envían en el mensaje AReq, siendo este un tipo de mensaje del Protocolo 3-D Secure, con el cual se da inicio al proceso de autenticación. Esta regla recibe los siguientes parámetros:

  - **Campo**, Hace referencia al campo contenido en el mensaje AReq. Se presenta una lista con todos los campos disponibles para validar. Seleccione uno.

  - **Condiciones**, En este campo se selecciona el operador con el cual se va a hacer la comparación de valores a validar. Según el campo seleccionado se despliegan unos operadores específicos.

  - **Valores**, Aquí se ingresa el valor con el cual se va a hacer la comparación que permite validar o no la regla.

Un ejemplo de regla para datos de autenticación es el siguiente:

  ![](https://wiki.placetopay.com/images/d/d4/Areq-rule.png)


*Reglas de puntuación:*

#### Puntuación del emisor:
Esta regla valida la solicitud de autenticación a partir de la puntuación que tenga el emisor que procesa la transacción. La regla permite asignar el operador de comparación con el valor final que le va a asignar.

#### Puntuación histórica:
Esta regla valida la solicitud de autenticación a partir de la puntuación que tenga el tarjetahabiente históricamente. Se evalúa a partir de transacciones anteriores. La regla permite asignar el operador de comparación con el valor final que le va a asignar.

#### Puntuación RBA Master Card:
Esta regla valida la solicitud de autenticación a partir de la puntuación de riesgo evaluada para MasterCard. La regla permite asignar el operador de comparación con el valor final que le va a asignar.

 Los operadores disponibles para las reglas de puntuación son:
  - **Entre**, acepta un valor mínimo y uno máximo. El dato en la autenticación debe estar en el rango para pasar la validación.

  - **Menor que**, acepta un valor y valida que el dato de la autenticación sea menor al valor dado en la regla.

  - **Menor o igual que**, acepta un valor y valida que el dato de la autenticación sea menor o igual al valor dado en la regla.

  - **Mayor que**, acepta un valor y valida que el dato de la autenticación sea mayor al valor dado en la regla.

  - **Mayor o igual que**, acepta un valor y valida que el dato de la autenticación sea mayor o igual al valor dado en la regla.

  - **Igual a**, acepta un valor y valida que el dato de la autenticación sea igual al valor dado en la regla.

Un ejemplo de una regla de puntuación es el siguiente:

  ![](https://wiki.placetopay.com/images/8/8d/Score-rule.png)

*Reglas de coincidencia o match:*

#### Coincidencia para correo electrónico: 
Esta regla permite validar si el correo electrónico del tarjetahabiente que llega en los datos de autenticación, coincide con el correo electrónico guardado para el mismo tarjetahabiente en transacciones anteriores. 

Acepta uno de los siguientes dos valores: hacer match (encontrar coincidencia) o no hacer match (No encontrar coincidencia).

#### Coincidencia para teléfono móvil:
Esta regla permite validar si el teléfono móvil del tarjetahabiente que llega en los datos de autenticación, coincide con el número de teléfono móvil guardado para el mismo tarjetahabiente en transacciones anteriores. 

Acepta uno de los siguientes dos valores: hacer match (Encontrar coincidencia) o no hacer match (No encontrar coincidencia).

#### Coincidencia para teléfono fijo:
Esta regla permite validar si el teléfono fijo del tarjetahabiente que llega en los datos de autenticación, coincide con el número de teléfono fijo guardado para el mismo tarjetahabiente en transacciones anteriores. 

Acepta uno de los siguientes dos valores: hacer match (Encontrar coincidencia) o no hacer match (No encontrar coincidencia).

#### Coincidencia para teléfono del trabajo:
Esta regla permite validar si el teléfono del trabajo del tarjetahabiente que llega en los datos de autenticación, coincide con el número de teléfono del trabajo guardado para el mismo tarjetahabiente en transacciones anteriores. 

Acepta uno de los siguientes dos valores: hacer match (Encontrar coincidencia) o no hacer match (No encontrar coincidencia).

#### Coincidencia para el dispositivo:
Esta regla permite validar si el fingerprint o huella digital del tarjetahabiente que se crea en la transacción, coincide con algún fingerprint guardado para el mismo tarjetahabiente en transacciones exitosas anteriores. El fingerprint es un método que registra automáticamente un identificador de un usuario, a partir de la información captada con el dispositivo usado al realizar una transacción o un movimiento digital.

Acepta uno de los siguientes dos valores: hacer match (Encontrar coincidencia) o no hacer match (No encontrar coincidencia).

Un ejemplo de una regla tipo match es el siguiente:

![](https://wiki.placetopay.com/images/3/33/Match-mobile-phone-rule.png)

Encontrará en el campo *Valor*, una lista con dos opciones, hacer match (Encontrar coincidencia) o no hacer match (No encontrar coincidencia) con el dato guardado en ACS.


## Grupos de control antifraude:

Los grupos de control de fraude permiten clasificar y agrupar reglas para hacer validaciones con fines específicos. 

Por ejemplo, puede crear dos grupos, uno llamado *Lista blanca*, donde se podrían incluir números de tarjetas y datos de clientes con bajo riesgo de fraude y las acciones de las reglas podrían ser en su mayoría *Autenticar*. El otro grupo se llama *Lista negra*, aquí se podrían agregar los números de tarjeta e información personal asociada a clientes con historiales o reportes riesgosos y la acción de las reglas podría ser *No autenticar*.

### Índice de grupos de control de fraude:

En la siguiente imagen se muestra el listado de grupos de control de fraude de un emisor. La información se encuentra organizada en una tabla y muestra los datos principales de los grupos tales como: Nombre, Fecha, Reglas y Estado.

![](https://wiki.placetopay.com/images/7/7b/Group-index.png)

### ¿Cómo crear un nuevo grupo de reglas?

Para crear un grupo, haga clic el botón *Crear* ubicado en la parte lateral derecha del índice de grupos. Se desplegará un formulario similar al siguiente:

![](https://wiki.placetopay.com/images/0/08/Create-group.png)

En el formulario solo debe ingresar el nombre que desea que tenga el grupo y haga clic en el botón *Guardar*.

> Un grupo de reglas solo se ejecuta cuando al crear una nueva regla, se escoge la opción *Ejecutar grupo de reglas*, se selecciona el grupo específico, y posteriormente, se habilita la regla.

### Detalles de un grupo:

Para visualizar los detalles de un grupo, haga clic en el botón *Ver*, ubicado en la parte lateral derecha de la tabla, al frente de cada grupo.

Visualizará una vista como la siguiente:

![](https://wiki.placetopay.com/images/1/1c/Group-detail.png)

#### Habilitar y Deshabilitar un grupo:
Para habilitar o deshabilitar un grupo, haga clic en el menú lateral derecho con tres puntos y deslice el botón tipo switch para habilitar o deshabilitar según corresponda.

#### Reglas de un grupo:
En la parte inferior del detalle de un emisor, encontrará el listado de reglas en producción del grupo, listadas en una tabla que muestra el estado de la regla, el nombre y la acción que ejecutan al validar. 
Puede habilitarlas o deshabilitarlas, haciendo clic en el menú con tres puntos ubicado al final de cafa regla. También, puede visualizar los detalles de cada regla presionar el botón con ícono de ojo.

#### Solicitudes de reglas:
Esta funcionalidad se comporta igual a la sección de solicitudes de las *Reglas de control antifraude*, con la diferencia que las solicitudes de reglas que se hagan para crear, actualizar o eliminar reglas, se guardarán exclusivamente para el grupo escogido.

> Luego de crear una solicitud de regla, recuerde aprobarla y posteriormente, habilitarla en el menú de *Reglas en producción*.

<!-- type: tab-end -->