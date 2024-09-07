Una vez que el versionado está habilitado, cada objeto nuevo o modificado en el bucket recibirá un identificador de versión único.

#### 1. Subida de Objetos

- Al subir un objeto con el mismo nombre a un bucket versionado, S3 creará una nueva versión del objeto y asignará un nuevo identificador de versión.

#### 2. Listado de Versiones

- Puedes listar todas las versiones de los objetos en un bucket utilizando la consola de S3, AWS CLI o las APIs de AWS:
- `aws s3api list-object-versions --bucket nombre-del-bucket`

#### 3. Recuperar Versiones Anteriores

- Para descargar o restaurar una versión específica de un objeto, puedes utilizar la consola de S3 o la AWS CLI especificando el identificador de versión:
- `aws s3api get-object --bucket nombre-del-bucket --key nombre-del-objeto --version-id ID-de-version archivo-de-salida`

#### 4. Eliminación de Versiones

- Cuando eliminas un objeto en un bucket versionado, S3 no elimina las versiones anteriores, sino que crea un "marcador de eliminación". Puedes eliminar versiones específicas o marcadores de eliminación:
- `aws s3api delete-object --bucket nombre-del-bucket --key nombre-del-objeto --version-id ID-de-version`