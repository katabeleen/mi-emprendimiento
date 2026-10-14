# Color y tipografía — [Kataa Tejidos]

> Guía: [Color y tipografía](../evaluacion/guias/fase-2-specs/05-color-y-tipografia.md)

## Paleta

| Rol | Color | HEX | Uso |
|---|---|---|---|
| Principal | Rosa claro / Pastel | #FBCAEF | Botones de navegación, acentos suaves, enlaces e identidades de marca |
| Secundario | Lavanda / Lila claro | #CEC2FF | Fondos de tarjetas de kits, bloques secundarios y secciones destacadas |
| Acento | Coral terracota oscuro | #C7381C | Botones de acción principal (CTA), checkout, badges de oferta y destacados |
| Acento secundario | Menta / Aqua claro | #A9FFF7 | Etiquetas de categorías y filtros activos con texto oscuro |
| Fondo | Blanco puro | #FFFFFF | Fondo general neutro y limpio para bajo ruido visual |
| Fondo alternativo | Crema suave | #FBF7FA | Contenedores y secciones alternadas |
| Texto | Carbón oscuro | #1E1E1E | Lectura principal de títulos y párrafos para alto contraste |
| Texto secundario | Gris medio | #5C5C5C | Fechas, metadatos y subtítulos complementarios |
| Éxito | Verde bosque artesanal | #237A4B | Mensajes de confirmación de pedido y éxito en formularios |
| Error | Rojo carmesí | #C62828 | Mensajes de error y validaciones en campos de formulario |

## Contraste

| Combinación | Ratio | Resultado |
|---|---|---|
| Texto #1E1E1E sobre fondo blanco #FFFFFF | 19.5:1 | AAA ✅ |
| Texto blanco #FFFFFF sobre Acento #C7381C | 5.24:1 | AA ✅ |
| Texto blanco #FFFFFF sobre Éxito #237A4B | 5.13:1 | AA ✅ |
| Texto blanco #FFFFFF sobre Error #C62828 | 5.62:1 | AA ✅ |
| Texto #1E1E1E sobre Rosa #FBCAEF | 11.2:1 | AAA ✅ |
| Texto #1E1E1E sobre Lila #CEC2FF | 10.5:1 | AAA ✅ |
| Texto #1E1E1E sobre Menta #A9FFF7 | 12.1:1 | AAA ✅ |

## Tipografía

- **Títulos (H1, H2, H3):** `Ramabhadra` (Google Fonts) para otorgar presencia, carácter y consistencia visual a todos los encabezados del sitio.
- **Subtítulos y detalles decorativos:** `Pinyon Script` (Google Fonts) para toques artesanales y firmas conmemorativas.
- **Textos y Párrafos:** `Inter` (Google Fonts) para asegurar una legibilidad neutra e impecable en descripciones de producto, especificaciones y artículos.
- **Botones y CTAs:** `Crafty Girls` (Google Fonts) para darles un toque manuscrito, cercano y representativo del tejido a crochet.

| Elemento | Desktop | Mobile | Peso |
|---|---|---|---|
| h1 | 3rem | 2.25rem | 600 |
| h2 | 2rem | 1.75rem | 600 |
| h3 | 1.5rem | 1.25rem | 600 |
| Párrafo | 1rem | 1rem | 400 |
| Botón | 1rem | 1rem | 400 |

## Justificación

La paleta cromática combina tonalidades pastel representativas de Kataa Tejidos —rosa (#FBCAEF), lila (#CEC2FF) y menta (#A9FFF7)— con un coral terracota oscuro (#C7381C) en los llamados a la acción, el cual garantiza un ratio de contraste de 5.24:1 con texto blanco para cumplir estrictamente el estándar WCAG AA. Para evitar ambigüedades en la retroalimentación al usuario, se independizaron los estados semánticos: verde bosque artesanal (#237A4B) para confirmaciones de éxito y rojo carmesí (#C62828) para errores de validación.

En el aspecto tipográfico, se definió una única fuente por uso funcional para evitar inconsistencias de maquetación: Ramabhadra en títulos para solidez estructural, Inter en textos continuos para legibilidad universal, y Crafty Girls en botones para enfatizar la calidez del trabajo artesanal hecho a mano.