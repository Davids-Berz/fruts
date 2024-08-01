#### ¿Qué es un Grupo de Seguridad?

Un grupo de seguridad es un conjunto de reglas que controlan el tráfico de red hacia y desde las instancias EC2. Cada regla en un grupo de seguridad especifica:

- **Protocolo**: El protocolo de red (TCP, UDP, ICMP).
- **Puerto**: El número de puerto o rango de puertos.
- **Fuente/Destino**: Las direcciones IP o grupos de seguridad que pueden enviar o recibir tráfico.

#### Características Principales

1. **Estado**: Los grupos de seguridad son stateful, lo que significa que si permites una solicitud de entrada, la respuesta correspondiente también se permite automáticamente.
2. **Por Instancia**: Cada instancia puede asociarse a uno o más grupos de seguridad.
3. **Reglas de Entrada y Salida**: Puedes definir reglas separadas para el tráfico entrante (inbound) y saliente (outbound).