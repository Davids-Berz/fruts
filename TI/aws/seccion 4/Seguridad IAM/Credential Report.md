#seguridad 

**Descripción**: Reporte que proporciona información sobre el estado de las credenciales de IAM (usuarios y sus claves de acceso, contraseñas, MFA).

**Uso**:

- Auditar el estado de las credenciales.
- Identificar credenciales no utilizadas o configuraciones inseguras.

**Acceso**:

- Generar el reporte desde la consola de IAM o mediante AWS CLI:

```
aws iam generate-credential-report
aws iam get-credential-report
```

