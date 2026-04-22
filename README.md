# AIGEN 2026

Sitio oficial del workshop **AIGEN 2026: IA y Genómica para la Salud Pública**, construido con [Hugo](https://gohugo.io/) y preparado para despliegue en Netlify.

## Requisitos

- Hugo Extended 0.111 o superior

Verifica tu instalación:

```bash
hugo version
```

## Ejecutar localmente

Inicia el servidor de desarrollo:

```bash
hugo server
```

El sitio quedará disponible en `http://localhost:1313`.

Para generar la versión de producción:

```bash
hugo
```

Los archivos compilados se publican en `public/`.

## Estructura del proyecto

- `hugo.toml`: configuración principal del sitio, navegación y datos globales.
- `content/`: páginas editables en Markdown.
- `data/program.yaml`: programa estructurado de los dos días.
- `layouts/`: plantillas Hugo y partials reutilizables.
- `static/css/site.css`: tema visual personalizado.
- `static/images/`: logo del workshop e imágenes institucionales.
- `netlify.toml`: configuración de build para Netlify.

## Cómo editar contenido

### Páginas

Edita estos archivos Markdown:

- `content/_index.md`
- `content/program.md`
- `content/speakers.md`
- `content/venue.md`
- `content/registration.md`
- `content/organizers-sponsors.md`
- `content/contact.md`

Cada archivo usa front matter para mantener listas y tarjetas fáciles de actualizar.

### Programa

Edita `data/program.yaml` para modificar horarios, títulos o descripciones.

### Navegación y textos globales

Edita `hugo.toml` para cambiar:

- menú principal
- botones del hero
- datos de contacto
- instituciones del footer y logos strip

## Logos e imágenes

### Logo principal del workshop

El sitio usa:

- `static/images/logoAIGEN2026V5.png`

Si ya cuentas con el logo oficial final, reemplázalo manteniendo el mismo nombre o actualiza la referencia en:

- `layouts/partials/hero.html`
- `layouts/partials/site-header.html` si deseas reutilizarlo en otras secciones

### Logos institucionales

Los logos mostrados en la portada están en:

- `static/images/institutions/uoh.png`
- `static/images/institutions/gore-ohiggins.png`
- `static/images/institutions/hospital-franco-ravera.png`

Puedes sustituirlos por los archivos oficiales manteniendo esos nombres, o actualizar las rutas en `hugo.toml`.

## Despliegue en Netlify

1. Conecta este repositorio en Netlify.
2. Netlify detectará `netlify.toml`.
3. Usa estos valores si necesitas configurarlos manualmente:

```text
Build command: hugo --gc --minify
Publish directory: public
```

4. Define la variable de entorno `HUGO_VERSION` solo si quieres fijar una versión distinta a la indicada en `netlify.toml`.

## Mantenimiento

- El tema es completamente local y no depende de un tema Hugo externo.
- La portada usa partials para hero, navegación, logos institucionales y footer.
- El CSS está organizado con variables en `:root` para mantener la identidad visual consistente.
