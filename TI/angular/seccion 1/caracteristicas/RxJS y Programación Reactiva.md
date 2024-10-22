#### **Descripción:**

Angular utiliza **RxJS** (Reactive Extensions for JavaScript) para manejar programación asíncrona y eventos mediante **observables**. Esto permite manejar flujos de datos complejos de manera eficient

- **Manejo eficiente de datos asíncronos:** Facilita la gestión de múltiples flujos de datos.
- **Operadores poderosos:** Proporciona una amplia gama de operadores para transformar y combinar observables.
- **Integración con Angular:** Muchos módulos de Angular, como el enrutador y los formularios, están basados en RxJS.

#### **Características Clave:**

- **Observables:** Permiten suscribirse a flujos de datos que pueden emitir múltiples valores a lo largo del tiempo.
- **Operadores:** Funciones para transformar, filtrar y combinar observables, como `map`, `filter`, `merge`, `switchMap`, etc.
- **Suscripciones:** Permiten reaccionar a los datos emitidos por los observables.

```ad-important
title: RxJs
```
```
// search.component.ts
import { Component } from '@angular/core';
import { FormControl } from '@angular/forms';
import { debounceTime, distinctUntilChanged, switchMap } from 'rxjs/operators';
import { ApiService } from '../services/api.service';

@Component({
  selector: 'app-search',
  template: `
    <input type="text" [formControl]="searchControl" placeholder="Buscar...">
    <ul>
      <li *ngFor="let result of results">{{ result }}</li>
    </ul>
  `
})
export class SearchComponent {
  searchControl = new FormControl();
  results: string[] = [];

  constructor(private apiService: ApiService) {
    this.searchControl.valueChanges.pipe(
      debounceTime(300),
      distinctUntilChanged(),
      switchMap(term => this.apiService.search(term))
    ).subscribe(data => this.results = data);
  }
}
```
