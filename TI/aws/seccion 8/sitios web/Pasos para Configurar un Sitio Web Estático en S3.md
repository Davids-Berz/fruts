#### 1. Crear un Bucket en S3

1. **Accede a la Consola de Amazon S3**:
    
    - Inicia sesión en la [Consola de administración de AWS](https://aws.amazon.com/console/).

2. **Crear un Nuevo Bucket**:
    
    - Haz clic en "Create bucket".
    - Asigna un nombre único a tu bucket. El nombre del bucket debe ser globalmente único en S3, ya que los nombres de buckets son compartidos a nivel mundial.
    - Selecciona la región donde deseas crear el bucket.

3. **Configurar Opciones de Bucket**:
    
    - Deshabilita el bloqueo de acceso público si planeas hacer que el sitio sea accesible públicamente.
    - Puedes habilitar el versionado si deseas mantener versiones antiguas de tus archivos.

4. **Finalizar la Creación del Bucket**:
    
    - Revisa la configuración y haz clic en "Create bucket".

#### 2. Subir los Archivos del Sitio Web

1. **Seleccionar el Bucket**:
    
    - En la consola de S3, selecciona el bucket que acabas de crear.

2. **Subir los Archivos del Sitio Web**:
    
    - Haz clic en "Upload" y selecciona los archivos y carpetas que componen tu sitio web (por ejemplo, `index.html`, `styles.css`, `images/`, etc.).
    - Puedes arrastrar y soltar los archivos directamente en la consola o utilizar el botón de selección.

3. **Configurar Permisos**:
    
    - Asegúrate de que los archivos que deseas hacer públicos (como `index.html`) tengan configurados los permisos de acceso público, o configura una política de bucket para permitir el acceso público a todo el contenido del sitio.

#### 3. Configurar el Bucket para Hosting de Sitio Web Estático

1. **Configurar el Bucket como Sitio Web**:
    
    - En la consola de S3, ve a la pestaña "Properties" del bucket.
    - Busca la sección "Static website hosting" y haz clic en "Edit".
    - Selecciona "Use this bucket to host a website".
    - Especifica el nombre del archivo de índice, generalmente `index.html`. Si tienes un archivo de error personalizado, como `error.html`, también puedes especificarlo aquí.
    - Haz clic en "Save changes".

2. **Obtener la URL del Sitio Web**:
    
    - Una vez configurado, S3 generará una URL para tu sitio web. Esta URL tendrá el formato:
    - `http://your-bucket-name.s3-website-your-region.amazonaws.com`
    - Puedes usar esta URL para acceder a tu sitio web estático.

#### 4. Hacer Público el Bucket (Opcional)

Si el contenido de tu sitio web debe ser accesible para el público en general, necesitarás configurar el bucket para permitir el acceso público:

1. **Configurar una Política de Bucket**:
    
    - Ve a la pestaña "Permissions" en la consola de S3.
    - Haz clic en "Bucket Policy" y agrega una política como la siguiente para permitir el acceso público:

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::your-bucket-name/*"
    }
  ]
}
```

- Reemplaza `your-bucket-name` con el nombre de tu bucket.

2. **Verificar el Acceso Público**:
    
    - Asegúrate de que el acceso público está habilitado en la sección "Block public access settings for this bucket".

#### 5. Configurar un Nombre de Dominio Personalizado (Opcional)

Si deseas utilizar un dominio personalizado en lugar de la URL generada por S3, sigue estos pasos:

1. **Registrar un Dominio**:
    
    - Si no tienes un dominio, puedes registrar uno usando Amazon Route 53 o cualquier otro registrador de dominios.

2. **Configurar un Alias en Route 53**:
    
    - Ve a Amazon Route 53 en la consola de AWS.
    - Selecciona o crea una zona hospedada para tu dominio.
    - Crea un nuevo registro tipo "A" o "CNAME" con el nombre de tu dominio y como valor, selecciona "Alias" y apunta al bucket de S3 configurado como sitio web.

3. **Actualizar Configuración del Bucket**:
    
    - Asegúrate de que el nombre de tu bucket coincide exactamente con el nombre de tu dominio (por ejemplo, `www.example.com`).
    - S3 redirigirá automáticamente el tráfico de `http://www.example.com` a tu sitio web estático en S3.

#### 6. Implementar SSL/TLS (HTTPS) (Opcional)

Para habilitar HTTPS en tu sitio web:

1. **Usar Amazon CloudFront**:
    
    - Crea una distribución de Amazon CloudFront para tu sitio web.
    - Configura CloudFront para que tenga como origen tu bucket S3.
    - Asocia un certificado SSL/TLS a través de AWS Certificate Manager (ACM) para el dominio de tu sitio web.

2. **Configurar el Bucket**:
    
    - Configura el bucket para no permitir acceso directo y forzar el acceso a través de CloudFront.