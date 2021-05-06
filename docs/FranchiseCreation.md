# Franquicias en ACS

## ¿Qué es una franquicia?

Una franquicia de una tarjeta de crédito, es una compañía aliada con los bancos emisores de tarjetas de crédito. Tienen como función proveer diversos beneficios bancarios a sus clientes, siendo estos los tarjetabientes. 
Las franquicias son las que gestionan el uso y los beneficios asociados a las tarjetas emitidas por los bancos emisores.

## ¿Cómo acceder a la gestión de franquicias de ACS?

Para acceder al listado de franquicias de la aplicación siga los siguientes pasos:

1. Remítase al menú lateral izquierdo dónde visualizará tres opciones, "Dashboard", "Sistema" y "Seguridad", como muestra la siguiente imagen:

![](../assets/images/lateral-menu.png)

2. Haga clic en el menú "Sistema", se desplegará un listado de opciones, haga clic en la opción "Franquicias".

3. Visualizará una pantalla similar a la ilustrada en la siguiente imagen:

![](../assets/images/franchise-index.png)

## Listado y funciones de las franquicias

En esta sección se visualiza el listado de franquicias en una tabla donde se muestran los datos principales de cada una, tales como: Marca, Patrón, Algoritmo para el CAVV, Algoritmo para el ECI, Estado y Acciones. Estos datos se explican más adelante. 

En el título "Acciones" ubicado en la parte lateral derecha,se encuentra un menú con tres puntos, haga clic en este menú y despliegue las acciones o funcionalidades disponibles para cada franquicia. En el menú se encuentran las siguientes acciones:

**Ver:** Seleccione para visualizar más detalles de la franquicia.

**Editar:** Seleccione para actualizar los datos de registro de la franquicia.

**Habilitar o Deshabilitar:** Deslice el botón para habilitar la franquicia si se encuentra deshabilitada o para deshabilitarla cuando se encuentre habilitada. Tenga en cuenta que si una franquicia se encuentra deshabilitada, no podrá hacer movimientos con ella en la aplicación.


![](https://wiki.placetopay.com/images/6/62/Acs-franchise-index.png)

## ¿Cómo crear una franquicia en ACS?

Para crear una franquicia, haga clic en el botón crear y diligencia los datos teniendo en cuenta la siguiente información:

- **Marca,** Nombre de la franquicia, por ejemplo Matercard, VISA...

- **Patrón,** Se ingresa un patrón basado en una expresión regular, con este se valida que el número de tarjeta que llegue al ACS, sea válido según los estándares propios de cada franquicia.

- **Algoritmo para el CAVV,** El Cardholder Authentication Verification Value (CAVV), es un valor de verificación de autenticación del titular de la tarjeta. Aquí se debe seleccionar un algoritmo que valide este valor, el cual resulta de hacer una transacción. En el momento ACS cuenta con un algoritmo para VISA y otro para MASTERCARD.

- **Algoritmo para el ECI,** El Electronic Commerce
Indicator (ECI), es un valor para indicar los resultados del intento de autenticación. En ACS hay tres algoritmos disponibles, para las franquicias de VISA, MASTERCARD y JCB.

- **Logo,** Puede adjuntar una imagen con el logo de la franquicia.

En la siguientes imagen se puede visualizar un ejemplo de creación de franquicia:

![](https://wiki.placetopay.com/images/a/a0/Acs-create-franchise.png)

