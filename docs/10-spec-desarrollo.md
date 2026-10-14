# Spec de desarrollo — Kataa Tejidos

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
├── index.html                  ← Landing (Página de inicio)
├── tienda.html                 ← Catálogo general de la tienda
├── producto.html               ← Ficha de detalle de producto
├── carrito.html                ← Carrito de compras y cálculo de despacho
├── blog.html                   ← Blog y tutoriales de tejido
├── articulo.html               ← Artículo individual con venta cruzada
├── contacto.html               ← Formulario de contacto y encargos
├── preguntas-frecuentes.html   ← Preguntas frecuentes (FAQ)
├── terminos.html               ← Términos y condiciones
├── privacidad.html             ← Política de privacidad
├── 404.html                    ← Página de error 404 (no encontrada)
├── DESIGN.md                   ← Design system (tokens y componentes)
├── css/
│   └── styles.css              ← Estilos globales del sitio (variables, layout y componentes)
├── img/
│   ├── productos/              ← Fotografías de amigurumis, kits y patrones
│   └── blog/                   ← Imágenes de tutoriales y guías de tejido
├── stitch/                     ← Código exportado de Stitch (referencia)
└── docs/                       ← Documentación del proyecto
```

---

## 2. Páginas y navegación

### Navegación global (presente en todas las páginas)

- **Navbar superior (`<header>`):**
  - **Logo Kataa Tejidos:** Enlaza a `index.html`.
  - **Inicio:** Enlaza a `index.html`.
  - **Tienda:** Enlaza a `tienda.html`.
  - **Blog:** Enlaza a `blog.html`.
  - **Contacto:** Enlaza a `contacto.html`.
  - **Ícono de Carrito:** Enlaza a `carrito.html` (muestra badge con contador de ítems).
- **Footer (`<footer>`):**
  - **Enlaces rápidos:** Inicio (`index.html`), Tienda Online (`tienda.html`), Blog & Tutoriales (`blog.html`), Contacto (`contacto.html`), Preguntas Frecuentes (`preguntas-frecuentes.html`).
  - **Legal:** Términos y Condiciones (`terminos.html`), Política de Privacidad (`privacidad.html`).
  - **Contacto directo y Redes:** Email directo, WhatsApp y enlaces a Instagram (`@kataatejidos`).

### Tabla completa de navegación

| Desde | Elemento interactivo | Lleva a | Propósito |
|---|---|---|---|
| **Todas las páginas** | Logo "Kataa Tejidos" en Navbar | `index.html` | Retorno al inicio |
| **Todas las páginas** | Menú "Inicio" | `index.html` | Navegación principal |
| **Todas las páginas** | Menú "Tienda" | `tienda.html` | Explorar catálogo de productos |
| **Todas las páginas** | Menú "Blog" | `blog.html` | Leer guías y tutoriales |
| **Todas las páginas** | Menú "Contacto" | `contacto.html` | Formulario de consultas |
| **Todas las páginas** | Ícono / Botón de Carrito | `carrito.html` | Revisar productos agregados |
| **Todas las páginas** | Enlace Footer "Preguntas Frecuentes" | `preguntas-frecuentes.html` | Resolver dudas de envíos y pagos |
| **Todas las páginas** | Enlace Footer "Términos y Condiciones" | `terminos.html` | Información legal de compra |
| **Todas las páginas** | Enlace Footer "Política de Privacidad" | `privacidad.html` | Tratamiento de datos de clientes |
| **index.html** | Botón principal "Explorar Tienda" (Hero) | `tienda.html` | Llevar al usuario a comprar |
| **index.html** | Botón secundario "Cotizar Pedido Especial" (Hero) | `contacto.html` | Solicitud directa de presupuesto |
| **index.html** | Card de Producto en Carrusel Destacados | `producto.html` | Ver detalle de amigurumi destacado |
| **index.html** | Formulario "¿Buscas un amigurumi personalizado?" | `contacto.html` / Envío | Envío de solicitud de encargo |
| **tienda.html** | Filtros de categoría / Disponibilidad | Misma página (filtrado) | Refinar productos en pantalla |
| **tienda.html** | Botón "Ver detalles" en cada Product Card | `producto.html` | Acceder a la ficha del producto |
| **producto.html** | Breadcrumb "Inicio > Tienda" | `tienda.html` | Volver a la categoría anterior |
| **producto.html** | Botón principal "Agregar al Carrito" | `carrito.html` | Añadir producto y avanzar al checkout |
| **producto.html** | Botón secundario "Cotizar por WhatsApp" | `https://wa.me/569XXXXXXXX` | Consulta personalizada directa |
| **producto.html** | Tarjeta de Producto Relacionado | `producto.html` | Explorar producto complementario |
| **carrito.html** | Botón "Seguir comprando" | `tienda.html` | Retornar al catálogo |
| **carrito.html** | Botón "Proceder al Pago Seguro" | Pasarela de Pago | Confirmar orden y pagar |
| **blog.html** | Tarjeta o enlace "Leer artículo" | `articulo.html` | Ingresar a la lectura del tutorial |
| **articulo.html** | Breadcrumb "Inicio > Blog" | `blog.html` | Retornar al listado de artículos |
| **articulo.html** | Mini Product Card en módulo de venta cruzada | `producto.html` | Comprar patrón digital o kit del tutorial |
| **articulo.html** | Botones de compartir en redes sociales | Red social externa / Copiar | Difundir el contenido |
| **404.html** | Botón "Volver al Inicio" | `index.html` | Recuperar navegación tras error |

---

## 3. Estructura semántica de cada página

### 3.1. `index.html` (Landing)

```html
<header>
  <nav class="navbar-global"> <!-- Logo, enlaces, búsqueda y carrito --> </nav>
</header>
<main>
  <section class="hero-banner">
    <h1>Amigurumis y tejidos hechos a mano con amor en Chile</h1>
    <p>Subtítulo de propuesta de valor...</p>
    <div class="hero-actions">
      <a class="btn-primary" href="tienda.html">Explorar Tienda</a>
      <a class="btn-secondary" href="contacto.html">Cotizar Pedido Especial</a>
    </div>
    <figure class="hero-image"> <!-- Imagen destacada del Puerco Real --> </figure>
  </section>
  <section class="beneficios" aria-label="Beneficios de comprar en Kataa Tejidos">
    <!-- 4 columnas: Artesanal, Personalizado, Envíos Chile, Patrones PDF -->
  </section>
  <section class="productos-destacados">
    <h2>Nuestras Creaciones Favoritas</h2>
    <div class="carrusel-cards">
      <article class="card-product"> <!-- Foto, título, precio, enlace --> </article>
    </div>
  </section>
  <section class="cotizacion-destacada">
    <h2>¿Buscas un amigurumi personalizado?</h2>
    <form class="form-cotizacion"> <!-- Inputs: nombre, email, tipo encargo, botón submit --> </form>
  </section>
</main>
<footer class="footer-global"> <!-- Enlaces rápidos, contacto, redes y copyright --> </footer>
```

### 3.2. `tienda.html` (Catálogo)

```html
<header>
  <nav class="navbar-global"></nav>
</header>
<nav class="breadcrumbs" aria-label="Ruta de navegación">
  <ol><li><a href="index.html">Inicio</a></li><li>Tienda</li></ol>
</nav>
<main class="tienda-layout">
  <header class="catalogo-header">
    <h1>Nuestra Tienda</h1>
    <div class="selector-orden"> <!-- Ordenar por: Más populares / Menor precio --> </div>
  </header>
  <aside class="filtros-sidebar" aria-label="Filtros del catálogo">
    <form>
      <fieldset class="filtro-categoria"> <!-- Checkboxes categorías --> </fieldset>
      <fieldset class="filtro-precio"> <!-- Rango slider CLP --> </fieldset>
      <fieldset class="filtro-disponibilidad"> <!-- Inmediata / Encargo --> </fieldset>
      <fieldset class="filtro-nivel"> <!-- Principiante / Intermedio --> </fieldset>
    </form>
  </aside>
  <section class="grilla-productos">
    <article class="card-product"> <!-- 6 productos: foto, título, color, precio CLP, CTA --> </article>
    <nav class="paginacion" aria-label="Paginación de productos">
      <ol> <!-- Botones: [1], [2], [>] --> </ol>
    </nav>
  </section>
  <section class="badges-confianza">
    <!-- Envíos a todo Chile | Pago 100% Seguro | Entrega Inmediata -->
  </section>
</main>
<footer class="footer-global"></footer>
```

### 3.3. `producto.html` (Ficha de producto)

```html
<header>
  <nav class="navbar-global"></nav>
</header>
<nav class="breadcrumbs">
  <ol><li><a href="index.html">Inicio</a></li><li><a href="tienda.html">Tienda</a></li><li>Puerco Real Amigurumi</li></ol>
</nav>
<main class="ficha-producto-layout">
  <section class="producto-principal">
    <figure class="galeria-fotos">
      <img class="foto-principal" src="..." alt="Puerco Real Amigurumi">
      <div class="miniaturas"> <!-- 3 fotos miniatura --> </div>
    </figure>
    <div class="producto-detalles-compra">
      <span class="badge-coleccion">Colección Granja Real</span>
      <h1>Puerco Real Amigurumi</h1>
      <p class="precio">$18.990 CLP</p>
      <form class="form-variantes">
        <fieldset class="selector-color"> <!-- Círculos de color --> </fieldset>
        <fieldset class="selector-tamano"> <!-- Botones: Pequeño, Estándar, Grande --> </fieldset>
        <div class="selector-cantidad"> <!-- Botones - 1 + --> </div>
        <button type="submit" class="btn-primary">Agregar al Carrito</button>
        <a class="btn-whatsapp" href="https://wa.me/569XXXXXXXX">Cotizar por WhatsApp</a>
      </form>
    </div>
  </section>
  <section class="acordeon-informacion">
    <details open><summary>Descripción del producto</summary><p>...</p></details>
    <details><summary>Tiempos de confección y envío</summary><p>...</p></details>
    <details><summary>Cuidados y lavado</summary><p>...</p></details>
  </section>
  <section class="productos-relacionados">
    <h2>Completa tu Colección de Ternura</h2>
    <div class="grilla-relacionados"> <!-- 3 card-product --> </div>
  </section>
</main>
<footer class="footer-global"></footer>
```

### 3.4. `carrito.html` (Carrito de compras)

```html
<header>
  <nav class="navbar-global"></nav>
</header>
<nav class="breadcrumbs">
  <ol><li><a href="index.html">Inicio</a></li><li>Carrito</li></ol>
</nav>
<main class="carrito-layout">
  <h1>Tu Carrito de Compras</h1>
  <section class="lista-items-carrito">
    <table class="tabla-carrito">
      <thead>
        <tr><th>Producto</th><th>Precio</th><th>Cantidad</th><th>Subtotal</th><th></th></tr>
      </thead>
      <tbody>
        <tr> <!-- Fila producto con foto, nombre, precio, control cantidad y botón eliminar --> </tr>
      </tbody>
    </table>
    <div class="bloque-adicionales">
      <form class="form-cupon"> <!-- Input cupón y botón canjear --> </form>
      <form class="form-calculo-envio"> <!-- Selector región/comuna de Chile --> </form>
    </div>
  </section>
  <aside class="resumen-pago-tarjeta">
    <h2>Resumen de la orden</h2>
    <dl class="desglose-costos">
      <dt>Subtotal productos</dt><dd>$30.970 CLP</dd>
      <dt>Costo de envío</dt><dd>$3.990 CLP</dd>
      <dt class="total-destacado">Total a pagar</dt><dd class="total-destacado">$34.960 CLP</dd>
    </dl>
    <a class="btn-accent" href="#">Proceder al Pago Seguro</a>
    <div class="medios-pago-badges"> <!-- Webpay, Transferencia bancaria --> </div>
  </aside>
</main>
<footer class="footer-global"></footer>
```

### 3.5. `blog.html` (Blog & Tutoriales)

```html
<header>
  <nav class="navbar-global"></nav>
</header>
<main class="blog-layout">
  <header class="blog-encabezado">
    <h1>El Blog de Kataa Tejidos</h1>
    <p>Consejos, guías y tutoriales de tejido amigurumi con amor</p>
  </header>
  <section class="articulo-destacado-hero">
    <article class="card-hero-post">
      <span class="badge-tag">Técnica Artesanal</span>
      <h2>El Secreto de la Tensión: Cómo Lograr que tus Amigurumis Queden Perfectos</h2>
      <p>Bajada del artículo...</p>
      <a class="btn-link" href="articulo.html">Leer artículo completo</a>
      <img src="..." alt="Taller de tensión crochet">
    </article>
  </section>
  <section class="grilla-entradas-blog">
    <article class="card-blog-entry"> <!-- 3 tarjetas con imagen, tag, título, extracto y enlace --> </article>
  </section>
  <section class="newsletter-suscripcion">
    <h2>Únete al Club de Tejedoras Kataa</h2>
    <p>Recibe patrones gratuitos y novedades en tu correo</p>
    <form class="form-newsletter"> <!-- Input email y botón suscribirme --> </form>
  </section>
</main>
<footer class="footer-global"></footer>
```

### 3.6. `articulo.html` (Entrada de blog y venta cruzada)

```html
<header>
  <nav class="navbar-global"></nav>
</header>
<nav class="breadcrumbs">
  <ol><li><a href="index.html">Inicio</a></li><li><a href="blog.html">Blog</a></li><li>El Secreto de la Tensión</li></ol>
</nav>
<main class="articulo-layout">
  <article class="articulo-completo">
    <header class="articulo-header">
      <span class="badge-tag">Guías y Consejos</span>
      <h1>El Secreto de la Tensión: Cómo Lograr que tus Amigurumis Queden Perfectos</h1>
      <div class="metadata-autor">
        <span>Por Kataa Tejidos • 12 Oct, 2026 • 5 min de lectura</span>
        <div class="botones-compartir"> <!-- Iconos compartir Instagram, Pinterest, Copiar enlace --> </div>
      </div>
    </header>
    <figure class="cover-articulo">
      <img src="..." alt="Mano tejiendo con ganchillo ergonómico y lana rosa">
      <figcaption>Muestra tejida con punto bajo en X para mayor firmeza</figcaption>
    </figure>
    <div class="contenido-cuerpo">
      <p>Texto introductorio sobre la tensión en amigurumis...</p>
      <section class="callout-consejos"> <!-- Cajas destacadas de agarre y ritmo --> </section>
      <blockquote class="pull-quote">
        <p>"Truco maestro: teje el punto bajo en forma de 'X' (yarn under) en lugar de 'V'..."</p>
      </blockquote>
      <table class="tabla-regla-oro"> <!-- Tabla de grosores de hilo vs número de ganchillo --> </table>
    </div>
    <aside class="modulo-cross-selling" aria-label="Productos recomendados del artículo">
      <h2>¿Quieres poner en práctica esta técnica?</h2>
      <div class="productos-sugeridos">
        <article class="mini-card-product">
          <h3>Patrón Digital Duende Real (PDF)</h3>
          <p>$4.000 CLP</p>
          <a class="btn-secondary" href="producto.html">Ver patrón</a>
        </article>
        <article class="mini-card-product">
          <h3>Kit Iniciación Crochet</h3>
          <p>$12.990 CLP</p>
          <a class="btn-secondary" href="producto.html">Ver kit</a>
        </article>
      </div>
    </aside>
  </article>
</main>
<footer class="footer-global"></footer>
```

### 3.7. Páginas auxiliares (`contacto.html`, `preguntas-frecuentes.html`, `terminos.html`, `privacidad.html`, `404.html`)

```html
<header><nav class="navbar-global"></nav></header>
<main class="pagina-institucional">
  <h1>Título de la página (Ej: Preguntas Frecuentes / Contacto)</h1>
  <section class="contenido-texto-o-formulario">
    <!-- Acordeones de preguntas frecuentes, formulario de cotización personalizada o cláusulas legales -->
  </section>
</main>
<footer class="footer-global"></footer>
```

---

## 4. Organización del CSS

```css
:root {
  /* Colores del Design System (Kataa Tejidos) */
  --color-primary: #FBCAEF;          /* Rosa pastel principal */
  --color-primary-hover: #F8AEE6;
  --color-secondary: #CEC2FF;        /* Lila claro para kits y fondos suaves */
  --color-secondary-hover: #B9A7FF;
  --color-accent: #C7381C;           /* Coral terracota oscuro (contraste AA 5.24:1 sobre blanco) */
  --color-accent-hover: #A82D16;
  --color-accent-mint: #A9FFF7;      /* Menta para badges y tags activos */
  --color-bg: #FFFFFF;               /* Fondo limpio */
  --color-surface-variant: #FBF7FA;  /* Crema suave para bloques alternados */
  --color-text: #1E1E1E;             /* Carbón oscuro de alto contraste */
  --color-text-muted: #5C5C5C;       /* Gris medio para metadatos */
  --color-disabled: #E8E8E8;
  --color-success: #237A4B;          /* Verde bosque artesanal para confirmaciones */
  --color-error: #C62828;            /* Rojo carmesí para validaciones de formulario */

  /* Tipografías únicas por uso funcional */
  --font-title: 'Ramabhadra', sans-serif;
  --font-subtitle: 'Pinyon Script', cursive;
  --font-body: 'Inter', sans-serif;
  --font-button: 'Crafty Girls', cursive;

  /* Escala de espaciados */
  --space-xs: 4px;
  --space-sm: 8px;
  --space-md: 16px;
  --space-lg: 24px;
  --space-xl: 32px;
  --space-2xl: 48px;
  --space-3xl: 64px;

  /* Radios de borde */
  --radius-sm: 4px;
  --radius-md: 8px;
  --radius-card: 16px;
  --radius-pill: 9999px;

  /* Sombras y elevaciones sutiles */
  --shadow-sm: 0 2px 6px rgba(30, 30, 30, 0.04);
  --shadow-card: 0 4px 12px rgba(30, 30, 30, 0.05);
  --shadow-hover: 0 8px 24px rgba(199, 56, 28, 0.12);
}
```

- **Convención de clases:** Nombres en inglés con guiones claros (`.navbar-global`, `.hero-banner`, `.btn-primary`, `.btn-accent`, `.card-product`, `.card-blog-entry`).
- **Breakpoints:**
  - Mobile: hasta `767px` (1 columna vertical, layout 100%, menú hamburguesa).
  - Tablet: de `768px` a `1023px` (2 columnas flexibles).
  - Desktop: desde `1024px` (ancho máximo `1200px` centrado con layout completo).
- **Enfoque de diseño:** Mobile-first con CSS nativo y variables centralizadas.

---

## 5. Criterios de aceptación

**Navegación y flujos**
- [ ] La Navbar y el Footer están presentes, idénticos y completamente funcionales en todas las páginas.
- [ ] El Flujo de Compra de Tamara se completa fluidamente: Landing → Tienda → Ficha de producto → Carrito.
- [ ] El Flujo de Contenido de Ignacia se completa con éxito: Blog → Artículo tutorial → Módulo de venta cruzada → Ficha/Carrito.
- [ ] Todos los enlaces internos y externos apuntan a destinos válidos sin enlaces rotos.

**Funcionalidades**
- [ ] La tienda cuenta con filtros interactivos por categoría, rango de precio, disponibilidad y nivel de patrones.
- [ ] La ficha de producto incluye galería de imágenes, selector de color, selector de tamaño, contador de cantidad y acordeón informativo con tiempos de elaboración.
- [ ] El carrito desglosa claramente subtotal, selector para cálculo de despacho regional y total final en CLP.
- [ ] Los artículos del blog incorporan botones de compartir y bloque de venta cruzada a patrones descargables en PDF.

**Diseño y estilos**
- [ ] Todos los colores y tipografías se consumen desde las variables `:root` definidas en el `DESIGN.md`.
- [ ] Los botones con fondo coral oscuro (`#C7381C`) y texto blanco cumplen con el ratio de contraste WCAG AA (5.24:1).
- [ ] Los estados de éxito (`#237A4B`) y error (`#C62828`) se encuentran claramente diferenciados.
- [ ] Todos los elementos interactivos cuentan con estados de hover visualmente perceptibles.

**Responsive y accesibilidad**
- [ ] El sitio es 100% responsive y no genera scroll horizontal en resoluciones móviles de 375px.
- [ ] Las grillas de productos y tarjetas de resumen se apilan correctamente en una sola columna vertical en mobile.
- [ ] Cada página posee un único elemento `<h1>` con jerarquía de títulos lógica (`<h2>`, `<h3>`).
- [ ] Todas las imágenes poseen atributos `alt` descriptivos y contextuales.
