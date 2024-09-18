**AWS Snowball Edge** es un dispositivo más robusto y versátil que Snowcone, diseñado para mover grandes volúmenes de datos, con opciones adicionales para el procesamiento en el borde y soporte para varios casos de uso industrial.

#### Variantes de Snowball Edge:

- **Snowball Edge Storage Optimized**: Diseñado para transferir grandes cantidades de datos con capacidad de almacenamiento ampliada.
- **Snowball Edge Compute Optimized**: Combina capacidad de cómputo con almacenamiento para ejecutar cargas de trabajo de procesamiento en el borde (edge computing) mientras los datos se recopilan y se transfieren.

#### Características Principales:

- **Capacidad de Almacenamiento**:
    - **Storage Optimized**: Hasta 80 TB de almacenamiento utilizable.
    - **Compute Optimized**: Almacenamiento más pequeño (~42 TB) pero con mayor capacidad de procesamiento.
- **Cómputo en el Borde**: Ejecuta instancias de Amazon EC2 y contenedores Docker para procesar los datos localmente antes de transferirlos a la nube.
- **Durabilidad**: Snowball Edge está diseñado para ser robusto, resistente a golpes, vibraciones y entornos duros, como sitios industriales.
- **Seguridad**: Cifrado de datos de extremo a extremo utilizando claves gestionadas por el cliente mediante AWS Key Management Service (KMS).
- **Transferencia de Datos**: Los datos se transfieren físicamente a AWS y se copian a Amazon S3.

#### Casos de Uso:

- Migraciones de grandes cantidades de datos a AWS, como copias de seguridad masivas, archivos o bases de datos grandes.
- Procesamiento en el borde en fábricas, entornos militares o sitios de extracción donde no hay conectividad confiable.
- Implementación de instancias EC2 en ubicaciones remotas para ejecutar aplicaciones cerca de donde se generan los datos.

#### Cómo Funciona:

1. **Pedido del Dispositivo**: Se solicita el dispositivo desde la consola de AWS.
2. **Carga de Datos**: Una vez que llega el dispositivo, los datos se cargan utilizando la interfaz local del dispositivo o mediante herramientas como el cliente de AWS Snowball.
3. **Envío a AWS**: El dispositivo se devuelve a AWS, donde los datos se copian a S3. Los datos se cifran durante el transporte y solo el cliente puede descifrar los datos.