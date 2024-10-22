#### 2.1. **Esquema en Lectura**

Athena sigue el modelo de "esquema en lectura", lo que significa que los datos no se estructuran hasta que son consultados. Esto es opuesto al "esquema en escritura", donde los datos se estructuran antes de almacenarse. En Athena:

- Los datos permanecen en su formato original en S3.
- Definimos un **esquema** para que Athena interprete los datos al momento de la consulta.

#### 2.2. **Configuración de Consultas en Athena**

1. **Crear una Base de Datos y Tablas**: Puedes crear una base de datos en Athena y definir tablas que representen los datos almacenados en S3. Estas tablas contienen información sobre el formato, ubicación y estructura de los datos.
    
    Ejemplo de creación de una tabla:

```
CREATE EXTERNAL TABLE IF NOT EXISTS my_table (
  id STRING,
  date STRING,
  value DOUBLE
)
ROW FORMAT SERDE 'org.apache.hadoop.hive.serde2.lazy.LazySimpleSerDe'
WITH SERDEPROPERTIES (
  'serialization.format' = ','
) LOCATION 's3://my-bucket/path-to-data/';
```

2. **Ejecutar Consultas SQL**: Una vez que las tablas están definidas, puedes ejecutar consultas SQL sobre los datos almacenados en S3.

Ejemplo de consulta simple:

```
SELECT id, AVG(value)
FROM my_table
WHERE date > '2024-01-01'
GROUP BY id;
```

3. 1. **Integración con el Catálogo de Datos de AWS Glue**: Puedes integrar Athena con el **Catálogo de Datos de AWS Glue** para automatizar el descubrimiento de esquemas y la gestión de metadatos.
    

#### 2.3. **Optimización de Costos con Compresión y Formatos Eficientes**

Athena cobra en función de la cantidad de datos escaneados por consulta, por lo que es crucial optimizar las consultas y los datos para minimizar los costos:

- **Compresión**: Utilizar formatos de datos comprimidos como **Parquet** o **ORC** reduce significativamente el volumen de datos escaneados, lo que baja los costos.
- **Particiones**: Al particionar los datos en S3 (por ejemplo, por fechas o regiones), puedes limitar las consultas a solo las particiones relevantes, reduciendo la cantidad de datos escaneados.
