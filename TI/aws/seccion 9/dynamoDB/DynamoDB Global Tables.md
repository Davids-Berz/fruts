**Global Tables** permite replicar una tabla de DynamoDB en múltiples regiones de AWS, proporcionando consistencia global de los datos y baja latencia para usuarios distribuidos en diferentes ubicaciones geográficas.

#### Características Clave de Global Tables:

- **Alta Disponibilidad Global**: Si una región experimenta un problema, DynamoDB redirige el tráfico automáticamente a otra región disponible.
- **Lecturas y Escrituras Multi-Maestro**: Los datos pueden escribirse y leerse en múltiples regiones, y DynamoDB se encarga de sincronizar automáticamente las actualizaciones entre las regiones.

#### Casos de Uso:

- **Aplicaciones globales con alta disponibilidad**: Ideal para aplicaciones que necesitan estar disponibles en todo el mundo con bajas latencias.
- **Recuperación ante desastres**: Puedes configurar tablas globales para mantener una copia de los datos en diferentes regiones, asegurando la continuidad del negocio.