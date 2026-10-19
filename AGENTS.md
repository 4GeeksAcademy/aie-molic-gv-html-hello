# Instrucciones del proyecto

## Objetivo

Crear una landing de demostración para el personaje ficticio Álex Vega, ilustrador. El contenido de ejemplo debe identificarse como ficticio y no presentarse como información real sobre una persona.

## Tecnologías y estructura

- Usa HTML5 semántico y CSS3 en un archivo separado.
- Mantén `data/artist.json` como archivo de referencia y organización del contenido ficticio; no lo cargues ni lo proceses desde la web.
- Escribe directamente en `index.html` todo el contenido visible. Cuando se cambie el contenido, actualiza manualmente el JSON y el HTML para mantenerlos coherentes.
- Usa Flexbox para organizar los elementos y adaptar los diseños.
- La web debe usar exclusivamente HTML5 y CSS3. No uses JavaScript, `fetch()`, Flask, frameworks, bibliotecas externas ni herramientas de generación o compilación.
- Mantén el código claro, conciso y fácil de mantener.
- No añadas dependencias ni herramientas de compilación sin autorización.

## Contenido y diseño

- Prioriza la obra y la identidad del artista: incluye una presentación breve, una selección de trabajos, una biografía y vías de contacto.
- El perfil, la biografía, las obras, presentaciones y contactos de la demo serán ficticios y se identificarán como contenido de muestra. No los presentes como hechos reales ni uses información de personas reales.
- No inventes credenciales, premios o datos sobre artistas reales.
- Mantén la navegación clara y coherente en todas las páginas.
- Presenta las imágenes de las obras con el contexto disponible, como título, técnica, fecha o descripción.
- Evita elementos decorativos que dificulten la lectura o distraigan de las obras.

## Diseño adaptable

- Diseña primero para pantallas pequeñas y adapta la presentación a pantallas mayores.
- Usa Flexbox con reglas flexibles, unidades relativas y puntos de quiebre justificados por el contenido.
- Evita anchos rígidos que provoquen desplazamiento horizontal.
- Comprueba que el contenido, las imágenes y los controles se mantengan legibles y utilizables en móvil y escritorio.

## Accesibilidad

- Usa landmarks semánticos, jerarquía de encabezados lógica y enlaces con nombres descriptivos.
- Asegura que todas las funciones puedan usarse con teclado y que el foco sea visible.
- Mantén contraste suficiente y no transmitas información únicamente mediante color.
- Añade texto alternativo útil a las imágenes; usa texto alternativo vacío solo para imágenes decorativas.
- Para ilustraciones compuestas con CSS, proporciona un nombre accesible con `role="img"` y `aria-label`, tomado de la descripción definida para ese visual.
- Asocia etiquetas explícitas a los campos de formularios y comunica sus errores de manera comprensible.
- Respeta las preferencias de movimiento reducido y evita animaciones innecesarias.

## SEO y GEO

- Proporciona un título y una descripción únicos y precisos para cada página.
- Usa una URL canónica cuando corresponda y metadatos sociales coherentes con el contenido visible.
- Organiza el contenido con encabezados descriptivos y texto claro, específico y verificable.
- Mantén coherentes el nombre artístico, la biografía, la ubicación y los enlaces oficiales en todo el sitio.
- Facilita que buscadores y sistemas de respuesta puedan identificar al artista y comprender sus obras; no rellenes el contenido con palabras clave ni generes afirmaciones no verificadas.
- Evita que los datos ficticios de demostración se indexen o se divulguen como un perfil real.
- Usa enlaces descriptivos y asegúrate de que las páginas importantes sean accesibles mediante enlaces HTML normales.

## Datos estructurados

- Usa vocabulario de Schema.org e implementa los datos estructurados como Microdata o JSON-LD no ejecutable.
- Representa únicamente información visible en la página; los datos de demostración deben identificarse como ficticios y no exponerse como información real.
- Elige tipos adecuados al contenido, como `Person`, `VisualArtwork` o `WebSite`, y usa propiedades pertinentes.
- No inventes identificadores, fechas, premios, ubicaciones ni perfiles sociales.
- JSON-LD es un formato de datos, no lógica de JavaScript; no añadas JavaScript ejecutable.

## Verificación

- Comprueba que el HTML sea válido y que la estructura semántica sea coherente.
- Revisa navegación por teclado, textos alternativos, contraste y presentación en móvil.
- Verifica que los metadatos y los datos estructurados coincidan con el contenido visible.
- No afirmes que una comprobación se realizó si no se ejecutó.