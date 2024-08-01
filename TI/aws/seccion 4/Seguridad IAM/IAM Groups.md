#seguridad 

**Descripción**: Conjuntos de usuarios que comparten los mismos permisos. Permite gestionar permisos de forma más eficiente.

**Uso**:

- Agrupar usuarios por función o departamento (e.g., administradores, desarrolladores).
- Adjuntar políticas a grupos en lugar de a usuarios individuales.

**Ejemplo de Creación de Grupo y Asignación de Políticas**:

```
aws iam create-group --group-name Developers
aws iam attach-group-policy --group-name Developers --policy-arn arn:aws:iam::aws:policy/AmazonS3FullAccess
```

