# Autenticaciones Desacopladas

Para acceder a la gestión de autenticaciones de la aplicación vaya al menú lateral izquierdo, seleccione la opción *Dashboard* y luego *Autenticaciones desacopladas*.

![](https://wiki.placetopay.com/images/2/20/Menu-desacopladas.png)

## Índice de autenticaciones desacopladas:

En esta sección registran las autenticaciones que entraron a un proceso de desacople a cargo del banco
emisor para corroborar la identidad del tarjetabiente.

La sesion de *Autenticaciones desacopladas*, se divide en tres modulos, en los cuales se gestiona una
autenticación dependiendo de la acción que se va a realizar.

**1. Módulo Mis autenticaciones:** Cuando un usuario selecciona una autenticación del módulo de *Autenticaciones desacopladas*, estas se ubican en el presente módulo, permitiendo así, tener una buena organización y gestionar mejor las autenticaciones, al poder identificar fácilmente aquellas en las cuales ha trabajado. 

**2. Módulo Autenticaciones desacopladas:** En este módulo ingresan todas las autenticaciones que aún no se han desacoplado y están en espera de ser solucionadas por un usuario con permisos.

**3. Módulo Autenticaciones seleccionadas por otros usuarios:** Este módulo permite observar las autenticaciones seleccionadas por otro usuario. Aquí se debe tener en cuenta que una autenticación solo la puede resolver un usuario, aún así, pueden ser observadas por varios usuarios con el permiso de autenticar.

> La división de las autenticaciones desacopladas permite que los usuarios que las vayan a resolver tengan una mayor organización, y no se presenten conflictos en el momento de resolverlas.


## Autenticación sin un usuario asignado

En el módulo de *Autenticaciones desacopladas*, se muestran las autenticaciones que no han sido seleccionadas por algún usuario. Por lo cual, para ser asignada, el usuario debe ingresar a la información de la autenticación, y el sistema se la asignará de manera automática para ser resuelta.

### Liberación de autenticaciones desacopladas:

Se debe tener en cuenta que si el usuario no desea resolverla, tendrá que liberarla a través de un clic en
el botón ubicado en el extremo derecho, con el nombre **Liberar**, así otro usuario la podrá resolver.

Cada autenticación cuenta con un tiempo promedio para ser resuelta, tiempo que se configura con el banco emisor. Si una autenticación no es resuelta en este tiempo, cambiará a un estado *U* = Autenticación no realizada. Se presentó un error técnico durante el proceso.

![](https://wiki.placetopay.com/images/c/cb/Acs-deocupled-1.png)

### Resolver autenticación:
La acción de resolver una autenticación la debe realizar un usuario con el conocimiento y permisos, teniendo en cuenta que el sistema solo muestra los datos de la transacción e información de ella.

Para autenticarla o no autenticar, se debe ingresar a través de un clic en el botón de **Resolver autenticación**.
La aplicación muestra una ventana emergente con las dos opciones, el usuario selecciona uno de los
dos estados, luego envía su respuesta, el sistema reconoce la acción y cambia su estado e informa con un mensaje el cambio en la autenticación.

![](https://wiki.placetopay.com/images/e/ee/Acs-ecoupled-2.png)

La aplicación muestra la información de la autenticación, con el cambio del estado en la parte superior
izquierda.

![](https://wiki.placetopay.com/images/4/40/Acs-decoupled-3.png)

### Información de una autenticación:

#### Información básica: 

Dentro de este módulo se muestra la información básica de una autenticación. Esta es:

- Estado actual de la autenticación
- Número de la tarjeta (oculto), teniendo en cuenta que el usuario autorizado puede verla, sin embargo, el sistema informa al administrador principal la acción a través de un correo, y guardando un log con la información del usuario.
- BIN del adquiriente
- Monto
- Emisor
- Dispositivo del canal
- Categoría del mensaje

![](https://wiki.placetopay.com/images/d/d3/Informacion-general-tx.png)

#### Titular de la tarjeta:

- Correo electrónico
- Teléfono de la casa
- Teléfono móvil
- Teléfono del trabajo

![](https://wiki.placetopay.com/images/9/95/Acs-decoupled-5.png)

#### Información del comercio:

- Nombre del comercio
- Código de categoría de comercio
- Nombre del código de categoría de comercio
- País

![](https://wiki.placetopay.com/images/b/b5/Acs-decoupled-6.png)

## Autenticación Relacionada

El presente módulo solo se puede observar cuando la autenticación se encuentra en un estado desacoplada, teniendo en cuenta que es información con datos comunes y sirve como historial de una autenticación semejante, por eso se muestra como una tabla, porque son
varias autenticaciones como respaldo de la actual. En algunos casos toda información es común, como en
otros casos solo tienen un dato en común.

La tabla se divide en:
- Comercio
- Emisor
- Monto
- Número de la tarjeta parcialmente oculto
- Correo electrónico
- Dispositivo del canal
- Flujo
- Estado

![](https://wiki.placetopay.com/images/b/b8/Acs-decoupled-7.png)

### Información de la cuenta del titular de la tarjeta:

Como el anterior módulo, este también solo se muestra en las
autenticaciones desacopladas. Contiene información del banco emisor como:

- Fecha de creación de la cuenta del titular de la tarjeta
- Indicador de edad de la cuenta del titular de la tarjeta
- Cambio de cuenta del titular de la tarjeta
- Cambio de contraseña de cuenta de titular de tarjeta
- Edad de cuenta de pago
- Indicador de edad de la cuenta de pago
- Indicador de cambio de cuenta del titular de la tarjeta
- Cantidad de transacciones por día
- Cantidad de transacciones por año
- Indicador de cambio de contraseña de cuenta del titular de la tarjeta
- Uso de la dirección de envío
- Cuenta de compra de la cuenta del titular de la tarjeta
- Indicador de nombre de envío
- Indicador de uso de la dirección de envío
- Número de intentos de aprovisionamiento por día
- Actividad de cuenta sospechosa

![](https://wiki.placetopay.com/images/f/f1/Acs-decoupled-8.png)

## Traza de la autenticación

En este módulo se presentan los mensajes de petición y de respuesta que se han presentado durante todo el flujo de la autenticación.

![](https://wiki.placetopay.com/images/4/4d/Traza-desacopladp.png)
