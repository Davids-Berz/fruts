#### 4.1. **Cifrado en Reposo y en Tránsito**

- Athena admite el **cifrado de datos en reposo** en S3 utilizando **AWS KMS** para proteger los datos almacenados.
- El cifrado en tránsito está habilitado de forma predeterminada, garantizando que los datos consultados estén protegidos mediante SSL/TLS durante su transmisión.

#### 4.2. **Control de Acceso con IAM**

- Puedes controlar el acceso a Amazon Athena y sus consultas a través de **AWS Identity and Access Management (IAM)**. Las políticas de IAM te permiten definir permisos detallados sobre quién puede ejecutar consultas y qué datos pueden consultar.

#### 4.3. **Amazon VPC y Red Privada**

- Aunque Athena es un servicio público, puedes conectarlo a datos en S3 que estén dentro de una **Amazon VPC** (Virtual Private Cloud) utilizando **VPC endpoints** para mayor seguridad y control del tráfico de red.