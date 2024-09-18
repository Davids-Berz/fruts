**S3 Glacier Vault Lock** permite aplicar políticas de retención inmutables a los "vaults" de Amazon S3 Glacier, bloqueando los datos almacenados en ellos de forma irreversible para cumplir con normativas regulatorias y políticas corporativas. Una vez que una política de bloqueo de vault se establece, no se puede cambiar ni eliminar.

#### Características de Glacier Vault Lock

1. **Inmutabilidad de la Política**:
    
    - Una vez que una política de bloqueo de vault está activada, no se puede modificar ni eliminar, lo que asegura que los datos almacenados en el vault no se puedan modificar o eliminar hasta que finalice el período de retención.
2. **Políticas de Retención**:
    
    - Puedes definir períodos de retención que aplican a todos los archivos almacenados en el vault, asegurando que los archivos permanezcan inmutables durante ese tiempo.
3. **Aplicación de la Política de Cumplimiento**:
    
    - S3 Glacier Vault Lock cumple con los requisitos regulatorios más estrictos al garantizar que nadie, ni siquiera los administradores, pueda modificar o eliminar los datos durante el período de retención.

#### Casos de Uso de Glacier Vault Lock

- **Cumplimiento Regulatorio de Archivos a Largo Plazo**:
    - Cumplir con requisitos legales y regulatorios que requieren la inmutabilidad de datos archivados durante años o décadas.
- **Protección de Datos Sensibles**:
    - Garantizar que archivos legales, financieros o médicos se mantengan inalterables durante un período de tiempo definido.
- **Recuperación ante Desastres**:
    - Proteger datos de recuperación ante desastres que no deben modificarse ni eliminarse hasta que se necesiten para una restauración.

#### Cómo Habilitar Glacier Vault Lock

1. **Crear un Vault en S3 Glacier**:
    
    - Accede a la consola de Amazon S3 Glacier y crea un vault donde almacenarás los archivos que deseas proteger con Vault Lock.
2. **Definir una Política de Vault Lock**:
    
    - Utiliza AWS CLI o la consola de administración de AWS para definir una política de retención inmutable. Una vez establecida, la política no se puede modificar.
    
    Ejemplo de política de Vault Lock que impide la eliminación de archivos durante 365 días:

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PreventDeletion",
      "Effect": "Deny",
      "Principal": "*",
      "Action": "glacier:DeleteArchive",
      "Resource": "arn:aws:glacier:us-west-2:123456789012:vaults/my-vault",
      "Condition": {
        "NumericLessThanEquals": {
          "glacier:ArchiveAgeInDays": 365
        }
      }
    }
  ]
}
```

3. **Completar el Proceso de Vault Lock**:

- La política de Vault Lock pasa por un proceso de "configuración" y "bloqueo". Durante la configuración, puedes ajustar la política, pero una vez que se bloquea, no puede ser cambiada ni eliminada.

Comando para bloquear la política de Vault Lock:

```
aws glacier complete-vault-lock --account-id 123456789012 --vault-name my-vault --lock-id LOCK_ID
```

