#### **Descripción:**

Los **servicios** son clases que encapsulan lógica de negocio, como llamadas a APIs, manipulación de datos o lógica compartida entre componentes. **La inyección de dependencias** permite que Angular suministre instancias de servicios a los componentes que los necesitan.

#### **Características Clave:**

- **Reutilización:** Los servicios pueden ser inyectados en múltiples componentes.
- **Desacoplamiento:** Separa la lógica de negocio de la presentación.
- **Singleton por defecto:** Un servicio es una única instancia dentro de un módulo a menos que se especifique lo contrario.

```ad-important
title: Dependency Injection
```
```
// data.service.ts
import { Injectable } from '@angular/core';

@Injectable({
  providedIn: 'root' // Disponible en toda la aplicación
})
export class DataService {
  private data: string[] = ['Dato 1', 'Dato 2', 'Dato 3'];

  getData(): string[] {
    return this.data;
  }

  addData(item: string) {
    this.data.push(item);
  }
}
```

```
// home.component.ts
import { Component, OnInit } from '@angular/core';
import { DataService } from '../services/data.service';

@Component({
  selector: 'app-home',
  template: `
    <h1>Datos</h1>
    <ul>
      <li *ngFor="let item of data">{{ item }}</li>
    </ul>
    <button (click)="addItem()">Añadir Dato</button>
  `
})
export class HomeComponent implements OnInit {
  data: string[] = [];

  constructor(private dataService: DataService) { }

  ngOnInit() {
    this.data = this.dataService.getData();
  }

  addItem() {
    this.dataService.addData('Nuevo Dato');
    this.data = this.dataService.getData();
  }
}
```

