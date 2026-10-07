# Normas del equipo y flujo de trabajo

## 1. Metodología y diseño previo

### Prioridad de desarrollo

- **IMPORTANTE:** Empezar siempre por el layout y el diseño en Figma antes de tocar código.
- Definir primero en Figma la paleta de colores, tipografías y componentes.
- No desarrollar hasta tener la guía de estilos.

### Gestión en GitHub

- Trabajar apoyándose en las Issues de GitHub para marcar el progreso de las tareas.
- Cada cambio o rama debe estar alineado con su correspondiente tarea de la lista.

## 2. Estrategia de ramas (Git)

### `main`

- Rama de producción.
- Prohibido hacer commits directos o trabajar sobre ella.

### `dev`

- Rama base de desarrollo.
- Se utiliza como origen para crear todas las ramas de trabajo.
- Prohibido programar o hacer commits directos sobre ella.
- Se integra el código mediante *merge* únicamente tras revisión del equipo.

### Nomenclatura de ramas

- Formato vinculado a las Issues de GitHub: `T<NúmeroTarea>_<Fichero/Tema>`.
- Ejemplo: `T4_inventario.html_Inventario`.

## 3. Reglas de commits

### Formato del mensaje

- Usar el formato de *Conventional Commits*: `<tipo>(<ámbito>): <descripción>`.
- El ámbito es opcional y debe indicar la parte afectada, por ejemplo `catalogo` o `estilos`.
- Escribir la descripción en minúsculas, en modo imperativo y sin punto final.
- Mantener cada commit centrado en un único cambio lógico.

### Tipos permitidos

- `feat`: nueva funcionalidad.
- `fix`: corrección de un error.
- `docs`: cambios en documentación.
- `style`: formato o estilos visuales sin cambios de comportamiento.
- `refactor`: reorganización de código sin cambiar su comportamiento.
- `test`: añadir o modificar pruebas.
- `chore`: tareas de mantenimiento o configuración.

### Ejemplos

**Commit normal (nueva funcionalidad):**

```text
feat(catalogo): añadir filtros por plataforma
```

**Fix puntual (corrección concreta):**

```text
fix(inventario): corregir el cálculo del stock
```

### Buenas prácticas

- Crear commits pequeños y coherentes; evitar mensajes como `cambios`, `arreglos` o `update`.
- Relacionar el trabajo con su Issue. Añadir `Refs #<número>` en el cuerpo del commit; usar `Closes #<número>` solo cuando el commit cierre realmente la Issue.
- Revisar los archivos preparados y ejecutar las comprobaciones pertinentes antes de confirmar el commit.
- No incluir credenciales, archivos temporales ni cambios ajenos a la tarea.
- Los commits se realizan en ramas de trabajo, nunca directamente en `main` ni en `dev`.

## 4. Reglas de código y buenas prácticas

### HTML semántico

- Usar etiquetas estructurales (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`).
- Solo un `<h1>` por página.
- Atributo `alt` obligatorio en todas las imágenes.

### CSS y nomenclatura

- Prohibido el uso de estilos en línea (nada de `style="..."`).
- Clases en minúsculas y separadas por guiones (*kebab-case*, por ejemplo, `.etiqueta-stock`).
- IDs únicamente para elementos únicos o anclas.
- Uso obligatorio de variables CSS en `:root` para colores, fuentes y espaciados.

### Metodología de desarrollo

- Enfoque *Mobile First*: diseñar y maquetar pensando primero en dispositivos móviles.
- Uso de unidades relativas (`rem`, `%`, `fr`) en lugar de valores fijos en `px`.

## 5. Entregables y exposición

### Documentación

- El `README.md` debe incluir obligatoriamente el listado de integrantes y el enlace a GitHub Pages.

### Preparación de la demo

- Coordinar la presentación en equipo para mostrar la web en portátil y móvil, justificando el uso de Flexbox, Grid, `@media` y animaciones.
