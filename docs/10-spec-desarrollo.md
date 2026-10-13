# Spec de desarrollo — [Kataa Tejidos]

> Guía: [Spec de desarrollo](../evaluacion/guias/fase-2-specs/07-spec-de-desarrollo.md)

## Insumos y prompt para el asistente

```text
Lee DESIGN.md, docs/09-spec-diseno.md y docs/10-spec-desarrollo.md.
En la carpeta stitch/ está el código exportado de Stitch de cada pantalla.
Construye el sitio siguiendo exactamente docs/10-spec-desarrollo.md:
solo HTML y CSS, la estructura de archivos y la navegación definidas,
las variables de :root con los valores de DESIGN.md y la estructura
semántica de cada página. Usa el código de Stitch solo como referencia
visual. Al terminar, revisa cada criterio de aceptación y dime cuáles
se cumplen y cuáles no.
```

## 1. Estructura de archivos

```text
kataa-tejidos/
├── index.html          ← Landing
├── tienda.html         ← Tienda
├── producto.html       ← Ficha de producto
├── carrito.html        ← Carrito
├── blog.html           ← Blog
├── articulo.html       ← Artículo de blog
├── DESIGN.md           ← Design system (tokens y componentes)
├── css/
│   └── styles.css      ← Estilos globales del sitio
├── img/
│   ├── productos/      ← Imágenes de amigurumis y kits
│   └── blog/           ← Imágenes de tutoriales
├── stitch/             ← Código exportado de Stitch (referencia)
└── docs/               ← Documentación del proyecto
```

## 2. Páginas y navegación

| Desde | Elemento | Lleva a |
|---|---|---|
| index.html | Botón "Explorar Tienda" del Hero | tienda.html |
| tienda.html | Botón "Ver detalles" de cada Product Card | producto.html |
| producto.html | Botón "Agregar al Carrito" | carrito.html |
| producto.html | Botón "Encargo especial por Instagram" | https://www.instagram.com/kataatejidos/ |
| articulo.html | Mini Product Card recomendada | producto.html |
| blog.html | Enlace "Leer artículo" | articulo.html |

## 3. Estructura semántica

### Para todas las páginas principales (Ej: tienda.html)
- `<header>`: Navbar global con logo, enlaces e ícono de carrito.
- `<main>`: Contenido principal de la vista.
- `<section>`: Bloques de contenido, grillas de productos o artículos.
- `<aside>`: Barra lateral de filtros (en la tienda).
- `<article>`: Tarjetas individuales de productos o entradas de blog.
- `<footer>`: Pie de página con enlaces y redes sociales.

## 4. Organización del CSS

```css
:root {
/* Colores */
  --color-primary: #FBCAEF;
  --color-secondary: #CEC2FF;
  --color-accent: #F55D3E;
  --color-accent-mint: #A9FFF7;
  --color-accent-yellow: #FFFD82;
  --color-bg: #FFFFFF;
  --color-cream: #FBF9F7;
  --color-text: #1E1E1E;

  /* Tipografía */
  --font-title: 'Ramabhadra', sans-serif;
  --font-subtitle: 'Pinyon Script', cursive;
  --font-body: 'Inter', 'Plus Jakarta Sans', sans-serif;
  --font-button: 'Crafty Girls', cursive;

  /* Espaciados y Radios */
  --radius-card: 12px;
  --radius-pill: 9999px;
}
```

## 5. Criterios de aceptación

**Navegación**
- [ ] La navbar y el footer están presentes y son idénticos en todas las páginas.
- [ ] Se puede completar el flujo de compra desde la Landing hasta el Carrito.
- [ ] Los enlaces cruzados del blog llevan correctamente a la ficha de producto.

**Funcionalidades**
- [ ] La tienda cuenta con filtros interactivos por categorías.
- [ ] La ficha de producto muestra variantes de color, selector de cantidad y precio en CLP.
- [ ] El carrito desglosa subtítulos, costos de envío y total final.

**Diseño**
- [ ] Todos los colores del sitio se aplican mediante variables CSS desde `:root`.
- [ ] Las fuentes coinciden exactamente con las definidas en el `DESIGN.md`.
- [ ] Los botones principales tienen estados de interacción (hover).

**Responsive**
- [ ] El diseño se adapta perfectamente a dispositivos móviles (375px) sin scroll horizontal.
- [ ] Las grillas de productos se apilan correctamente en una sola columna en mobile.

**Accesibilidad y publicación**
- [ ] Todas las imágenes cuentan con atributos alternativos (`alt`).
- [ ] Cada página utiliza un único título principal (`h1`).
