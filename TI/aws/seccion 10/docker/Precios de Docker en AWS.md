El costo de ejecutar Docker en AWS depende de los servicios que utilices:

- **Amazon ECS y Amazon EKS**: Se cobra por las instancias de EC2 o por el uso de AWS Fargate si eliges la opción serverless. El costo se basa en la cantidad de recursos (CPU, memoria, etc.) consumidos por los contenedores.
- **Amazon ECR**: ECR cobra por la cantidad de almacenamiento utilizado para almacenar imágenes de Docker y por las transferencias de datos cuando se extraen imágenes.