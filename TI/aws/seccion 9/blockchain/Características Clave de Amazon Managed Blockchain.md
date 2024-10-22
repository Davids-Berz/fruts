#### 1.1. **Soporte para Hyperledger Fabric y Ethereum**

Amazon Managed Blockchain admite dos de los frameworks de blockchain más populares:

- **Hyperledger Fabric**: Es una plataforma de blockchain privada y empresarial que se utiliza principalmente para casos de uso donde varias organizaciones requieren un **control de acceso** y privacidad específicos. Ideal para aplicaciones de consorcio, comercio y cadena de suministro.
- **Ethereum**: Es una plataforma de blockchain pública y descentralizada que se utiliza comúnmente para crear **contratos inteligentes** y aplicaciones descentralizadas (**dApps**). Managed Blockchain soporta la creación de nodos y la conexión a la **red principal de Ethereum** o redes de prueba como **Rinkeby** y **Ropsten**.

#### 1.2. **Creación y Gestión de Redes de Blockchain**

Managed Blockchain simplifica el proceso de creación de redes de blockchain al proporcionar una interfaz fácil de usar para establecer redes de blockchain nuevas o unirse a redes existentes. Permite:

- **Crear una Red**: Puedes definir la configuración inicial de una red, los miembros y las políticas de gobernanza para controlar el acceso y la participación.
- **Unirse a una Red Existente**: Managed Blockchain permite unirse a redes de blockchain privadas o públicas y gestionar los nodos desde la consola de AWS.
- **Gestionar Miembros y Políticas**: Puedes gestionar quién puede unirse a la red, configurar permisos para cada participante y establecer políticas de votación y consenso.

#### 1.3. **Gestión Totalmente Automatizada**

Managed Blockchain se encarga de las tareas operativas como:

- **Aprovisionamiento de Nodos**: Crear y configurar nodos de blockchain automáticamente, sin necesidad de intervención manual.
- **Escalado Automático**: Managed Blockchain escala los nodos según la demanda para garantizar un rendimiento óptimo sin interrupciones.
- **Parches y Actualizaciones**: El servicio aplica automáticamente parches de seguridad y actualizaciones de software a los nodos sin interrupciones.

#### 1.4. **Mecanismos de Consenso**

Managed Blockchain ofrece soporte para varios **mecanismos de consenso**, dependiendo del framework utilizado:

- **Hyperledger Fabric**: Utiliza un enfoque de consenso basado en miembros, donde los participantes votan y acuerdan las transacciones antes de que sean validadas.
- **Ethereum**: Utiliza el protocolo de consenso **Proof of Work (PoW)** para validar transacciones y asegurar la red.

#### 1.5. **Alta Disponibilidad y Seguridad**

Managed Blockchain está diseñado para proporcionar **alta disponibilidad** y **seguridad**. Cada nodo de la red está alojado en la infraestructura de AWS, lo que asegura que la red esté disponible en todo momento y que los nodos estén protegidos contra fallos.

- **Almacenamiento Duradero**: Los datos de la blockchain se almacenan de manera duradera y se replican automáticamente, lo que asegura la integridad de las transacciones.
- **Seguridad Avanzada**: Managed Blockchain utiliza las características de seguridad de AWS, como el **cifrado en reposo** y **en tránsito**, para proteger los datos en la red de blockchain.

#### 1.6. **Integración con AWS Services**

Managed Blockchain se integra con otros servicios de AWS, como **Amazon CloudWatch** para monitorear el rendimiento de los nodos, **AWS CloudTrail** para auditar las transacciones en la red, y **AWS Key Management Service (KMS)** para administrar claves criptográficas y proteger las transacciones.