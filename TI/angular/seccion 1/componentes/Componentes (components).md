#### **Descripción:**

Los **componentes** son las unidades básicas de la interfaz de usuario en Angular. Cada componente controla una parte específica de la pantalla llamada **vista**.

#### **Características Clave:**

- **Plantilla (Template):** Define la estructura y apariencia visual utilizando HTML.
- **Clase (Class):** Contiene la lógica del componente y está escrita en TypeScript.
- **Metadatos:** Configuran cómo debe comportarse el componente, incluyendo su selector, estilos, etc.

```ad-important
title: Components
```
```
import { Component } from '@angular/core';

@Component({
  selector: 'app-home',
  template: `
    <h1>Bienvenido a la Página de Inicio</h1>
    <p>Esta es la vista principal de la aplicación.</p>
  `,
  styles: [`
    h1 { color: #2c3e50; }
    p { font-size: 16px; }
  `]
})
export class HomeComponent { }
```


