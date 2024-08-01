#### Paso 1: Crear un Grupo de Seguridad

1. Accede a la [Consola de administración de AWS](https://aws.amazon.com/console/).
2. Navega a **EC2** y selecciona **Security Groups** en el menú de la izquierda.
3. Haz clic en **Create Security Group**.
4. Proporciona un nombre y una descripción para el grupo de seguridad.
5. Selecciona la VPC a la que pertenecerá el grupo de seguridad.

#### Paso 2: Configurar Reglas de Entrada

Configura las reglas para controlar el tráfico entrante. Aquí hay algunos ejemplos de reglas comunes:

1. **SSH (Secure Shell) - Puerto 22**:
    
    - **Protocolo**: TCP
    - **Puerto**: 22
    - **Fuente**: Tu dirección IP (por ejemplo, 203.0.113.0/32) para permitir el acceso SSH solo desde tu IP.
2. **HTTP - Puerto 80**:
    
    - **Protocolo**: TCP
    - **Puerto**: 80
    - **Fuente**: 0.0.0.0/0 (permitir acceso desde cualquier lugar).
3. **HTTPS - Puerto 443**:
    
    - **Protocolo**: TCP
    - **Puerto**: 443
    - **Fuente**: 0.0.0.0/0 (permitir acceso desde cualquier lugar).
4. **RDP (Remote Desktop Protocol) - Puerto 3389**:
    
    - **Protocolo**: TCP
    - **Puerto**: 3389
    - **Fuente**: Tu dirección IP (por ejemplo, 203.0.113.0/32) para permitir el acceso RDP solo desde tu IP.

#### Paso 3: Configurar Reglas de Salida

Configura las reglas para controlar el tráfico saliente. Por defecto, los grupos de seguridad permiten todo el tráfico saliente. Puedes restringirlo si es necesario.

1. **Permitir todo el tráfico saliente** (regla predeterminada):
    - **Protocolo**: ALL
    - **Puerto**: ALL
    - **Destino**: 0.0.0.0/0

#### Paso 4: Asociar el Grupo de Seguridad a una Instancia

1. Al lanzar una nueva instancia EC2, selecciona el grupo de seguridad que has creado.
2. Para instancias existentes, puedes cambiar el grupo de seguridad desde la consola de EC2 seleccionando la instancia, haciendo clic en "Actions" y luego en "Networking" > "Change Security Groups".