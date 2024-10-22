Un **Dockerfile** basado en una imagen de **JDK** (Java Development Kit) es útil cuando necesitas ejecutar aplicaciones Java en un contenedor Docker. A continuación, te muestro cómo crear un Dockerfile básico que usa una imagen de **OpenJDK**, la versión de código abierto del JDK, para ejecutar una aplicación Java.

## Ejemplo básico de un Dockerfile usando OpenJDK

1. Crea un archivo llamado `Dockerfile` en el directorio de tu proyecto.
2. El siguiente contenido en el Dockerfile descargará la imagen de OpenJDK, copiará el código Java compilado a la imagen y ejecutará la aplicación.

#### Contenido del Dockerfile:

```ad-example
title: Dockerfile
```
```
# Usar la imagen base de Amazon Corretto JDK 11
FROM amazoncorretto:11.0.25

# Establecer el directorio de trabajo en el contenedor
WORKDIR /app

# Copiar el archivo JAR de la aplicación al contenedor
COPY target/mi-aplicacion.jar /app/mi-aplicacion.jar

# Establecer el comando de inicio para ejecutar la aplicación
ENTRYPOINT ["java", "-jar", "mi-aplicacion.jar"]
```

### Explicación:

- **`FROM amazoncorretto:11.0.25`**: Esta línea especifica que estamos utilizando la imagen de Amazon Corretto 11 (versión 11.0.25). Amazon Corretto es una distribución certificada de OpenJDK con actualizaciones de seguridad de Amazon.
    
- **`WORKDIR /app`**: Establece el directorio de trabajo en `/app`, donde todos los archivos serán copiados y donde se ejecutará la aplicación.
    
- **`COPY target/mi-aplicacion.jar /app/mi-aplicacion.jar`**: Copia el archivo JAR generado por tu proyecto desde la carpeta `target` (o la carpeta donde esté tu JAR) al contenedor Docker.
    
- **`ENTRYPOINT ["java", "-jar", "mi-aplicacion.jar"]`**: Define que al iniciar el contenedor, se ejecutará la aplicación Java con el archivo JAR especificado.

## Cómo construir y ejecutar el contenedor

### Paso 1: Compilar tu proyecto Java

1. **Compilar tu proyecto Java** (Maven, Gradle o cualquier herramienta que uses) para generar el archivo JAR. Por ejemplo, si usas Maven:

```
mvn clean package
```

### Paso 2: Construir la imagen Docker

2. **Construir la imagen Docker** con el siguiente comando (en el directorio donde tienes el Dockerfile):

```
docker build -t mi-aplicacion .
```

- **`-t mi-aplicacion`**: Esta opción asigna una etiqueta (`mi-aplicacion`) a la imagen que estás construyendo.
- **`.`**: Indica que el contexto de construcción está en el directorio actual (donde está el Dockerfile).

### Paso 3: Ejecutar el contenedor

Una vez que la imagen se haya construido exitosamente, puedes ejecutar tu aplicación Java dentro de un contenedor Docker.

```
docker run -it --rm mi-aplicacion
```

- **`-it`**: Te permite interactuar con el contenedor de forma interactiva si tu aplicación requiere entrada de consola.
- **`--rm`**: Elimina automáticamente el contenedor cuando la aplicación se detiene.
- **`mi-aplicacion`**: Es la imagen que acabas de construir.

Este comando ejecuta tu aplicación dentro de un contenedor. La opción `--rm` asegura que el contenedor se elimine automáticamente cuando termine su ejecución.

### Paso 4: Verificar la ejecución del contenedor

Si la aplicación se ejecuta correctamente, verás los mensajes o logs que tu aplicación Java normalmente imprimiría en la consola. Asegúrate de revisar que se comporta de acuerdo con lo esperado.

### Paso 5: Opciones adicionales para ejecutar contenedores

Dependiendo de tus necesidades, puedes ejecutar el contenedor con varias configuraciones adicionales:

- **Mapeo de puertos**: Si tu aplicación expone un servicio web o algún puerto, puedes mapear los puertos del contenedor al host.
    
    Por ejemplo, si tu aplicación escucha en el puerto `8080`, puedes ejecutar el contenedor así:

```
docker run -it --rm -p 8080:8080 mi-aplicacion
```

- Esto expondrá el puerto 8080 del contenedor al puerto 8080 del host, permitiendo que accedas a tu aplicación desde tu navegador o herramientas de prueba.
    
- **Montaje de volúmenes**: Si tu aplicación necesita leer o escribir en archivos, puedes montar un volumen del sistema de archivos del host al contenedor:

```
docker run -it --rm -v /ruta/del/host:/app/data mi-aplicacion
```

Esto montará el directorio `/ruta/del/host` en el contenedor bajo `/app/data`.

### Paso 6: Publicar la imagen en un repositorio de Docker

Si deseas compartir tu imagen con otros o desplegarla en un servidor, puedes **subir la imagen a Docker Hub** o a otro registro de imágenes Docker.

1. Inicia sesión en Docker Hub:

```
docker login
```

2. Etiqueta la imagen con tu nombre de usuario de Docker Hub:

```
docker tag mi-aplicacion tu-usuario/mi-aplicacion
```

3. Sube la imagen:

```
docker push tu-usuario/mi-aplicacion
```

Esto hará que tu imagen esté disponible para que cualquiera con acceso al registro pueda descargarla y ejecutarla.

### Opciones adicionales

- Si tu aplicación requiere variables de entorno, puedes agregarlas en el Dockerfile usando `ENV`:

```
ENV APP_ENV=produccion
```

- Si necesitas instalar paquetes adicionales dentro del contenedor, puedes usar el comando `RUN` antes de copiar el JAR:

```
RUN apk add --no-cache curl
```

### Ventajas de Amazon Corretto:

- **Actualizaciones de seguridad**: Amazon Corretto recibe actualizaciones y parches de seguridad de manera regular.
- **Compatibilidad con OpenJDK**: Es totalmente compatible con OpenJDK, por lo que no deberías notar diferencias si ya estás usando otra versión de OpenJDK.
- **Desempeño optimizado**: Corretto está optimizado para entornos de producción y es probado extensivamente.