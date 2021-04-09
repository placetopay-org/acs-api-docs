<!--
type: tab
title: Motor Antifraude
-->

# Motor de Control de Fraude

La principal funcionabilidad de ACS es el motor de control antifraude, este permite validar la información que se recibe en la petición de autenticación, a través de un conjunto de reglas que se procesan mediante grupos específicos creados para validar las autenticaciones de cada emisor registrado.

### Grupos de control antifraude:

Para cada banco emisor registrado en el ACS, se creará un grupo predeterminado conformado por una serie de reglas antifraude que permiten validar las solicitudes de autenticación. Además de este grupo prederteminado, se podrán agregar otros nuevos al emisor.

### Reglas antifraude:

Los grupos de control antifraude están conformados por reglas que permiten hacer las validaciones de los datos recibidos en las autenticaciones. Estas reglas evalúan la coincidencia de las condiciones contenidas en la regla y de los datos obtenidos en la solicitud de autenticación.

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
title: Autenticaciones
-->

# Autenticaciones

En esta módulo se registra la información de todas las autenticaciones procesadas por el ACS. Contienen el estado de la autenticación además de la información básica de la transacción, la información del tarjetahabiente, del comercio, la ubicación en el mapa de dónde se generó la transacción, los datos de entrega y una línea de tiempo con los detalles de todo el proceso de autenticación y de la información captada por cada uno de los mensajes presentes en el proceso y correspondientes al protocolo 3-D Secure.

<!--
type: tab
title: Autenticaciones Desacopladas
-->

# Autenticaciones Desacopladas

En esta sección registran las autenticaciones que entraron a un proceso de desafío desacoplado a cargo del banco emisor para corroborar la identidad del tarjetabiente. 
Se detalla la fecha, el emisor, el BIN, número de tarjeta, monto y tiempo restante para la aprobación de la autenticación. Aquí se da la opción de resolver las autenticaciones manualmente, con base en el análisis de la información dada.

<!--
type: tab
title: Reportes
-->

# Reportes de Autenticaciones

El sistema de reportes permite generar un archivo con el reporte de las autenticaciones procesadas por ACS. Para el reporte se puede definir un rango de fechas, identificador de la transacción, BIN de tarjetas, banco emisor y uno o varios estados de las autenticaciones que se desean registrar en el reporte.

# Reportes de Abandonos 

Con este reporte se generan los datos de las autenticaciones que son abandonadas en el ACS. Para el reporte se puede definir un rango de fechas y el banco emisor.

## Tipos de archivos generados para los reportes
- Archivo separado por comas.
- Archivo separado por tabuladores.
- Archivo de Excel

<!--
type: tab
title: Métricas
-->

# Métricas por monto de transacción

Esta métrica muestra en una gráfica el monto de las transacciones procesadas por el ACS, filtradas por un rango de fechas y diferenciadas por el estatus obtenido en la autenticación.


# Métricas por estado de transacción

Esta métrica muestra en una gráfica la cantidad de transacciones procesadas por el ACS, filtradas por un rango de fechas y diferenciadas por el estatus obtenido en la autenticación.


<!-- type: tab-end -->

