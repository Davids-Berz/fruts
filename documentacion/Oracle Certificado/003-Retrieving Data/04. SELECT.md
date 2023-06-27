La sentencia `SELECT` es una de las sentencias fundamentales de SQL y se utiliza para recuperar datos de una o varias tablas. En Oracle, la sintaxis básica de la sentencia `SELECT` es la siguiente:

```ad-important
title: SELECT
```
```
SELECT columna1, columna2, ...
FROM tabla
WHERE condición;
```

-   `columna1`, `columna2`, ...: una o varias columnas de la tabla que se desean recuperar. Si se quiere recuperar todas las columnas, se puede usar el carácter comodín `*`.
-   `tabla`: la tabla de la que se quieren recuperar los datos.
-   `condición`: una condición opcional que se aplica a las filas de la tabla antes de recuperar los datos.

Por ejemplo, para recuperar todas las filas y columnas de la tabla `clientes`, se puede usar la siguiente sentencia:

```
SELECT * FROM clientes;
```

Para recuperar solo el nombre y la edad de los clientes que tienen más de 30 años, se puede usar la siguiente sentencia:

```
SELECT nombre, edad FROM clientes WHERE edad > 30;
```

Además de la sentencia `SELECT` básica, Oracle proporciona muchas características adicionales, como funciones de agregación, ordenamiento, agrupación y unión de varias tablas, que permiten realizar consultas más complejas.