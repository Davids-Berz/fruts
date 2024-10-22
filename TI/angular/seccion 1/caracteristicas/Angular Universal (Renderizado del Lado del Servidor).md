#### **Descripción:**

**Angular Universal** permite el **renderizado del lado del servidor (SSR)**, lo que mejora el rendimiento y la optimización para motores de búsqueda (SEO) al generar el HTML de la aplicación en el servidor antes de enviarlo al cliente.

#### **Características Clave:**

- **Mejor SEO:** Los motores de búsqueda pueden indexar el contenido de la aplicación más fácilmente.
- **Tiempo de Carga Inicial Más Rápido:** El usuario ve el contenido renderizado más rápidamente.
- **Compatibilidad con Navegadores:** Mejora la experiencia en navegadores que no ejecutan JavaScript de manera eficiente.

#### **Pasos Básicos para Configurar Angular Universal:**

1. Agregar Angular Universal al Proyecto:

```
ng add @nguniversal/express-engine
```

2. Construir la Aplicación para SSR:

```
npm run build:ssr
```

3. Ejecutar el Servidor SSR:

```
npm run serve:ssr
```

