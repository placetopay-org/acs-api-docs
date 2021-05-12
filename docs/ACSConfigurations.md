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

![](https://wiki.placetopay.com/images/2/2d/Acs-imports-index.png)


<!--
type: tab
title: Reportes
-->

# Reportes

Los reportes son archivos que contienen registros de las autenticaciones procesadas por ACS. La siguiente imagen muestra un ejemplo de la vista con el índice de reportes generados. Estos reportes se pueden ver y descargar.

![](https://wiki.placetopay.com/images/1/12/Acs-report-index.png)

Para crear un nuevo reporte haga clic en el botón *Crear*. 
Actualmente se manejan dos tipos de reportes:

## Reportes de Autenticaciones

El sistema de reportes permite generar un archivo con el reporte de las autenticaciones procesadas por ACS. Para el reporte se puede definir un rango de fechas, identificador de la transacción, BIN de tarjetas, banco emisor y uno o varios estados de las autenticaciones que se desean registrar en el reporte. El siguiente es un ejemplo de creación de un reporte de autenticaciones:

![](https://wiki.placetopay.com/images/b/bd/Acs-auth-report.png)

## Reportes de Abandonos 

Con este reporte se generan los datos de las autenticaciones que son abandonadas en el ACS. Para el reporte se puede definir un rango de fechas y el banco emisor. El siguiente es un ejemplo de creación de un reporte de abandonos:

![](https://wiki.placetopay.com/images/4/42/Acs-abandoned-report.png)


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

![](https://wiki.placetopay.com/images/6/62/Acs-franchise-index.png)


Para crear una franquicia, haga clic en el botón crear y diligencia los datos teniendo en cuenta la siguiente información:

- **Marca,** Nombre de la franquicia, por ejemplo Matercard, VISA...

- **Patrón,** Se ingresa un patrón basado en una expresión regular, con este se valida que el número de tarjeta que llegue al ACS, sea válido según los estándares propios de cada franquicia.

- **Algoritmo para el CAVV,** El Cardholder Authentication Verification Value (CAVV), es un valor de verificación de autenticación del titular de la tarjeta. Aquí se debe seleccionar un algoritmo que valide este valor, el cual resulta de hacer una transacción. En el momento ACS cuenta con un algoritmo para VISA y otro para MASTERCARD.

- **Algoritmo para el ECI,** El Electronic Commerce
Indicator (ECI), es un valor para indicar los resultados del intento de autenticación. En ACS hay tres algoritmos disponibles, para las franquicias de VISA, MASTERCARD y JCB.

- **Logo,** Puede adjuntar una imagen con el logo de la franquicia.

En la siguientes imagen se puede visualizar un ejemplo de creación de franquicia:

![](https://wiki.placetopay.com/images/a/a0/Acs-create-franchise.png)

<!--
type: tab
title: Invitaciones
-->

# Invitaciones de usuarios

En este módulo se gestionan las invitaciones que realiza un usuario registrado en ACS a otro usuario que desea utilizar la aplicación.

Es a través de una invitación que se pueden crear nuevos usuarios, esta se envía a un correo y allí redirecciona al usuario al inicio de sesión gestionado por la aplicación de Accounts, creada en PlacetoPay, en esta redirección el usuario podrá registrarse y acceder.

> Los datos que registre deben ser los mismos que se utilizaron para enviar la invitación.

Para crear una invitación, haga clic en el botón *Crear* del módulo de invitaciones, visualizará un formulario como el siguiente:

![](https://wiki.placetopay.com/images/1/15/Acs-create-invitation.png)

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

![](https://wiki.placetopay.com/images/a/ae/Acs-users-index.png)

<!-- theme: warning -->

> Los usuarios no se pueden eliminar ni editar.

<!--
type: tab
title: Monedas
-->

# Monedas utilizadas en ACS

En esta sección se visualizan las monedas creadas para utilizarse en ACS, pueden visualizarse los detalles, editar,habilitar o deshabilitar según las necesidades y requerimientos del cliente.

Para crear una nueva moneda, debe diligenciar un formulario similar al siguiente:

![](https://wiki.placetopay.com/images/9/92/Acs-create-currency.png)

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

![](https://wiki.placetopay.com/images/3/31/Acs-merchant-codes-index.png)

La anterior imagen muestra un ejemplo de la vista del módulo, las funcionalidades que están disponibles son:

- **Búsqueda de códigos:** Mediante el recuadro de búsqueda ubicado en la parte superior izquierda de la pantalla, podrá buscar un código específico, puede buscar con un fragmento del código, el código completo o un fragmento de la descripción del código.

- **Edición y Eliminación:** En el menú ubicado al final de cada código se despliega una lista con los botones de editar y eliminar el código. Esta funcionalidad se utiliza según los requerimientos del cliente.

- **Creación de un nuevo código:** Para crear un nuevo código, haga clic en el botón *Crear* ubicado en la parte lateral derecha de la pantalla. Se presentará un formulario como el siguiente:

![](https://wiki.placetopay.com/images/c/c8/Acs-merchant-code-create.png)

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

![](https://wiki.placetopay.com/images/8/89/Acs-certificates-index.png)

Los certificados se pueden editar y visualizar los detalles del mismo, haciendo clic en el menú con tres puntos ubicado en la parte lateral derecha de cada certificado.

## Creación de un certificado:

Para crear un nuevo certificado en ACS, haga clic en el botón *Crear*. La solicitud o creación del certificado consta de tres partes:

#### 1. Creación de la llave privada:

![](https://wiki.placetopay.com/images/3/3b/Acs-step-one.png)

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

![](https://wiki.placetopay.com/images/f/fd/Acs-step-two.png)

Aquí se registran los datos de información general sobre el solicitante de la llave:

- **País:** Seleccione el país donde se crea el certificado de la lista desplegable.
- **Estado:** Ingrese el nombre del estado del país en el cual está ubicado.
- **Localidad:** Ingrese el nombre de la ciudad en el cual está ubicado.
- **Nombre de la organización:** Ingrese el nombre de la organización para la cual se crea el certificado.
- **Nombre de la unidad organizacional:** Ingrese el nombre del área de la organización para la cual se genera el certificado.
- **Nombre común:** Ingrese un nombre de dominio válido, siendo este el título o nombre de la página web de la organización.
- **Correo electrónico:** Ingrese la dirección de correo electrónico del solicitante del certificado.


#### 3. Información de rastreo:

![](https://wiki.placetopay.com/images/a/a4/Acs-step-three.png)

Permite la identificación a partir de un slug, el cual forma parte de la URL que se va a consultar para acceder al servidor mediante el certificado.


## Registro y firma del certificado:

Una vez creado el certificado, le mostrará los datos que diligenció en el formulario.

Un ejemplo es el siguiente:

![](https://wiki.placetopay.com/images/5/59/Acs-ertificate-detail.png)

#### ¿Cómo firmar el certificado?

1. Debe copiar este bloque, correspondiente a la solicitud de firma del certificado. Copie el bloque incluyendo las etiquetas de "---BEGIN CERTIFICATE REQUEST---" y "---END CERTIFICATE REQUEST---". 

![](https://wiki.placetopay.com/images/b/bb/Acs-signature-certificate-request.png)

2. Cree su llave privada y firme el certificado con el bloque de texto que copió.

3. Al finalizar el proceso de creación de llaves y firma del certificado, obtendrá un bloque de texto similar al primero que copió. Copie este bloque, incluyendo también las etiquetas de "---BEGIN CERTIFICATE REQUEST---" y "---END CERTIFICATE REQUEST---". 

4. En el detalle del certificado, al final encontrará la opción de registrar su certificado, haga clic en el enlace con el nombre *Aquí!*.

![](https://wiki.placetopay.com/images/b/b8/Acs-request.png)

5. Esto lo direccionará a la siguiente vista, donde debe pegar el segundo bloque de texto que copió, el cual corresponde a su certificado, en el campo *Certificado*, así:

![](https://wiki.placetopay.com/images/8/83/Acs-register-certificate.png)

6. Haga clic en guardar y con esto obtiene un certificado firmado válido para asegurar la transferencia de información con ACS.

<!-- type: tab-end -->