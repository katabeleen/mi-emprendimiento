# Arquitectura de la información — [Nombre del emprendimiento]

> Guía: [Arquitectura de la información](../evaluacion/guias/fase-1-requerimientos/05-arquitectura.md)

## Mapa de sitio

<!-- Incluye landing, blog, tienda y las páginas obligatorias:
contacto, preguntas frecuentes, términos, privacidad y 404. -->

```text
INICIO / LANDING
│
├── TIENDA
│   ├── Amigurumis personalizados
│   ├── Amigurumis disponibles
│   └── Patrones digitales
│
├── BLOG
│   ├── Crochet
│   ├── Amigurumis
│   └── Ideas para regalar
│
├── CONTACTO
├── PREGUNTAS FRECUENTES
├── TÉRMINOS Y CONDICIONES
├── POLÍTICA DE PRIVACIDAD
└── 404 – Página no encontrada
```

## User flows

> Guía: [User flow](../evaluacion/guias/fase-1-requerimientos/06-user-flow.md)

### Flujo 1: Compra de un amigurumi personalizado (Tamara - Proto-persona principal)

1. **Página de Inicio:** El usuario ingresa al sitio web, conoce la marca y hace clic en el botón principal *"Ver catálogo"* o *"Encargar"*.
2. **Tienda:** Navega entre los productos, aplica filtros por categoría o temática y selecciona la opción de *"Amigurumi personalizado"*.
3. **Detalle del producto:** Revisa la galería de fotos, el precio base y la descripción de los materiales.
4. **Personalización:** Selecciona las opciones de personalización (tamaño, colores, accesorios) y hace clic en *"Solicitar cotización"*.
5. **Formulario de solicitud:** Completa sus datos de contacto y adjunta referencias del pedido deseado.
6. **Confirmación:** Envía la solicitud y recibe un mensaje en pantalla confirmando la recepción y el tiempo estimado de respuesta.

### Flujo 2: Lectura de contenido y navegación a la tienda (Ignacia - Proto-persona secundaria)

1. **Página de Inicio:** El usuario accede al sitio y hace clic en la sección *"Blog"* desde el menú principal.
2. **Blog:** Explora las categorías del blog y selecciona una entrada sobre *"Cuidados y consejos"* o *"Ideas para regalar"*.
3. **Artículo del blog:** Lee la publicación e interactúa con el contenido (revisa recomendaciones o guías técnicas).
4. **Producto relacionado:** Hace clic en el enlace al *"Producto relacionado"* o banner sugerido al final del artículo.
5. **Tienda:** Accede a la vista del producto/patrón relacionado para revisar sus detalles técnicos o realizar una compra.

## Categorías

> Guía: [Categorías de productos y temas del blog](../evaluacion/guias/fase-1-requerimientos/07-categorias.md)

### Categorías de productos

| Categoría | Productos |
| --- | --- |
| Amigurumis personalizados | Tamaños de amigurumis, parejas, personalizados, personas a crochet |
| Disponibles | Amigurumis con disponibilidad inmediata ya realizados, como personajes conocidos, muñecas, etc. |
| Ocasiones especiales | Amigurumis para cumpleaños, de personajes, películas, animados, parejas, profesionales, graduados |
| Festividades | Amigurumis navideños |
| Patrones de pago | Patrones digitales (PDF) |

### Categorías del blog

| Categoría | Idea de artículo | Necesidad o motivación de la proto-persona | Producto relacionado |
| --- | --- | --- | --- |
| Ideas para regalar | 5 ideas de regalos personalizados para sorprender a alguien especial | Tamara busca un regalo original y con significado | Amigurumis personalizados |
| Amigurumis personalizados | ¿Cómo puedo personalizar un amigurumi? | Necesita conocer qué elementos puede personalizar antes de realizar su pedido y quiere asegurarse de que el resultado se adapte a lo que busca | Amigurumis personalizados |
| Cuidados y consejos | Cómo cuidar tu amigurumi para que dure más tiempo | Quiere conservar un producto hecho a mano en buen estado y que su compra tenga una buena duración | Amigurumis |