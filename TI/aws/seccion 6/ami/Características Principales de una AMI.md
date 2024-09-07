- **Plantilla para Instancias EC2**:
    
    - Una AMI es una plantilla a partir de la cual se crean instancias EC2. Cada instancia lanzada desde una AMI es una réplica exacta del entorno de software definido en esa AMI.

- **Componentes de una AMI**:
    
    - **Imagen del Sistema Operativo**: Incluye el sistema operativo (como Linux, Windows) y el software preinstalado.
    - **Volúmenes de Almacenamiento**: Especifica los volúmenes de almacenamiento que deben adjuntarse a la instancia cuando se lanza.
    - **Permisos de Lanzamiento**: Define quién puede usar la AMI para lanzar instancias (por ejemplo, solo el propietario, cuentas específicas, o el público).
    - **Mapeo de Dispositivos**: Especifica cómo se deben configurar los dispositivos de almacenamiento (como EBS o volúmenes efímeros) cuando se lanza una instancia.

- **Tipos de AMIs**:
    
    - **AMIs Públicas**: AMIs disponibles para todos los usuarios de AWS. Incluyen AMIs oficiales proporcionadas por AWS y AMIs compartidas por otros usuarios.
    - **AMIs Privadas**: AMIs que solo están disponibles para el propietario o para cuentas específicas con las que se han compartido.
    - **AMIs Pagas**: AMIs disponibles en AWS Marketplace, que pueden incluir software comercial o configuraciones especializadas.