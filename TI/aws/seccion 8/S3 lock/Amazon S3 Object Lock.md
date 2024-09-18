**S3 Object Lock** permite evitar la eliminación o modificación de objetos durante un período de retención definido. Esto es particularmente útil para cumplir con normativas que requieren que los datos sean inmutables durante un tiempo determinado, como en sectores financieros, legales o de salud.

#### Características de S3 Object Lock

1. **Inmutabilidad**:
    
    - Bloquea los objetos para que no puedan ser eliminados o sobrescritos durante un período de retención, asegurando que los datos permanezcan inalterados.
2. **Modos de Bloqueo**:
    
    - **Modo de Gobernanza (Governance Mode)**:
        - Los usuarios con permisos especiales (como `s3:BypassGovernanceRetention`) pueden eliminar o modificar los objetos bloqueados antes de que finalice el período de retención.
    - **Modo de Cumplimiento (Compliance Mode)**:
        - Los objetos no se pueden modificar o eliminar por nadie, ni siquiera por el administrador de la cuenta, hasta que el período de retención haya expirado. Este modo cumple con los requisitos más estrictos de inmutabilidad de datos.
3. **Períodos de Retención**:
    
    - Puedes establecer un período de retención en días o años durante el cual los objetos están protegidos. Durante este tiempo, los objetos están bloqueados y no pueden ser eliminados o sobrescritos.
4. **Marcadores de Eliminación Legal (Legal Hold)**:
    
    - Un marcador de "Legal Hold" es similar a un bloqueo, pero no tiene un período de retención específico. Puede aplicarse para mantener los objetos protegidos indefinidamente hasta que se elimine manualmente el marcador de retención legal.

#### Casos de Uso de S3 Object Lock

- **Cumplimiento Regulatorio**:
    - Cumplir con regulaciones como SEC Rule 17a-4(f) que requieren que los registros permanezcan inmutables durante un cierto tiempo.
- **Protección de Backups**:
    - Evitar la eliminación o modificación de copias de seguridad críticas durante un período de tiempo determinado.
- **Mitigación de Ransomware**:
    - Proteger los objetos de modificaciones no autorizadas en caso de ataques de ransomware o amenazas internas.

#### Cómo Habilitar S3 Object Lock

1. **Crear un Bucket con Object Lock**:
    
    - Al crear un bucket en Amazon S3, debes habilitar Object Lock. No puedes habilitar Object Lock en un bucket existente.
    
    En la consola de S3, selecciona "Enable Object Lock" cuando crees el bucket.
    
2. **Configurar la Política de Retención**:
    
    - Una vez habilitado Object Lock en el bucket, puedes aplicar políticas de retención a nivel de objeto o configurar una política predeterminada de retención para todo el bucket.
3. **Usar AWS CLI o la Consola para Aplicar el Bloqueo**:
    
    - Usa la consola de S3 o la AWS CLI para cargar objetos y aplicar un período de retención y el modo de bloqueo deseado.

Ejemplo de cómo habilitar Object Lock en un objeto mediante AWS CLI:

```
aws s3api put-object-lock-configuration \
    --bucket nombre-del-bucket \
    --object-lock-enabled-for-bucket
```

