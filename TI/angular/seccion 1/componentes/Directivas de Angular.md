#### **Descripción:**

Las **directivas** son instrucciones en el DOM que permiten manipular la estructura o el comportamiento de los elementos. Angular las clasifica en **directivas estructurales**, **directivas de atributos** y **directivas personalizadas**.

#### **Tipos Principales:**

1. **Directivas Estructurales:**
    
    - **`*ngIf`**: Muestra u oculta un elemento basado en una condición.
    - **`*ngFor`**: Itera sobre una colección para generar múltiples instancias de un elemento.
2. **Directivas de Atributo:**
    
    - **`ngClass`**: Añade o elimina clases CSS dinámicamente.
    - **`ngStyle`**: Aplica estilos CSS dinámicamente.
3. **Directivas Personalizadas:**
    
    - Puedes crear directivas propias para reutilizar lógica específica.

```ad-important
title: Directivas
```
```
// highlight.directive.ts
import { Directive, ElementRef, HostListener } from '@angular/core';

@Directive({
  selector: '[appHighlight]'
})
export class HighlightDirective {
  constructor(private el: ElementRef) { }

  @HostListener('mouseenter') onMouseEnter() {
    this.highlight('yellow');
  }

  @HostListener('mouseleave') onMouseLeave() {
    this.highlight(null);
  }

  private highlight(color: string | null) {
    this.el.nativeElement.style.backgroundColor = color;
  }
}
```

```
<!-- Uso de la directiva personalizada -->
<p appHighlight>Este párrafo se resaltará al pasar el ratón sobre él.</p>
```

