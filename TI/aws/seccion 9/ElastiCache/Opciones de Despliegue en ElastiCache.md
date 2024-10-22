#### 4.1. **Despliegue de Nodo Único**

- Un único nodo de caché se implementa en la arquitectura de la aplicación. Es útil para pruebas, pero no ofrece tolerancia a fallos.

#### 4.2. **Despliegue Multi-Nodo (Clúster)**

- Redis y Memcached pueden implementarse como un clúster de múltiples nodos, lo que permite la **distribución de datos entre nodos** para manejar más datos y mejorar el rendimiento.
- **Redis Cluster** permite particionar los datos automáticamente entre varios fragmentos.

#### 4.3. **Implementaciones Multi-AZ con Redis**

- En Redis, los nodos principales pueden estar replicados en múltiples zonas de disponibilidad, lo que permite alta disponibilidad y **failover automático** si el nodo principal falla.