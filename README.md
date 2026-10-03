# Sitio web en HTML semántico

Práctica del curso **Desarrollo Web**: un sitio de varias páginas hecho **solo con HTML** (sin CSS ni JavaScript).
El tema (arquitectura de software) es solo el contenido de ejemplo; el objetivo es practicar la **estructura y semántica de HTML5**.

## Estructura

```
src/
├── index.html      Página de inicio
├── conceptos.html  Contenido con tablas, glosario y código
├── contacto.html   Datos de contacto y formulario
└── assets/
    └── capas.svg   Imagen usada en el inicio
```

## Qué se practica

| Tema | Etiquetas usadas |
|------|------------------|
| Estructura del documento | `<!DOCTYPE>`, `<html lang>`, `<head>`, `<meta>` (charset, viewport, description, author) |
| Semántica | `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>` |
| Navegación | Enlaces entre páginas, anclas internas (`#id`), `aria-current="page"` |
| Texto | `<strong>`, `<em>`, `<mark>`, `<abbr>`, `<blockquote>`, `<cite>`, `<pre>`, `<code>` |
| Listas | `<ul>`, `<ol>`, listas anidadas, `<dl>` (glosario) |
| Multimedia | `<figure>`, `<figcaption>`, `<img>` con `alt`, `width` y `height` |
| Tablas | `<caption>`, `<thead>`, `<tbody>`, `<th scope>` |
| Formularios | `<form>`, `<fieldset>`, `<legend>`, `<label>`, `<input>` (text, email, radio, checkbox), `<select>`, `<textarea>`, `required` |
| Otros | `<address>`, `<time>` |

## Cómo verlo

Abre `src/index.html` en cualquier navegador. No necesita servidor ni instalación.

## Autor

Noe Santiago - 2026
