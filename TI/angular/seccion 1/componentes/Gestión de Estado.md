#### **Descripción:**

En aplicaciones complejas, gestionar el estado de manera eficiente es crucial. Angular no impone una solución específica, pero existen bibliotecas populares como **NgRx** que implementan el patrón Redux para la gestión del estado.

#### **Características Clave de NgRx:**

- **Store:** Almacena el estado de la aplicación de manera centralizada.
- **Actions:** Representan eventos que describen cambios en el estado.
- **Reducers:** Funciones puras que actualizan el estado basado en las acciones.
- **Selectors:** Facilitan la selección y derivación de datos del estado.
- **Effects:** Manejan operaciones asíncronas como llamadas a APIs.

#### **Ejemplo Básico de Configuración de NgRx:**

1. **Instalar NgRx:**

```ad-note
title: Instalar NgRx
```
```
ng add @ngrx/store@latest
```

2. **Definir el Estado y Reducer:**

```
// counter.reducer.ts
import { createReducer, on } from '@ngrx/store';
import { increment, decrement, reset } from './counter.actions';

export const initialState = 0;

const _counterReducer = createReducer(initialState,
  on(increment, state => state + 1),
  on(decrement, state => state - 1),
  on(reset, state => 0)
);

export function counterReducer(state, action) {
  return _counterReducer(state, action);
}
```

3. **Definir las Actions:**

```
// counter.actions.ts
import { createAction } from '@ngrx/store';

export const increment = createAction('[Counter] Incrementar');
export const decrement = createAction('[Counter] Decrementar');
export const reset = createAction('[Counter] Reiniciar');
```

4. **Configurar el Store en el Módulo:**

```
// app.module.ts
import { StoreModule } from '@ngrx/store';
import { counterReducer } from './counter.reducer';

@NgModule({
  imports: [
    StoreModule.forRoot({ count: counterReducer }),
    // Otros módulos
  ],
  // ...
})
export class AppModule { }
```


5. **Usar el Store en un Componente:**

```
// counter.component.ts
import { Component } from '@angular/core';
import { Store } from '@ngrx/store';
import { Observable } from 'rxjs';
import { increment, decrement, reset } from './counter.actions';

@Component({
  selector: 'app-counter',
  template: `
    <div>
      <h1>Contador: {{ count$ | async }}</h1>
      <button (click)="increment()">Incrementar</button>
      <button (click)="decrement()">Decrementar</button>
      <button (click)="reset()">Reiniciar</button>
    </div>
  `
})
export class CounterComponent {
  count$: Observable<number>;

  constructor(private store: Store<{ count: number }>) {
    this.count$ = store.select('count');
  }

  increment() {
    this.store.dispatch(increment());
  }

  decrement() {
    this.store.dispatch(decrement());
  }

  reset() {
    this.store.dispatch(reset());
  }
}
```

