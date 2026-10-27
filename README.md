# FoxHeart — Meet & Greet · Micrositio de enlaces

Landing de una pantalla para presentar los enlaces oficiales del Meet & Greet de FoxHeart. Actualización del repositorio público [`foxheartof/vercel-link`](https://github.com/foxheartof/vercel-link), preparada para Vercel y compatible también con GitHub Pages.

## Qué incluye

- Logo original de FoxHeart servido desde su [sitio oficial](https://foxheartof.github.io/assets/logo.png), con respaldo SVG local cuando no esté disponible.
- Encabezado **Meet&Greet**.
- **Ver Información** (principal dorado, con una animación suave de flotación): https://foxheartof.github.io/
- **Comprar** (secundario rosado, con brillo animado): https://mpago.la/1xB6cLS
- **Contactar por Telegram** (secundario): https://t.me/FoxHeart_OF
- Diseño responsive, con buenas prácticas de accesibilidad y opción `prefers-reduced-motion`.
- HTML + CSS estáticos. No se necesitan Node, npm, frameworks, cookies ni claves API.

> Los pagos se realizan exclusivamente en Mercado Pago. Este micrositio no procesa ni almacena datos personales o de pago.

## Subir a GitHub y publicar en Vercel

1. Extrae el ZIP y **sube el contenido de la carpeta** a la raíz de `foxheartof/vercel-link` (o al repositorio que esté conectado a Vercel).
2. Confirma que `index.html`, `styles.css`, `vercel.json` y `assets/` queden en la raíz, sin una carpeta extra envolviéndolos.
3. Vercel desplegará automáticamente si ya está conectado a la rama `main`. En un proyecto nuevo, importa el repositorio y selecciona **Other / No Framework**; no hace falta comando de compilación.
4. Abre la URL de Vercel y prueba los tres enlaces tanto en móvil como en escritorio.

El viejo acceso `/visitar` continúa enviando al sitio oficial mediante una **redirección HTTP 302**. El nuevo botón principal apunta directamente a la URL oficial y funciona también en GitHub Pages. No hay encubrimiento ni diferenciación de destinos por tipo de visitante.

### Publicar también en GitHub Pages (opcional)

Si prefieres actualizar `foxheartof/link`, sube este mismo contenido al repositorio y configura **Settings → Pages → Deploy from a branch → main / (root)**. Los estilos y el favicon usan rutas relativas para funcionar también bajo `/link/`. GitHub Pages no procesa `vercel.json`: la ruta antigua `/visitar` solo estará operativa en Vercel.

## Personalización

| Archivo | Para qué sirve |
| --- | --- |
| `index.html` | Logo, textos, botones, URLs y metadatos. |
| `styles.css` | Colores, composición, tamaños y animaciones CSS. |
| `assets/favicon.svg` | Favicon independiente en rosa y dorado. |
| `assets/logo-fallback.svg` | Respaldo del logo cuando falla la URL oficial. |
| `vercel.json` | Compatibilidad con la ruta `/visitar` en Vercel. |

La paleta reproduce los tonos del sitio oficial: fondo `#120c11`, rosa `#ff7ca9` y dorado `#f0c541`.

### Si quieres alojar también el logo original dentro del repositorio

Descarga el archivo **original** [`https://foxheartof.github.io/assets/logo.png`](https://foxheartof.github.io/assets/logo.png), guárdalo como `assets/logo.png` y cambia en `index.html` el valor de `src` de la imagen a `./assets/logo.png`. La versión entregada **ya funciona sin hacer este paso** porque usa la imagen del dominio oficial y dispone de respaldo local.

## Probar localmente

Puedes abrir `index.html` directamente. Para servirlo con un servidor local (opcional):

```bash
python3 -m http.server 8000
```

Después abre `http://localhost:8000/`.

## Estructura

```text
.
├── .nojekyll
├── index.html
├── styles.css
├── vercel.json
├── README.md
└── assets/
    ├── favicon.svg
    └── logo-fallback.svg
```
