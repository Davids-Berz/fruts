#### **Descripción:**

Los **módulos** son contenedores que agrupan componentes, directivas, servicios y otros módulos relacionados. Ayudan a organizar el código en bloques funcionales cohesivos.

#### **Características Clave:**

- **Declaraciones:** Lista de componentes, directivas y pipes que pertenecen al módulo.
- **Importaciones:** Otros módulos cuyas funcionalidades se necesitan.
- **Proveedores (Providers):** Servicios que estarán disponibles para inyección de dependencias.
- **Exportaciones:** Componentes, directivas y pipes que pueden ser utilizados por otros módulos.
- **Bootstrap:** Componente raíz que Angular crea e inserta en el DOM durante el arranque.

```ad-important
title: modulos
```
```
import { NgModule } from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';
import { AppComponent } from './app.component';
import { HomeComponent } from './home/home.component';

@NgModule({
  declarations: [
    AppComponent,
    HomeComponent
  ],
  imports: [
    BrowserModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```

