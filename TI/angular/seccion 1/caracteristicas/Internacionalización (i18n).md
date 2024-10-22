#### **Descripción:**

Angular facilita la creación de aplicaciones multilingües mediante su soporte integrado para **internacionalización (i18n)**, permitiendo adaptar la aplicación a diferentes idiomas y regiones.

#### **Características Clave:**

- **Traducción de Texto:** Utiliza archivos de traducción para diferentes idiomas.
- **Formato de Fechas y Números:** Adapta el formato según la localización.
- **Directivas y Pipes Específicos:** Facilitan la manipulación de contenido multilingüe.

1. Marcar Texto para Traducción:
```ad-important
title: i18n
```
```
<p i18n="Descripción del saludo">Hola, bienvenido a nuestra aplicación!</p>
```

2. Extraer las Cadenas para Traducción
```
ng extract-i18n
```

Esto genera un archivo `messages.xlf` con las cadenas a traducir.

3.  Crear Archivos de Traducción:
    
    - `messages.es.xlf` para español.
    - `messages.fr.xlf` para francés, etc.

4.  Configurar el Módulo de Traducción:

```
// app.module.ts
import { NgModule } from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';
import { AppComponent } from './app.component';
import { HttpClientModule } from '@angular/common/http';
import { TranslateModule, TranslateLoader } from '@ngx-translate/core';
import { TranslateHttpLoader } from '@ngx-translate/http-loader';
import { HttpClient } from '@angular/common/http';

// Función para crear el loader
export function HttpLoaderFactory(http: HttpClient) {
  return new TranslateHttpLoader(http);
}

@NgModule({
  declarations: [AppComponent],
  imports: [
    BrowserModule,
    HttpClientModule,
    TranslateModule.forRoot({
      loader: {
        provide: TranslateLoader,
        useFactory: HttpLoaderFactory,
        deps: [HttpClient]
      }
    })
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```

5. Uso de Traducciones en Componentes:

```
// app.component.ts
import { Component } from '@angular/core';
import { TranslateService } from '@ngx-translate/core';

@Component({
  selector: 'app-root',
  template: `
    <div>
      <h1>{{ 'HELLO' | translate }}</h1>
      <button (click)="changeLanguage('es')">Español</button>
      <button (click)="changeLanguage('fr')">Francés</button>
    </div>
  `
})
export class AppComponent {
  constructor(private translate: TranslateService) {
    translate.setDefaultLang('en');
  }

  changeLanguage(lang: string) {
    this.translate.use(lang);
  }
}
```

