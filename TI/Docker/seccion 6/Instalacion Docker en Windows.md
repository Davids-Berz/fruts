La instalación de Docker en Windows con **Hyper-V** es un proceso sencillo, ya que Docker Desktop utiliza Hyper-V como el sistema de virtualización por defecto en Windows. A continuación te detallo los pasos para instalarlo:

### Requisitos Previos

1. **Windows 10/11 Pro, Enterprise o Education**: Docker Desktop requiere una versión de Windows que soporte **Hyper-V**.
2. **Habilitar la virtualización**: Asegúrate de que la virtualización esté habilitada en la BIOS de tu computadora.
3. **Hyper-V**: Hyper-V debe estar habilitado en tu sistema.

### Comandos Completos para Habilitar Hyper-V y Containers

1. Abre **PowerShell** como administrador.
    
2. Ejecuta estos dos comandos para habilitar **Hyper-V** y **Containers**:

```
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V -All
```

Y el siguiente para habilitar la funcionalidad de **Containers**:

```
Enable-WindowsOptionalFeature -Online -FeatureName Containers -All
```

3. Reinicia tu computadora cuando se te solicite.

### Paso 3: Instalar Docker Desktop

1. Abre el archivo descargado e inicia el proceso de instalación.
2. Durante la instalación, asegúrate de seleccionar la opción **Use WSL 2 instead of Hyper-V** si prefieres usar WSL 2. Pero si deseas usar Hyper-V, déjala desmarcada.
3. Docker Desktop instalará los componentes necesarios y configurará **Hyper-V** automáticamente si aún no lo habías hecho.
4. Al finalizar la instalación, te pedirá reiniciar tu sistema.

### Paso 4: Verificar la instalación

1. Después de reiniciar tu sistema, abre **Docker Desktop**. Debería iniciar sin problemas.
    
2. Verifica que Docker esté funcionando ejecutando el siguiente comando en **PowerShell** o **CMD**:

```
docker --version
```

Esto debería mostrar la versión de Docker instalada.

3. Ejecuta el contenedor de prueba:

```
docker run hello-world
```

1. Si todo está configurado correctamente, este comando descargará una imagen de prueba y ejecutará un contenedor que imprimirá un mensaje de éxito.
    

### Paso 5: Configuración adicional

- Si deseas cambiar la configuración, como asignar más recursos (CPU, memoria, etc.), puedes hacerlo desde la interfaz de **Docker Desktop** en la pestaña **Settings**.

### Paso 6: Comprobar Hyper-V

Puedes verificar que Docker esté usando **Hyper-V** al ejecutar los contenedores verificando que las máquinas virtuales de Docker aparezcan en el Administrador de Hyper-V.

