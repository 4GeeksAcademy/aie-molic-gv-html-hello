# Instrucciones del proyecto

## Objetivo

Mantener un portfolio personal real para molicgv.art, nombre artístico de Mónica Gómez, artista emergente especializada en pintura acrílica texturizada.

## Tecnologías y estructura

- Usa HTML5 semántico y CSS3 en un archivo separado.
- Escribe directamente en `index.html` todo el contenido visible; este HTML es la fuente de contenido de la web.
- `data/artist.json`, si existe, es únicamente una referencia opcional. No lo cargues ni lo proceses desde la web, y su actualización no bloquea la implementación.
- Usa HTML5 semántico y CSS3, con Flexbox y CSS Grid cuando cada uno resulte adecuado.
- La web debe usar exclusivamente HTML5 y CSS3. No uses JavaScript, `fetch()`, Flask/Jinja para renderizar, frameworks, bibliotecas externas ni herramientas de generación o compilación.
- `server.py` puede utilizarse únicamente para previsualizar la web durante el desarrollo; no debe ser una dependencia de renderizado.
- Mantén el código claro, conciso y fácil de mantener.
- No añadas dependencias ni herramientas de compilación sin autorización.
- No bloquees la implementación ni intentes eludir restricciones de acceso del editor por un JSON de referencia inaccesible.

## Contenido y diseño

- Prioriza la obra y la identidad del artista: incluye una presentación breve, una selección de trabajos, una biografía y vías de contacto.
- Presenta únicamente datos confirmados por la artista. No inventes títulos, fechas, dimensiones, trayectoria, premios, exposiciones, estudios, clientes, ventas, colaboraciones ni eventos.
- No presentes proyectos futuros como realizados. RUST está en desarrollo; no le atribuyas detalles ni uses imágenes inexistentes.
- Mantén la navegación clara y coherente en todas las páginas.
- Presenta las imágenes de las obras con el contexto disponible, como título, técnica, fecha o descripción.
- Usa las rutas relativas originales de `assets/images/` y no modifiques ni sobrescribas las fotografías originales.
- Evita elementos decorativos que dificulten la lectura o distraigan de las obras.

## Diseño adaptable

- Diseña primero para pantallas pequeñas y adapta la presentación a pantallas mayores.
- Usa Flexbox con reglas flexibles, unidades relativas y puntos de quiebre justificados por el contenido.
- Evita anchos rígidos que provoquen desplazamiento horizontal.
- Comprueba que el contenido, las imágenes y los controles se mantengan legibles y utilizables en móvil y escritorio.

## Accesibilidad

- Usa landmarks semánticos, jerarquía de encabezados lógica y enlaces con nombres descriptivos.
- Asegura que todas las funciones puedan usarse con teclado y que el foco sea visible.
- Incluye un enlace para saltar al contenido principal.
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
- Facilita que buscadores y sistemas de respuesta puedan identificar a la artista y comprender sus obras; no rellenes el contenido con palabras clave ni generes afirmaciones no verificadas.
- No añadas una URL canónica hasta confirmar que el dominio está registrado y publicado.
- Conserva la directiva `noindex` existente hasta recibir autorización expresa para cambiar la política de indexación.
- Usa enlaces descriptivos y asegúrate de que las páginas importantes sean accesibles mediante enlaces HTML normales.

## Datos estructurados

- Usa vocabulario de Schema.org e implementa los datos estructurados con Microdata HTML; no uses JSON-LD.
- Representa únicamente información real y visible en la página.
- Elige tipos adecuados al contenido, como `Person`, `VisualArtwork` o `WebSite`, y usa propiedades pertinentes.
- No inventes identificadores, fechas, premios, ubicaciones ni perfiles sociales.

## Verificación

- Comprueba que el HTML sea válido y que la estructura semántica sea coherente.
- Revisa navegación por teclado, textos alternativos, contraste y presentación en móvil.
- Verifica que los metadatos y los datos estructurados coincidan con el contenido visible.
- No afirmes que una comprobación se realizó si no se ejecutó.