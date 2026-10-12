# Librería Entre Páginas

Proyecto del curso **Desarrollo Web**: una librería construida **solo con HTML**, sin CSS ni JavaScript. El sitio evoluciona desde un ejemplo sobre arquitectura de software hacia un producto con catálogo, solicitudes de pedidos, club de lectores y contenido multimedia.

Esta etapa desarrolla la estructura y semántica de las páginas. Los precios son de ejemplo y los formularios todavía no guardan información, crean cuentas ni procesan pedidos o pagos.

## Páginas

| Archivo | Contenido |
| --- | --- |
| [index.html](src/index.html) | Presentación, libros destacados, categorías y acceso a los demás apartados. |
| [table.html](src/table.html) | Catálogo de cuatro libros con autores, categorías, precios en soles y total de referencia. |
| [conceptos.html](src/conceptos.html) | Solicitud de pedido con libro, cantidad, contacto y preferencias de entrega. |
| [form.html](src/form.html) | Club de lectores con datos del perfil, preferencias y controles de entrada. |
| [contacto.html](src/contacto.html) | Contacto del responsable y formulario de consultas. |
| [video_basic.html](src/video_basic.html) | Video de muestra y audio de bienvenida con transcripción. |
| [video_adv.html](src/video_adv.html) | Video con portada, fuentes MP4 y WebM y subtítulos en español e inglés. |

Se conservan los nombres de archivo de las prácticas. `conceptos.html` ahora corresponde a pedidos.

## Estructura

```text
PrimeraPaginaWeb/
├── README.md
└── src/
    ├── index.html
    ├── table.html
    ├── conceptos.html
    ├── form.html
    ├── contacto.html
    ├── video_basic.html
    ├── video_adv.html
    └── assets/
        └── media/
            ├── lectura-pausa.mp4
            ├── lectura-pausa.webm
            ├── portada-lectura.png
            ├── lectura-es.vtt
            ├── lectura-en.vtt
            └── bienvenida.wav
```

## Cómo abrir el proyecto

### Con Live Server en VS Code

1. Abre la carpeta raíz del proyecto en VS Code.
2. Instala la extensión **Live Server** si todavía no la tienes.
3. Abre `src/index.html` y selecciona **Open with Live Server**, o pulsa **Go Live**.
4. Navega utilizando el menú del sitio.

Si el servidor utiliza el puerto 5500 y sirve la carpeta raíz, la dirección será:

```text
http://127.0.0.1:5500/src/index.html
```

El puerto y la ruta pueden variar según la configuración y la carpeta abierta. Usa la dirección que abra la extensión.

### Con Python

Si tienes Python instalado, ejecuta desde la raíz del proyecto:

```powershell
python -m http.server 5500 --bind 127.0.0.1
```

Abre `http://127.0.0.1:5500/src/index.html` y deja la terminal en ejecución. Para detener el servidor, pulsa `Ctrl+C`.

Puedes abrir los HTML directamente para revisar su estructura, pero utiliza un servidor HTTP local para probar los subtítulos. Si aparece `ERR_CONNECTION_REFUSED`, comprueba que el servidor siga activo y que la dirección use su puerto correcto. No inicies dos servidores en el mismo puerto.

## Contenido multimedia

- **Video:** clip de naturaleza de aproximadamente cinco segundos, procedente de la [colección CC0 de MDN](https://github.com/mdn/interactive-examples/tree/main/live-examples/media/cc0-videos). Se guarda localmente en MP4 y WebM y se identifica como muestra; no representa una librería real.
- **Audio:** bienvenida original para el proyecto, de aproximadamente dieciséis segundos, generada con una voz sintetizada en español. Su transcripción está disponible en la página.
- **Portada:** imagen creada para Librería Entre Páginas.
- **Subtítulos:** archivos WebVTT en español e inglés con mensajes de acompañamiento, no una transcripción de diálogo. Se seleccionan desde los controles nativos del reproductor.

No hay reproducción automática. Los recursos pueden sustituirse por contenido propio actualizando las rutas, la portada, los subtítulos y la transcripción correspondientes.

## HTML practicado y guías

| Tema | Elementos y atributos utilizados |
| --- | --- |
| Estructura y semántica | `<!DOCTYPE html>`, `html lang`, metadatos, `header`, `nav`, `main`, `section`, `article`, `aside`, `footer`. |
| Navegación y accesibilidad | Enlaces, anclas, salto al contenido, `aria-current`, `aria-label`, `aria-labelledby`, `aria-describedby`. |
| Contenido | Encabezados, párrafos, `strong`, `mark`, `abbr`, listas, `address`, `details` y `summary`. |
| Tablas | `table`, `caption`, `thead`, `tbody`, `tfoot`, `tr`, `th`, `td`, `scope` y `colspan`. |
| Formularios | `form`, `fieldset`, `legend`, `label`, `select`, `textarea`, `required`, `autocomplete`, `min`, `max` y `step`. |
| Controles de entrada | Texto, correo, teléfono, número, fecha, contraseña, color, rango, archivo, radio y casilla de verificación. |
| Video y audio | `video`, `audio`, `source`, `track`, `controls`, `width`, `poster`, `preload`, `playsinline`, `figure` y `figcaption`. |

Las prácticas se adaptan al producto conservando los elementos solicitados:

- **Labs_form:** estructura del formulario y controles de entrada de los pasos 01 y 02. La carga de archivos utiliza `enctype="multipart/form-data"`.
- **Labs_tabla / Labs_tabla (1):** tabla de libros con encabezado, cuerpo, pie, título y celdas combinadas de los pasos 01 a 05. Los precios se adaptan a soles; el total de ejemplo es **S/ 245.00** por un ejemplar de cada título y no representa un carrito.
- **Labs_video:** reproductor básico y video con varios formatos, portada y subtítulos de los pasos 01 y 02. Se añade un reproductor de audio con transcripción.

Los ejemplos de JavaScript de las guías y el reproductor personalizado con CSS y JavaScript quedan para etapas posteriores.

## Estado y próximos pasos

La navegación, las tablas, los controles nativos de los formularios y los reproductores están implementados. Los formularios apuntan a `/submit`, un marcador de posición sin servidor de procesamiento: al enviarlos todavía no se registra una solicitud. Utiliza datos ficticios para probarlos.

El desarrollo continuará por etapas:

1. **CSS:** identidad visual, distribución y adaptación a celulares.
2. **JavaScript:** interacción, validaciones adicionales y carrito de compras.
3. **Servidor y base de datos:** registro de pedidos, consultas y perfiles.
4. **Contenido real y publicación:** catálogo, precios, disponibilidad y recursos propios.

## Autor

Noe Santiago · 2026
