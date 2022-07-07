# Tarjetas de Prueba

Los siguientes números de tarjetas de crédito, le permitirán hacer peticiones al servicio y obtener los comportamientos específicos que se describen para cada una.

Franquicia | Número de Tarjeta | Indicador de estado en 3DS | Estado en 3DS | Comportamiento en 3DS | Código de autorización | Estado de autorización | Código de autorización final (opcional) | Estado de autorización final (opcional) |
:---------:|:---------:|:---------:|:---------:|:---------:|:---------:|:---------:|:---------:|:---------:|
 Visa        | 4111111111111111  |   Y    | Successful | Genera una transacción con autenticación satisfactoria y sin fricción. | 00 | APPROVED | N/A | N/A |
 MasterCard        | 5180300000000005  |   Y    | Successful | Genera una transacción con autenticación satisfactoria y sin fricción. | 00 | APPROVED | N/A | N/A |
  Visa       | 4110760000000008  |   C    | Challenge | Genera una transacción que requiere desafío de autenticación (flujo con fricción). | 00 | APPROVED | N/A | N/A |
  Visa       | 4110760000000032  |   C    | Challenge | Genera una transacción que requiere desafío de autenticación (flujo con fricción). | 88 | PENDING INTERDIN | 00 | APPROVED |
  MasterCard       | 5292594382060745  |   C    | Challenge | Genera una transacción que requiere desafío de autenticación (flujo con fricción). | 11 | APPROVED VIP| N/A | N/A |
  MasterCard       | 5180300000000047  |   C    | Challenge | Genera una transacción que requiere desafío de autenticación (flujo con fricción). | 88 | PENDING INTERDIN | 00 | APPROVED |
 Visa       | 4110760000000040  |   A    | Attempt | Genera una transacción con intento de autenticación. | 88 | PENDING INTERDIN | 05 | GENERAL REJECTION |
 MasterCard      | 5180300000000054  |   A    | Attempt | Genera una transacción con intento de autenticación. | 88 | PENDING INTERDIN | 05 | GENERAL REJECTION |
  Visa      | 4110760000000065  |   N    | Not authenticated | Genera una transacción no autenticada por el emisor.  | 05 | GENERAL REJECTION | N/A | N/A |
  MasterCard       | 5180300000000039  |   N    | Not authenticated | Genera una transacción no autenticada por el emisor.  | 05 | GENERAL REJECTION | N/A | N/A |


# Datos de prueba para el desafío

El siguiente código deberá ser ingresado en autenticaciones de prueba con desafío.

Código OTP | Descripción                               |
-----------|-------------------------------------------|
 12345     | Pasa el desafío y autentica exitosamente. |  

 # Respuestas para desafíos con cuestionarios de selección simple y múltiple

 ## Cuestionario de selección simple

 1. ¿En qué banco tiene una cuenta de ahorros?. Respuesta: **Bancolombia**.
 2. ¿En que Banco tuvo crédito en los últimos 6 meses?. Respuesta: **Banco Davivienda**.

 ## Cuestionario de selección múltiple

1. Seleccione los bancos en los que ha tenido una cuenta. Respuestas: **Banco de Bogotá**, **Banco de New York**.
2. ¿En que Bancos ha tenido crédito en los últimos 6 meses?. Respuestas: **Banco de Bogotá**, **Banco de Occidente**.

