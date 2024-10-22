Aquí tienes una lista de los **comandos más comunes de Docker**, que te serán útiles para administrar imágenes, contenedores, redes y volúmenes en Docker.

### 1. **Comandos sobre Imágenes**

1. **Listar imágenes disponibles:**
	- `Docker images`
	- Muestra todas las imágenes descargadas localmente en tu sistema.
    
2. **Descargar una imagen:**
	- `docker pull <nombre-de-la-imagen>`
	- Descarga la imagen desde Docker Hub (o desde otro registro si está configurado).
    
3. Eliminar una imagen:
	- `docker rmi <id-de-la-imagen>`
	- Elimina una imagen de tu sistema local. Puedes usar el nombre o el ID de la imagen.
    
4. **Construir una imagen a partir de un Dockerfile:**
	- `docker build -t <nombre-de-la-imagen> .`
	- Crea una imagen basada en un Dockerfile. La opción `-t` asigna un nombre a la imagen.

### 2. **Comandos sobre Contenedores**

1. Crear y ejecutar un contenedor:
	- `docker run -it --name <nombre-del-contenedor> <nombre-de-la-imagen>`
	- Crea y ejecuta un nuevo contenedor. La opción `-it` permite interacción en la terminal, y `--name` asigna un nombre al contenedor.

2. Ejecutar un contenedor en segundo plano (detached mode):
	- `docker run -d <nombre-de-la-imagen>`
	- Inicia el contenedor en modo "detached" (segundo plano).

3. **Listar contenedores activos:**
	- `docker ps`
	- Muestra todos los contenedores en ejecución.

4. **Detener un contenedor:**
	- `docker stop <id-del-contenedor>`
	- Detiene un contenedor en ejecución.

5. **Eliminar un contenedor:**
	- `docker rm <id-del-contenedor>`
	- Elimina un contenedor detenido.

6. **Ejecutar un comando dentro de un contenedor en ejecución:**
	- `docker exec -it <nombre-del-contenedor> /bin/bash`
	- Abre una sesión interactiva en el contenedor con Bash.

7. **Reiniciar un contenedor:**
	- `docker restart <id-del-contenedor>`
	- Reinicia un contenedor en ejecución.


### 3. **Comandos sobre Volúmenes**

1. **Crear un volumen:**
	- `docker volume create <nombre-del-volumen>`
	- Crea un volumen persistente.

2. **Listar volúmenes:**
	- `docker volume ls`
	- Muestra los volúmenes existentes.

3. **Eliminar un volumen:**
	- `docker volume rm <nombre-del-volumen>`
	- Elimina un volumen específico.

4. **Montar un volumen al ejecutar un contenedor:**
	- `docker run -v <nombre-del-volumen>:/ruta/dentro-del-contenedor <nombre-de-la-imagen>`
	- Monta un volumen en el contenedor en la ruta especificada.

### 4. **Comandos sobre Redes**

1. **Crear una red:**
	- `docker network create <nombre-de-la-red>`
	- Crea una red de Docker.

2. **Listar redes:**
	- `docker network ls`
	- Lista las redes Docker disponibles.

3. **Conectar un contenedor a una red:**
	- `docker network connect <nombre-de-la-red> <nombre-del-contenedor>`
	- Conecta un contenedor a una red específica.

4. **Desconectar un contenedor de una red:**
	- `docker network disconnect <nombre-de-la-red> <nombre-del-contenedor>`

5. **Eliminar una red:**
	- `docker network rm <nombre-de-la-red>`

### 5. **Limpiar el sistema**

1. **Eliminar contenedores detenidos:**
	- `docker container prune`
	- Elimina todos los contenedores que no están en ejecución.

2. **Eliminar imágenes sin utilizar:**
	- `docker image prune`
	- Elimina imágenes que no tienen contenedores asociados.

3. **Eliminar volúmenes no utilizados:**
	- `docker volume prune
	- Limpia los volúmenes no utilizados.

4. **Eliminar redes no utilizadas:**
	- `docker network prune`

### 6. **Inspeccionar Contenedores e Imágenes**

1. **Ver detalles de un contenedor:**
	- `docker inspect <id-del-contenedor>`

2. **Ver los logs de un contenedor:**
	- `docker logs <id-del-contenedor>`

3. **Ver el uso de recursos del contenedor:**
	- `docker stats`

---
