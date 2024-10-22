### **Pruebas Unitarias y de Integración**

- **Jasmine:** Framework de pruebas para escribir especificaciones (specs) de pruebas.
    
    **Documentación:** jasmine.github.io
    
- **Karma:** Ejecuta las pruebas unitarias en diferentes navegadores.
    
    **Documentación:** karma-runner.github.io
    

**Configuración automática:** Angular CLI configura Jasmine y Karma por defecto al crear un proyecto.

```
ng test
```

### **Pruebas End-to-End (E2E)**

- **Protractor:** Herramienta de testing E2E tradicionalmente usada con Angular.
    
    **Nota:** Protractor está en desuso y se recomienda migrar a herramientas más modernas como Cypress.
    
- **Cypress:** Herramienta moderna de testing E2E que ofrece una experiencia de desarrollo más rápida y robusta.

```ad-note
title: Instalacion
```
```
npm install cypress --save-dev
```

```
npx cypress open
```

**Documentación:** [cypress.io](https://www.cypress.io/)

