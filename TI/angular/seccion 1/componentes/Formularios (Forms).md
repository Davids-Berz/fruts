Angular proporciona dos enfoques principales para manejar formularios: **formularios basados en plantillas** y **formularios reactivos**.

#### **a. Formularios Basados en Plantillas (Template-Driven Forms)**

##### **Descripción:**

Utilizan directivas en la plantilla para gestionar el estado y las validaciones del formulario. Son más sencillos y adecuados para formularios simples.

##### **Características Clave:**

- **ngModel:** Vinculación bidireccional de datos.
- **Directivas de Validación:** Como `required`, `minlength`, `maxlength`, etc.
- **Feedback de Validación:** Muestra mensajes de error basados en el estado del formulario.

```ad-important
title: Forms de Plantillas
```
```
<!-- template-driven-form.component.html -->
<form #form="ngForm" (ngSubmit)="onSubmit(form)">
  <label for="name">Nombre:</label>
  <input type="text" id="name" name="name" ngModel required>
  <div *ngIf="form.controls.name?.invalid && form.controls.name?.touched">
    El nombre es requerido.
  </div>

  <button type="submit" [disabled]="form.invalid">Enviar</button>
</form>
```

```
// template-driven-form.component.ts
import { Component } from '@angular/core';
import { NgForm } from '@angular/forms';

@Component({
  selector: 'app-template-driven-form',
  templateUrl: './template-driven-form.component.html'
})
export class TemplateDrivenFormComponent {
  onSubmit(form: NgForm) {
    console.log('Formulario enviado:', form.value);
  }
}
```

#### **b. Formularios Reactivos (Reactive Forms)**

##### **Descripción:**

Ofrecen una mayor flexibilidad y escalabilidad, ideales para formularios complejos. Se gestionan principalmente en la clase del componente.

##### **Características Clave:**

- **FormControl, FormGroup, FormArray:** Objetos para manejar el estado y la estructura del formulario.
- **Validaciones Síncronas y Asíncronas:** Definidas en la clase del componente.
- **Mayor Control:** Facilita la manipulación programática del formulario.

```ad-important
title: Forms Reactivos
```
```
// reactive-form.component.ts
import { Component, OnInit } from '@angular/core';
import { FormGroup, FormControl, Validators } from '@angular/forms';

@Component({
  selector: 'app-reactive-form',
  templateUrl: './reactive-form.component.html'
})
export class ReactiveFormComponent implements OnInit {
  myForm: FormGroup;

  ngOnInit() {
    this.myForm = new FormGroup({
      name: new FormControl('', [Validators.required, Validators.minLength(3)]),
      email: new FormControl('', [Validators.required, Validators.email])
    });
  }

  onSubmit() {
    if (this.myForm.valid) {
      console.log('Formulario enviado:', this.myForm.value);
    }
  }
}
```

```
<!-- reactive-form.component.html -->
<form [formGroup]="myForm" (ngSubmit)="onSubmit()">
  <label for="name">Nombre:</label>
  <input id="name" formControlName="name">
  <div *ngIf="myForm.get('name')?.invalid && myForm.get('name')?.touched">
    El nombre es requerido y debe tener al menos 3 caracteres.
  </div>

  <label for="email">Email:</label>
  <input id="email" formControlName="email">
  <div *ngIf="myForm.get('email')?.invalid && myForm.get('email')?.touched">
    Debes ingresar un email válido.
  </div>

  <button type="submit" [disabled]="myForm.invalid">Enviar</button>
</form>
```

