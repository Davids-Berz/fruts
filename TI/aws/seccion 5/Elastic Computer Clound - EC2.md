#Principal #Presupuesto
## Fundamentos de EC2

Amazon Elastic Compute Cloud (Amazon EC2) es un servicio web que proporciona capacidad de computación escalable en la nube. Está diseñado para facilitar el uso de la computación en la nube de una manera simple, permitiendo a los desarrolladores desplegar y gestionar instancias de servidores virtuales con facilidad. A continuación se presentan los fundamentos de EC2, incluyendo sus componentes, tipos de instancias, características y cómo empezar a usarlo.

1. [[Componentes de Amazon EC2]]
2. [[Características Principales de Amazon EC2]]
3. [[Cómo Empezar con Amazon EC2]]
4. [[Buenas Prácticas para Usar EC2]]

Amazon EC2 proporciona una plataforma poderosa y flexible para ejecutar aplicaciones y servicios en la nube, ofreciendo escalabilidad, disponibilidad y una gestión eficiente de costos. Con una configuración adecuada y el uso de buenas prácticas, puedes optimizar el rendimiento y la seguridad de tus recursos en la nube.

---
## Configuración de Presupuesto AWS


Configurar un presupuesto en AWS es una práctica esencial para gestionar y controlar los costos de tus servicios en la nube. AWS Budgets te permite establecer límites de gasto y recibir alertas cuando se acercan o superan esos límites. A continuación se describen los pasos detallados para configurar un presupuesto en AWS.

1. [[Pasos para Configurar un Presupuesto en AWS]]
2. [[Ejemplo de Configuración de un Presupuesto]]
3. [[Buenas Prácticas para la Gestión de Presupuestos en AWS]]

Configurar y gestionar presupuestos en AWS es crucial para mantener el control sobre los costos y asegurar que tu uso de la nube se mantenga dentro de los límites financieros planificados. Con las herramientas y prácticas adecuadas, puedes optimizar el uso de AWS y evitar sorpresas en la facturación.

---
## Crear Una Instancia EC2


Crear una instancia EC2 en AWS es un proceso sencillo que se puede realizar a través de la consola de administración de AWS. A continuación se presentan los pasos detallados para lanzar una instancia EC2, desde la selección de una Amazon Machine Image (AMI) hasta la conexión a la instancia una vez que se ha lanzado.

### [[Pasos para Crear una Instancia EC2]]

---
## Tipos de Instancia


Amazon EC2 ofrece una variedad de tipos de instancias diseñadas para diferentes casos de uso, con configuraciones de CPU, memoria, almacenamiento y capacidad de red optimizadas para diferentes aplicaciones. Aquí se presenta un resumen de los tipos de instancias EC2 más comunes:

1. [[General Purpose (Propósito General)]]
2. [[Compute Optimized (Optimizadas para Computación)]]
3. [[Memory Optimized (Optimizadas para Memoria)]]
4. [[Storage Optimized (Optimizadas para Almacenamiento)]]
5. [[Accelerated Computing (Computación Acelerada)]]
6. [[Configuración de una Instancia EC2]]

Estos son los fundamentos y tipos de instancias EC2 disponibles en AWS. Seleccionar el tipo de instancia adecuado depende de las necesidades específicas de tu aplicación y las cargas de trabajo que planeas ejecutar.

---
## Grupos de Seguridad y Puertos Clasicos


Los grupos de seguridad en AWS son componentes fundamentales de la red que actúan como firewalls virtuales para controlar el tráfico de entrada y salida de las instancias EC2. Configurar correctamente los grupos de seguridad es crucial para asegurar que solo el tráfico autorizado pueda acceder a tus instancias.

1. [[Grupos de Seguridad en AWS]]
2. [[Configuración de Grupos de Seguridad]]
3. [[Ejemplos de Configuración de Grupos de Seguridad]]
4. [[Buenas Prácticas para Grupos de Seguridad]]

Los grupos de seguridad son una parte esencial de la gestión de la seguridad en AWS. Configurarlos correctamente ayuda a proteger tus instancias y asegurar que solo el tráfico autorizado pueda acceder a tus recursos.

---
## Visión general de SSH


Secure Shell (SSH) es un protocolo de red criptográfico para operar servicios de red de forma segura sobre una red no segura. SSH proporciona un canal seguro sobre una red insegura al usar una arquitectura cliente-servidor, conectando una aplicación cliente SSH con un servidor SSH. Es comúnmente utilizado para acceso remoto a sistemas y administración de servidores.

1. [[Características Principales de SSH]]
2. [[Componentes de SSH]]
3. [[Uso Común de SSH]]
4. [[Ejemplo de Uso de SSH]]
5. [[Seguridad en SSH]]
6. [[Ejemplo de Configuración de SSH]]

SSH es una herramienta esencial para la administración de sistemas y servidores remotos, proporcionando una conexión segura y cifrada. Configurar y utilizar SSH adecuadamente mejora significativamente la seguridad y eficiencia de las operaciones remotas.

7. [[Tabla Resumen - SSH en Grupos de Seguridad]]

---
## Utilizar SSH usando Linux y Mac


Utilizar SSH en Linux y Mac es muy similar, ya que ambos sistemas operativos tienen clientes SSH preinstalados y se manejan principalmente a través de la terminal. Aquí te proporciono una guía paso a paso sobre cómo utilizar SSH en estos sistemas.

1. [[Generar un Par de Claves SSH]]
2. [[Copiar la Clave Pública al Servidor]]
3. [[Conectarse al Servidor Usando SSH]]
4. [[Configurar el Archivo ssh config (Opcional)]]
5. [[Transferir Archivos Usando SCP]]
6. [[Seguridad Adicional]]

Usar SSH en Linux y Mac es una manera eficiente y segura de administrar servidores remotos. Siguiendo estos pasos, puedes generar claves SSH, copiarlas al servidor, conectarte de forma segura y realizar transferencias de archivos. Además, puedes mejorar la seguridad cambiando el puerto SSH y deshabilitando la autenticación por contraseña.

---
## Utilizar SSH usando Windows


Para utilizar SSH en una instancia EC2 desde Windows utilizando un archivo PEM, puedes seguir los pasos detallados a continuación. Utilizaremos la línea de comandos de Windows y OpenSSH, que está incluido en Windows 10 y versiones posteriores.

1. [[Instalar y Configurar OpenSSH en Windows]]
2. [[Configurar los Permisos del Archivo PEM]]
3. [[Conectarse a la Instancia EC2 Usando SSH]]

Siguiendo estos pasos, deberías poder conectarte a tu instancia EC2 desde Windows utilizando un archivo PEM y SSH. Configurar los permisos correctamente y asegurarte de usar los comandos adecuados garantizará una conexión segura y exitosa.

---
## EC2 Instance Connect


EC2 Instance Connect es una característica que te permite conectar a tus instancias EC2 utilizando SSH sin necesidad de una clave SSH (PEM) pre-configurada en tu máquina local. Es una alternativa fácil y segura para administrar el acceso SSH a las instancias EC2.

1. [[Configuración y Uso de EC2 Instance Connect]]

### Beneficios de EC2 Instance Connect

- **Simplicidad**: No necesitas distribuir claves SSH por adelantado.
- **Seguridad**: Los usuarios pueden autenticarse temporalmente sin necesidad de claves SSH persistentes.
- **Facilidad de Uso**: Integración directa con la consola de administración de AWS y soporte para AWS CLI.

### Consideraciones de Seguridad

- **Roles de IAM**: Asegúrate de que los roles de IAM estén configurados correctamente con los permisos mínimos necesarios.
- **Reglas de Seguridad**: Restringe el acceso SSH en los grupos de seguridad solo a las IPs necesarias para minimizar el riesgo de acceso no autorizado.

EC2 Instance Connect es una herramienta poderosa y fácil de usar que facilita el acceso SSH a las instancias EC2 sin la necesidad de claves SSH pre-distribuidas. Es especialmente útil para administradores que necesitan acceso temporal o para situaciones en las que la distribución de claves es complicada.