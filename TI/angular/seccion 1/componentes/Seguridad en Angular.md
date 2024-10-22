#### **Descripción:**

La **seguridad** es fundamental en el desarrollo de aplicaciones web. Angular proporciona varias herramientas y prácticas para proteger la aplicación contra vulnerabilidades comunes como ataques de **Cross-Site Scripting (XSS)** y **Cross-Site Request Forgery (CSRF)**.

#### **Características Clave:**

1. **Escapado Automático de Datos:** Angular escapa automáticamente los valores interpolados en las plantillas para prevenir inyecciones de código malicioso.
    
2. **Sanitización de URLs:** Las URLs que se utilizan en enlaces y recursos son sanitizadas para evitar la ejecución de código no deseado.
    
3. **Directiva `DomSanitizer`:** Permite manejar contenido considerado inseguro de manera controlada, útil para casos como incrustar contenido HTML desde fuentes externas.
    
4. **Protección CSRF:** Utiliza tokens CSRF en solicitudes HTTP para prevenir ataques de falsificación de solicitudes.
    
5. **Guards de Rutas:** Controla el acceso a rutas sensibles mediante autenticación y autorización.

```ad-important
title: DomSanitizer
```
```
// safe-html.component.ts
import { Component } from '@angular/core';
import { DomSanitizer, SafeHtml } from '@angular/platform-browser';

@Component({
  selector: 'app-safe-html',
  template: `
    <div [innerHTML]="safeContent"></div>
  `
})
export class SafeHtmlComponent {
  safeContent: SafeHtml;

  constructor(private sanitizer: DomSanitizer) {
    const maliciousContent = '<img src=x onerror=alert("XSS") />';
    this.safeContent = this.sanitizer.bypassSecurityTrustHtml(maliciousContent);
  }
}
```

