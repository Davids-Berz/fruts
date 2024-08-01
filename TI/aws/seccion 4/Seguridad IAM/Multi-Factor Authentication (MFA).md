#seguridad 

**Descripción**: Añade una capa adicional de seguridad mediante el requerimiento de un segundo factor de autenticación (e.g., un código generado por un dispositivo MFA).

**Uso**:

- Habilitar MFA para usuarios con permisos sensibles.
- Configurar dispositivos MFA virtuales o de hardware.

**Ejemplo de Habilitación de MFA**:

```
aws iam enable-mfa-device --user-name JohnDoe --serial-number "arn:aws:iam::123456789012:mfa/JohnDoe" --authentication-code1 123456 --authentication-code2 789012
```

