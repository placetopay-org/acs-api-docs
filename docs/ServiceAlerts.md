# Alertas del servicio

ACS hace un seguimiento constante del correcto funcionamiento de la aplicación, para esto las alertas permiten notificar oportunamente irregularidades u otros aspectos a tener en cuenta, que se puedan presentar durante el flujo de autenticación y en la configuración de la aplicación.

En el momento ACS cuenta con dos alertas que requieren ser gestionadas cuando se notifiquen:

## 1. Alerta de error en los servicios de autenticación con desafío:

Cuando una transacción requiere desafío, utiliza un servicio de información de tarjetahabiente específico para procesarlo, este servicio puede requerir un consumo externo, por lo cual en este flujo pueden presentarse diferentes errores que muchas veces se deben a dificultades con el servicio externo. 

Por esta razón ACS creó una alerta que permite notificar cuando ocurre un error de este tipo. Esta alerta se envía por correo electrónico al área de operaciones con el asunto **"Error en ejecución de servicio"**, y se visualiza como se muestra en la siguiente imagen:

![](https://wiki.placetopay.com/images/e/ec/Error-challenge-service.png)

### ¿Qué acción tomar cuando se reciba esta alerta?

Esta alerta permite avisar oportunamente de un error que está ocurriendo en un servicio y que no permite a un cliente autenticarse adecuadamente. Por esta razón se debe comunicar con los representantes del servicio externo para verificar que esté funcionando correctamente, a qué se debió el error y qué acciones se pueden tomar para prevenir que siga ocurriendo y así evitar la pérdida de autenticación de transacciones.

## 2. Alerta de expiración de certificados SSL:

Los certificados SSL son de vital importancia para el correcto funcionamiento de ACS, ya que son utilizados para suscribir una franquicia a un emisor, de tal forma que si el certificado expirara, esta franquicia no podría procesar transacciones para ese emisor.

Esta alerta se envía por correo electrónico al área de operaciones con el asunto **"Se encontraron certificados próximos a expirar"**, y se visualiza como se muestra en la siguiente imagen:

![](https://wiki.placetopay.com/images/2/2f/Certificate-next-to-expire.png)

Este correo también se puede visualizar de la siguiente forma, cuando informa el vencimiento del certificado.

![](https://wiki.placetopay.com/images/f/f2/Expired-certificate.png)

### ¿Qué acción tomar cuando se reciba esta alerta?

Esta alerta permite avisar cuando un certificado está cerca de vencerse, con el fin de que se gestione la renovación del mismo con la persona encargada de realizar tal proceso. Así mismo da aviso si ya el certificado está vencido, la idea es siempre gestionarlo antes de que esto ocurra para evitar errores en el proceso de autenticación de transacciones.