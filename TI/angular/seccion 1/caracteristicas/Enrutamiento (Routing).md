El **enrutamiento** en Angular permite gestionar la navegación entre diferentes vistas o componentes de la aplicación. Características clave:

- **Rutas definidas:** Configura rutas en el módulo de enrutamiento para mapear URLs a componentes específicos.
- **Parámetros de ruta:** Permite pasar datos a través de la URL.
- **Protección de rutas:** Implementa guardias (guards) para controlar el acceso a ciertas rutas basadas en condiciones como autenticación.

```ad-important
title: Routing
```
```
// app-routing.module.ts
import { NgModule } from '@angular/core';
import { RouterModule, Routes } from '@angular/router';
import { HomeComponent } from './home/home.component';
import { AboutComponent } from './about/about.component';
import { AuthGuard } from './guards/auth.guard';

const routes: Routes = [
  { path: '', component: HomeComponent },
  { path: 'about', component: AboutComponent },
  { path: 'admin', component: AdminComponent, canActivate: [AuthGuard] }, // Ruta protegida
  { path: '**', redirectTo: '' } // Ruta por defecto para páginas no encontradas
];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
})
export class AppRoutingModule { }
```

```
<!-- app.component.html -->
<nav>
  <a routerLink="/">Inicio</a>
  <a routerLink="/about">Acerca de</a>
  <a routerLink="/admin">Admin</a>
</nav>
<router-outlet></router-outlet> <!-- Punto de inserción para componentes según la ruta -->
```

