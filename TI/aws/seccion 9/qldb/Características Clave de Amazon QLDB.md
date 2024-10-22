#### 1.1. **Registro Inmutable**

Una de las características más importantes de QLDB es que cada cambio en los datos se registra en un **historial inmutable**. Ninguna transacción registrada en QLDB puede ser modificada o eliminada, lo que asegura un registro permanente y auditable de todas las operaciones.

#### 1.2. **Libro Mayor Centralizado y Verificable**

QLDB está diseñado como un **ledger** centralizado donde las transacciones pueden verificarse de forma criptográfica. Utiliza un **árbol Merkle** para generar hashes de los registros de transacciones, lo que permite a los usuarios verificar de manera eficiente si un registro ha sido alterado desde su inserción en la base de datos. Esto proporciona un nivel de seguridad y confianza que es útil para auditorías y cumplimiento normativo.

#### 1.3. **Totalmente Gestionado**

QLDB es un servicio totalmente gestionado, lo que significa que AWS se encarga de todas las tareas operativas, como la configuración, parches, backups, escalabilidad y recuperación ante desastres. Esto permite a los usuarios centrarse en el desarrollo de aplicaciones sin tener que preocuparse por la infraestructura subyacente.

#### 1.4. **Transacciones ACID**

QLDB soporta transacciones con las propiedades **ACID** (Atomicidad, Consistencia, Aislamiento, Durabilidad), lo que garantiza que las operaciones sobre los datos se ejecuten de manera segura, confiable y consistente.

#### 1.5. **Escalabilidad Transparente**

QLDB escala automáticamente según las necesidades de la aplicación. A medida que crecen las transacciones y los datos, QLDB ajusta el rendimiento y el almacenamiento sin necesidad de intervención manual. Esto asegura que las aplicaciones puedan manejar un gran volumen de transacciones sin preocuparse por la capacidad de la base de datos.

#### 1.6. **Consultas Flexibles con PartiQL**

QLDB utiliza **PartiQL**, un lenguaje de consulta SQL-compatible que permite a los usuarios realizar consultas sobre datos almacenados en formato de documento JSON. PartiQL facilita las consultas sobre los registros en el libro mayor y proporciona la flexibilidad de acceder tanto a datos actuales como históricos.

#### 1.7. **Historia Completa y Seguimiento de Cambios**

QLDB permite realizar **consultas temporales** que acceden a versiones anteriores de los datos. Esto significa que puedes ver el estado de cualquier dato en un punto de tiempo específico y reconstruir su historial completo. Esta capacidad es clave para auditorías, ya que proporciona un rastro claro de todas las modificaciones y el estado de los datos a lo largo del tiempo.

#### 1.8. **Backup y Recuperación Automática**

QLDB realiza **backups automáticos** de los datos y permite la **recuperación en un punto en el tiempo** para proteger la integridad y disponibilidad de los datos. Los backups no afectan el rendimiento de la base de datos, lo que asegura que las operaciones continúan sin interrupciones.