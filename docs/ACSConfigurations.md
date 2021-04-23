<!--
type: tab
title: Emisores
-->

# Emisores

En la sección de emisores se encuentran diferentes funcionalidades relacionadas con los emisores, siendo estos las instituciones financieras que se encargan de emitir tarjetas de pago y servicios relacionados con estas tarjetas.

En la siguiente imagen se visualiza un ejemplo de la vista de *Detalles del emisor*, además se puede editar y habilitar o deshabilitar con el menú lateral derecho.

![](../assets/images/issuers.png)


### Configuraciones:
En este apartado se encuentra toda la gestión de configuración de campos para un banco emisor, puede ver los detalles de cada uno, qué función desempeña, puede editarlos, deshabilitarlos y habilitarlos según se requiera. 

![](../assets/images/issuers-configurations.png)

También, en la pestaña *Services*, se encuentran las estrategias disponibles para ejecutar los servicios para el emisor.

- otpStrategy, información acerca de cómo se va a implementar el servicio del OTP (Autenticación con contraseña de un solo uso).

- cardholderStrategy, información acerca de cómo se va a implementar el servicio de información del tarjetabiente.

#### Campos de configuración:

Estas configuraciones se gestionan desde la sección *Campos de configuración* del ACS. Allí se encuentra un listado de los campos creados para configurar los emisores, puede habilitarlos, deshabilitarlos, editarlos y ver sus detalles.

![](../assets/images/configurations-actions.png)

Además, con el botón *Crear*, puede adicionar nuevos campos con diferentes tipos de datos a recibir:

- **SELECT:** Recibe un dato que se ha seleccionado de una lista de valores disponibles.

- **BOOLEAN:** Recibe únicamente las opciones de falso y verdadero.

- **DATE:** Recibe una fecha con un formato dado.

- **NUMERIC:** Recibe valores numéricos.

- **STRING:** Recibe un dato que puede incluir cadena de texto, números y signos.

- **PASSWORD:** El dato que se recibe en este campo es guardado de forma segura. SU valor original suele reemplazarse con carácteres especiales o con un algoritmo de criptografía.

- **TRANSLATABLE:** Recibe un dato que puede ser traducido.

![](../assets/images/configuration-fields.png)

### Gestión de bines:
Aquí se gestionan los bines del adquiriente. En primer lugar obtendrá un listado de los bines creados anteriormente para el emisor, además puede crear otros bines nuevos, editarlos y eliminarlos.

![](../assets/images/bines.png)

Al dar clic en el botón *Crear* como ilustra la imagen, tendrá tres opciones para crear bines:

- Crear un único BIN para el emisor.
- Crear un rango de bines para el emisor, el cuál contendrá un valor mínimo y un valor máximo de bines, creando así un grupo de números de tarjetas de crédito a gestionar.
- Crear importación, para la importación se aceptan los formatos de archivo .csv, .tsv y .txt


### Gestión de rangos de tarjetas:
En esta sección se importan y crean los rangos de tarjetas aceptadas para un emisor específico. Puede ver los detalles de cada rango, editarlos y eliminarlos.

![](../assets/images/card-ranges-index.png)

Al dar clic en el botón *Crear*, se desplegarán dos opciones para crear rangos:

- **Crear un rango de tarjetas,** este permite crear un rango de forma manual, se solicitará el BIN para el rango, el cual debe ser de 8 dígitos, el valor inicial y el final, la franquicia y la clase o tipo de las tarjetas asociadas al rango.

- **Crear importación,** para crear una importación visualizará un formulario similar al siguiente:

![](../assets/images/create-import-ranges.png)

Debe seleccionar la franquicia para la cual se van a cargar los rangos y un archivo de tipo CSV (archivo de valores separados por comas) que contenga la información de los rangos. Un ejemplo del archivo es este:

![](../assets/images/file-import-example.png)

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

### Gestión del control de fraude:
Estas funcionalidades están descritas detalladamente en la sección de *Motor Antifraude*. Aquí se hace la gestión de las reglas y de los grupos donde están contenidas, las cuales permiten validar los datos que llegan al ACS y garantizar la seguridad de la información, lo cual permitirá aceptar las solicitudes de autenticación que sean realmente válidas y tener filtros que permitan optimizar este proceso de validación.


<!--
type: tab
title: Motor Antifraude
-->

# Motor de Control de Fraude

La principal funcionalidad de ACS es el motor de control antifraude, este permite validar la información que se recibe en la petición de autenticación, a través de un conjunto de reglas que validan las autenticaciones de cada emisor registrado.

Esta funcionalidad se gestiona desde la sección de Emisores de la aplicación.

### Listas de control de fraude:

Las listas de control de fraude son el primer filtro que puede validar una autenticación. Estas listas son temporales y se dividen en dos clases:

- **Permisivas:** Estas listas van a crear un filtro que va a permitir que las autenticaciones que cumplan con los valores registrados en estas, puedan eximirse de la ejecución de los grupos de reglas y continúe con el proceso de autenticación.

- **Restrictivas:** Por el contrario, este tipo de listas, al evaluar que los datos de la autenticación coinciden con los datos de la lista, enviará las autenticaciones directamente a evaluar los grupos de reglas.

> Las listas de control antifraude se ejecutan antes de los grupos de control antifraude y según los resultados que obtenga de sus validaciones, puede evitar que una autenticación tenga que pasar por las validaciones de los grupos de reglas.

![](../assets/images/fraud-list-index.png)

Para crear una lista de control se direccionará a un formulario como este:

![](../assets/images/create-fraud-list.png)

Se solicitará:

- **Fecha de inicio:** Fecha en la que se va a iniciar la validación de la lista de reglas.

- **Fecha de finalización:** Fecha en la que se va a finalizar la validación de la lista de reglas.

- **Tipo de lista:** ACS dispone de dos tipos de listas:
    - PERMISSIVE
    - RESTRICTIVE

- **Tipo de valor:** Aquí se selecciona el parámetro por el cual se van a hacer los filtros de las autenticaciones. 

- **Valor:** Corresponde al valor del tipo de parámetro seleccionado en el campo anterior. Con este valor se procede a hacer las validaciones y a verificar la coincidencia del dato con los recibidos en la autenticación.

### Grupos de control antifraude:

Para cada banco emisor registrado en el ACS, se creará un grupo predeterminado conformado por una serie de reglas antifraude que permiten validar las solicitudes de autenticación. Además de este grupo prederteminado, se podrán agregar otros nuevos al emisor.

En la imagen se muestra el listado de grupos de control de fraude de un emisor. En esta vista se pueden crear nuevos grupos con el botón *Crear* y se pueden visualizar los detalles y las reglas de cada grupo dando clic en la opción *Ver*.

En la imagen ejemplo, se visualizan dos grupos, uno llamado *Lista blanca*, donde se podrían incluir por ejemplo números de tarjetas y datos de clientes con bajo riesgo de fraude y las acciones de las reglas podrían ser en su mayoría *Autenticar*. El otro grupo se llama *Lista negra*, aquí se podrían agregar los números de tarjeta e información personal asociada a clientes con historiales o reportes y la acción de las reglas podría ser *No autenticar*.

![](../assets/images/fraud-groups.png)

### Reglas antifraude:

Los grupos de control antifraude están conformados por reglas que permiten hacer las validaciones de los datos recibidos en las autenticaciones. Estas reglas evalúan la coincidencia de las condiciones contenidas en la regla y de los datos obtenidos en la solicitud de autenticación.

Al presionar la opción *Ver* de un grupo de control antifraude, le mostrará una vista similar a esta.

![](../assets/images/group-details.png)

Aquí se encuentran los detalles del grupo seleccionado, puede habilitarlo o deshabilitarlo en el menú lateral derecho. Además, encontrará el listado de reglas correspondientes al grupo, la acción que ejecutan, puede habilitarlas o deshabilitarlas y puede visualizar los detalles y condiciones de la misma.

En la pestaña *Solicitudes de reglas*, se pueden visualizar las peticiones de creación, actualización o eliminación de reglas, las cuales se encuentran pendientes por aprobar o denegar. También, puede crear una petición de reglas nueva, haciendo clic en el botón *Crear petición de regla*.

![](../assets/images/rule-create.png)

Luego visualizará una ventana como esta, dónde le solicitan la acción que desea hacer con la regla.

![](../assets/images/rule-create-actions.png)

Para crear una petición de regla, debe seleccionar la opción *Crear*, y se desplegará una vista como la siguiente:

![](../assets/images/conditions-rule.png)

Los datos requeridos son:
- **Nombre:** ¿Cómo desea nombrar la regla a crear?
- **Acción:** Se refiere a la función que va a cumplir la regla en el proceso de autenticación. Estas acciones se describen detalladamente en el siguiente título.
- **Tipo de regla:** Hace referencia al tipo de regla que desea crear, por ejemplo es una regla que valida números de tarjeta de crédito, o valida emails, o rangos de bines...
- **Valor:** Es el valor que requiere una regla para validar y comparar los datos presentes en la misma y en la solicitud de autenticación.

> Puede además agregar otras condiciones para una misma regla.

También hay otros tipos de reglas que ofrecen más posibilidades, en la siguiente imagen puede visualizar una regla donde puede escoger que el valor tenga un rango, un valor mínimo o máximo por ejemplo.

![](../assets/images/others-rule-conditions.png)

Luego de enviar la solicitud de regla, esta se agregará al listado de *Solicitudes de regla*, allí tiene la opción de *Aceptar* o *Denegar*, con los botones de la parte lateral derecha.

![](../assets/images/accept-deny.png)

> Hasta que no acepte la solicitud de regla, esta no podrá visualizarse ni utilizarse en producción. Luego de aceptarla recuerde habilitarla.

### Acciones de las reglas: 
Al crear una regla se le define un tipo de acción específica que va a ejecutar. Estas acciones permiten definir el transStatus (estado de autenticación de la transacción). Las acciones permitidas son las siguientes:

- **Autenticar:** Las reglas que contengan esta acción, permitirán validar la solicitud de autenticación y aprobarla automáticamente, generando un estatus Y (autenticación satisfactoria). Por ejemplo una regla de tipo *BinRange* va a contener un rango mínimo y máximo de BIN, las tarjetas cuyo BIN entren en este rango, podrán ser autenticadas automáticamente, creando una especie de lista blanca de datos.

- **Realizar desafío:** Las reglas cuya acción es realizar desafío, al validarse generarán el estatus C (requiere desafío), con este estatus el tarjetahabiente será direccionado a una interfaz de usuario en la cual se le pedirá aceptar un desafío para validar su identidad. 

- **Desafío desacoplado:** Las reglas que contengan esta acción, al validarse generarán un estatus D y la petición de autenticación se pondrá en pausa y el emisor se encargará de realizar el desafío manualmente con el tarjetahabiente.
 
- **No autenticar:** Las reglas con acción de no autenticar, al cumplirse la validación, lanzarán automáticamente un estado *N* (Autenticación fallida). Los datos incluídos en estas reglas se conciben con un alto grado de riesgo o posible fraude. Las reglas con esta acción pemriten crear un tipo de lista negra de datos.

- **Ejecutar un grupo:** Las reglas creadas con esta acción pueden ejecutar todo las reglas contenidas en otro grupo de reglas del emisor.

- **Ninguno:** Las reglas con esta acción, tomarán la acción por defecto y generarán un estatus N (No autenticado).

> La función de ejecutar un grupo de reglas permitirá hacer validaciones no secuenciales entre los diferentes grupos registrados para un emisor.

<!--
type: tab
title: Importes
-->

# Importes de rangos de tarjetas

En esta sección se pueden visualizar las importaciones de archivos realizadas en ACS, por ejemplo se encuentran los archivos que importan un listado de rangos de tarjetas para un emisor.

En este índice de importes puede visualizar los detalles de cada importe y el estado en el cual se encuentra la importanción.

Los estados posibles son:

- Completado
- Fallido
- Pendiente

![](../assets/images/imports-index.png)


<!--
type: tab
title: Reportes
-->

# Reportes

Los reportes son archivos que contienen registros de las autenticaciones procesadas por ACS. La siguiente imagen muestra un ejemplo de la vista con el índice de reportes generados. Estos reportes se pueden ver y descargar.

![](../assets/images/report-index.png)

Para crear un nuevo reporte haga clic en el botón *Crear*. 
Actualmente se manejan dos tipos de reportes:

## Reportes de Autenticaciones

El sistema de reportes permite generar un archivo con el reporte de las autenticaciones procesadas por ACS. Para el reporte se puede definir un rango de fechas, identificador de la transacción, BIN de tarjetas, banco emisor y uno o varios estados de las autenticaciones que se desean registrar en el reporte. El siguiente es un ejemplo de creación de un reporte de autenticaciones:

![](../assets/images/auth-report.png)

## Reportes de Abandonos 

Con este reporte se generan los datos de las autenticaciones que son abandonadas en el ACS. Para el reporte se puede definir un rango de fechas y el banco emisor. El siguiente es un ejemplo de creación de un reporte de abandonos:

![](../assets/images/abandoned-report.png)


## Tipos de archivos generados para los reportes
- Archivo separado por comas.
- Archivo separado por tabuladores.
- Archivo de Excel


<!--
type: tab
title: Franquicias
-->

# Franquicias

Aquí se gestionan las franquicias que funcionan en ACS, siendo la franquicia una compañía aliada con los bancos emisores de tarjetas de crédito, las cuales proveen diversos beneficios bancarios a sus clientes.

En esta sección se visualiza el listado de franquicias, los detalles de cada una, se pueden editar, habilitar y deshabilitar.

![](../assets/images/franchise-index.png)


Para crear una franquicia, haga clic en el botón crear y diligencia los datos teniendo en cuenta la siguiente información:

- **Marca,** Nombre de la franquicia, por ejemplo Matercard, VISA...

- **Patrón,** Se ingresa un patrón basado en una expresión regular, con este se valida que el número de tarjeta que llegue al ACS, sea válido según los estándares propios de cada franquicia.

- **Algoritmo para el CAVV,** El Cardholder Authentication Verification Value (CAVV), es un valor de verificación de autenticación del titular de la tarjeta. Aquí se debe seleccionar un algoritmo que valide este valor, el cual resulta de hacer una transacción. En el momento ACS cuenta con un algoritmo para VISA y otro para MASTERCARD.

- **Algoritmo para el ECI,** El Electronic Commerce
Indicator (ECI), es un valor para indicar los resultados del intento de autenticación. En ACS hay tres algoritmos disponibles, para las franquicias de VISA, MASTERCARD y JCB.

- **Logo,** Puede adjuntar una imagen con el logo de la franquicia.

En la siguientes imagen se puede visualizar un ejemplo de creación de franquicia:

![](../assets/images/create-franchise.png)

<!--
type: tab
title: Invitaciones
-->

# Invitaciones de usuarios

En este módulo se gestionan las invitaciones que realiza un usuario registrado en ACS a otro usuario que desea utilizar la aplicación.

Es a través de una invitación que se pueden crear nuevos usuarios, esta se envía a un correo y allí redirecciona al usuario al inicio de sesión gestionado por la aplicación de Accounts, creada en PlacetoPay, en esta redirección el usuario podrá registrarse y acceder.

> Los datos que registre deben ser los mismos que se utilizaron para enviar la invitación.

Para crear una invitación, haga clic en el botón *Crear* del módulo de invitaciones, visualizará un formulario como el siguiente:

![](../assets/images/create-invitation.png)

Datos a diligenciar:

- **Nombre:** Corresponde al nombre que va a identificar al nuevo usuario.

- **Correo electrónico:** Debe ser un correo válido porque allí es dónde se enviará la invitación.

- **Perfil:** Seleccione el perfil que desea otorgarle al nuevo usuario.

<!--
type: tab
title: Usuarios
-->

# Listado de usuarios

En este módulo se puede visualizar el listado de usuarios con acceso a ACS. El listado contiene el nombre y el correo electrónico asociado al usuario.

> Es importante recordar que los usuarios se crean a través del módulo invitaciones y solo aparece en este módulo, cuando haya aceptado la invitación para unirse a ACS, creado el usuario y haya iniciado sesión sin conflicto alguno.

El siguiente es un ejemplo de una vista del módulo usuarios.

![](../assets/images/users-index.png)

<!-- theme: warning -->

> Los usuarios no se pueden eliminar ni editar.

<!--
type: tab
title: Monedas
-->

# Monedas utilizadas en ACS

En esta sección se visualizan las monedas creadas para utilizarse en ACS, pueden visualizarse los detalles, editar,habilitar o deshabilitar según las necesidades y requerimientos del cliente.

Para crear una nueva moneda, debe diligenciar un formulario similar al siguiente:

![](../assets/images/create-currency.png)

Datos a diligenciar:

- **Nombre:** Nombre por el cual se reconoce a la divisa que va a crear.

- **Código alfabético:** Para este campo debe buscar el código alfabético correspondiente a la moneda que va a crear. El código debe ser el establecido por el estándar internacional ISO. Este contiene tres carácteres.

- **Código numérico:** Para este campo debe buscar el código numérico correspondiente a la moneda que va a crear. El código debe ser el establecido por el estándar internacional ISO y consta de tres dígitos.

- **Unidad menor:** Ingrese un número que indique la menor denominación o el menor valor que puede tener la moneda que está creando.

<!--
type: tab
title: Códigos del comercio
-->

# Códigos de categoría del comercio

En este módulo se encuentran registrados todos los códigos relacionados con las categorías de los comercios a los cuales ACS les procesa autenticaciones. Este módulo se pone a disposición del cliente a modo informativo y aclaratorio, ya que las autenticaciones en la recepción del mensaje *AReq* procesa un campo llamado *mcc* (Merchant Category Code), el cual contiene el código de categoría del comercio, un valor numérico de 4 dígitos que por sí mismo no es muy claro, así que este listado de códigos va a facilitar la aclaración del tipo de comercio y la descripción a la cual hace referencia el código.

![](../assets/images/merchant-codes-index.png)

La anterior imagen muestra un ejemplo de la vista del módulo, las funcionalidades que están disponibles son:

- **Búsqueda de códigos:** Mediante el recuadro de búsqueda ubicado en la parte superior izquierda de la pantalla, podrá buscar un código específico, puede buscar con un fragmento del código, el código completo o un fragmento de la descripción del código.

- **Edición y Eliminación:** En el menú ubicado al final de cada código se despliega una lista con los botones de editar y eliminar el código. Esta funcionalidad se utiliza según los requerimientos del cliente.

- **Creación de un nuevo código:** Para crear un nuevo código, haga clic en el botón *Crear* ubicado en la parte lateral derecha de la pantalla. Se presentará un formulario como el siguiente:

![](../assets/images/merchant-code-create.png)

Diligencie teniendo en cuenta lo siguiente:

- **Código:** Ingrese un valor numérico de 4 dígitos que esté incluído en el listado en el ISO 18245, el cual es una normatividad encargada de la asignación de códigos de categoría de comerciantes para utilizarse en servicios financieros.

- **Descripción:** Se presentan dos campos, en el que contiene el prefijo *en*, ingrese la descripción en inglés para el código a crear, y en el campo con prefijo *es*, ingrese la misma descripción en español.


<!--
type: tab
title: Certificados
-->

# Certificados SSL

En esta sección se crean los certificados SSL, los cuales son títulos digitales que vinculan digitalmente una clave criptográfica con los datos de una organización. Los certificados SSL permiten autenticar la identidad de un sitio web y cifrar la información que se envía al servidor.
El certificado permite que cuando un usuario intente enviar información de las credenciales al servidor web, el navegador del usuario accede al certificado digital del servidor y establece una conexión segura. De esta forma, estos certificados proveen en esencia seguridad de los datos manejados en ACS.

La siguiente imagen muestra un ejemplo de la vista de un índice de certificados:

![](../assets/images/certificates-index.png)

Los certificados se pueden editar y visualizar los detalles del mismo. 

## Creación de un certificado:

Para crear un nuevo certificado haga clic en el botón *Crear*. La solicitud o creación del certificado consta de tres partes:

#### 1. Creación de la llave privada:

![](../assets/images/step-one.png)

1.1. Solicitud del tipo de llave con el cual se va a cifrar el certificado, están disponibles los siguientes tipos de llaves:

- **RSA,** es una llave creada a partir del algoritmo RSA, un sistema criptográfico de clave pública que utiliza factorización de números enteros y cifra bloques de datos. Es el algoritmo más utilizado para crear estas llaves.

> Una llave privada solo puede descifrarla la llave pública que se crea y que es asociada a una única llave privada.

- **EC,** es una llave basada en la Criptografía de curva elíptica (ECC), la cual promete una seguridad más fuerte y mejor rendimiento ya que utiliza claves más cortas. El sistema criptográfico utilizado está basado en las matemáticas de curvas elípticas.

> La llave es la que permite al usuario autenticarse por medio de la conexión SSH al servidor web. Para esto deberá contar con una llave privada y una llave pública que contiene el servidor y con la cual se va a conectar. 

1.2. Selección del tipo de cifrador para el certificado. Se debe seleccionar dependiendo del tipo de conexión y están disponibles dos tipos:

- **AES_128_CBC:** Es un tipo de cifrado, donde Advanced Encryption Standard (AES), es un esquema de cifrado por bloques y Cipher Block Chaining (CBC), es un modo de operación para una unidad de cifrado por bloques. Este tipo de cifrado tiene un tamaño de 128 bytes. Es el más utilizado.

- **AES_256_CBC:** Es un tipo de cifrado por bloques, que utiliza el modo de operación CBC. Este tipo de cifrado tiene un tamaño de 256 bytes.


3. Tamaño de la llave en bits.

4. Contraseña de la llave.

5. Tipo de llave. La llave va a funcionar para un cliente, un servidor o un SDK.

6. Banco emisor.

7. Tipo de franquicia.


#### 2. Solicitud de firma del certificado:

![](../assets/images/step-two.png)

Aquí se registran los datos de información general sobre el solicitante de la llave:

- Ubicación.
- Organización.
- Nombre, debe ser un dominio.
- Correo electrónico.


#### 3. Información de rastreo:

![](../assets/images/step-three.png)

Permite la identificación a partir de un slug, el cual forma parte de la URL que se va a consultar para acceder al servidor mediante el certificado.


## Registro y firma del certificado:

Una vez creado el certificado, le mostrará los datos que diligenció en el formulario. Además, de eso creará una solicitud de firma de certificado, como la siguiente:

![](../assets/images/signature-certificate-request.png)

Debe copiar este bloque incluidas las etiquetas de BEGIN y END CERTIFICATE REQUEST. Con esta información debe proceder a crear su llave privada y a firmar el certificado.

Una vez tenga su certificado firmado, obtendrá otro bloque similar al de la imagen, debe copiarlo incluyendo también las etiquetas de BEGIN y END CERTIFICATE REQUEST.

Luego, en el detalle del certificado, al final encontrará la opción de registrar su certificado:

![](../assets/images/request.png)

Haga clic allí, lo llevará a la siguiente vista, donde debe pegar su certificado en el campo *Certificado*, así:

![](../assets/images/register-certificate.png)


<!-- type: tab-end -->