#### 2.1. **Funciones Lambda**

Una **función Lambda** es el código que escribes para realizar una tarea específica. Cada función se ejecuta en respuesta a un evento y se escala automáticamente para manejar la cantidad de invocaciones simultáneas necesarias.

- **Código de la Función**: El código puede ser escrito directamente en la consola de AWS o subido desde tu máquina local. También puedes utilizar **AWS Lambda Layers** para compartir y reutilizar librerías y dependencias en múltiples funciones.

Ejemplo de una función Lambda en Python que responde a un evento de S3:

```
import json
import boto3

def lambda_handler(event, context):
    s3 = boto3.client('s3')
    bucket = event['Records'][0]['s3']['bucket']['name']
    key = event['Records'][0]['s3']['object']['key']
    
    response = s3.get_object(Bucket=bucket, Key=key)
    file_content = response['Body'].read().decode('utf-8')
    
    print(f'File content: {file_content}')
    return {
        'statusCode': 200,
        'body': json.dumps('File processed successfully!')
    }
```

#### 2.2. **Triggers**

Los **triggers** son los eventos que activan una función Lambda. Estos pueden ser eventos provenientes de otros servicios de AWS o solicitudes HTTP recibidas a través de **Amazon API Gateway**.

Algunos triggers comunes incluyen:

- **S3**: Al cargar un archivo en un bucket de S3.
- **DynamoDB**: Al actualizar un registro en una tabla.
- **API Gateway**: Al recibir una solicitud HTTP.

#### 2.3. **Layers (Capas)**

Las **capas de Lambda** te permiten agrupar y compartir código, librerías o configuraciones comunes entre varias funciones Lambda. Esto es útil para evitar la duplicación de código y reducir el tamaño de los paquetes de implementación.

#### 2.4. **Environment Variables (Variables de Entorno)**

Puedes definir variables de entorno para tus funciones Lambda. Estas variables pueden contener configuraciones, credenciales u otros datos que tu función necesita para ejecutarse. Las variables de entorno pueden cifrarse con **AWS Key Management Service (KMS)** para mayor seguridad.

#### 2.5. **Permisos e IAM Roles**

Cada función Lambda necesita un **rol de IAM** que define los permisos para acceder a otros recursos de AWS. Por ejemplo, si tu función necesita leer un archivo de S3 o escribir en DynamoDB, el rol debe tener los permisos adecuados para acceder a esos recursos.