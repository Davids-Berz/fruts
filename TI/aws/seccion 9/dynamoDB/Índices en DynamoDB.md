DynamoDB admite dos tipos de índices secundarios que permiten realizar consultas basadas en atributos adicionales a la clave principal:

#### 4.1. **Índice Secundario Global (Global Secondary Index, GSI)**

- **Atributos de Partición y Orden Personalizados**: Permite definir un índice sobre cualquier atributo de la tabla, lo que facilita la realización de consultas avanzadas.
- **Acceso Rápido a Datos**: Los GSI permiten realizar consultas eficientes en atributos que no forman parte de la clave principal de la tabla.

#### 4.2. **Índice Secundario Local (Local Secondary Index, LSI)**

- **Mismo Atributo de Partición, Atributo de Orden Diferente**: Los LSI permiten realizar consultas adicionales basadas en un atributo de orden distinto de la clave primaria, manteniendo el mismo atributo de partición.
- **Usado en Escenarios Específicos**: Se utiliza cuando necesitas realizar consultas avanzadas con diferentes atributos de orden en una misma partición.