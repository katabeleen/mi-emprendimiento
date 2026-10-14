---
version: alpha
name: "Kataa Tejidos"
description: "Design system para tienda online de amigurumis hechos a mano y patrones digitales en Chile"
colors:
  primary: "#FBCAEF"
  primary-hover: "#F8AEE6"
  on-primary: "#1E1E1E"
  secondary: "#CEC2FF"
  secondary-hover: "#B9A7FF"
  on-secondary: "#1E1E1E"
  tertiary: "#C7381C"
  tertiary-hover: "#A82D16"
  on-tertiary: "#FFFFFF"
  accent-mint: "#A9FFF7"
  on-accent-mint: "#1E1E1E"
  neutral: "#FFFFFF"
  surface: "#FFFFFF"
  surface-variant: "#FBF7FA"
  on-surface: "#1E1E1E"
  on-surface-variant: "#5C5C5C"
  disabled: "#E8E8E8"
  on-disabled: "#8C8C8C"
  success: "#237A4B"
  on-success: "#FFFFFF"
  error: "#C62828"
  on-error: "#FFFFFF"
typography:
  headline-display:
    fontFamily: Ramabhadra
    fontSize: 48px
    fontWeight: 600
    lineHeight: 1.1
  headline-lg:
    fontFamily: Ramabhadra
    fontSize: 32px
    fontWeight: 600
    lineHeight: 1.2
  headline-md:
    fontFamily: Ramabhadra
    fontSize: 24px
    fontWeight: 600
    lineHeight: 1.25
  title-md:
    fontFamily: Ramabhadra
    fontSize: 18px
    fontWeight: 600
    lineHeight: 1.3
  body-md:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.6
  body-sm:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.5
  label-md:
    fontFamily: Crafty Girls
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1
rounded:
  sm: 4px
  md: 8px
  lg: 16px
  full: 9999px
spacing:
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 32px
  2xl: 48px
  3xl: 64px
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.full}"
    padding: 12px 24px
  button-primary-hover:
    backgroundColor: "{colors.primary-hover}"
    textColor: "{colors.on-primary}"
  button-primary-disabled:
    backgroundColor: "{colors.disabled}"
    textColor: "{colors.on-disabled}"
  button-secondary:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.label-md}"
    rounded: "{rounded.full}"
    padding: 12px 24px
  button-secondary-hover:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.on-secondary}"
  button-accent:
    backgroundColor: "{colors.tertiary}"
    textColor: "{colors.on-tertiary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.full}"
    padding: 12px 24px
  button-accent-hover:
    backgroundColor: "{colors.tertiary-hover}"
    textColor: "{colors.on-tertiary}"
  card-product:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    rounded: "{rounded.lg}"
    padding: "{spacing.md}"
  card-kit:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.on-secondary}"
    rounded: "{rounded.lg}"
    padding: "{spacing.md}"
  tag-offer:
    backgroundColor: "{colors.tertiary}"
    textColor: "{colors.on-tertiary}"
    rounded: "{rounded.full}"
  tag-category:
    backgroundColor: "{colors.accent-mint}"
    textColor: "{colors.on-accent-mint}"
    rounded: "{rounded.full}"
  input-field:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    padding: 12px 14px
  message-success:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.success}"
  message-error:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.error}"
  page:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface}"
  text-secondary:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface-variant}"
---

# Kataa Tejidos — Design system

## Overview

Kataa Tejidos es una tienda online chilena de amigurumis hechos a mano con amor y venta de patrones digitales en formato PDF. Su proto-persona principal es **Tamara (24 años)**, quien busca regalos significativos, tiernos y originales sin perder tiempo ni temer por la calidad de confección. Su proto-persona secundaria es **Ignacia (29 años)**, compradora de patrones técnicos con instrucciones claras.

La interfaz transmite una personalidad **tierna, artesanal, cálida, alegre y confiable**, combinando tonos pasteles suaves (rosa, lila, menta) con acentos vibrantes de coral y toques manuales en la tipografía de interacción.

## Colors

- **Primary (#FBCAEF - Rosa Pastel):** Se utiliza en botones de navegación principal, chips de selección y detalles destacados de marca. Texto oscuro `#1E1E1E` (contraste 11.2:1, AAA).
- **Secondary (#CEC2FF - Lila Claro):** Fondos de tarjetas de kits, banners secundarios y bloques de suscripción ("Club de Tejedoras").
- **Tertiary / Accent (#C7381C - Coral Terracota Oscuro):** Llamados a la acción prioritarios (CTA de checkout), badges de oferta destacada y botones de conversión con texto blanco `#FFFFFF` (contraste 5.24:1, supera el estándar WCAG AA de 4.5:1).
- **Accent Mint (#A9FFF7 - Menta / Aqua):** Etiquetas de categorías activas, disponibilidad inmediata y filtros seleccionados con texto `#1E1E1E`.
- **Success (#237A4B - Verde Bosque Artesanal):** Mensajes de confirmación de pedido y éxito en envíos de formularios.
- **Error (#C62828 - Rojo Carmesí):** Alertas de validación y campos incompletos en formularios.
- **Surface & Neutral (#FFFFFF / #FBF7FA):** Fondo general y contenedores de tarjetas para asegurar amplitud visual y alto contraste.
- **On-Surface (#1E1E1E):** Títulos, textos y descripciones para cumplir estándares de accesibilidad WCAG AAA (>10:1 sobre blanco y pasteles).

## Typography

- **Títulos (H1 a H4):** `Ramabhadra` (Google Fonts), tipografía estructurada pero amigable que otorga identidad visual sólida a los encabezados.
- **Textos y Párrafos:** `Inter` (Google Fonts), tipografía limpia y neutral que garantiza lectura óptima de descripciones de productos, especificaciones técnicas y artículos del blog.
- **Botones y CTAs:** `Crafty Girls` (Google Fonts), aporta el toque manuscrito y artesanal representativo del crochet y el trabajo hecho a mano.

### Escala tipográfica
- `headline-display`: 48px / weight 600 (Desktop Hero)
- `headline-lg`: 32px / weight 600 (Títulos de página H1)
- `headline-md`: 24px / weight 600 (Títulos de sección H2)
- `title-md`: 18px / weight 600 (Títulos de tarjetas de producto H3)
- `body-md`: 16px / weight 400 (Párrafos y descripciones)
- `body-sm`: 14px / weight 400 (Metadatos, fechas, notas al pie)

## Layout

- **Ancho máximo:** 1200px centrado con padding lateral de 24px en desktop.
- **Breakpoints:**
  - **Mobile (< 768px):** 1 sola columna vertical (100% de ancho). La navbar se convierte en menú hamburguesa (☰) con logo centrado y carrito. Los filtros de la tienda se colapsan en un botón desplegable y el resumen del carrito se apila siempre debajo de la lista de productos.
  - **Tablet (768px a 1023px):** 2 columnas para tienda (filtros arriba o drawer lateral, grilla de 2 columnas) y ficha de producto.
  - **Desktop (>= 1024px):** Layout completo de 2 columnas en Tienda (filtros laterales fijos de 260px + grilla de 3 columnas de productos), Ficha en 2 columnas y Carrito en 2 columnas (lista de productos 65% + resumen de pago 35%).

## Elevation & Depth

- **Superficie base:** Capa plana sin sombras pesadas, manteniendo la estética ligera y limpia del estilo pastel.
- **Tarjetas y contenedores:** Sombra sutil `0 4px 12px rgba(30, 30, 30, 0.05)` con borde suave `1px solid rgba(206, 194, 255, 0.3)`.
- **Hover:** Elevación ligera a `0 8px 24px rgba(199, 56, 28, 0.12)` y micro-interacción de escala (+2%).

## Shapes

- **Botones principales:** Redondeado completo (`rounded.full: 9999px`) tipo píldora para una sensación suave y amigable al tacto.
- **Tarjetas (`card-product`, `card-kit`):** Borde redondeado suave (`rounded.lg: 16px`).
- **Campos de formulario (`input-field`):** Borde redondeado estándar (`rounded.md: 8px`).

## Components

### Botón principal (`button-primary`)
Fondo `#FBCAEF`, texto `#1E1E1E`, tipografía Crafty Girls y esquinas redondeadas completas. Se utiliza para acciones de avance como "Explorar Tienda" o "Agregar al Carrito".
- **Hover:** `#F8AEE6`.
- **Disabled:** `#E8E8E8` con texto `#8C8C8C`.

### Botón acento (`button-accent`)
Fondo `#C7381C` (coral terracota oscuro) con texto `#FFFFFF`. Reservado para el llamado a la acción final más importante ("Proceder al Pago Seguro"), superando el ratio de contraste WCAG AA (5.24:1).
- **Hover:** `#A82D16`.

### Tarjeta de producto (`card-product`)
Contenedor vertical con imagen cuadrada (aspect ratio 1:1), badge de disponibilidad o categoría, título de producto en `title-md`, selector visual de muestras de color, precio visible en CLP y botón "Ver detalles".
- **Regla:** El precio en CLP siempre debe estar visible sin necesidad de hover o interacción.
- **Regla:** Máximo 2 líneas de texto para el título.

### Ficha de producto (`ficha-producto`)
Estructura de dos columnas con galería de fotos, badges de colección, título, valoración de estrellas, selectores obligatorios de color y tamaño, botón principal "Agregar al Carrito", botón de cotización por WhatsApp y acordeón con tiempos de elaboración (5 a 7 días hábiles) y cuidados.

## Do's and Don'ts

- **Do:** Mostrar siempre los precios en pesos chilenos (CLP) con separador de miles.
- **Do:** Especificar las dimensiones exactas o selector de tamaño en cada ficha de amigurumi para evitar malentendidos.
- **Do:** Apilar el resumen de la orden debajo de los productos en la vista mobile del carrito.
- **Don't:** Usar el coral claro sin oscurecer como fondo de botones con texto blanco (el coral `#C7381C` asegura cumplimiento WCAG AA).
- **Don't:** Usar el mismo color para éxito y error (se utiliza `#237A4B` para éxito y `#C62828` para error).
- **Don't:** Mantener dos columnas paralelas en pantallas de menos de 768px de ancho.
- **Don't:** Publicar patrones digitales sin aclarar el nivel de dificultad técnico (principiante, intermedio o avanzado).
