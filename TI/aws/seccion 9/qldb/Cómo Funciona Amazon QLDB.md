#### 2.1. **Modelo de Libro Mayor**

QLDB utiliza un modelo de datos basado en un **libro mayor**, donde cada transacción se escribe de manera secuencial y se almacena en un **registro inmutable**. Las transacciones incluyen tanto los datos originales como el historial de todos los cambios, lo que permite rastrear la evolución de cada entrada en la base de datos.

#### 2.2. **Árbol Merkle para Verificación Criptográfica**

Para garantizar que los datos no hayan sido alterados, QLDB utiliza un **árbol Merkle** para realizar un **hash criptográfico** de las transacciones. Este hash permite a los usuarios verificar que una transacción específica no ha sido modificada desde que fue escrita en el libro mayor. Los árboles Merkle son estructuras de datos que facilitan la verificación eficiente de la integridad de grandes conjuntos de datos, lo que es clave en auditorías y casos donde se requiere transparencia.

#### 2.3. **Consultas con PartiQL**

QLDB utiliza **PartiQL** para realizar consultas sobre los datos. PartiQL es compatible con SQL, lo que facilita la búsqueda y extracción de datos tanto actuales como históricos. Puedes realizar consultas tradicionales sobre los datos o acceder a su historial completo para verificar cuándo se realizó un cambio y qué fue modificado.

Ejemplo de una consulta PartiQL para buscar transacciones específicas:

```
SELECT * FROM history('my_table') WHERE transaction_id = 'tx12345';
```

