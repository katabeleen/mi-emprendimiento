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

### Flujo 1: compra

```text
Inicio -> Tienda -> Seleccionar producto -> Ver detalles -> Personalizar -> Solicitar cotización -> Confirmar pedido
```

### Flujo 2: contenido

```text
Inicio -> Blog -> Categoría -> Artículo -> Producto relacionado -> Tienda
```

## Categorías

> Guía: [Categorías de productos y temas del blog](../evaluacion/guias/fase-1-requerimientos/07-categorias.md)

### Categorías de productos

| Categoría | Productos |
| Amigurumis personalizados | Tamaños de amigurumis, parejas, personalizados, personas a crochet |
| Disponibles | Amigurumis con disponibilidad inmediata ya realizados, como personajes conocidos, muñecas, etc |
| Ocasiones especiales | Amigurumis para cumpleaños, de personajes, películas, animados, parejas, profesionales, graduados |
| Festividades | Amigurumis navideños |
| Patrones de pago | Patrones digitales (PDF) |

### Categorías del blog

| Categoría | Idea de artículo | Necesidad o motivación de la proto-persona | Producto relacionado |
| Ideas para regalar | 5 ideas de regalos personalizados para sorprender a alguien especial | Tamara busca un regalo original y con significado | Amigurumis personalizados |
| Amigurumis personalizados | ¿Cómo puedo personalizar un amigurumi? | Necesita conocer qué elementos puede personalizar antes de realizar su pedido y quiere asegurarse de que el resultado se adapte a lo que busca | Amigurumis personalizados |
| Cuidados y consejos | Cómo cuidar tu amigurumi para que dure más tiempo | Quiere conservar un producto hecho a mano en buen estado y que su compra tenga una buena duración | Amigurumis |