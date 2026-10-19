# Especificación: landing page de Álex Vega

## Objetivo

Crear una landing page de demostración para el personaje ficticio Álex Vega, ilustrador. Un archivo JSON editable organizará el contenido ficticio como referencia; el contenido que verá el usuario estará escrito directamente en el HTML. La demostración no debe presentarse como información real ni publicarse como perfil factual.

## Alcance

Una landing page de una sola página con navegación por anclas y estas secciones, en este orden:

1. Inicio: portada con nombre, profesión, imagen y una frase de presentación.
2. Sobre mí: biografía breve.
3. Trayectoria: selección de ilustraciones, campañas de marketing, portadas u otros trabajos relevantes.
4. Próximas presentaciones: fechas y lugares confirmados.
5. Footer: enlaces de redes sociales y medios de contacto disponibles.

La navegación incluirá Inicio, Sobre mí, Trayectoria y Próximas presentaciones. Cada enlace llevará a la sección correspondiente mediante un identificador único. El footer podrá incluir un enlace de contacto sin requerir una sección de navegación adicional.

## Requisitos funcionales y de contenido

- La navegación debe permitir llegar directamente a cada sección mediante enlaces HTML normales.
- Cada trabajo mostrado debe incluir el contexto disponible, como título, tipo de proyecto, técnica, fecha o descripción.
- El perfil de demostración, las obras, las presentaciones y los datos de contacto serán ficticios y estarán marcados como contenido de muestra.
- `data/artist.json` organizará como referencia el perfil, las obras, las presentaciones y el contacto ficticios; no será una fuente de datos dinámica.
- El contenido visible de la web debe estar escrito directamente en `index.html` y coincidir con los datos de referencia del JSON. Los cambios de contenido se reflejarán manualmente en ambos archivos.
- Los datos JSON incluirán, según corresponda, nombre, profesión, frase, biografía, ubicación ficticia, imagen y texto alternativo; obras con título, tipo, técnica, fecha, descripción e imagen; presentaciones con fecha, lugar y descripción; y enlaces de contacto/redes ficticios.
- Los datos deben poder ampliarse o modificarse en el JSON sin cambiar el esquema de presentación, siempre que se respeten los campos definidos.
- El contenido ficticio debe identificarse como demostración en el entorno correspondiente. Antes de una publicación real, deberá sustituirse por información proporcionada y aprobada; no se presentarán mocks como hechos reales.
- Las imágenes deben corresponder a la obra presentada y contar con texto alternativo útil. El texto alternativo vacío se reservará para imágenes decorativas.

## Requisito de organización y coherencia de datos

- `data/artist.json` es únicamente un archivo editable para organizar y consultar el contenido ficticio; no se cargará ni procesará desde la web.
- La página se implementará exclusivamente con HTML5 y CSS3. No se usarán JavaScript, `fetch()`, Flask, frameworks, bibliotecas externas ni herramientas de generación.
- Al editar los datos de referencia, se actualizará manualmente el contenido correspondiente de `index.html`; ambos deben permanecer coherentes.

## Estructura de `data/artist.json`

- `contentStatus` (string, requerido): valor fijo `fictional-demo` para identificar el contenido ficticio.
- `artist` (objeto, requerido): `name`, `profession`, `tagline`, `biography` y `location` (strings); `portrait` (objeto con `visualKey` y `alt` strings, y `src` opcional solo si se proporciona una imagen local aprobada).
- `works` (array, requerido): cada elemento contiene `title`, `category`, `medium`, `year` (number), `description` (strings) e `image` (objeto con `visualKey` y `alt` strings, y `src` opcional solo si se proporciona una imagen local aprobada).
- `presentations` (array, requerido): cada elemento contiene `title`, `date`, `venue`, `location` y `description` (strings ficticios).
- `contact` (objeto, requerido): `email` (string de demostración) y `socialProfiles` (array de objetos con `network`, `label` y `url` strings de demostración).
- Los textos alternativos describen las imágenes representadas. No se usarán direcciones reales ni datos de contacto de personas reales.
- La estructura sirve para organizar y revisar el contenido, no para generar la página. El HTML visible debe actualizarse manualmente junto con el JSON.

## Contenido ficticio de referencia

Todo el contenido de esta sección es ficticio y solo sirve para la demostración. La página debe mostrar un aviso visible de que el perfil, las obras y los eventos son de muestra.

- Perfil: «Álex Vega», «Ilustrador»; frase: «Pequeñas historias para mirar la ciudad de otra manera.»; biografía: «Ilustrador ficticio especializado en narrativa visual, portadas editoriales y campañas ilustradas. Su trabajo de muestra combina formas orgánicas y escenas urbanas.»; ubicación: «Valencia (ficticia)»; clave visual del retrato: `portrait-lines`; alternativa: «Retrato ilustrado de un personaje ficticio, compuesto por formas vegetales y geométricas.»
- Obra 1: «Jardín de paso»; categoría: ilustración editorial; técnica: tinta digital y color plano; año: 2025; descripción: «Una escena ficticia sobre pequeños espacios verdes entre edificios.»; clave visual: `garden-passage`; alternativa: «Ilustración ficticia de plantas que crecen entre edificios geométricos.»
- Obra 2: «La ciudad en pausa»; categoría: portada editorial; técnica: grafito y color digital; año: 2024; descripción: «Una portada de muestra que imagina una plaza tranquila al amanecer.»; clave visual: `city-pause`; alternativa: «Plaza urbana ficticia al amanecer, con una figura leyendo.»
- Obra 3: «Pequeños futuros»; categoría: campaña ilustrada; técnica: collage digital y color plano; año: 2026; descripción: «Una campaña ficticia que reúne objetos cotidianos transformados en paisajes.»; clave visual: `small-futures`; alternativa: «Composición ficticia de objetos cotidianos convertidos en un paisaje.»
- Presentación 1: «Formas que cuentan»; fecha: 2026-11-14; lugar: «Espacio Lumen (ficticio)»; ciudad: «Valencia (ficticia)»; descripción: «Encuentro de muestra sobre ilustración narrativa.»
- Presentación 2: «Mundos de bolsillo»; fecha: 2026-12-05; lugar: «Sala Papel (ficticia)»; ciudad: «Madrid (ficticia)»; descripción: «Presentación ficticia de proyectos editoriales e ilustración.»
- Contacto de demostración: `hola@alexvega.example`; perfil: `@alexvega-demo`, URL `https://social.example/alexvega-demo`.
- Los valores `.example` y los nombres de lugares y perfiles son marcadores ficticios; no deben reemplazarse por datos reales sin autorización.

## Recursos visuales de demostración

- No hay imágenes aprobadas del artista o de sus obras en el repositorio. No se utilizará `.vscode/rigo-baby.jpeg`, ya que es un recurso genérico ajeno a la demo.
- Los visuales identificados por `visualKey` se crearán con CSS3, sin imágenes externas, SVG ni bibliotecas.
- Cada visual CSS se expondrá como imagen accesible mediante `role="img"` y `aria-label`, usando el texto alternativo descrito para su `visualKey` en el JSON de referencia.

## Requisitos de diseño y tecnología

- En escritorio, cada sección principal debe ocupar aproximadamente el alto visible de una pantalla, manteniendo todo el contenido legible y sin recortes. La altura podrá crecer si el contenido lo requiere.
- El diseño será adaptable y se planteará primero para pantallas pequeñas. No debe provocar desplazamiento horizontal en móvil.
- Se usará HTML semántico y CSS en un archivo separado; Flexbox será el sistema de organización de elementos.
- No se usarán frameworks, bibliotecas externas ni JavaScript. No se añadirán dependencias ni herramientas de compilación.
- La presentación debe priorizar la obra y la identidad del artista, evitando decoración que distraiga o dificulte la lectura.

## Accesibilidad

- La página tendrá landmarks semánticos y una jerarquía lógica de encabezados.
- Todos los enlaces y controles serán utilizables con teclado, tendrán nombres descriptivos y mostrarán un indicador de foco visible.
- El contraste será suficiente y el color no será el único medio para comunicar información.
- Las imágenes tendrán alternativas textuales adecuadas.
- Si se incluye un formulario, cada campo tendrá una etiqueta explícita y los errores se comunicarán de forma comprensible.
- Se respetará la preferencia de movimiento reducido y se evitarán animaciones innecesarias.

## SEO y GEO

- La página tendrá un título y una descripción precisos y coherentes con el contenido visible.
- Se incluirá una URL canónica cuando exista una URL pública definitiva. Los metadatos sociales, si se añaden, coincidirán con el contenido de la página.
- El contenido usará encabezados descriptivos y lenguaje claro, específico y verificable, sin acumulación artificial de palabras clave.
- El nombre artístico, la profesión, la biografía, la ubicación y los enlaces serán consistentes en todos los elementos visibles y metadatos; en la demostración se identificarán como ficticios.
- El contenido mock no debe indexarse ni divulgarse como identidad, trayectoria o contacto reales. Para publicar el sitio, primero se reemplazarán los datos ficticios con información aprobada.
- Las secciones y contenidos importantes serán accesibles mediante enlaces HTML normales.

## Datos estructurados

- Se implementarán datos estructurados con vocabulario de Schema.org, mediante JSON-LD o Microdata.
- Se podrán usar tipos adecuados al contenido, como `Person`, `VisualArtwork` o `WebSite`, con propiedades que coincidan con el contenido visible en HTML y el JSON de referencia.
- Los datos estructurados deben coincidir con el contenido visible. En la demostración, reflejarán únicamente los datos ficticios presentes en la página y no se expondrán como información real para indexación pública.
- JSON-LD se tratará como datos estructurados y no se añadirá JavaScript ejecutable.

## Criterios de aceptación

- [ ] La página presenta las cinco áreas de contenido definidas y la navegación muestra los cuatro enlaces solicitados.
- [ ] Cada enlace de navegación apunta a una sección existente con identificador único; la navegación funciona con teclado.
- [ ] En escritorio, las secciones principales se aproximan al alto de la ventana sin ocultar texto, imágenes ni controles; en móvil, el contenido se adapta sin desbordamiento horizontal.
- [ ] La portada comunica el nombre «Álex Vega», la profesión de ilustrador, una imagen con alternativa textual y una frase de presentación.
- [ ] La biografía, la trayectoria, las presentaciones y el contacto se generan a partir de datos ficticios identificados como contenido de demostración.
- [ ] La trayectoria presenta los trabajos disponibles con el contexto que se conozca para cada uno.
- [ ] Las presentaciones y sus fechas/lugares de muestra proceden del JSON y se identifican como ficticios; no se interpretan como eventos reales.
- [ ] Existe `data/artist.json` con los campos de referencia para perfil, obras, presentaciones y contacto.
- [ ] El contenido visible está escrito directamente en `index.html` y coincide con el JSON de referencia.
- [ ] Al cambiar contenido, el JSON y el HTML se actualizan manualmente; la web no carga ni procesa el JSON.
- [ ] Los datos ficticios se identifican como demostración y no se indexan ni se presentan como información real.
- [ ] El HTML usa landmarks semánticos y encabezados con jerarquía lógica; el foco es visible, el contraste es suficiente y el contenido puede recorrerse con teclado.
- [ ] Las imágenes informativas tienen texto alternativo útil y las decorativas no generan descripciones redundantes.
- [ ] Se usan HTML5 y CSS3 con Flexbox y CSS separado, sin JavaScript, `fetch()`, Flask, frameworks, bibliotecas externas ni herramientas de generación o compilación.
- [ ] El título, la descripción y los metadatos opcionales representan fielmente la página; la URL canónica solo se establece si se conoce la URL definitiva.
- [ ] Los datos estructurados de Schema.org son válidos y coinciden con los datos JSON visibles en la demostración; no se exponen como datos reales para indexación.
- [ ] Antes de publicar como web real, los datos ficticios se reemplazan y se revisan los metadatos, el SEO/GEO y los datos estructurados para usar solo información aprobada.
- [ ] La validación del HTML y la revisión de accesibilidad, metadatos y datos estructurados se ejecutan antes de declarar la página terminada; no se reportan verificaciones que no se hayan realizado.