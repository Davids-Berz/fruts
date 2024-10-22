#### 6.1. **Cifrado en Tránsito y en Reposo**

EMR cifra los datos en reposo utilizando **AWS Key Management Service (KMS)** y asegura que los datos transferidos entre los nodos o entre EMR y otros servicios como S3 se cifren utilizando **SSL/TLS**.

#### 6.2. **Control de Acceso con IAM**

Utiliza **AWS IAM** para controlar qué usuarios pueden acceder y gestionar los clústeres de EMR. Puedes definir políticas detalladas que restringen el acceso a los datos procesados y a las instancias de EMR.

#### 6.3. **Amazon VPC**

Implementa tus clústeres de EMR dentro de una **Amazon Virtual Private Cloud (VPC)** para controlar completamente el tráfico de red entrante y saliente, aislando los recursos en una red privada.