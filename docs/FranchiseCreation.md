# Franquicias en ACS

## ¿Qué es una franquicia?

Una franquicia de una tarjeta de crédito, es una compañía aliada con los bancos emisores de tarjetas de crédito. Tienen como función proveer diversos beneficios bancarios a sus clientes, siendo estos los tarjetabientes. 
Las franquicias son las que gestionan el uso y los beneficios asociados a las tarjetas emitidas por los bancos emisores.

## ¿Cómo acceder a la gestión de franquicias de ACS?

Para acceder al listado de franquicias de la aplicación siga los siguientes pasos:

1. Remítase al menú lateral izquierdo dónde visualizará tres opciones, "Dashboard", "Sistema" y "Seguridad", como muestra la siguiente imagen:

![](https://wiki.placetopay.com/images/a/ac/Lateral-menu.png)

2. Haga clic en el menú "Sistema", se desplegará un listado de opciones, haga clic en la opción "Franquicias".

3. Visualizará una pantalla similar a la ilustrada en la siguiente imagen:

![](https://wiki.placetopay.com/images/4/4c/Franchise-index.png)

## ¿Cómo crear una franquicia en ACS?

Para crear una franquicia, haga clic en el botón *Crear* ubicado en la parte lateral derecha del índice de franquicias, posteriormente diligencia los datos del formulario teniendo en cuenta la siguiente información:

- **Marca,** Nombre de la franquicia, por ejemplo Mastercard, VISA...

- **Patrón,** Ingrese un patrón basado en una expresión regular, con este se valida que el número de tarjeta que llegue al ACS, sea válido según los estándares propios de cada franquicia.

- **Algoritmo para el CAVV,** El Cardholder Authentication Verification Value (CAVV), es un valor de verificación de autenticación del titular de la tarjeta. Aquí se debe seleccionar un algoritmo que valide este valor, el cual resulta de hacer una transacción. En el momento ACS cuenta con un algoritmo para VISA y otro para MASTERCARD.

- **Algoritmo para el ECI,** El Electronic Commerce
Indicator (ECI), es un valor para indicar los resultados del intento de autenticación. En ACS hay tres algoritmos disponibles, para las franquicias de VISA, MASTERCARD y JCB.

- **Logo,** Puede adjuntar una imagen con el logo de la franquicia.

En la siguiente imagen se puede visualizar un ejemplo del formulario de creación de una franquicia:

![](https://wiki.placetopay.com/images/a/a0/Acs-create-franchise.png)

## ¿Cuáles son los requerimientos para crear una franquicia en ACS?

Para crear una franquicia, esta debe haber pasado por un proceso de certificación para ACS con PlacetoPay Evertec.

También, la franquicia debe proporcionar información como el tipo de tarjetas que soportan, las clases y los bines aceptados, para proceder a realizar una creación exitosa de franquicia en ACS y que esta coincida con las especificaciones y requerimientos de la franquicia en específico.

## Listado y funciones de las franquicias

En esta sección se visualiza el listado o índice de franquicias en una tabla donde se muestran los datos principales de cada una, tales como: Marca, Patrón, Algoritmo para el CAVV, Algoritmo para el ECI, Estado y Acciones. Estos datos se explican más adelante. 

En el título "Acciones" ubicado en la parte lateral derecha,se encuentra un menú con tres puntos, haga clic en este menú y despliegue las acciones o funcionalidades disponibles para cada franquicia. En el menú se encuentran las siguientes acciones:

![](https://wiki.placetopay.com/images/6/62/Acs-franchise-index.png)

### Acciones para las franquicias:

- **Ver:** Seleccione esta opción para visualizar más detalles de la franquicia.

  Visualizará una vista similar a la siguiente:

![](https://wiki.placetopay.com/images/7/7d/Franchise-detail.png)

- **Editar:** Seleccione esta opción para actualizar o corregir los datos con los cuales creó la franquicia. 

  Visualizará un formulario similar al de creación de la franquicia.

![](https://wiki.placetopay.com/images/5/5d/Edit-franchise.png)

- **Habilitar o Deshabilitar:** Deslice el botóntipo switch para habilitar la franquicia si se encuentra deshabilitada o para deshabilitarla cuando se encuentre habilitada. 

![](https://wiki.placetopay.com/images/a/a9/Franchise-toggle.png)

Al habilitar o deshabilitar, la aplicación le entregará un mensaje de confirmación similar al siguiente e inmediatamente cambiará el estado en la franquicia editada.

![](https://wiki.placetopay.com/images/0/09/Enable-franchise.png)

### ¿Qué ocurre al deshabilitar una franquicia?

Tenga en cuenta que si una franquicia se encuentra deshabilitada, no podrá hacer movimientos con ella en la aplicación. Por ejemplo no puede visualizar una franquicia deshabilitada en el listado de franquicias disponibles, al momento de crear un certificado o un emisor. 

Tampoco podrán autenticarse las transacciones cuyas tarjetas pertenezcan a una franquicia deshabilitada. 

Así mismo puede causar el fallo en los emisores que tengan suscrita tal franquicia.





