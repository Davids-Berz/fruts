1. **S3 Standard (Estándar)**
    
    - **Descripción**: Esta es la clase de almacenamiento por defecto en S3. Está diseñada para datos a los que se accede frecuentemente y proporciona baja latencia y alta tasa de transferencia de datos.
    - **Características**:
        - Alta durabilidad: 99.999999999% (11 nueves).
        - Alta disponibilidad: 99.99%.
        - Almacenamiento redundante en múltiples zonas de disponibilidad (AZs).
        - No tiene cargos adicionales por recuperación de datos.
    - **Casos de Uso**:
        - Aplicaciones críticas donde el acceso a los datos es frecuente.
        - Sitios web, contenido multimedia, y sistemas de big data.
    - **Costo**: Es la opción más costosa en términos de almacenamiento, pero sin costos adicionales por recuperar los datos.
2. **S3 Intelligent-Tiering**
    
    - **Descripción**: Esta clase de almacenamiento optimiza los costos automáticamente al mover los datos entre los niveles de acceso frecuente e infrecuente según los patrones de acceso. Es ideal para datos con patrones de acceso impredecibles.
    - **Características**:
        - Alta durabilidad (99.999999999%).
        - Sin tarifas por recuperación de datos.
        - Ofrece varios niveles de almacenamiento: acceso frecuente, infrecuente, acceso esporádico y almacenamiento profundo de acceso infrecuente (Deep Archive).
        - Monitoreo y movimiento automático de objetos entre niveles según el acceso.
    - **Casos de Uso**:
        - Datos cuyo patrón de acceso no es predecible o cambia con el tiempo.
        - Datos analíticos, backups automáticos, logs.
    - **Costo**: Tarifa mensual baja para monitoreo y gestión, pero los costos de almacenamiento dependen de qué nivel de acceso utiliza el objeto.
3. **S3 Standard-IA (Infrequent Access, Acceso Infrecuente)**
    
    - **Descripción**: Diseñada para datos que se acceden con poca frecuencia pero que requieren una recuperación rápida cuando se acceden. Tiene un costo de almacenamiento menor que S3 Standard, pero cobra por la recuperación de datos.
    - **Características**:
        - Durabilidad: 99.999999999%.
        - Alta disponibilidad: 99.9%.
        - Almacenamiento redundante en múltiples zonas de disponibilidad.
        - Costo por recuperación de datos (GET requests).
    - **Casos de Uso**:
        - Backups, datos de recuperación ante desastres, archivos menos accedidos pero importantes.
    - **Costo**: Costos de almacenamiento más bajos que S3 Standard, pero con tarifas por recuperación de datos y acceso.
4. **S3 One Zone-IA**
    
    - **Descripción**: Similar a S3 Standard-IA, pero los datos se almacenan en una única zona de disponibilidad, lo que lo hace más económico. Es adecuado para datos a los que se accede con poca frecuencia y que no requieren la misma resiliencia que los datos almacenados en múltiples zonas.
    - **Características**:
        - Durabilidad: 99.999999999% en una única zona de disponibilidad.
        - Alta disponibilidad: 99.5%.
        - Menor costo de almacenamiento que S3 Standard-IA.
        - Costo por recuperación de datos.
    - **Casos de Uso**:
        - Datos que pueden ser recreados fácilmente o donde la resiliencia no es crítica.
        - Copias de datos temporales o almacenamiento de datos no críticos.
    - **Costo**: Más económico que S3 Standard-IA, pero con el riesgo de pérdida de datos si la zona de disponibilidad falla.
5. **S3 Glacier**
    
    - **Descripción**: Diseñada para el archivado de datos a largo plazo con costos extremadamente bajos. Los datos almacenados en S3 Glacier no se acceden frecuentemente y tienen tiempos de recuperación de minutos a horas.
    - **Características**:
        - Durabilidad: 99.999999999%.
        - Baja disponibilidad.
        - Recuperación de datos dentro de minutos o hasta varias horas, dependiendo de la opción de recuperación seleccionada.
        - Diseñado para datos de archivo a largo plazo.
    - **Casos de Uso**:
        - Archivos, copias de seguridad a largo plazo, almacenamiento de registros legales o financieros.
        - Datos que raramente necesitan ser recuperados, pero que deben almacenarse de manera segura.
    - **Costo**: Muy bajo costo de almacenamiento, pero los tiempos de recuperación y costos de extracción de datos son altos.
6. **S3 Glacier Deep Archive**
    
    - **Descripción**: Esta es la opción más económica de almacenamiento en Amazon S3, diseñada para datos que rara vez se acceden pero que deben conservarse durante largos periodos de tiempo, como décadas. Los tiempos de recuperación son más largos que en S3 Glacier.
    - **Características**:
        - Durabilidad: 99.999999999%.
        - Recuperación de datos entre 12 y 48 horas.
        - Diseñado para almacenamiento a largo plazo con acceso mínimo.
    - **Casos de Uso**:
        - Cumplimiento normativo, archivos históricos, backups a largo plazo.
    - **Costo**: El costo de almacenamiento más bajo de todas las clases de S3, pero los tiempos de recuperación son los más largos y tiene costos asociados por recuperación.