#### 1. **Despliegue de una sola AZ (Single-AZ Deployment)**

- En este tipo de despliegue, la base de datos se ejecuta en una única **zona de disponibilidad** (AZ).
- **Uso recomendado**: Aplicaciones no críticas o entornos de desarrollo/pruebas donde la alta disponibilidad no sea una prioridad.
- **Ventajas**: Menor costo, ya que solo se ejecuta una instancia de base de datos.
- **Desventaja**: No es tolerante a fallos, por lo que si la AZ falla, la base de datos no estará disponible hasta que se recupere.

#### 2. **Despliegue Multi-AZ**

- En este despliegue, RDS crea una **instancia en espera** en otra zona de disponibilidad (AZ) dentro de la misma región.
- **Tolerancia a Fallos**: Si la instancia principal falla (debido a una actualización, fallo de hardware, etc.), RDS realiza un failover automático a la instancia en espera.
- **Uso recomendado**: Aplicaciones críticas que requieren alta disponibilidad y mínima interrupción en caso de fallos.
- **Desventaja**: Mayor costo en comparación con Single-AZ, ya que se están ejecutando instancias redundantes.

#### 3. **Réplicas de Lectura**

- Las **réplicas de lectura** permiten distribuir las operaciones de lectura a otras instancias, aliviando la carga de la instancia principal.
- Las réplicas se sincronizan automáticamente con la base de datos principal.
- **Tipos de réplicas**:
    - **In-Region**: Réplicas dentro de la misma región, utilizadas para distribuir la carga de lectura local.
    - **Cross-Region**: Réplicas en otras regiones, útiles para mejorar el acceso geográfico y para recuperación ante desastres.

#### 4. **Despliegue Multi-Región**

- Permite tener instancias de base de datos replicadas en diferentes regiones de AWS, lo que proporciona redundancia geográfica.
- Ideal para escenarios en los que la disponibilidad global es crítica o se deben cumplir con requisitos normativos específicos sobre la ubicación de los datos.