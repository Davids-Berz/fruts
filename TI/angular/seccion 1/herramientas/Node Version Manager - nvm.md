**Descripción:**  
**nvm** es una herramienta que te permite gestionar múltiples versiones de Node.js en tu sistema. Es especialmente útil cuando trabajas en diferentes proyectos que requieren distintas versiones de Node.js.

**Ventajas de usar nvm:**

- **Flexibilidad:** Cambia fácilmente entre versiones de Node.js según las necesidades del proyecto.
- **Aislamiento:** Evita conflictos entre dependencias que pueden surgir al usar diferentes versiones de Node.js.
- **Facilidad de Actualización:** Actualiza Node.js sin afectar otros proyectos.

**Instalación de nvm:**

1. **En sistemas Unix (Linux y macOS):**

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
```

_Nota:_ Verifica la última versión de nvm en [su repositorio oficial](https://github.com/nvm-sh/nvm) y actualiza el número de versión en el comando si es necesario.

2. **En Windows:**

Utiliza **nvm-windows**, una versión adaptada para Windows.

- **Descarga el instalador:** [nvm-windows releases](https://github.com/coreybutler/nvm-windows/releases)
- Ejecuta el instalador y sigue las instrucciones en pantalla.

```
nvm ls-remote
nvm install 16.14.0
nvm ls
nvm use 16.14.0
nvm alias default 16.14.0
```

**Ejemplo de Flujo de Trabajo con nvm:**

1. **Instalar nvm** siguiendo los pasos anteriores.
2. **Instalar la versión requerida de Node.js** para tu proyecto Angular:

```
nvm install 18.16.0
```

3. **Seleccionar la versión instalada**:

```
nvm use 18.16.0
```

4. **Verificar la versión activa de Node.js:**

```
node -v  # Debería mostrar v18.16.0
```

**Recursos Adicionales:**

- [Repositorio Oficial de nvm](https://github.com/nvm-sh/nvm)
- [Guía de nvm-windows](https://github.com/coreybutler/nvm-windows)

