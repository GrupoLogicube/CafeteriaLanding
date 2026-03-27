# Directivas Globales para Desarrollo Web Estático (HTML/CSS)

## 1. Estructura HTML (Semántica y Accesibilidad)
* Usa etiquetas semánticas de HTML5 (<header>, <nav>, <main>, <section>, <article>, <footer>).
* Prohibido el "Div Soup". No uses <div> a menos que sea para agrupación estricta de diseño.
* Accesibilidad: Toda imagen requiere atributo `alt`. Todo botón/icono requiere `aria-label`.

## 2. Metodología CSS
* Utiliza BEM (Block Element Modifier) para nombrar clases (ej. `.card`, `.card__title`, `.card--dark`).
* PROHIBIDO usar `!important`. Resuelve conflictos por especificidad.
* PROHIBIDO usar estilos en línea en el HTML (`style="..."`).

## 3. Diseño Responsivo
* Mobile-First: Escribe el CSS base para móviles. Usa `@media (min-width: ...)` para pantallas grandes.
* Utiliza variables CSS (`:root`) para colores primarios, espaciados y tipografías.

## 4. Animaciones y Micro-interacciones (Librerías Permitidas)
* Regla estricta: No escribas `@keyframes` personalizados a menos que la animación no exista en las librerías base.
* Scroll Animations: Utiliza exclusivamente **AOS (Animate On Scroll)**. 
  - Inyecta su CDN (CSS y JS) en el HTML e inicializa con `AOS.init();`.
  - Aplica clases con el atributo `data-aos`.
* Interacciones de UI: Utiliza **Animate.css**.
  - Inyecta su CDN en el `<head>`.
  - Usa clases como `animate__animated animate__fadeIn`.
