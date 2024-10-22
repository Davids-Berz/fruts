#### **Descripción:**

**Angular Material** es una biblioteca de componentes UI basada en las especificaciones de **Material Design** de Google. Proporciona componentes preconstruidos y estilizados que facilitan la creación de interfaces de usuario atractivas y coherentes.

#### **Características Clave:**

- **Componentes Preconstruidos:** Botones, tarjetas, formularios, diálogos, tablas, etc.
- **Temas Personalizables:** Facilita la aplicación de diferentes temas y esquemas de color.
- **Accesibilidad:** Componentes diseñados con consideraciones de accesibilidad.
- **Responsive:** Adaptados para funcionar bien en diferentes tamaños de pantalla y dispositivos.

#### **Ejemplo de Uso de Angular Material:**

1. Instalar Angular Material:

```ad-note
title: Instalar Angular Material
```
```
ng add @angular/material
```

2. Importar Módulos de Material:

```ad-important
title: importar modulo
```
```
// app.module.ts
import { MatButtonModule } from '@angular/material/button';
import { MatToolbarModule } from '@angular/material/toolbar';
// Importa otros módulos según sea necesario

@NgModule({
  imports: [
    MatButtonModule,
    MatToolbarModule,
    // Otros módulos
  ],
  // ...
})
export class AppModule { }
```

3. Usar Componentes de Material en Plantillas:

```
<!-- app.component.html -->
<mat-toolbar color="primary">
  <span>Mi Aplicación Angular</span>
</mat-toolbar>

<div class="content">
  <button mat-raised-button color="accent">Click Me</button>
</div>
```

