1. **Abrir PowerShell**:
    
    - Abre PowerShell en Windows (puedes buscar "PowerShell" en el menú de inicio).
2. **Configurar Permisos del Archivo PEM**:
    
    - Aunque Windows no utiliza los permisos de archivo de la misma manera que Linux, puedes asegurar que solo tú tengas acceso al archivo usando el siguiente comando:

```
icacls "C:\ruta\a\EC2Tutorial.pem" /inheritance:r /grant:r tu-usuario:F
```

- Reemplaza `"C:\ruta\a\EC2Tutorial.pem"` con la ruta completa a tu archivo PEM y `tu-usuario` con tu nombre de usuario en Windows.