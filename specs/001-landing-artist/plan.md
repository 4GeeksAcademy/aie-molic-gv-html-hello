# Plan técnico: landing page de Álex Vega

## Objetivo

Construir una landing de demostración de una sola página para el personaje ficticio Álex Vega. Respetar `AGENTS.md`: usar solo HTML5 y CSS3; el JSON será referencia, y el HTML contendrá directamente el contenido visible. Este documento define el plan; no implementa la web.

## Archivos previstos

- `index.html`: estructura semántica, navegación por anclas, metadatos y marcado de datos estructurados.
- `styles.css`: estilos separados, mobile-first, Flexbox, foco visible y adaptación a escritorio.
- `data/artist.json`: referencia editable para organizar los datos ficticios; no se consume desde la web.
- `assets/images/`: imágenes del artista y de sus obras, solo cuando se proporcionen y autoricen.
- `server.py`: reutilizar solo para previsualización; no modificarlo ni usarlo para procesar datos.

## Pasos principales

1. Definir el esquema de `data/artist.json` y preparar contenido ficticio para el perfil, obras, presentaciones y contacto. Identificarlo como demostración, sin presentarlo como información real.
2. Completar `index.html` con Inicio (`#inicio`), Sobre mí (`#sobre-mi`), Trayectoria (`#trayectoria`) y Próximas presentaciones (`#presentaciones`), más footer. Escribir directamente en HTML el contenido visible y mantenerlo coherente con el JSON.
3. Crear `styles.css` con diseño adaptable y Flexbox. En escritorio, aproximar cada sección principal al alto de la ventana sin recortar contenido; en móvil, permitir el alto necesario y evitar desbordamientos.
4. Crear con CSS3 los visuales ficticios definidos por las claves de `data/artist.json`, proporcionando `role="img"` y `aria-label` útiles. No usar la imagen genérica `.vscode/rigo-baby.jpeg`.
5. Añadir metadatos que identifiquen el carácter demostrativo y eviten indexar el perfil ficticio como real. Derivar los datos Schema.org únicamente del contenido visible.
6. Validar HTML, navegación por teclado, foco, contraste, textos alternativos, metadatos, Schema.org y presentación móvil/escritorio. Previsualizar con `server.py` sin modificarlo.

## Fuente de contenido

`data/artist.json` será una referencia editable, no una fuente dinámica. El contenido visible se escribirá directamente en `index.html`; cada cambio de contenido se reflejará manualmente en ambos. La web no cargará ni procesará el JSON y no usará JavaScript, `fetch()`, Flask, frameworks ni herramientas de generación. Los datos ficticios se identificarán como demostración y no se indexarán ni divulgarán como hechos sobre una persona real.

## Criterios de aceptación

- [ ] `data/artist.json` existe como referencia editable y no se consume desde la web.
- [ ] Todo el contenido visible se encuentra directamente en `index.html` y coincide con la referencia JSON.
- [ ] La implementación usa únicamente HTML5 y CSS3, sin JavaScript, `fetch()`, Flask, frameworks, bibliotecas externas ni herramientas de generación o compilación.
- [ ] Ningún dato ficticio se presenta ni se indexa como información real.
- [ ] La landing tiene las cuatro secciones con IDs únicos, navegación por anclas y footer con contacto disponible.
- [ ] La presentación es adaptable; en escritorio las secciones se aproximan al alto de la ventana sin ocultar contenido, y en móvil no hay desbordamiento horizontal.
- [ ] Se cumplen los requisitos de semántica, teclado, foco visible, contraste, alternativas textuales, SEO/GEO y Schema.org definidos en `AGENTS.md`.
- [ ] Las validaciones se ejecutan antes de declarar terminada la implementación y no se reportan comprobaciones no realizadas.
