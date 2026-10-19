
## Objetivo

Transformar el proyecto existente de landing en el portfolio artístico de Mónica Gómez, nombre artístico molicgv.art, sin empezar desde cero y manteniendo las restricciones de 4Geeks.

## Archivos autorizados

- `AGENTS.md`: reglas permanentes para identidad real, HTML/CSS, accesibilidad, SEO y Microdata.
- `specs/001-landing-artist/spec.md`: requisitos, contenido confirmado, recursos y criterios de aceptación.
- `specs/001-landing-artist/plan.md`: este plan de implementación.
- `specs/001-landing-artist/tasks.md`: tareas en orden y su estado.
- `data/artist.json`: referencia opcional, no fuente de verdad ni dependencia funcional; no se modifica ni se carga desde la web en esta implementación.
- `index.html`: contenido visible, navegación, fotografías, metadatos y Microdata.
- `styles.css`: identidad «Galería marina», composición, responsive, foco y movimiento reducido.

No modificar `assets/images/*`, `server.py`, `README*` ni otros archivos. No hacer commits ni pushes.

## Fases

1. **Documentación SDD:** adaptar AGENTS, spec, plan y tasks a la identidad real, los datos confirmados, la distribución de fotos y las políticas de indexación.
2. **Contenido:** usar `index.html` como única fuente funcional. La actualización futura de `data/artist.json` es opcional, manual y no bloqueante; el sitio nunca lo carga ni lo procesa.
3. **HTML:** sustituir la identidad de la demo anterior por el portfolio en `index.html`: skip link, navegación por anclas, hero con `portada.jpeg`, Sobre mí con `MG.jpg`, galería con el tríptico y `playa.jpeg`, proceso con `textura-detalle_2.jpg`, mensaje de eventos y footer con enlaces de contacto.
4. **Microdata y SEO:** marcar solo datos reales y visibles con Microdata Schema.org. Actualizar title y description; no añadir canonical y conservar el `noindex` actual hasta autorización expresa.
5. **CSS:** implementar la paleta marina en variables `:root`, tipografía local, galería responsive, imágenes sin distorsión, espaciado editorial, hovers discretos, foco visible y `prefers-reduced-motion`.
6. **Validación:** comprobar que el HTML es autocontenido, enlaces, rutas y carga de imágenes WebP/JPEG, estructura y Microdata, navegación por teclado, contraste y responsive en tamaños móvil, tablet y escritorio. No comparar ni cargar el JSON. No instalar dependencias; usar `server.py` solo si ya puede arrancar, sin convertirlo en dependencia.

## Datos y límites

- Confirmados: marca molicgv.art; artista Mónica Gómez; pintura acrílica texturizada; inspiración marina; perfiles de Instagram, TikTok y correo indicados en la especificación.
- No inventar títulos, fechas, dimensiones de obras, ubicación, historial profesional, premios, exposiciones, clientes, ventas ni colaboraciones.
- Presentaciones: ninguna programada. RUST: en desarrollo, sin foto ni más detalles.
- Fotografías y dimensiones: `portada.jpeg` 1512×1512; `MG.jpg` 1000×1000; `triptico-marino.jpg` 3090×2091; `playa.jpeg` 900×697; `textura-detalle_2.jpg` 511×561.
- `molicgv.art` es el nombre artístico; el registro del dominio no está confirmado. No afirmar que el dominio está publicado.

## Criterio de cierre

La página muestra exclusivamente contenido aprobado, las cinco fotos tienen WebP y JPEG fallback desde sus rutas relativas, la presentación es responsive y accesible, los metadatos no inventan dominio y la política `noindex` se conserva. No se incorporan JavaScript, frameworks, dependencias ni herramientas de generación.

## Estado de cierre

- Implementado: diez derivados WebP responsive, `<picture>`/`srcset`/`sizes`, JPEG fallback, prioridad de carga del hero y lazy loading bajo el contenido inicial.
- Implementado: Microdata con `knowsAbout` para la especialidad y sin `jobTitle` ni `artform` oculto.
- Verificado automáticamente: decodificación de variantes, dimensiones/proporciones, rutas, anclas internas, JPEG fallbacks, `alt`, dimensiones HTML, un H1, Microdata básico, `noindex` y ausencia de JavaScript/canonical.
- Hallazgo pendiente: `Person.name` toma el texto completo «Hola, soy Mónica Gómez.»; corregirlo a «Mónica Gómez» requiere una modificación HTML posterior.
- Pendiente de revisión manual: recorrido con teclado/lector de pantalla, inspección visual en móvil/tablet/escritorio y respuesta HTTP de los enlaces externos. La vista previa se abrió localmente, pero no se generaron capturas de viewport.
