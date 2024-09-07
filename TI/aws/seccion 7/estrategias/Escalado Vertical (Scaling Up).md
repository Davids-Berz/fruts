**Definición**: Escalar verticalmente implica aumentar los recursos (como CPU, memoria o almacenamiento) de una única instancia o nodo en lugar de agregar más instancias.

#### Características:

- **Simplicidad**: Es más fácil de implementar, ya que no requiere cambios en la arquitectura de la aplicación.
- **Límites Físicos**: Está limitado por la capacidad máxima del hardware; eventualmente, no puedes seguir escalando verticalmente más allá de un cierto punto.
- **Tiempo de Inactividad**: En algunos casos, puede requerir detener y reiniciar la instancia para aplicar los cambios.

#### Ejemplo:

- Cambiar una instancia EC2 de un tipo `t2.micro` a un tipo `t2.large` para obtener más CPU y memoria.

#### Uso Recomendado:

- Aplicaciones monolíticas o bases de datos que no son fácilmente distribuidas.
- Escenarios donde la demanda crece pero sigue estando dentro de los límites de un solo servidor.