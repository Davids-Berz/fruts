### **Sentry**

**Descripción:** Plataforma para monitorear y reportar errores en tiempo real, permitiendo detectar y solucionar problemas rápidamente.

```ad-note
title: Instalacion
```
```
npm install @sentry/angular @sentry/tracing
```

```ad-info
title: Configuracion
```
```
// app.module.ts
import { BrowserModule } from '@angular/platform-browser';
import { NgModule, ErrorHandler } from '@angular/core';
import * as Sentry from "@sentry/angular";
import { Integrations } from "@sentry/tracing";

@NgModule({
  declarations: [AppComponent],
  imports: [
    BrowserModule,
    // Inicializar Sentry
    Sentry.init({
      dsn: "https://examplePublicKey@o0.ingest.sentry.io/0",
      integrations: [
        new Integrations.BrowserTracing({
          tracingOrigins: ["localhost", /^\//],
          routingInstrumentation: Sentry.routingInstrumentation,
        }),
      ],
      tracesSampleRate: 1.0,
    }),
  ],
  providers: [
    {
      provide: ErrorHandler,
      useValue: Sentry.createErrorHandler(),
    },
    {
      provide: Sentry.TraceService,
      useValue: {},
    },
  ],
  bootstrap: [AppComponent],
})
export class AppModule {}
```

**Documentación:** sentry.io

---
