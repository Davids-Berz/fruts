- **Replicación Asíncrona**:
    
    - La replicación de objetos en S3 es asíncrona, lo que significa que los objetos se copian después de ser subidos o modificados en el bucket de origen. S3 garantiza que las copias eventualmente se realizarán, pero no hay una garantía estricta de tiempo de replicación.

- **Replicación de Metadatos**:
    
    - Además de los datos, S3 replica los metadatos asociados, como las etiquetas de los objetos y el estado de cifrado.

- **Replicación de Todo o Parte del Bucket**:
    
    - Puedes replicar todos los objetos en un bucket o configurar reglas para replicar solo ciertos objetos según el prefijo, la etiqueta, o la clase de almacenamiento.

- **Replicación de Versiones**:
    
    - Si el versionado está habilitado en ambos el bucket de origen y el de destino, S3 replicará todas las versiones de los objetos.

- **Opciones de Cifrado**:
    
    - Los objetos se pueden cifrar en el bucket de destino utilizando el mismo esquema de cifrado que el origen o un esquema diferente (por ejemplo, cambiando de claves gestionadas por el cliente a claves gestionadas por AWS KMS).

- **Soporte para Replicación de Objetos Existentes**:
    
    - A través de la replicación S3 Batch Operations, puedes replicar objetos existentes en el bucket de origen al de destino, además de los nuevos objetos creados después de habilitar la replicación.