#### **Descripción:**

Los **pipes** transforman datos en las plantillas. Angular incluye varios pipes integrados y permite crear pipes personalizados para necesidades específicas.

#### **Características Clave:**

- **Pipes Integrados:** Como `DatePipe`, `UpperCasePipe`, `LowerCasePipe`, `CurrencyPipe`, entre otros.
- **Pipes Personalizados:** Creas pipes propios para transformaciones específicas.

```ad-important
title: Pipes Integrados
```
```
<p>Fecha actual: {{ today | date:'fullDate' }}</p>
<p>Nombre en mayúsculas: {{ name | uppercase }}</p>
<p>Precio: {{ price | currency:'EUR' }}</p>
```

```
// home.component.ts
export class HomeComponent {
  today: number = Date.now();
  name: string = 'Juan Pérez';
  price: number = 123.45;
}
```

```ad-important
title: Pipes Personalizados
```
```
// truncate.pipe.ts
import { Pipe, PipeTransform } from '@angular/core';

@Pipe({
  name: 'truncate'
})
export class TruncatePipe implements PipeTransform {
  transform(value: string, limit: number = 20): string {
    return value.length > limit ? value.substring(0, limit) + '...' : value;
  }
}
```

```
<!-- Uso del pipe personalizado -->
<p>{{ description | truncate:50 }}</p>
```

