1. **Automatización del Proceso de Construcción de Imágenes**:
    
    - EC2 Image Builder permite automatizar el proceso de creación de imágenes mediante pipelines (canales de integración continua), lo que facilita la actualización y distribución de imágenes.

2. **Componentes Personalizados**:
    
    - Permite añadir software y configuraciones personalizadas a las imágenes. Puedes definir scripts, instalar aplicaciones, aplicar parches y más.

3. **Pruebas Integradas**:
    
    - Ofrece la posibilidad de ejecutar pruebas automatizadas en las imágenes creadas para asegurarse de que cumplen con los requisitos antes de ser distribuidas o utilizadas.

4. **Distribución Regional**:
    
    - Facilita la copia de AMIs creadas a múltiples regiones de AWS, asegurando que las imágenes estén disponibles donde las necesites.

5. **Integración con Servicios de AWS**:
    
    - Se integra con otros servicios de AWS como Amazon S3, AWS Systems Manager, y AWS CloudWatch para almacenar artefactos, gestionar configuraciones y monitorizar el proceso de creación.

## Proceso de Creación de Imágenes con EC2 Image Builder

#### Paso 1: Definir una Plantilla de Imagen

1. **Acceder a la Consola de AWS**:
    
    - Inicia sesión en la [Consola de administración de AWS](https://aws.amazon.com/console/).

2. **Navegar a EC2 Image Builder**:
    
    - Ve a **EC2** en el menú de servicios y selecciona **Image Builder**.

3. **Crear una Nueva Plantilla de Imagen**:
    
    - Haz clic en **Create image pipeline**.
    - Define un nombre y una descripción para tu pipeline.

4. **Seleccionar un Sistema Operativo Base**:
    
    - Selecciona un sistema operativo base desde una AMI existente, como Amazon Linux 2, Ubuntu, o Windows Server.

5. **Añadir Componentes**:
    
    - Añade componentes personalizados para configurar el software, aplicar parches, y ejecutar scripts en la imagen.
    - Los componentes pueden ser proporcionados por AWS o creados y cargados por ti.

#### Paso 2: Configurar el Pipeline

1. **Configurar la Frecuencia de Construcción**:
    
    - Define la frecuencia con la que se ejecutará el pipeline para crear nuevas imágenes. Puede ser diario, semanal, mensual, o manual.

2. **Configurar Pruebas**:
    
    - Añade fases de prueba automatizadas para verificar que la imagen cumple con los requisitos. Las pruebas pueden incluir validaciones de configuración, pruebas de integración, y más.

3. **Seleccionar Regiones de Distribución**:
    
    - Configura en qué regiones de AWS se copiará la imagen una vez creada.

4. **Configurar Notificaciones**:
    
    - Configura notificaciones a través de Amazon SNS para recibir alertas sobre el estado de las construcciones de imágenes.

5. **Configurar Políticas de Retención**:
    
    - Define cuánto tiempo se conservarán las imágenes anteriores antes de ser eliminadas automáticamente.

#### Paso 3: Construir y Gestionar Imágenes

1. **Lanzar la Construcción**:
    
    - Una vez que el pipeline está configurado, puedes lanzarlo manualmente o esperar a que se ejecute en la siguiente ventana programada.

2. **Monitorear el Proceso**:
    
    - Utiliza Amazon CloudWatch para monitorear el proceso de construcción y recibir alertas sobre el éxito o fracaso de las operaciones.

3. **Ver las Imágenes Construidas**:
    
    - Después de que una imagen ha sido construida y probada, estará disponible en la consola de EC2 bajo **AMIs**.

4. **Utilizar o Distribuir la Imagen**:
    
    - Puedes lanzar nuevas instancias EC2 utilizando la AMI construida, compartirla con otras cuentas, o copiarla a diferentes regiones.