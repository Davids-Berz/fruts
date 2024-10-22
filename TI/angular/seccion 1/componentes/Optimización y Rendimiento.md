#### **Descripción:**

Para garantizar que las aplicaciones Angular sean rápidas y eficientes, es importante implementar prácticas de optimización y aprovechar las herramientas que el framework ofrece.

#### **Prácticas Clave:**

1. **Lazy Loading de Módulos:** Carga módulos solo cuando son necesarios para reducir el tamaño inicial de la aplicación.
    
2. **Change Detection Estratégico:** Usa estrategias de detección de cambios como `OnPush` para mejorar el rendimiento en componentes específicos.
    
3. **Tree Shaking:** Elimina código no utilizado durante el proceso de construcción para reducir el tamaño del bundle.
    
4. **Optimización de Imágenes y Recursos:** Comprime y optimiza imágenes y otros recursos estáticos.
    
5. **Uso de Angular Universal:** Mejora el tiempo de carga inicial mediante el renderizado del lado del servidor.
    
6. **Precompilación Ahead-of-Time (AOT):** Compila la aplicación durante la construcción para reducir el tiempo de carga en el cliente.

```ad-important
title: Lazy Loading
```
```
// app-routing.module.ts
const routes: Routes = [
  { path: '', component: HomeComponent },
  { 
    path: 'admin',
    loadChildren: () => import('./admin/admin.module').then(m => m.AdminModule)
  },
  { path: '**', redirectTo: '' }
];
```

```
// admin-routing.module.ts
import { NgModule } from '@angular/core';
import { RouterModule, Routes } from '@angular/router';
import { AdminDashboardComponent } from './admin-dashboard/admin-dashboard.component';

const routes: Routes = [
  { path: '', component: AdminDashboardComponent }
];

@NgModule({
  imports: [RouterModule.forChild(routes)],
  exports: [RouterModule]
})
export class AdminRoutingModule { }
```

```
// admin.module.ts
import { NgModule } from '@angular/core';
import { CommonModule } from '@angular/common';
import { AdminDashboardComponent } from './admin-dashboard/admin-dashboard.component';
import { AdminRoutingModule } from './admin-routing.module';

@NgModule({
  declarations: [AdminDashboardComponent],
  imports: [
    CommonModule,
    AdminRoutingModule
  ]
})
export class AdminModule { }
```

