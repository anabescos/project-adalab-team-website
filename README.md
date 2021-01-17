Este es el proyecto de DEVROCKETS, el equipo 1 del módulo 1 del curso de front-ender de Adalab. El objetivo es crear una página web a partir de un enunciado dado, aplicando los conocimientos adquiridos durante este módulo del curso, que son los siguientes: 
Maquetación: HTML5, CSS3, Flexbox, CSS Grid, SASS, Bootstrap. Considerando añadir animaciones, transiciones, ramas en GitHub, formularios y aportaciones extra autorizadas por el Product Owner.
                        
En este proyecto hay 3 tipos de ficheros y carpetas:
•	Los ficheros que están sueltos en la raíz del repositorio, como gulpfile.js, package.json. Son la configuración del proyecto y no he necesitado modificarlos.
•	La carpeta src/: son los ficheros de mi ejercicio, como HTML, CSS, JS...
•	Las carpetas public/ y docs/, se han generado automáticamente cuando al arrancar el proyecto. El Kit lee los ficheros que hay dentro de src/, los procesa y los genera dentro de public/ y docs/.

Además hemos añadido transiciones y algún pequeño cambio autorizado por el Product Owner.



[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[






[Una vez hemos instalado las dependencias, vamos a arrancar el proyecto. **El proyecto hay que arrancarlo cada vez que te pongas a programar.** Para ello ejecuta el comando:

```bash
npm start
```

Este comando:

- **Abre una ventana de Chrome y muestra tu página web**, al igual que hace el plugin de VS Code Live Server (Go live).
- También **observa** todos los ficheros que hay dentro de la carpeta `src/`, para que cada vez que modifiques un fichero **refresca tu página en Chrome**.
- También **procesa los ficheros** HTML, SASS / CSS y JS y los **genera y guarda en la carpeta `public/`**. Por ejemplo:
   - Convierte los ficheros SASS en CSS.
   - Combina los diferentes ficheros de HTML y los agrupa en uno o varios ficheros HTML.

Después de ejecutar `npm start` ya puedes empezar a editar todos los ficheros que están dentro de la carpeta `src/` y programar cómodamente.

### Pasos para publicar el proyecto en GitHub Pages:

Para generar tu página para producción ejecuta el comando:

```bash
npm run docs
```

Y a continuación:

1. Sube a tu repo la carpeta `docs/` que se te acaba de generar.
1. Entra en la pestaña `settings` de tu repo.
1. Y en el apartado de GitHub Pages activa la opción **master branch /docs folder**.
1. Y ya estaría!!!

Además, los comandos:

```bash
npm run push-docs
```
o

```bash
npm run deploy
```

son un atajo que nos genera la versión de producción y hace push de la carpeta `docs/` del tirón. Te recomendamos ver el fichero `package.json` para aprender cómo funciona.

## Flujo de archivos con Gulp

Estas tareas de Gulp producen el siguiente flujo de archivos:

![Gulp flow](./gulp-flow.png)

## `gulpfile.js` y `config.json`

Nuestro **gulpfile.js** usa el fichero `config.json` de configuración con las rutas de los archivos a generar / observar.

De esta manera separarmos las acciones que están en `gulpfile.js` de la configuración de las acciones que están en `config.json`.

## Estructura de carpetas

La estructura de carpetas tiene esta pinta:

```
src
 ├─ api // los ficheros de esta carpeta se copian en public/api/
 |  └─ data.json
 ├─ images
 |  └─ logo.jpg
 ├─ js // los ficheros de esta carpeta se concatenan en el fichero main.js y este se guarda en public/main.js
 |  ├─ main.js
 |  └─ events.js
 ├─ scss
 |  ├─ components
 |  ├─ core
 |  ├─ layout
 |  └─ pages
 └─ html
    └─ partials]
```

]]]]]]]]]]
