Docker es una plataforma que facilita la creación, implementación y gestión de aplicaciones mediante **contenedores**. Los contenedores son entornos ligeros y portátiles que empaquetan todo lo necesario para ejecutar una aplicación: su código, bibliotecas, dependencias y configuraciones, asegurando que la aplicación funcione de manera consistente en cualquier sistema operativo o entorno, ya sea en tu computadora, en un servidor o en la nube.

### Características clave de Docker:

1. **Portabilidad**: Los contenedores creados en Docker pueden ejecutarse en cualquier lugar donde Docker esté instalado, sin importar el entorno subyacente.
2. **Aislamiento**: Cada contenedor es independiente y está aislado del sistema operativo del host, así como de otros contenedores. Esto permite evitar conflictos de dependencias.
3. **Ligero**: A diferencia de las máquinas virtuales (VMs), los contenedores no requieren un sistema operativo completo, lo que los hace mucho más livianos y rápidos de iniciar.
4. **Eficiencia**: Docker permite que varios contenedores compartan los mismos recursos del sistema (como el kernel del sistema operativo), lo que reduce el uso de recursos.

### ¿Cómo funciona?

- **Imágenes**: Son plantillas que contienen las instrucciones necesarias para ejecutar una aplicación. Las imágenes son inmutables y se usan como base para crear contenedores.
- **Contenedores**: Son instancias ejecutables de imágenes. Puedes ejecutar varias instancias (contenedores) de la misma imagen, cada una con sus propios datos o configuración.
- **Docker Engine**: Es el motor que gestiona todo en Docker, desde la construcción de imágenes hasta la ejecución de contenedores.
- **Docker Hub**: Un repositorio en línea donde puedes encontrar imágenes de Docker preconfiguradas o compartir las tuyas propias.

### Diferencia entre Docker y las máquinas virtuales

- **Máquinas Virtuales (VMs)**: Ejecutan un sistema operativo completo y requieren muchos recursos. Cada VM tiene su propio sistema operativo y aplicaciones, y se ejecutan sobre un hipervisor.
- **Docker (Contenedores)**: Comparte el sistema operativo del host, lo que lo hace mucho más ligero y eficiente. Cada contenedor tiene su aplicación y sus dependencias, pero no necesita un sistema operativo separado.