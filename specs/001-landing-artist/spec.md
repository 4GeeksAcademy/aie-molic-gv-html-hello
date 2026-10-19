# Especificación: portfolio molicgv.art

## Objetivo

Transformar la landing existente en el portfolio artístico real de molicgv.art, nombre artístico de Mónica Gómez, artista emergente especializada en pintura acrílica texturizada inspirada en el mar, las olas, los paisajes costeros y las texturas naturales.

## Alcance

Una landing page de una sola página con navegación por anclas y estas secciones, en este orden:

1. Inicio: portada con molicgv.art, una frase de marca, texto de presentación y fotografía de una obra real.
2. Sobre mí: presentación personal de Mónica Gómez con su fotografía.
3. Trayectoria: evolución artística, obras reales y proceso creativo, sin afirmar una trayectoria profesional consolidada.
4. Próximas presentaciones: mensaje de que actualmente no hay exposiciones programadas y enlace a Instagram.
5. Footer: marca, especialidad, Instagram, TikTok y correo electrónico.

La navegación incluirá Inicio, Sobre mí, Trayectoria y Próximas presentaciones. Cada enlace llevará a la sección correspondiente mediante un identificador único. El footer podrá incluir un enlace de contacto sin requerir una sección de navegación adicional.

## Requisitos funcionales y de contenido

- La navegación debe permitir llegar directamente a cada sección mediante enlaces HTML normales.
- Usa exclusivamente los datos confirmados en esta especificación y en el contenido proporcionado por la artista.
- No inventes títulos, fechas, dimensiones, premios, exposiciones, estudios, clientes, ventas, colaboraciones, trayectoria ni eventos. No presentes proyectos en desarrollo como terminados.
- Escribe directamente en `index.html` todo el contenido visible; ese HTML es la única fuente funcional de la web.
- `data/artist.json`, si existe, es solo referencia opcional. No se carga ni procesa desde la web, no es la fuente de verdad y su actualización no bloquea la implementación.
- Las fotografías usarán las rutas relativas existentes y sus originales no se modificarán ni sobrescribirán.
- Las imágenes informativas tendrán texto alternativo descriptivo; añade `width` y `height` según las dimensiones confirmadas de los archivos.
- «RUST» puede mencionarse únicamente como obra en desarrollo, sin añadir detalles ni mostrar una imagen inexistente.

## Tecnologías y organización de datos

- La web usa exclusivamente HTML5 y CSS3. No se usan JavaScript, `fetch()`, Flask/Jinja para renderizado, frameworks, bibliotecas externas ni herramientas de generación.
- `server.py` solo puede usarse para previsualizar durante el desarrollo, nunca como dependencia de renderizado.
- Flexbox se usa para composición y navegación; CSS Grid puede usarse para la galería si aporta una distribución clara.
- La web no depende de `data/artist.json`; si se actualiza más adelante, se hará manualmente como referencia, sin alterar la arquitectura ni bloquear el sitio.

## Contenido confirmado del portfolio

- Identidad: marca `molicgv.art`, nombre `Mónica Gómez`, especialidad `Pintura acrílica texturizada` e inspiración en el mar, olas, paisajes costeros y texturas naturales.
- Presentación: «Arte inspirado en el mar, creado a través de la textura.»
- Texto introductorio: «Pintura acrílica, volumen y paisajes marinos que buscan trasladar al lienzo la fuerza y la calma del océano».
- Biografía: «Hola, soy Mónica. Exploro la pintura acrílica texturizada como forma de representar el movimiento del agua, la luz y los paisajes marinos. A través de diferentes materiales y relieves, experimento con las posibilidades de cada lienzo».
- Fotografías y referencias: `portada.jpeg` para hero; `MG.jpg` para Sobre mí; `triptico-marino.jpg` y `playa.jpeg` para obras; `textura-detalle_2.jpg` para proceso creativo.
- Obras: un tríptico marino de tres lienzos y una obra individual inspirada en el mar. No se asignarán títulos, fechas ni dimensiones no confirmadas.
- Proceso: fotografía de detalle de textura y relieves; no inferir técnicas o materiales que no estén confirmados.
- Proyecto: `RUST`, en desarrollo, sin imagen ni detalles adicionales.
- Presentaciones: lista vacía; mensaje visible «Actualmente no hay exposiciones programadas. Mientras tanto, puedes seguir mis nuevas obras y procesos creativos en Instagram».
- Contacto: Instagram `https://www.instagram.com/molicgv.art/?hl=es`, TikTok `https://www.tiktok.com/@molicgv.art` y correo `molicgv.art@gmail.com`.
- No añadir ubicación, títulos, fechas ni dimensiones de obras mientras no se confirmen.

## Fotografías disponibles

- `assets/images/portada.jpeg`: 1512 × 1512, hero.
- `assets/images/MG.jpg`: 1000 × 1000, sección Sobre mí.
- `assets/images/triptico-marino.jpg`: 3090 × 2091, galería.
- `assets/images/playa.jpeg`: 900 × 697, galería.
- `assets/images/textura-detalle_2.jpg`: 511 × 561, proceso creativo.
- Usa `width` y `height` con estas dimensiones, además de `loading="lazy"` para imágenes fuera del hero cuando corresponda. No distorsiones las proporciones.

## Requisitos de diseño y tecnología

- En escritorio, cada sección principal debe ocupar aproximadamente el alto visible de una pantalla, manteniendo todo el contenido legible y sin recortes. La altura podrá crecer si el contenido lo requiere.
- El diseño será adaptable y se planteará primero para pantallas pequeñas. No debe provocar desplazamiento horizontal en móvil.
- Se usará HTML semántico y CSS en un archivo separado; Flexbox y CSS Grid se aplicarán según la composición.
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
- El nombre artístico, el nombre de la artista, la especialidad y los enlaces serán consistentes en todos los elementos visibles y metadatos.
- No se añadirá canonical hasta confirmar el dominio público. Se mantendrá el `noindex` que ya existe en la página; cambiar esa política requiere consultar a la artista.
- Las secciones y contenidos importantes serán accesibles mediante enlaces HTML normales.

## Datos estructurados

- Se implementarán datos estructurados con Microdata HTML, no JSON-LD.
- Se usarán tipos y propiedades adecuados como `Person` y `VisualArtwork` solo para información real y visible.
- Los datos estructurados deben coincidir con el contenido visible y no incluir títulos, fechas, dimensiones ni otras afirmaciones no confirmadas.

## Criterios de aceptación

- [ ] La identidad visible es molicgv.art / Mónica Gómez y no quedan datos ni contenidos de la demo anterior.
- [ ] La navegación tiene Inicio, Sobre mí, Trayectoria y Próximas presentaciones, con anclas válidas.
- [ ] El hero utiliza `portada.jpeg`; Sobre mí utiliza `MG.jpg`; la galería muestra `triptico-marino.jpg` y `playa.jpeg`; el proceso usa `textura-detalle_2.jpg`.
- [ ] Las imágenes usan rutas relativas, alt descriptivo y dimensiones intrínsecas; los originales no se modifican.
- [ ] No se muestran títulos, fechas, dimensiones, credenciales, eventos ni trayectoria profesional no confirmados; RUST aparece únicamente como proyecto en desarrollo sin imagen.
- [ ] Próximas presentaciones indica que no hay exposiciones programadas e incluye el Instagram confirmado.
- [ ] Footer enlaza Instagram, TikTok y correo usando URLs confirmadas y `mailto:`.
- [ ] El diseño usa la paleta «Galería marina», variables CSS, composición responsive, imágenes sin distorsión y movimiento reducido.
- [ ] El HTML tiene un H1, landmarks semánticos, enlace para saltar al contenido, foco visible y navegación por teclado.
- [ ] El título y la descripción son precisos; no se añade canonical y se conserva `noindex` hasta consulta expresa.
- [ ] Microdata Schema.org refleja únicamente información visible y confirmada; no se usa JSON-LD ni JavaScript.
- [ ] HTML, CSS, enlaces, carga de fotos, accesibilidad y diseño responsive se revisan; no se declaran pruebas no ejecutadas.