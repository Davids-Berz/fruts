### **Gulp**

**Descripción:** Gulp es un sistema de automatización de tareas que puede ser utilizado para compilar estilos, optimizar imágenes, entre otras tareas.

```ad-note
title: Instalacion
```
```
npm install --save-dev gulp
```

```ad-example
title: GulpFile
```
```
const gulp = require('gulp');
const sass = require('gulp-sass')(require('sass'));

// Compilar archivos Sass a CSS
gulp.task('sass', function() {
  return gulp.src('src/styles/**/*.scss')
    .pipe(sass())
    .pipe(gulp.dest('dist/styles'));
});

// Tarea por defecto
gulp.task('default', gulp.series('sass'));
```

**Documentación:** [gulpjs.com](https://gulpjs.com/)

