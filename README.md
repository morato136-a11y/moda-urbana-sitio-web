# Moda Urbana — Sitio Web Comercial Responsive

**Proyecto formativo — Módulo HTML/CSS — INCAP**
**Formador:** Heladio Polo Castro
**Tipo de proyecto:** Empresa de ventas de ropa

---

## 1. Link de la plantilla / recursos originales

Este sitio **no usa una plantilla externa completa**: está construido desde
cero usando el framework **Bootstrap 5** (CSS y JS oficiales, cargados desde
el CDN de jsDelivr) como base de diseño responsive, más una hoja de estilos
propia (`css/styles.css`).

- Bootstrap 5.3.3 (CSS): https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css
- Bootstrap 5.3.3 (JS): https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js
- Imágenes de ejemplo (placeholders): https://placehold.co
- Video de demostración: https://www.w3schools.com/html/mov_bbb.mp4 (video de ejemplo, de uso libre, usado comúnmente en tutoriales de HTML)

> Nota: las imágenes son "placeholders" (imágenes de relleno con texto) y el
> video es uno de ejemplo libre. Para la entrega final real se recomienda
> reemplazarlos por fotos y video propios de la tienda.

---

## 2. Estructura del proyecto

```
tienda-ropa-responsive/
│
├── index.html        → Página de inicio (carrusel, categorías, video)
├── catalogo.html      → Catálogo de productos (tarjetas + tabla de tallas)
├── nosotros.html       → Información de la empresa (valores, sedes)
├── contacto.html       → Formulario de contacto + horarios
│
├── css/
│   └── styles.css      → Hoja de estilos propia del proyecto
│
└── README.md          → Este manual técnico-usuario
```

Las 4 páginas están enlazadas entre sí por el menú de navegación (navbar),
que aparece igual en todas las páginas, así que se puede navegar entre
cualquiera de ellas sin que se rompa ningún enlace.

---

## 3. Explicación del código HTML

Cada página sigue la misma estructura básica:

1. **`<head>`**: aquí se carga Bootstrap, nuestra hoja de estilos propia
   (`css/styles.css`) y se configura el `viewport` para que el sitio sea
   responsive (se adapte a celular, tablet y computador).
2. **`<nav>`**: la barra de menú, con la clase `navbar-expand-lg` de
   Bootstrap, que convierte el menú en un ícono de "hamburguesa" en
   pantallas pequeñas. Tiene 4 enlaces (`<a>`) a las 4 páginas del sitio.
3. **Contenido propio de cada página**:
   - `index.html`: un carrusel (`<div class="carousel">`) con 3 imágenes,
     una lista (`<ul>`) de categorías, y un video (`<video>`).
   - `catalogo.html`: 6 tarjetas de producto (`<div class="card">`) con
     imagen, nombre, precio y botón, más una tabla (`<table>`) de tallas
     disponibles.
   - `nosotros.html`: texto e imagen de la empresa, una lista ordenada
     (`<ol>`) de valores, y una tabla de sedes.
   - `contacto.html`: un formulario (`<form>`) con campos de nombre,
     correo, teléfono, asunto y mensaje, más una tabla de horarios.
4. **`<footer>`**: pie de página igual en las 4 páginas, con el copyright
   y enlaces a redes sociales.

Todo el HTML usa clases de **Bootstrap** (`container`, `row`, `col-*`,
`card`, `btn`, `table`, `navbar`, `carousel`, etc.) para que el diseño sea
responsive sin tener que escribir CSS personalizado para cada tamaño de
pantalla.

---

## 4. Explicación del código CSS (`css/styles.css`)

El archivo `css/styles.css` contiene **solo lo que Bootstrap no trae por
defecto**, o lo que queremos personalizar:

- Variables de color (`:root`) para reutilizar los mismos colores en todo
  el sitio sin repetir código.
- Estilo del menú (`navbar-personalizada`) con el color de marca.
- Estilo de las tarjetas de producto (`tarjeta-producto`), con sombra y un
  efecto de elevación al pasar el mouse.
- Estilo del botón de acento (`btn-acento`) con el color naranja de marca.
- Estilo del pie de página (`footer`).

Cada bloque del archivo tiene un comentario explicando para qué sirve.

---

## 5. Guía de uso (para el usuario final del sitio)

1. Abre `index.html` en cualquier navegador (Chrome, Edge, Firefox) haciendo
   doble clic sobre el archivo, o súbelo a un servicio de hosting (ver
   sección 6).
2. En la parte de arriba encontrarás el menú: **Inicio, Catálogo, Nosotros,
   Contacto**. Haz clic en cualquiera para navegar.
3. En **Inicio** puedes ver las promociones del carrusel (las flechas a los
   lados cambian de imagen) y un video de presentación de la tienda.
4. En **Catálogo** puedes ver los productos disponibles, su precio y la
   tabla de tallas.
5. En **Nosotros** puedes conocer la historia, valores y sedes de la
   empresa.
6. En **Contacto** puedes llenar el formulario con tu nombre, correo y
   mensaje (nota: en esta versión de práctica el formulario no envía datos a
   ningún servidor real, es solo una demostración del uso de formularios en
   HTML).
7. El sitio se adapta automáticamente si lo abres desde un celular o una
   tablet: el menú se convierte en un ícono de hamburguesa y las tarjetas de
   producto se acomodan en una sola columna.

---

## 6. Cómo subir el proyecto a GitHub y a un hosting gratuito

1. Crea una cuenta en [github.com](https://github.com) si no tienes una.
2. Crea un repositorio nuevo, por ejemplo `moda-urbana-sitio-web`.
3. Sube todos los archivos de esta carpeta (`index.html`, `catalogo.html`,
   `nosotros.html`, `contacto.html`, la carpeta `css/` y este `README.md`)
   al repositorio (puedes arrastrar los archivos desde la página web de
   GitHub, en el botón "Add file" > "Upload files").
4. Para publicarlo como página web gratis, ve a **Settings > Pages** del
   repositorio, selecciona la rama `main` y la carpeta `/root`, y guarda.
   GitHub te dará un link público tipo
   `https://tu-usuario.github.io/moda-urbana-sitio-web/`.
5. Copia ese link del repositorio y el link de la página publicada, y
   colócalos en la entrega del proyecto en Q10, junto con la carpeta
   comprimida (.zip) de este proyecto.

---

## 7. Checklist de cumplimiento (según lineamientos del proyecto)

- [x] Diseño web responsive (Bootstrap 5)
- [x] Framework CSS Bootstrap aplicado
- [x] Menú de opciones con hipervínculos a 4 páginas diferentes
- [x] Integración de enlaces entre páginas (sin enlaces rotos)
- [x] Etiquetas HTML vistas: imágenes, video, tablas, listas
- [x] Hoja de estilos CSS propia (`css/styles.css`)
- [x] Slider / carrusel de imágenes
- [x] Catálogo de productos
- [x] Formulario de contacto personalizado
- [x] Manual técnico-usuario (este documento)
