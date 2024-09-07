#### Caso de Uso 1: Copia de Seguridad y Restauración de una Base de Datos

- **Copia de Seguridad**:
    - Crear snapshots diarios de un volumen EBS donde se almacena la base de datos.
- **Restauración**:
    - En caso de corrupción de datos, crea un nuevo volumen desde el snapshot más reciente y adjúntalo a la instancia EC2 para restaurar la base de datos.

#### Caso de Uso 2: Migración entre Regiones

- **Copia del Snapshot**:
    - Copiar un snapshot de un volumen EBS a una región diferente.
- **Restauración en la Nueva Región**:
    - Crear un nuevo volumen en la región de destino y adjuntarlo a una instancia EC2 en esa región.

#### Caso de Uso 3: Mantenimiento y Pruebas

- **Snapshot de Prueba**:
    - Antes de realizar actualizaciones de software, crea un snapshot del volumen.
- **Reversión Rápida**:
    - Si algo sale mal durante la actualización, restaura el volumen desde el snapshot.