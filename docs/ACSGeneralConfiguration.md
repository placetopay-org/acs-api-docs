# ¿Cómo configurar ACS?

Para obtener un óptimo funcionamiento de la aplicación, esta se debe configurar adecuadamente con el fin de que pueda validar, aprobar y denegar solicitudes de autenticación acorde al flujo con el cual se diseñó, que a su vez fue guiado por las especificaciones dadas por el Protocolo 3-D Secure.

## Pasos para la configuración:

1. Primero debe contar con un **usuario con permisos** y accesos suficientes para hacer el proceso de configuración, e ingresar a la aplicación con el usuario y la contraseña asignada.

2. Seleccione el **idioma** con el cual desea que se presente toda la información y funcionalidades en la aplicación. Están disponibles los idiomas español e inglés. Esta opción se encuentra ubicada en la parte superior derecha de la aplicación, en un menú desplegable.

![](https://wiki.placetopay.com/images/3/34/Language-configuration.png)

3. Ubique y **familiarícese con los módulos** en los cuales se divide la aplicación y las funcionalidades que contienen. Estos se encuentran en un menú ubicado en la parte lateral izquierda de la aplicación. Y se visualizan así:

![](https://wiki.placetopay.com/images/f/f5/Lateral-menu-options.png)

#### Dashboard:
En este módulo se encuentran las principales funcionalidades de ACS, conformando el tablero principal con el cual el usuario se va a relacionar más.

  En este menú se encuentran:

  - Métricas de procesamiento y funcionamiento de la aplicación.
  - Registros y funciones para las autenticaciones procesadas.
  - Registros y funciones para las autenticaciones desacopladas.
  - Listado y funciones de los reportes generados en ACS.
  - Listado y estados de disputas de autenticaciones.


> Este módulo y sus funcionalidades, se revisan y explican detalladamente en la sección de *Funcionalidades* de esta documentación.

#### Sistema:
En este módulo se encuentran los componentes que permiten configurar ACS y gestionar su buen funcionamiento. 

  Se encuentran en el módulo:

  - Listado, funciones y configuraciones de los emisores.
  - Listado y funciones para los certificados SSL.
  - Listado y funciones para las franquicias.
  - Listado y funciones para los códigos de categoría del comercio.
  - Listado y funciones para las monedas aceptadas en ACS.
  - Listado y funciones para los países aceptados en ACS.
  - Listado y funciones para los campos de configuración para emisores.
  - Listado y funciones de los importes creados en la aplicación.

> Este módulo y sus funcionalidades, se revisan y explican detalladamente en la presente sección de *Configuración*  y en los artículos que la componen.

#### Seguridad:
En este módulo se encuentran los componentes que gestionan los registros de movimientos, accesos y seguridad para ACS.

  Se encuentran en el módulo:
   - Listado y funciones para los usuarios registrados en ACS.
  - Listado y funciones de invitaciones para crear nuevos usuarios en ACS.
   - Registros y gestión de roles para usuarios de ACS.
   - Registros y gestión de perfiles para usuarios de ACS.
   - Listados y gestión de los registros de movimientos realizados por los diferentes usuarios de ACS.

 > Este módulo y sus funcionalidades, se revisan y explican detalladamente en la sección de *Seguridad* de esta documentación.

4. Cree las **franquicias** con las cuales esté certificada ACS, en el menú de *Franquicias*, y habílitelas según las requiera.

5. Cree un **emisor** con el cual tenga relación ACS, en el menú de *Emisores* y habilítelo.

6. Para el **emisor** creado, diríjase a los detalles del mismo y ejecute las siguientes **configuraciones**:
 
    - Habilite y edite los **campos de configuración** requeridos según la lógica de negocio del emisor, en la sección de *Configuraciones* ubicada en el detalle del emisor.
    
    - Habilite las **estrategias** que indican al ACS qué implementación debe tomar para el servicio de la información del tarjetahabiente y para el servicio del OTP, para cada franquicia. Las estrategias se ubican en la sección de *Configuraciones* en la última pestaña con nombre *Servicios*, en el detalle del emisor.

    - Suscriba las **franquicias** disponibles para el emisor en la sección de *Operaciones* y luego *Franquicias suscritas* ubicada en el detalle del emisor.

    - Cree manualmente o importe los **rangos de tarjeta** que acepta el emisor que está configurando, para los rangos requiere también relacionarlos con sus respectivas franquicias.

    - Puede crear una o varias **listas de reglas** para el control antifraude, en la sección *Gestionar control fraude* y luego *Gestionar listas de control de fraude* en el detalle del emisor, estas listas hacen el primer filtro de validación de una autenticación.

    - Al crear un emisor, se crean automáticamente unas **reglas predeterminadas** para validar las autenticaciones. Estas reglas se encuentran en la sección *Reglas de control de fraude* en el detalle del emisor. Revise las reglas predeterminadas, edítelas si es necesario y habilíteles o deshabilítelas según los requerimientos del emisor. Siempre debe existir al menos una regla para validar las autenticaciones conforme al flujo establecido en ACS. Entre más reglas tenga habilitadas, más seguro puede llegar a ser el proceso de autenticación del tarjetahabiente. Además, puede crear múltiples reglas en esta sección.

    - Opcionalmente, puede crear **grupos de reglas** en la sección *Grupos de control de fraude* en el detalle del emisor. Estos grupos permiten clasificar y agrupar reglas para hacer validaciones con fines específicos.

> En este punto es muy importante tener en cuenta que todos los pasos anteriormente descritos, se explican detalladamente con sus finalidades, ubicaciones y procesos en las secciones de *Configuración de franquicias*, *Configuración de emisores* y *Otras configuraciones*, disponibles en el menú *Funcionamiento de ACS* y luego en el menú *Configuración* presentes en esta documentación.

7. Habilite y deshabilite las **monedas** en la sección de *Monedas*, según los requerimientos del territorio dónde se va a utilizar ACS.

8. Cree un **certificado SSL** en la sección de *Certificados*, este certificado permite establecer una conexión segura.

    #### Crear llave privada: 
  En esta sección y para que funcione eficazmente el emisor, debe crear un certificado de tipo **CLIENT**, seleccionar el emisor configurado previamente y una franquicia que esté suscrita en el emisor seleccionado. 

    #### CSR: Solicitud de firma del certificado:
  En esta parte, diligencie los datos de ubicación de dónde se va a utilizar el certificado. Posteriormente, ingrese el slug para la URL y se procederá a crear el CSR, Certificate Signing Request, el cual se visualiza como un bloque de texto cifrado que contiene toda la información anteriormente diligenciada y la llave pública.

    #### Genere el certificado SSL con la autoridad certificadora:
  Remítase a la autoridad certificadora para obtener el certificado SSL a partir del CSR generado anteriormente, cuando obtenga el certificado, el cual también se visualizará como un bloque de texto cifrado, copiélo y peguélo en el campo *Certificado* de la *Solicitud de certificado* y haga clic en *Guardar*.
  
  > Todo lo relacionado con los conceptos, finalidades y creación del certificado, se especifica en la sección de *Otras configuraciones* y luego en *Certificados* presentes en esta documentación.

9. Para controlar los **accesos** y permisos a la aplicación, gestione (conceda y deniegue) los permisos para las diferentes funcionalidades y usuarios en la sección de **Roles**.

10. Puede crear nuevos **permisos** y accesos en la sección de **Perfiles** y gestionar el control de acceso a los diferentes módulos de la aplicación.

11. Proceda a recibir solicitudes de autenticación, a validarlas con el motor antifraude y a registrarlas y visualizarlas en la sección de ***Autenticaciones***.

12. Gestione **disputas** reportadas para las autenticaciones procesadas por ACS en el menú de *Disputas*. Haga seguimiento a los estados y descargue los reportes del proceso. Recuerde que las disputas son aquellas reclamaciones relacionadas con los cargos de una transacción que resulta inválida o fraudulenta.

13. Haga seguimiento y gestione las **autenticaciones desacopladas** que se originan en el proceso de autenticación en ACS, recuerde que estas autenticaciones son aquellas que requieren de una validación manual por parte del emisor para verificar la identidad del tarjetahabiente.

14. Gestione, revise y evalúe el funcionamiento de la aplicación con los datos de las **métricas** para transacciones.

15. Haga seguimiento a los **movimientos** realizados en la aplicación, en la sección de **Logs**.

16. Cree invitaciones en la sección de *Invitaciones*, para agregar nuevos **usuarios** a la aplicación. Y realice seguimiento del registro de los usuarios en la sección de *Usuarios*.

17. Haga seguimiento a los **importes** de datos creados en ACS, en la sección de *Importes. Los importes pueden ser de rangos de tarjetas o de listas de reglas antifraude.

18. Haga seguimiento de las autenticaciones y abandonos en el proceso de autenticación en ACS, mediante la creación de **reportes de autenticaciones y abandonos**, en la sección de *Reportes*.

19. Confirme, edite y familiarícese con los **comercios** con los cuáles suele transar, a partir de los códigos ubicados en la sección *Códigos del comercio*.

> Todas las funcionalidades anteriormente mencionadas, se describen a fondo en las respectivas secciones de la documentación, puede guiarse por los títulos y por la guía general presentada al inicio de este documento.

