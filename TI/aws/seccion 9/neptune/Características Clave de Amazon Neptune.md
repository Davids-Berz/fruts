#### 1.1. **Compatibilidad con Modelos de Grafo**

Amazon Neptune admite dos tipos principales de bases de datos de grafos:

- **Property Graph**: Se consulta utilizando **Gremlin**, el lenguaje de consultas para grafos de Apache TinkerPop.
- **RDF**: Se consulta utilizando **SPARQL**, el estándar de la W3C para consultar bases de datos RDF.

Esto permite a los usuarios elegir el modelo de datos que mejor se ajuste a sus necesidades y migrar aplicaciones basadas en grafos existentes a Neptune sin necesidad de realizar grandes modificaciones.

#### 1.2. **Alto Rendimiento y Escalabilidad**

Neptune está optimizado para consultas y análisis de grafos altamente conectados:

- **Lecturas Rápidas y Escalables**: Puedes escalar las operaciones de lectura horizontalmente añadiendo hasta **15 réplicas de lectura** en diferentes zonas de disponibilidad (AZs). Esto permite que las aplicaciones manejen consultas concurrentes con baja latencia.
- **Transacciones ACID**: Neptune garantiza transacciones **ACID** (Atomicidad, Consistencia, Aislamiento y Durabilidad), lo que asegura que las operaciones sobre los datos sean consistentes y fiables, incluso en aplicaciones de misión crítica.

#### 1.3. **Alta Disponibilidad y Failover Automático**

Neptune está diseñado para ofrecer alta disponibilidad mediante la replicación automática de los datos en **tres zonas de disponibilidad (AZs)** dentro de una región de AWS. En caso de un fallo en la instancia principal, Neptune realiza un **failover automático** hacia una réplica en otra AZ en menos de 30 segundos, asegurando que las aplicaciones sigan operando sin interrupciones.

#### 1.4. **Consultas Complejas y Flexibles**

Neptune permite realizar consultas complejas sobre datos en grafos utilizando los lenguajes **Gremlin** (para Property Graph) y **SPARQL** (para RDF). Estos lenguajes permiten explorar relaciones profundas entre los datos, realizar análisis de rutas, encontrar patrones específicos, y mucho más. Esto hace que Neptune sea ideal para aplicaciones que dependen de relaciones complejas entre datos, como motores de recomendación y análisis de redes.

#### 1.5. **Totalmente Gestionado**

Neptune es un servicio de base de datos totalmente gestionado por AWS, lo que significa que AWS se encarga de tareas como la **configuración**, **parcheo**, **respaldo**, **recuperación** y **escalabilidad**. Esto libera a los desarrolladores de la necesidad de gestionar la infraestructura subyacente, permitiéndoles concentrarse en el desarrollo de la aplicación.

#### 1.6. **Seguridad Integrada**

Neptune proporciona varias capas de seguridad para proteger los datos:

- **Cifrado de datos en reposo** utilizando **AWS Key Management Service (KMS)**.
- **Cifrado en tránsito** mediante **SSL/TLS** para proteger las comunicaciones entre Neptune y las aplicaciones.
- **Control de acceso granular** mediante **AWS Identity and Access Management (IAM)**, lo que permite definir permisos detallados para usuarios y aplicaciones.

#### 1.7. **Backup Automático y Recuperación en Punto en el Tiempo**

Neptune realiza **backups automáticos continuos** de los datos en Amazon S3 y permite la **recuperación en un punto en el tiempo** hasta los últimos 35 días. Los backups automáticos no afectan el rendimiento de la base de datos, y puedes restaurar una base de datos en cualquier momento utilizando un backup.