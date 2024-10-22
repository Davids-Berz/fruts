En Docker, una **imagen** está formada por una serie de **capas** que se construyen a partir de las instrucciones en un **Dockerfile**. Cada instrucción en el Dockerfile genera una nueva capa. Las capas ayudan a mejorar la eficiencia y la reutilización, ya que Docker guarda las capas en caché, de modo que si una capa no ha cambiado, puede reutilizarse sin necesidad de reconstruirla.

### Tipos de Capas en Docker

1. **Capas base:** La primera capa de una imagen Docker suele ser una **imagen base** (como una distribución de Linux, o en tu caso, una imagen JDK). Por ejemplo, la instrucción `FROM amazoncorretto:11.0.25` en tu Dockerfile descarga y utiliza la imagen base de Amazon Corretto.
    
2. **Capas intermedias:** Cada comando en un Dockerfile (como `RUN`, `COPY`, `ADD`, `ENV`, etc.) crea una nueva capa. Estas capas intermedias se apilan sobre la capa base y constituyen la lógica de construcción de tu aplicación.
    
3. **Capa superior:** La última capa contiene los cambios más recientes y es la capa que suele modificarse más frecuentemente, por ejemplo, cuando cambias tu código de aplicación y lo copias a la imagen.
    

### Cómo funcionan las capas

Las capas son **inmutables**. Esto significa que una vez que se crea una capa, no se puede cambiar. Si modificas un archivo o realizas un cambio en una capa, Docker no cambia la capa existente, sino que crea una nueva capa encima de las capas anteriores.

### Ejemplo de capas en un Dockerfile

```ad-note
title: Capas de la Imagen
```
```
# Capa base: una imagen JDK de Amazon Corretto
FROM amazoncorretto:11.0.25

# Capa intermedia: establece el directorio de trabajo
WORKDIR /usr/src/app

# Capa intermedia: copia el archivo jar de tu aplicación
COPY target/mi-aplicacion.jar .

# Capa intermedia: expone el puerto 8080
EXPOSE 8080

# Capa final: ejecuta la aplicación
CMD ["java", "-jar", "mi-aplicacion.jar"]
```

En este Dockerfile:

1. **`FROM amazoncorretto:11.0.25`**: Esto crea la **capa base** con la imagen de Amazon Corretto.
2. **`WORKDIR /usr/src/app`**: Crea una capa para definir el directorio de trabajo.
3. **`COPY target/mi-aplicacion.jar .`**: Crea una nueva capa que copia tu archivo `.jar` dentro del contenedor.
4. **`EXPOSE 8080`**: Crea una capa que informa a Docker sobre el puerto expuesto.
5. **`CMD ["java", "-jar", "mi-aplicacion.jar"]`**: Define la instrucción para ejecutar la aplicación cuando se ejecute el contenedor.

Cada una de estas instrucciones crea una capa nueva. Si cambias alguna de las instrucciones (por ejemplo, el archivo `.jar` que copias), solo se reconstruirán las capas desde esa instrucción en adelante, mientras que las anteriores serán reutilizadas desde la caché.

### Ventajas del sistema de capas

- **Eficiencia en la construcción:** Si no cambias una instrucción en tu Dockerfile, la capa correspondiente no se reconstruye. Esto ahorra tiempo y recursos.
- **Reutilización:** Varias imágenes pueden compartir capas comunes, lo que reduce el uso de espacio en disco y acelera las descargas.
- **Versionado:** Cada capa es independiente y se puede rastrear, lo que facilita el versionado de las imágenes.

### Cómo ver las capas de una imagen

Puedes ver las capas de una imagen utilizando el comando `docker history`:

```
docker history <nombre-de-la-imagen>
```

Por ejemplo:

```
docker history amazoncorretto:11.0.25
```

Este comando te mostrará todas las capas de la imagen y qué instrucciones en el Dockerfile las generaron.