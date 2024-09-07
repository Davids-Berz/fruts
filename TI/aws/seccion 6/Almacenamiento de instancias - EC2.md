#EBS #snapshots #ami #sfx

## Visión General EBS

Amazon Elastic Block Store (EBS) es un servicio de almacenamiento en bloque de alto rendimiento y fácil de usar diseñado para su uso con instancias EC2 (*Elastic Compute Cloud*) en Amazon Web Services (AWS). EBS proporciona volúmenes de almacenamiento persistentes que se pueden adjuntar a instancias EC2 para el almacenamiento de datos que necesitan persistir más allá del ciclo de vida de la instancia.

1. [[Características Principales de EBS]]
2. [[Tipos de Volúmenes EBS]]
3. [[Gestión de EBS]]
4. [[Ejemplo de Uso de EBS]]

Amazon EBS es una solución de almacenamiento en bloque flexible y de alto rendimiento adecuada para una amplia variedad de aplicaciones. Proporciona persistencia, escalabilidad, seguridad y opciones de rendimiento que permiten a los usuarios optimizar el almacenamiento según las necesidades específicas de sus aplicaciones.

---
## Visión General EBS Snapshots


Los snapshots (instantáneas) de Amazon Elastic Block Store (EBS) son copias de seguridad puntuales de los volúmenes EBS. Estas instantáneas permiten realizar copias de seguridad de los datos almacenados en volúmenes EBS y restaurarlos en cualquier momento. Son una herramienta esencial para la gestión de datos y la recuperación ante desastres en AWS.

1. [[Características Principales de EBS Snapshots]]
2. [[Creación y Uso de Snapshots]]
3. [[Ejemplos de Uso de EBS Snapshots]]
4. [[Costos y Gestión de Snapshots]]

Los snapshots de EBS son una herramienta crítica para la gestión de datos, permitiendo copias de seguridad confiables, recuperación rápida y migraciones entre regiones. La capacidad de automatizar la creación y gestión de snapshots facilita la administración de entornos complejos y mejora la resiliencia frente a fallos.

---
## Visión General de AMI


Una Amazon Machine Image (AMI) es una plantilla que contiene una configuración de software (incluyendo el sistema operativo, aplicaciones, y configuraciones) que se utiliza para lanzar instancias de Amazon EC2 (Elastic Compute Cloud). Una AMI proporciona la información necesaria para lanzar una instancia, lo que permite crear instancias nuevas que son réplicas exactas de una configuración específica.

1. [[TI/aws/seccion 6/ami/Características Principales de una AMI]]
2. [[TI/aws/seccion 6/ami/Crear y Gestionar AMIs]]
3. [[TI/aws/seccion 6/ami/Usos Comunes de AMIs]]
4. [[TI/aws/seccion 6/ami/Costos Asociados]]
5. [[TI/aws/seccion 6/ami/Buenas Prácticas]]

Las Amazon Machine Images (AMIs) son una herramienta fundamental en AWS para gestionar la configuración de instancias EC2. Facilitan el escalado, la distribución de software y la recuperación ante desastres, y son esenciales para la automatización y la gestión eficiente de infraestructuras en la nube.

---
## Contructor de imagenes EC2


El Amazon EC2 Image Builder es un servicio de AWS que facilita la creación, gestión y automatización de imágenes de máquinas personalizadas, incluyendo Amazon Machine Images (AMIs) para EC2. Este servicio simplifica el proceso de construcción, prueba y despliegue de imágenes de sistema operativo, permitiendo a los usuarios mantener sus imágenes seguras, actualizadas y consistentes.

1. [[Características Principales de EC2 Image Builder]]
2. [[Ejemplo de Uso]]
3. [[Beneficios del Uso de EC2 Image Builder]]

Amazon EC2 Image Builder es una herramienta poderosa que facilita la creación y gestión de imágenes personalizadas en AWS. Permite a los usuarios definir pipelines automatizados para construir, probar y distribuir AMIs de manera consistente y segura, mejorando la eficiencia operativa y la seguridad de las aplicaciones desplegadas en la nube.

---

## Almacén de Instancias de EC2

El Almacén de Instancias de EC2, también conocido como "Instance Store," es un tipo de almacenamiento temporal y de alta velocidad proporcionado por Amazon Web Services (AWS) para las instancias EC2. A diferencia de Amazon EBS (Elastic Block Store), el almacenamiento de instancias no es persistente y está directamente vinculado al ciclo de vida de la instancia EC2.

1. [[Características Principales del Almacén de Instancias]]
2. [[TI/aws/seccion 6/instance store/Casos de Uso Comunes]]
3. [[Tipos de Instancias con Almacén de Instancias]]
4. [[Cómo Usar el Almacén de Instancias]]
5. [[TI/aws/seccion 6/instance store/Limitaciones y Consideraciones]]

El Almacén de Instancias de EC2 es una solución de almacenamiento temporal y de alto rendimiento ideal para cargas de trabajo que requieren un acceso rápido a datos efímeros. Es una herramienta poderosa cuando se utiliza en conjunto con otros servicios de almacenamiento persistente como EBS y S3, permitiendo a los usuarios optimizar tanto el rendimiento como el costo en sus aplicaciones en la nube.

---

## Vision General de EFS

Amazon Elastic File System (EFS) es un servicio de almacenamiento de archivos en la nube ofrecido por Amazon Web Services (AWS) que permite a los usuarios montar un sistema de archivos compartido en múltiples instancias de EC2, lo que lo hace ideal para casos de uso donde se necesita un sistema de archivos común accesible desde varios servidores. EFS es completamente administrado, escalable y diseñado para ofrecer alta disponibilidad y durabilidad.

1. [[Características Principales de Amazon EFS]]
2. [[TI/aws/seccion 6/efs/Casos de Uso Comunes|Casos de Uso Comunes]]
3. [[Cómo Configurar y Usar EFS]]
4. [[Beneficios de Usar EFS]]
5. [[TI/aws/seccion 6/efs/Limitaciones y Consideraciones|Limitaciones y Consideraciones]]

Amazon EFS es una solución de almacenamiento de archivos flexible y escalable, ideal para aplicaciones que requieren un sistema de archivos compartido accesible desde múltiples instancias. Con su alta disponibilidad, durabilidad y facilidad de uso, EFS es una excelente opción para aplicaciones distribuidas, entornos de desarrollo colaborativo, y muchas otras cargas de trabajo que requieren acceso concurrente a archivos.

---

## Vision General de Amazon FSx

Amazon FSx es un servicio completamente administrado que facilita la creación, configuración y gestión de sistemas de archivos altamente escalables y de alto rendimiento en la nube de Amazon Web Services (AWS). Amazon FSx ofrece múltiples opciones de sistemas de archivos diseñados para diferentes necesidades, como Amazon FSx for Windows File Server, Amazon FSx for Lustre, Amazon FSx for NetApp ONTAP, y Amazon FSx for OpenZFS. Estos sistemas de archivos están optimizados para diferentes tipos de cargas de trabajo, desde aplicaciones empresariales hasta computación intensiva y análisis de datos.

1. [[Tipos de Amazon FSx]]
2. [[Beneficios de Usar Amazon FSx]]
3. [[TI/aws/seccion 6/fsx/Casos de Uso Comunes|Casos de Uso Comunes]]
4. [[Configuración y Uso de Amazon FSx]]
5. [[Beneficios de Usar Amazon FSx]]
6. [[TI/aws/seccion 6/fsx/Limitaciones y Consideraciones|Limitaciones y Consideraciones]]

Amazon FSx ofrece una solución de almacenamiento de archivos flexible, escalable y de alto rendimiento, diseñada para satisfacer una amplia variedad de necesidades empresariales y técnicas. Con opciones optimizadas para diferentes tipos de cargas de trabajo, desde aplicaciones empresariales en Windows hasta computación de alto rendimiento, FSx proporciona las herramientas necesarias para gestionar eficientemente los datos en la nube.

---
