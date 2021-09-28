# Estados del proceso de autenticación

Los siguientes son los estados posibles que pueden obtenerse en un proceso de autenticación. Se presenta el indicador del estado y la descripción del mismo.

Estado | Descripción                                                                                               |
-------|-----------------------------------------------------------------------------------------------------------|
 Y     | Autenticación satisfactoria.                                                                              |  
 N     | Autenticación fallida. Se rechazó la autenticación sin embargo el comercio puede aprobar la transacción asociada.                                                                                                          |
 U     | Autenticación no realizada. Se presentó un error técnico durante el proceso.                              |
 A     | Se ejecutó un intento de autenticación.                                                                   |
 C     | Se requiere challenge para continuar el proceso de autenticación.                                         |
 R     | Autenticación rechazada. Una transacción cuya autenticación resulte en estado R no debería ser procesada debido al riesgo.                                                                                                  |
 D     | La autenticación requiere un desafío desacoplado, este es responsabilidad del emisor.                     |
 I     | Autenticación de tipo informativa, no soporta pago. Utilizada para verificar cuentas.                     |