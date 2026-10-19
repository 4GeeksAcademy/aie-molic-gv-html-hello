
# Tareas: portfolio molicgv.art

## Documentación SDD

- [x] 01. Revisar reglas 4Geeks, documentos existentes, archivos HTML/CSS, JSON y fotografías.
- [x] 02. Actualizar `AGENTS.md` para la identidad real, el uso de imágenes, tecnologías, accesibilidad, SEO y Microdata.
- [x] 03. Actualizar `spec.md` con contenido confirmado, asignación de fotografías, límites y criterios de aceptación.
- [x] 04. Actualizar `plan.md` y ordenar estas tareas antes de implementar.

## Implementación

- [x] 05. Conservar `data/artist.json` intacto; actualizarlo como referencia es opcional y no bloquea la web.
- [x] 06. Reemplazar en `index.html` la identidad por molicgv.art; añadir skip link, landmarks, un H1 y navegación por anclas.
- [x] 07. Construir el hero con `assets/images/portada.jpeg`, copy aprobado, alt y dimensiones intrínsecas.
- [x] 08. Construir Sobre mí con `assets/images/MG.jpg` y la presentación aprobada.
- [x] 09. Presentar `triptico-marino.jpg` y `playa.jpeg` en la galería y `textura-detalle_2.jpg` en proceso creativo, sin inventar títulos, fechas ni dimensiones.
- [x] 10. Mostrar RUST únicamente como proyecto en desarrollo, sin imagen ni afirmaciones añadidas.
- [x] 11. Mostrar que no hay exposiciones programadas y enlazar el Instagram confirmado.
- [x] 12. Añadir al footer los enlaces accesibles de Instagram, TikTok y correo con `mailto:`.
- [x] 13. Añadir Microdata Schema.org para datos reales y visibles; actualizar title y description, conservar `noindex` y omitir canonical.
- [x] 14. Sustituir la estética de demo en `styles.css` por «Galería marina», variables CSS, galería responsive, foco, hovers discretos y movimiento reducido.

## Validación

- [x] 15. Confirmar que todo contenido visible reside en `index.html` y que no se carga ni procesa JSON.
- [x] 16. Comprobar anclas internas y que los enlaces externos y `mailto:` coinciden con las direcciones confirmadas; no se comprobó su respuesta HTTP.
- [x] 17. Verificar las rutas, existencia, formato, dimensiones, alt y relación de aspecto de las cinco fotos y derivados, sin modificar originales.
- [x] 18. Revisar semántica, jerarquía de encabezados, skip link, foco declarado, contraste calculado y Microdata; se detectó que `Person.name` contiene el saludo completo.
- [ ] 19. Revisar visualmente el responsive en móvil, tablet y escritorio; no se generaron capturas de viewport.
- [x] 20. Confirmar que no hay JavaScript/frameworks, que el JSON no se carga, que `noindex` permanece y que no hay canonical.
- [ ] 21. Recorrer manualmente la página con teclado y lector de pantalla.
- [ ] 22. Comprobar desde un navegador que Instagram y TikTok responden y que `mailto:` abre el cliente de correo.
- [ ] 23. Corregir y validar `Person.name` para que el valor estructurado sea «Mónica Gómez», no «Hola, soy Mónica Gómez.»; requiere ajuste de HTML.
