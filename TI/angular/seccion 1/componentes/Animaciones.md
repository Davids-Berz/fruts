#### **Descripción:**

Angular incluye un módulo de animaciones que permite crear transiciones y efectos visuales fluidos en la aplicación.

#### **Características Clave:**

- **Transiciones de Estado:** Cambios animados entre diferentes estados de un componente.
- **Keyframes:** Definición de múltiples puntos intermedios en una animación.
- **Integración con Directivas:** Como `@angular/animations` para controlar animaciones en el DOM.

```ad-important
title: Animaciones
```
```
// animations.ts
import { trigger, state, style, transition, animate } from '@angular/animations';

export const fadeInOut = trigger('fadeInOut', [
  state('in', style({ opacity: 1 })),
  transition(':enter', [
    style({ opacity: 0 }),
    animate(300)
  ]),
  transition(':leave', [
    animate(300, style({ opacity: 0 }))
  ])
]);
```

```
// animated.component.ts
import { Component } from '@angular/core';
import { fadeInOut } from './animations';

@Component({
  selector: 'app-animated',
  template: `
    <div *ngIf="isVisible" @fadeInOut>
      Este contenido se desvanece al entrar y salir.
    </div>
    <button (click)="toggle()">Toggle</button>
  `,
  animations: [fadeInOut]
})
export class AnimatedComponent {
  isVisible = true;

  toggle() {
    this.isVisible = !this.isVisible;
  }
}
```

