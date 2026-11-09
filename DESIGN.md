---
name: Juan Marcelo - Soluciones de Software
description: Sistema de diseño para el portafolio y exhibición de software de gestión y mini apps comerciales.
colors:
  dark-bg: "#0B0D13"
  dark-surface: "#131620"
  dark-surface-hover: "#1A1E2C"
  dark-border: "#222738"
  dark-border-hover: "#323A52"
  dark-text-primary: "#F1F4F9"
  dark-text-secondary: "#94A1B8"
  dark-text-muted: "#64748B"
  
  light-bg: "#F8FAFC"
  light-surface: "#FFFFFF"
  light-surface-hover: "#F1F5F9"
  light-border: "#E2E8F0"
  light-border-hover: "#CBD5E1"
  light-text-primary: "#0F172A"
  light-text-secondary: "#475569"
  light-text-muted: "#94A3B8"
  
  accent-green: "#10B981"
  accent-green-dark: "#047857"
  accent-green-darker: "#065F46"
  accent-green-hover: "#059669"
  accent-green-glow: "rgba(16, 185, 129, 0.15)"
  accent-amber: "#F59E0B"
  accent-cyan: "#06B6D4"
typography:
  display:
    fontFamily: "'Figtree', system-ui, -apple-system, sans-serif"
    fontSize: "2.75rem"
    fontWeight: 800
    lineHeight: 1.15
    letterSpacing: "-0.03em"
  h2:
    fontFamily: "'Figtree', system-ui, -apple-system, sans-serif"
    fontSize: "2rem"
    fontWeight: 700
    lineHeight: 1.25
    letterSpacing: "-0.02em"
  h3:
    fontFamily: "'Figtree', system-ui, -apple-system, sans-serif"
    fontSize: "1.35rem"
    fontWeight: 700
    lineHeight: 1.35
  h4:
    fontFamily: "'Figtree', system-ui, -apple-system, sans-serif"
    fontSize: "1.1rem"
    fontWeight: 600
    lineHeight: 1.4
  body:
    fontFamily: "'Figtree', system-ui, -apple-system, sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: "0em"
  kbd:
    fontFamily: "'JetBrains Mono', monospace"
    fontSize: "11px"
    fontWeight: 500
  code:
    fontFamily: "'JetBrains Mono', monospace"
    fontSize: "0.875rem"
    fontWeight: 500
    lineHeight: 1.4
rounded:
  xs: "4px"
  sm: "6px"
  md: "8px"
  lg: "12px"
  xl: "16px"
  full: "9999px"
spacing:
  xs: "4px"
  sm: "8px"
  md: "16px"
  lg: "24px"
  xl: "32px"
  2xl: "48px"
  3xl: "64px"
components:
  button-primary:
    backgroundColor: "{colors.accent-green}"
    textColor: "#FFFFFF"
    rounded: "{rounded.md}"
    padding: "12px 24px"
---

# Design System & Visual Language

## 1. Filosofía Visual (Anti-Slop de Impeccable)

Este sistema de diseño rechaza de forma explícita los clichés del "AI slop" que degradan la percepción de calidad del software:
- **PROHIBIDO:** Fondos de gradiente violeta/azul genéricos.
- **PROHIBIDO:** Tarjetas anidadas dentro de tarjetas ("cards inside cards").
- **PROHIBIDO:** Texto con gradiente arcoíris o brillos exagerados.
- **PROHIBIDO:** Cejas o kickers innecesarios sobre los títulos (los títulos tienen fuerza propia).
- **OBLIGATORIO:** Contraste tipográfico superior a 4.5:1 para texto normal y 3:1 para texto grande.
- **OBLIGATORIO:** Tipografía uniforme con números tabulares (`tabular-nums`) para precios, cantidades y métricas.
- **OBLIGATORIO:** Iconografía vectorial coherente en trazo (1.5px/2px), sin recurrir a emojis decorativos.

## 2. Paleta Cromática y Atmósfera

### Modo Oscuro (Predeterminado - Estilo Linear / Raycast)
- Fondo base: `#0B0D13` (obsidiana profunda, de alta concentración visual).
- Superficies y contenedores: `#131620` con bordes sutiles en `#222738`.
- Estados activos y hover: Borde en `#323A52` y superficie en `#1A1E2C`.
- Color de acento comercial: `#10B981` (Verde esmeralda de precisión y crecimiento).

### Modo Claro (Alternable - Estilo Stripe / Square)
- Fondo base: `#F8FAFC` (gris perla fresco).
- Superficies y tarjetas: `#FFFFFF` con sombras suaves de offset real y bordes `#E2E8F0`.
- Textos: `#0F172A` para títulos (máxima nitidez y legibilidad bajo luz solar o de oficina).

## 3. Escala Tipográfica y Ritmo Vertical

- **Fuente:** `Figtree`, cargada con pesos 400, 500, 600, 700 y 800.
- **Títulos principales:** `tracking-tight` (-0.03em) para dar solidez y presencia ejecutiva.
- **Cuerpo de texto:** Ancho de lectura óptimo (65 a 75 caracteres por línea).
- **Precios y cifras:** Siempre en formato argentino: `ARS $ 15.400,00` con `font-mono` o `tabular-nums` para que los decimales no bailen visualmente.

## 4. Componentes e Interacción

- **Botón Principal:** Verde esmeralda sólido con micro-transición al hover (`scale: 1.01`, oscurecimiento sutil).
- **Botón Secundario:** Borde estructurado con fondo neutro translúcido, manteniendo siempre contraste legible.
- **Botón WhatsApp:** Color verde sobrio con texto de acción claro: *"Consultar por WhatsApp"*, sin emojis decorativos que puedan corromperse en enlaces.
- **Demos Interactivas:** Modal con backdrop blur controlado (`backdrop-blur-md`), accesible por teclado con tecla Escape y cierre visible.
