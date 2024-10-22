#### **Descripción:**

Las **plantillas** son definiciones declarativas de la vista que un componente maneja. Utilizan HTML enriquecido con **directivas** y **data binding** para interactuar con la lógica del componente.

#### **Características Clave:**

- **Interpolación:** Inserta datos del componente en la vista usando `{{ }}`.
- **Directivas Estructurales:** Modifican la estructura del DOM, como `*ngIf` y `*ngFor`.
- **Directivas de Atributo:** Cambian la apariencia o comportamiento de elementos, como `ngClass` y `ngStyle`.

```ad-important
title: Templates
```
```
<!-- home.component.html -->
<div>
  <h1>{{ title }}</h1>
  <ul>
    <li *ngFor="let item of items">{{ item }}</li>
  </ul>
  <p *ngIf="isLoggedIn">Has iniciado sesión.</p>
</div>
```

```
// home.component.ts
export class HomeComponent {
  title = 'Página de Inicio';
  items = ['Elemento 1', 'Elemento 2', 'Elemento 3'];
  isLoggedIn = true;
}
```

