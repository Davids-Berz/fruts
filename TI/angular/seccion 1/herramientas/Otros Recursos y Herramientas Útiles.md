### **a. Docker**

**Descripción:** Permite contenerizar tu aplicación Angular, asegurando que se ejecute de manera consistente en diferentes entornos.

**Descarga:** [docker.com](https://www.docker.com/)

```ad-info
title: Docker
```
```
# Usar una imagen base de Node
FROM node:14-alpine as build

# Establecer el directorio de trabajo
WORKDIR /app

# Copiar archivos package.json y package-lock.json
COPY package*.json ./

# Instalar dependencias
RUN npm install

# Copiar el resto de los archivos de la aplicación
COPY . .

# Construir la aplicación para producción
RUN npm run build --prod

# Usar una imagen de Nginx para servir la aplicación
FROM nginx:1.19-alpine

# Copiar los archivos compilados desde la etapa de build
COPY --from=build /app/dist/mi-aplicacion /usr/share/nginx/html

# Exponer el puerto 80
EXPOSE 80

# Comando para ejecutar Nginx
CMD ["nginx", "-g", "daemon off;"]
```

### **b. Prettier**

**Descripción:** Herramienta para formatear el código de manera consistente según reglas predefinidas, mejorando la legibilidad y manteniendo un estilo uniforme.

```ad-note
title: Instalacion
```
```
npm install --save-dev prettier
```

**Integración con VS Code:**

- Instala la extensión **Prettier - Code formatter** desde el marketplace.
- Configura VS Code para que formatee el código al guardar:

```
// settings.json
{
  "editor.formatOnSave": true,
  "prettier.singleQuote": true,
  "prettier.trailingComma": "es5"
}
```

### **c. ESLint**

**Descripción:** Herramienta de análisis estático para identificar y corregir problemas en el código, asegurando la calidad y consistencia.

```ad-note
title: Instalacion
```
```
ng add @angular-eslint/schematics
```

**Configuración:** Angular CLI puede migrar automáticamente de TSLint a ESLint.

**Documentación:** [eslint.org](https://eslint.org/)

---
