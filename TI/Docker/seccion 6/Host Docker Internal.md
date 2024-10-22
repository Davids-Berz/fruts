Para que tu imagen Docker con un archivo `.jar` pueda conectarse a una base de datos que está ejecutándose en tu máquina local, puedes usar `host.docker.internal` como la dirección del host para la base de datos.

### Pasos para conectar el `.jar` al `host.docker.internal`

1. **Configura tu archivo `.jar` para que use `host.docker.internal`:**
    
    Debes asegurarte de que la configuración de tu aplicación (la que está empaquetada en el `.jar`) use `host.docker.internal` como el host para la base de datos.
    
    Si tu aplicación utiliza un archivo de configuración, como un archivo `application.properties` o `application.yml` en un proyecto **Spring Boot**, o cualquier otro archivo de configuración que gestione las conexiones de base de datos, asegúrate de cambiar el valor del host a `host.docker.internal`.
    
    Ejemplo en **Spring Boot (`application.properties`)**:
```ad-note
title: properties
```
```
spring.datasource.url=jdbc:mysql://host.docker.internal:3306/nombre_base_de_datos
spring.datasource.username=mi_usuario
spring.datasource.password=mi_contraseña
```

- En este ejemplo, la URL de la base de datos apunta a `host.docker.internal`, que hace referencia a tu máquina local desde dentro del contenedor.
    
2. **Construye tu imagen Docker:**
    
    Si ya tienes un Dockerfile para tu aplicación, asegúrate de que todo esté bien configurado en tu `.jar`. Si aún no lo tienes, puedes usar este ejemplo básico de Dockerfile para un archivo `.jar`:

```
FROM openjdk:11-jre-slim

# Copia tu archivo .jar a la imagen
COPY target/mi-aplicacion.jar /usr/app/mi-aplicacion.jar

# Define el directorio de trabajo
WORKDIR /usr/app

# Expone el puerto de tu aplicación (si es necesario)
EXPOSE 8080

# Ejecuta la aplicación .jar
CMD ["java", "-jar", "mi-aplicacion.jar"]
```

3. **Ejecuta el contenedor de tu aplicación:**

Ejecuta el contenedor de tu aplicación y asegúrate de que Docker está usando la red correcta que le permitirá conectarse a `host.docker.internal`. Puedes hacerlo con el siguiente comando

```
docker run --name mi-aplicacion -p 8080:8080 mi-imagen
```

- Aquí:
    
    - **`--name mi-aplicacion`** es el nombre del contenedor.
    - **`-p 8080:8080`** mapea el puerto 8080 del contenedor al puerto 8080 de tu máquina local (si la aplicación expone ese puerto).
    - **`mi-imagen`** es el nombre de la imagen que creaste a partir de tu Dockerfile.
- **Verifica la conexión:**
    
    Si todo está configurado correctamente, tu aplicación debería poder conectarse a la base de datos MySQL (o cualquier otra base de datos) que se ejecuta en tu máquina local usando `host.docker.internal` como host.