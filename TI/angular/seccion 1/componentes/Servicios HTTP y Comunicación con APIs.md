#### **Descripción:**

Angular proporciona el módulo `HttpClient` para facilitar las solicitudes HTTP a APIs externas, permitiendo la comunicación con servidores backend.

#### **Características Clave:**

- **Operaciones CRUD:** Crear, leer, actualizar y eliminar datos.
- **Manejo de Observables:** Las solicitudes HTTP devuelven observables que pueden ser suscritos.
- **Interceptors:** Permiten interceptar y modificar las solicitudes o respuestas HTTP.

```ad-important
title: HTTP
```
```
// api.service.ts
import { Injectable } from '@angular/core';
import { HttpClient } from '@angular/common/http';
import { Observable } from 'rxjs';

@Injectable({
  providedIn: 'root'
})
export class ApiService {
  private apiURL = 'https://api.ejemplo.com/items';

  constructor(private http: HttpClient) { }

  getItems(): Observable<Item[]> {
    return this.http.get<Item[]>(this.apiURL);
  }

  addItem(item: Item): Observable<Item> {
    return this.http.post<Item>(this.apiURL, item);
  }

  updateItem(id: number, item: Item): Observable<Item> {
    return this.http.put<Item>(`${this.apiURL}/${id}`, item);
  }

  deleteItem(id: number): Observable<void> {
    return this.http.delete<void>(`${this.apiURL}/${id}`);
  }
}
```

```
// items.component.ts
import { Component, OnInit } from '@angular/core';
import { ApiService } from '../services/api.service';

@Component({
  selector: 'app-items',
  templateUrl: './items.component.html'
})
export class ItemsComponent implements OnInit {
  items: Item[] = [];

  constructor(private apiService: ApiService) { }

  ngOnInit() {
    this.apiService.getItems().subscribe(data => this.items = data);
  }

  addNewItem() {
    const newItem: Item = { name: 'Nuevo Item' };
    this.apiService.addItem(newItem).subscribe(item => this.items.push(item));
  }
}
```

