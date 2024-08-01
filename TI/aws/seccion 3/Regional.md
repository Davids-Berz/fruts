### Regiones

- **Definición**: Una región de AWS es una ubicación geográfica separada que contiene múltiples zonas de disponibilidad (AZ).
- **Características**:
    - Cada región es autónoma e independiente en términos de energía, refrigeración, y red.
    - Los datos y servicios en una región no se comparten automáticamente con otras regiones.
    - Esto permite a los usuarios cumplir con requisitos de ubicación de datos y normativas locales.
- **Ejemplos de Regiones**:
    - us-east-1 (Norte de Virginia)
    - eu-west-1 (Irlanda)
    - ap-southeast-1 (Singapur)

### Zonas de Disponibilidad (AZ)

- **Definición**: Una zona de disponibilidad es un centro de datos o un grupo de centros de datos dentro de una región.
- **Características**:
    - Cada región tiene al menos dos AZ para proporcionar alta disponibilidad y redundancia.
    - Las AZ dentro de una región están conectadas a través de redes de baja latencia y alta capacidad.
    - Los usuarios pueden diseñar aplicaciones que se repliquen entre múltiples AZ para mejorar la tolerancia a fallos.
- **Ejemplo de Estructura**:
    - us-east-1a, us-east-1b, us-east-1c (tres zonas de disponibilidad en la región de Norte de Virginia)

### Puntos de Presencia (PoP)

- **Definición**: Los puntos de presencia son ubicaciones donde AWS distribuye contenido a través de su red global para mejorar la entrega y la latencia.
- **Características**:
    - Incluyen Edge Locations y Regional Edge Caches.
    - Utilizados principalmente para servicios como Amazon CloudFront y AWS Global Accelerator.
    - Mejoran la entrega de contenido estático y dinámico a usuarios finales.
