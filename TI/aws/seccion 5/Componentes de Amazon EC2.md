- **Instancias**:
    - **Descripción**: Servidores virtuales que se ejecutan en la infraestructura de AWS.
    - **Uso**: Desplegar aplicaciones, ejecutar bases de datos, alojar sitios web y más.

- **Tipos de Instancias**:
    - **Descripción**: Diferentes configuraciones de CPU, memoria, almacenamiento y capacidad de red.
    - **Tipos Comunes**:
        - **General Purpose**: Instancias equilibradas en términos de CPU, memoria y red (e.g., t2.micro, m5.large).
        - **Compute Optimized**: Alta relación de CPU respecto a memoria (e.g., c5.large).
        - **Memory Optimized**: Alta capacidad de memoria respecto a CPU (e.g., r5.large).
        - **Storage Optimized**: Alta capacidad de almacenamiento y rendimiento IOPS (e.g., i3.large).
        - **Accelerated Computing**: Instancias con GPU para cargas de trabajo intensivas en computación (e.g., p3.2xlarge).

- **Amazon Machine Images (AMIs)**:
    - **Descripción**: Plantillas preconfiguradas que contienen el sistema operativo y el software necesario para lanzar una instancia.
    - **Uso**: Crear instancias EC2 rápidamente con configuraciones específicas.

- **Elastic Block Store (EBS)**:
    - **Descripción**: Volúmenes de almacenamiento persistente para instancias EC2.
    - **Uso**: Almacenar datos que persisten más allá del ciclo de vida de una instancia.

- **Security Groups**:
    - **Descripción**: Conjuntos de reglas de firewall que controlan el tráfico entrante y saliente de las instancias EC2.
    - **Uso**: Proteger instancias controlando el acceso basado en IP y puerto.

- **Elastic IP Addresses**:
    - **Descripción**: Direcciones IP estáticas que se pueden asignar a instancias EC2.
    - **Uso**: Mantener direcciones IP fijas para aplicaciones que requieren una IP estática.

- **Key Pairs**:
    - **Descripción**: Herramientas de autenticación utilizadas para conectarse de manera segura a instancias EC2.
    - **Uso**: Generar y usar claves SSH para acceder a instancias Linux/Unix y claves RDP para instancias Windows.
