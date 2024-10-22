#### **Descripción:**

Angular está diseñado con pruebas en mente, ofreciendo soporte integrado para **pruebas unitarias**, **pruebas de integración** y **pruebas end-to-end (E2E)**.

#### **Tipos de Pruebas:**

1. **Pruebas Unitarias:**
    
    - **Objetivo:** Probar componentes, servicios y otras unidades de código de forma aislada.
    - **Herramientas:** Jasmine (framework de pruebas) y Karma (ejecutor de pruebas).

```ad-important
title: testing
```
```
// home.component.spec.ts
import { ComponentFixture, TestBed } from '@angular/core/testing';
import { HomeComponent } from './home.component';

describe('HomeComponent', () => {
  let component: HomeComponent;
  let fixture: ComponentFixture<HomeComponent>;

  beforeEach(async () => {
    await TestBed.configureTestingModule({
      declarations: [ HomeComponent ]
    })
    .compileComponents();
  });

  beforeEach(() => {
    fixture = TestBed.createComponent(HomeComponent);
    component = fixture.componentInstance;
    fixture.detectChanges();
  });

  it('debería crear el componente', () => {
    expect(component).toBeTruthy();
  });

  it('debería tener un título definido', () => {
    expect(component.title).toBe('Página de Inicio');
  });
});
```

2. **Pruebas End-to-End (E2E):**

- **Objetivo:** Probar la aplicación completa desde la perspectiva del usuario, asegurando que los flujos principales funcionen correctamente.
- **Herramientas:** Protractor (tradicionalmente usado) o Cypress (más moderno y recomendado).

```ad-important
title: testing e2e
```
```
// cypress/integration/home.spec.js
describe('Página de Inicio', () => {
  it('debería mostrar el título correcto', () => {
    cy.visit('/');
    cy.contains('Bienvenido a la Página de Inicio').should('be.visible');
  });

  it('debería agregar un nuevo ítem a la lista', () => {
    cy.visit('/');
    cy.get('button').contains('Añadir Dato').click();
    cy.get('ul').children().should('have.length', 4);
  });
});
```

