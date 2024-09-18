En el **cifrado del lado del servidor**, Amazon S3 cifra los datos cuando los recibe y los descifra automáticamente cuando son recuperados. El cifrado se realiza dentro de los servidores de AWS después de recibir los datos y antes de almacenarlos en S3.

#### Opciones de Cifrado del Lado del Servidor:

1. **SSE-S3 (Server-Side Encryption with Amazon S3-Managed Keys)**:
    
    - **Descripción**: Amazon S3 gestiona automáticamente las claves de cifrado por ti.
    - **Características**:
        - Amazon S3 cifra los datos utilizando claves gestionadas por AWS y maneja automáticamente la rotación y protección de las claves.
        - No requiere gestión manual de claves por parte del usuario.
    - **Caso de uso**: Para aquellos que necesitan una solución de cifrado automática y sin complejidad adicional.
    - **Comando AWS CLI para habilitar SSE-S3**:

```
aws s3 cp archivo.txt s3://nombre-del-bucket/ --sse AES256
```

2. **SSE-KMS (Server-Side Encryption with AWS Key Management Service Keys)**:

- **Descripción**: AWS Key Management Service (KMS) gestiona las claves de cifrado. SSE-KMS proporciona control detallado sobre la gestión y el acceso a las claves.
- **Características**:
    - Las claves se gestionan utilizando AWS KMS, lo que permite control detallado sobre quién puede acceder a las claves y auditabilidad de las solicitudes de descifrado.
    - Compatible con la rotación automática de claves y proporciona registros de uso detallados a través de AWS CloudTrail.
- **Caso de uso**: Para organizaciones que requieren un mayor control sobre las claves de cifrado y desean monitorizar el uso de las mismas.
- **Comando AWS CLI para habilitar SSE-KMS**:

```
aws s3 cp archivo.txt s3://nombre-del-bucket/ --sse aws:kms --sse-kms-key-id arn:aws:kms:region:account-id:key/key-id
```

3. **SSE-C (Server-Side Encryption with Customer-Provided Keys)**:

- **Descripción**: Los usuarios proporcionan y gestionan sus propias claves de cifrado, pero AWS realiza el cifrado y descifrado con esas claves.
- **Características**:
    - Los clientes tienen control total sobre las claves de cifrado, pero AWS no las almacena ni las gestiona. Las claves se deben proporcionar con cada operación de carga y descarga.
    - AWS aplica el cifrado y descifrado en sus servidores, pero las claves nunca se almacenan en AWS.
- **Caso de uso**: Para organizaciones que necesitan un control completo sobre las claves de cifrado sin depender de AWS KMS.
- **Comando AWS CLI para habilitar SSE-C**

```
aws s3 cp archivo.txt s3://nombre-del-bucket/ --sse-c AES256 --sse-c-key <clave-base64>
```

