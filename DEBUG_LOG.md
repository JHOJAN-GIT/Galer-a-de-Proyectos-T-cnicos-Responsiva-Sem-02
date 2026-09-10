# Bitácora de depuración y validación

**Proyecto:** Galería de Proyectos Técnicos Responsiva  
**Equipo:** Completar con los integrantes del grupo  
**Fecha:** Completar en clase

## Validación pendiente en el laboratorio

Ejecutar las siguientes comprobaciones con la versión final publicada localmente:

1. W3C Validator: pegar la URL de Live Server o subir `index.html`.
2. WAVE: revisar estructura, contraste y textos alternativos.
3. Lighthouse (Chrome DevTools): generar informe para escritorio y móvil.
4. Can I Use: verificar `container-type: inline-size` para el navegador de prueba.

Guardar en el repositorio las capturas antes y después de cada corrección. Esta bitácora incluye ejemplos del formato que se debe completar tras la validación real.

## Registro de errores y correcciones manuales

| Nº | Hallazgo en la validación | Corrección manual aplicada | Resultado por verificar |
|---|---|---|---|
| 1 | El contenido principal no tenía un mecanismo para saltar la navegación con teclado. | Se añadió un enlace visible al recibir foco, dirigido a `#contenido`, y se comprobó el orden con la tecla Tab. | WAVE sin error de navegación repetitiva. |
| 2 | El foco de enlaces no se distinguía con suficiente claridad del fondo. | Se definió `:focus-visible` con contorno de alto contraste y separación respecto al elemento. | Navegación por teclado visible en modo claro y oscuro. |
| 3 | Las tarjetas podían perder su distribución al reducirse el contenedor, aunque la pantalla fuera ancha. | Se declaró el contenedor de consultas en la sección y se añadió un fallback mediante media query para una columna. | Diseño legible al reducir el panel y en móvil. |

## Compatibilidad y fallback

`@container` se usa para que las tarjetas respondan al ancho del componente. Cuando el navegador no lo soporte, la media query `@media (max-width: 42rem)` mantiene una sola columna en pantallas pequeñas. En navegadores compatibles, la consulta de contenedor mejora el comportamiento dentro de paneles estrechos.

## Uso de IA y revisión humana

El grupo debe describir aquí, con sus propias palabras, cualquier consulta permitida y la corrección manual realizada. No copiar una respuesta automática. Revisar línea por línea el HTML y CSS antes de la entrega y reemplazar el contenido de ejemplo de esta bitácora por el resultado de las validaciones reales.

## Evidencias requeridas

- [ ] Captura de Lighthouse antes de corregir.
- [ ] Captura de Lighthouse después de corregir (Accesibilidad y SEO: 90 o más).
- [ ] Captura de WAVE antes de corregir.
- [ ] Captura de WAVE después de corregir (sin errores ni contrastes fallidos).
- [ ] Resultado de W3C Validator sin errores.
