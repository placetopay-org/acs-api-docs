# Servicios Externos

La aplicación de ACS está desplegada en AWS (Amazon Web Service), una plataforma que permite almacenar proyectos en la nube y utilizar diversos de sus servicios. De esta forma, AWS contribuye a que ACS se mantenga y crezca como una aplicación sofisticada, innovadora, escalable y con alta fiabilidad y seguridad.

De los servicios prestados por AWS, la aplicación de ACS utiliza:

**Amazon API Gateway**, utiliza este servicio para la creación, publicación, mantenimiento, monitoreo y protección de la API REST de ACS.

**AWS Lambda**, este servicio permite ejecutar el código de ACS sin necesidad de servidores. Ejecutando éste solo cuando es necesario, de manera automática, y con una ejecución de miles de solicitudes por segundo.

**Almacenamiento en caché**, este servicio le permite a ACS contar con una memoria caché de alto rendimiento. La memoria caché se define como capa de almacenamiento de datos de alta velocidad, con una duración de almacenaje transitoria y la cual permite reutilizar de forma eficaz los datos recuperados o procesados anteriormente.

**Servicio de colas**, este servicio le ofrece a ACS el procesamiento de colas de mensajes (envío, almacenamiento y recepción) de una forma eficaz, segura, sin pérdida de datos y sin dependencia a disponibilidad de otras aplicaciones.

**AWS Certificate Manager**, es un servicio que le permite a ACS aprovisionarse, administrar e implementar con facilidad certificados SSL/TLS públicos y privados. Estos certificados permiten proteger comunicaciones por red y dar identidad a sitios web mediante Internet y recursos en redes privadas. 

**Amazon RDS**, ACS utiliza este servicio para configurar, utilizar y escalar su base de datos de tipo relacional en la nube. Permite automatizar tareas como el aprovisionamiento de hardware, la configuración de la base de datos, la implementación de parches y la creación de copias de seguridad. Mejorando con ello la rapidez, disponibilidad y seguridad de los datos.

**Amazon S3**, este servicio se encarga del almacenamiento de los datos de ACS, ofreciendo gran escalabilidad, disponibilidad, seguridad y rendimiento de los mismos. Tales datos son usados para la aplicación web, para procesos de copia de seguridad, restauración y archivado.

**Amazon EFS**, suministra un sistema de archivos NFS simple, escalable y administrado para utilizar con los servicios en la nube de AWS y los recursos de ACS. Este servicio evita interrumpciones en el funcionamiento de la aplicación, mediante la automatización del aumento y reducción de su capacidad a medida que se agregan o eliminan archivos. El sistema de archivos NFS se define como un protocolo que permite manipular archivos remotos e interacturar con estos como si se estuviera haciendo de forma local.
