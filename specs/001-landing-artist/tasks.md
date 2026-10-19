# Tareas: landing page de Álex Vega

## Preparación

- [x] 01. Alinear el plan y la especificación con `AGENTS.md`: los datos ficticios solo se usarán como mock y no se presentarán ni indexarán como información real.
- [x] 02. Definir como estrategia que todo el contenido editable se incluya directamente en HTML; no usar JSON, JavaScript, frameworks ni herramientas de generación.
- [x] 03. Armonizar `spec.md`: establecer `data/artist.json` como referencia editable y el HTML como contenido visible, sin carga dinámica.
- [x] 04. Definir el esquema de `data/artist.json` para perfil, obras, presentaciones y contacto, con marca de contenido ficticio.
- [x] 05. Preparar los datos ficticios de demostración para cada sección, sin usar información de personas reales.
- [x] 06. Identificar recursos visuales: descartar la imagen genérica del repositorio y definir ilustraciones CSS con nombres accesibles por cada `visualKey`.

## Construcción

- [x] 07. Crear `data/artist.json` como referencia editable de contenido ficticio, sin convertirlo en fuente dinámica.
- [x] 08. Completar `index.html` con landmarks semánticos y navegación a `#inicio`, `#sobre-mi`, `#trayectoria` y `#presentaciones`.
- [x] 09. Escribir en el HTML los textos ficticios de portada, biografía, trayectoria, presentaciones y contacto, manteniéndolos coherentes con el JSON.
- [x] 10. Crear `styles.css` con diseño mobile-first, Flexbox, foco visible y reglas responsivas.
- [x] 11. Ajustar las secciones para que en escritorio se aproximen al alto de la ventana sin recortar contenido y puedan crecer cuando sea necesario.
- [x] 12. Crear los visuales ficticios con CSS y usar sus descripciones como nombres accesibles; no representar imágenes genéricas como obras reales.
- [x] 13. Crear metadatos coherentes con la demostración y evitar la indexación del perfil ficticio.
- [x] 14. Añadir datos estructurados de Schema.org derivados del contenido visible, sin exponer mocks como información real indexable.

## Verificación

- [x] 15. Comprobar que todos los enlaces de navegación apuntan a IDs únicos y funcionan con teclado; verificar el foco visible.
- [x] 16. Revisar textos alternativos, contraste, jerarquía de encabezados y recorrido por teclado.
- [x] 17. Comprobar presentación móvil y escritorio, ausencia de desbordamiento horizontal y alturas de sección sin contenido recortado.
- [x] 18. Comparar manualmente el contenido de `index.html` con `data/artist.json` para confirmar que coinciden.
- [x] 19. Validar HTML, metadatos y Schema.org, y confirmar que el contenido ficticio se identifica como demostración y no se indexa como real.
- [x] 20. Previsualizar `index.html` directamente en el navegador, sin ejecutar el servidor Flask ni añadir dependencias; registrar que no hubo captura automatizada de viewports.