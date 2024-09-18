En el **cifrado del lado del cliente**, los datos se cifran antes de ser subidos a S3 y se descifran después de ser descargados por el cliente. El cliente gestiona el cifrado y descifrado de los datos, mientras que S3 almacena los objetos ya cifrados.

#### Opciones de Cifrado del Lado del Cliente:

1. **Claves gestionadas por AWS KMS**:
    
    - El cliente utiliza AWS KMS para generar y administrar claves, pero el cifrado y descifrado de los datos se realiza en el lado del cliente antes de subir los datos a S3.
2. **Claves gestionadas por el cliente**:
    
    - El cliente gestiona completamente sus claves de cifrado y realiza todas las operaciones de cifrado y descifrado de los datos antes y después de interactuar con S3.