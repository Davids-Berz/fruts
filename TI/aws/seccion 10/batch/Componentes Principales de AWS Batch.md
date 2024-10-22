#### 3.1. **Trabajos (Jobs)**

Un **trabajo** es la unidad básica de ejecución en AWS Batch. Cada trabajo define qué tarea debe ejecutarse, qué imagen de contenedor debe utilizarse, y los recursos necesarios (CPU, memoria, etc.).

#### 3.2. **Colas de Trabajos (Job Queues)**

Las **colas de trabajos** almacenan los trabajos que esperan ser ejecutados. Puedes tener múltiples colas con diferentes prioridades, lo que permite que los trabajos críticos o urgentes se ejecuten primero.

#### 3.3. **Entorno de Cómputo (Compute Environment)**

El **entorno de cómputo** es donde AWS Batch aprovisiona los recursos necesarios para ejecutar trabajos. Puedes usar un entorno gestionado por AWS Batch o configurarlo manualmente utilizando instancias EC2 o AWS Fargate.

#### 3.4. **Definiciones de Trabajos (Job Definitions)**

Una **definición de trabajo** especifica la configuración que AWS Batch utiliza para ejecutar un trabajo. Incluye detalles como la imagen de contenedor, la cantidad de CPU y memoria necesarios, y cualquier variable de entorno o configuración adicional.

#### 3.5. **Dependencias entre Trabajos**

Puedes definir dependencias entre trabajos, lo que permite que un trabajo espere hasta que otro haya terminado antes de comenzar. Esto es útil para pipelines de procesamiento de datos donde los resultados de un trabajo son necesarios para el siguiente.