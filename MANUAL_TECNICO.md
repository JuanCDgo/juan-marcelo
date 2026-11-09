# Manual Técnico · Portafolio y Plataforma Web de Juan Marcelo

> **Arquitectura, Sistema de Diseño Impeccable y Guía de Mantenimiento**  
> Desarrollado bajo las directivas del archivo maestro `GEMINI.md` y auditado con el motor determinista de `impeccable.style`.

---

## 1. Arquitectura General y Stack

El proyecto fue diseñado bajo el principio de **cero dependencias pesadas, carga instantánea y máxima resiliencia**:

- **Motor Frontend:** HTML5 semántico + Vanilla JavaScript (ES6+).
- **Estilos y Utilidades:** Tailwind CSS (CDN configurado con temas personalizados) + CSS nativo para jerarquía tipográfica estricta y variables de tema.
- **Tipografía Oficial:** `Figtree` (Google Fonts, pesos 400 a 800) para texto e interfaz + `JetBrains Mono` con `tabular-nums` para cifras monetarias y de inventario. Cumple con la directiva anti-slop de Impeccable (superando fuentes sobreexplotadas como Inter o Plus Jakarta Sans).
- **Diseño Responsivo:** Enfoque mobile-first, testeado en viewports de 360px a 1920px.
- **Compatibilidad de Despliegue:** 100% estático, listo para GitHub Pages (`JuanCDgo`) y funcionamiento como PWA instalable.

---

## 2. Integración y Certificación con Impeccable

El proyecto incluye las herramientas de calidad de **Impeccable** (`impeccable.style`, por Paul Bakaus):

- **Archivos de Autoridad:**
  - `PRODUCT.md`: Define el propósito del software, usuarios, audiencia y restricciones.
  - `DESIGN.md`: Especifica la escala cromática, la rampa tipográfica y las prohibiciones de diseño ("Anti-Slop").
- **Auditoría Determinista:**
  Se ejecuta en cualquier momento mediante:
  ```bash
  npx impeccable detect index.html
  ```
  *Estado actual:* **0 anti-patterns (Aprobación limpia con código de salida 0).**

---

## 3. Estructura de Componentes

| Sección | Elemento ID | Función |
| :--- | :--- | :--- |
| **Header** | `<header>` | Navegación rápida, logo personal `JM`, botón de alternancia Dark/Light y CTA de WhatsApp. |
| **Hero** | `<section>` | Titular aprobado, subtítulo, 3 pilares de resiliencia y simulador interactivo de cobro en mostrador. |
| **Sistema Unificado** | `#sistema-unificado` | Sección central con los 4 pilares operativos del SGU y accesos a la demo en vivo. |
| **Mini Apps Destacadas** | `#mini-apps` | Cuadrícula 2x2 con Mini CRM Preventa, Club de Fidelidad, Peluquería & Color y Bebidas. |
| **Catálogo Expandible** | `#moreAppsContainer` | Acordeón con 8 aplicaciones de nicho adicionales (Rotisería, Barbería, Gomería, Mascotas, etc.). |
| **Cómo Trabajo** | `#filosofia` | Comparativa honesta frente al software corporativo tradicional. |
| **Modal de Demo** | `#demoModal` | Visor en iframe a pantalla completa para interactuar con las apps reales sin salir del portal. |

---

## 4. Gestión de Temas (Dark / Light)

El estado del tema se controla mediante JavaScript puro y se persiste en `localStorage` con la clave `'theme'`:
- **Dark Mode (Default):** Fondo `#0B0D13`, contenedores `#131620`, bordes `#222738`, acento `#10B981` (Verde esmeralda).
- **Light Mode:** Fondo `#F8FAFC`, tarjetas `#FFFFFF`, bordes `#E2E8F0`, texto `#0F172A`.

Función de alternancia: `toggleTheme()`.

---

## 5. Cumplimiento Estricto de Reglas GEMINI.md

1. **Cero Rombos en WhatsApp:**
   - Todos los enlaces a WhatsApp utilizan la estructura:
     `https://api.whatsapp.com/send?text=...`
   - **Estrictamente prohibido el uso de caracteres emoji.** Los enlaces usan texto limpio codificado con `encodeURIComponent()`.
2. **Formatos Argentinos:**
   - Precios en pesos argentinos: `ARS $ 5.800,00` (punto para miles, coma para decimales).
   - Reloj de 24 horas y huso horario GMT-3.
3. **UI Limpia y sin redundancias:**
   - Cero cajas anidadas innecesarias ("nested cards").
   - Contrastes verificados con WCAG AA (superior a 4.5:1).
