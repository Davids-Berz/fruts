#### Crear una AMI Personalizada con Software Preinstalado

1. **Seleccionar AMI Base**:
    
    - Utiliza una AMI de Amazon Linux 2 como base.

2. **Añadir Componentes Personalizados**:
    
    - Añade componentes para instalar Apache, configurar un sitio web estático, y aplicar actualizaciones de seguridad.

3. **Configurar Pruebas**:
    
    - Añade pruebas que verifiquen que Apache está instalado y que el sitio web es accesible.

4. **Configurar Distribución**:
    
    - Configura el pipeline para copiar la AMI a las regiones `us-west-2` y `us-east-1` después de la construcción.

5. **Construir y Lanzar Instancias**:
    
    - Lanza el pipeline y, tras completar la construcción, utiliza la nueva AMI para lanzar instancias EC2 que estarán listas con Apache preconfigurado.