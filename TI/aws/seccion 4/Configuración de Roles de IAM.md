#### Paso 1: Crear un Rol

1. **Acceder a IAM**:
    
    - Inicia sesión en la consola de administración de AWS.
    - Navega a **IAM** en el menú de servicios.
2. **Crear un Nuevo Rol**:
    
    - En el panel lateral, selecciona **Roles** y luego haz clic en **Create role**.
3. **Seleccionar el Tipo de Entidad de Confianza**:
    
    - Selecciona el tipo de entidad que asumirá el rol. Las opciones comunes incluyen:
        - **AWS service**: Permite que un servicio de AWS asuma el rol.
        - **Another AWS account**: Permite que una cuenta de AWS externa asuma el rol.
        - **Web identity**: Permite que aplicaciones web o móviles asuman el rol mediante identidad federada.
        - **SAML 2.0 federation**: Permite que usuarios federados asuman el rol mediante SAML.
4. **Elegir el Servicio de AWS**:
    
    - Si seleccionaste **AWS service**, elige el servicio específico (e.g., EC2, Lambda, etc.) que asumirá el rol.
5. **Adjuntar Políticas**:
    
    - Selecciona las políticas que definirán los permisos del rol. Puedes elegir entre políticas gestionadas por AWS, políticas personalizadas, o crear una nueva política.
6. **Configurar la Política de Confianza**:
    
    - Define la política de confianza que especifica las entidades que pueden asumir el rol.
7. **Asignar un Nombre y Crear el Rol**:
    
    - Asigna un nombre y una descripción al rol.
    - Haz clic en **Create role** para finalizar la creación del rol.

#### Paso 2: Configurar la Política de Confianza

Ejemplo de una política de confianza para permitir que el servicio EC2 asuma un rol:

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": {
        "Service": "ec2.amazonaws.com"
      },
      "Action": "sts:AssumeRole"
    }
  ]
}
```

### Casos de Uso Comunes


