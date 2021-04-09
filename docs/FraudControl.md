# Motor de Control de Fraude

La principal funcionabilidad de ACS es el motor de control antifraude, este permite validar la información que recibe de la autenticación a través de un conjunto de reglas que se procesan mediante grupos específicos creados para validar las autenticaciones de cada emisor registrado.

### Grupos de control antifraude:

Para cada emisor registrado en el ACS se crean grupos de control antifraude, estos poseen un conjunto de reglas que permiten validar las autenticaciones y hacer un filtrado de los datos que se reciben de las autenticaciones.

### Reglas:

Los grupos de control antifraude están conformados por reglas que permiten hacer las validaciones de los datos recibidos en las autenticaciones. Estas reglas evalúan la coincidencia de las condiciones contenidas en la regla y de los datos obtenidos en la autenticación.

#### Acciones: 
Al crear una regla se le define un tipo de acción específica a la cual va a aplicar esta regla. Estas acciones corresponden a procesos tales como:

- **Autenticar:** Las reglas que contengan esta acción, permiten que las autenticaciones que pasen sus validaciones
puedan ser aprobadas de una forma más rápida ejecutando una especie de filtro de datos. Por ejemplo una regla de tipo *BinRange* va a contener un rango mínimo y máximo de BIN, las tarjetas cuyo BIN entren en este rango, podrán ser autenticadas automáticamente, creando una especie de lista blanca de datos.

- **Realizar desafío:** Las reglas cuya acción es realizar desafío, al cumplirse en una autenticación, permitirán que el tarjetahabiente sea direccionado inmediatamente a una interfaz de usuario en la cual se le pide aceptar un desafío para validar la autenticación, corroborando su identidad. 

- Desafío desacoplado 

- **No autenticar:** Las reglas con acción de no autenticar, al cumplirse la validación, lanzarán automáticamente un estado *N* (Autenticación fallida). Los datos incluídos en estas reglas se conciben con un alto grado de riesgo o posible fraude. Las reglas con esta acción pemriten crear una especie de lista negra de datos.
match
- Ninguno

