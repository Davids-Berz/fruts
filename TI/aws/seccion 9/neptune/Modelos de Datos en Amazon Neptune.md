#### 2.1. **Grafo de Propiedad (Property Graph)**

En el modelo de **grafos de propiedad**, los nodos y aristas pueden tener propiedades adicionales (pares clave-valor). Este modelo es ideal para representar datos con muchas relaciones complejas y atributos en los nodos o aristas.

- **Consulta con Gremlin**: Las consultas en Neptune para grafos de propiedad se realizan utilizando **Apache TinkerPop Gremlin**, un lenguaje de consultas que permite la navegación eficiente a través de los grafos. Gremlin se utiliza para realizar consultas sobre trayectorias, relaciones entre nodos y patrones específicos en el grafo.
    
    Ejemplo de una consulta Gremlin para encontrar los amigos de un usuario:

```
g.V().has('user', 'name', 'Alice').out('knows').values('name')
```

#### 2.2. **RDF (Resource Description Framework)**

El modelo **RDF** se utiliza para representar datos como **triplas** de sujeto-predicado-objeto. Es ampliamente utilizado en casos de uso de semántica y web semántica, como ontologías y gestión de conocimientos.

- **Consulta con SPARQL**: Las consultas RDF en Neptune se realizan utilizando **SPARQL**, que es un lenguaje estándar de la W3C. SPARQL permite buscar triplas basadas en los sujetos, predicados y objetos, y realizar consultas complejas para descubrir relaciones entre los datos.
    
    Ejemplo de una consulta SPARQL para encontrar todos los amigos de un usuario:

```
SELECT ?friend
WHERE {
  ?user <http://example.org/knows> ?friend .
  ?user <http://example.org/name> "Alice" .
}
```

