<!--
type: tab
title: Servicios
-->

# Servicios del emisor

## ¿Cómo acceder a este menú?

En la pestaña **Servicios** de las configuraciones, se encuentran las estrategias disponibles para ejecutar servicios de ACS para el emisor. Estas son:

<!--
type: tab
title: Servicio de Información del Tarjetahabiente
-->

# Cardholder Strategy

Esta estrategia permite definir cómo se va a implementar el servicio de información del tarjetabiente. Para ello en el valor del campo, se ingresa la estrategia correspondiente. 

  En el momento se dispone de las siguientes estregias:

  - **Standard Strategy:** Permite autenticar las solicitudes que lleguen al ACS con la estrategia estandar, mediante la cual se toma la decisión de autenticar o no, conforme a la información del tarjetahabiente recibida.

  - **Standard No Auth Strategy:** Permite no autenticar las solicitudes que lleguen al ACS con la estrategia estandar.

  - **No Service Strategy:** No valida la información del tarjetahabiente y pasa a ejecutar las reglas de validación correspondientes para aprobar o denegar la autenticación.

  - **SisCard Strategy:** Permite autenticar las solicitudes que lleguen al ACS mediante el servicio de SisCard.

  Para la estrategia seleccionada debe configurar los siguientes valores:

  - **cardholderInfoURL:** Ingrese una URL válida para conectar con el servicio externo para obtener la información del tarjetahabiente.

  - **cardholderInfoUser:** Ingrese el usuario provisto por el servicio de cardholder con el cual se va a conectar y el cual le permitirá autenticarse.

  - **cardholderInfoPassword:** Ingrese la contraseña provista por el servicio de cardholder para completar la autenticación.

<!--
type: tab
title: Servicio de OTP
-->

# Otp Strategy

Esta estrategia permite definir cómo se va a implementar el servicio del OTP (Autenticación con contraseña de un solo uso), para el emisor específico.  Para ello en el valor del campo, se ingresa la estrategia correspondiente. 

  En el momento se dispone de las siguientes estregias:

  - **Standard Strategy:** Para enviar y validar el OTP se utiliza un servicio propio de PlacetoPay.

  - **Diners Strategy:** Para enviar y validar el OTP se utiliza un servicio propio de Diners.

  Para la estrategia seleccionada debe configurar los siguientes valores:

  - **otpURL:** Ingrese una URL válida para consumir el servicio externo para el envío del OTP.

  - **otpSize:** Ingrese un número que indique el número de dígitos que debe tener el OTP.

  - **otpRuleRegex:** Ingrese la expresión regular que permitirá validar el OTP ingresado.
  
  - **otpAuthMethod:** Seleccione el indicador para el método de autenticación con el servicio de OTP.

<!--
type: tab
title: Servicio de Autenticación
-->

## Auth Strategy

Esta estrategia permite definir cómo se va a implementar el servicio de autorización a ACS. Este servicio se utilizará cuando ACS requiera consumir un servicio externo que a su vez necesite algún tipo de autenticación o autorización mediante token. Para ello en el valor del campo, se ingresa la estrategia de autenticación OAuth correspondiente. 

  En el momento se dispone solo de un tipo de estrategia:

- **Standard OAuth Strategy:** Permite autorizar el acceso a un servicio consumido por ACS con una estrategia estándar, mediante la utilización de un Bearer token.

 También debe configurar los siguientes valores para la estrategia:

  - **authURL:** Ingrese una URL válida para consumir el servicio externo de autorización OAuth.

  - **authUsername:** Ingrese el usuario provisto por el servicio de autorización OAuth con el cual se va a conectar y el cual le permitirá autenticarse.

  - **cardholderInfoPassword:** Ingrese la contraseña provista por el servicio de autorización OAuth para completar la autenticación.
  

> Estas estrategias deben estar tener sus valores particulares de configuración diligenciados, para poder habilitarse posteriormente.

<!-- type: tab-end -->