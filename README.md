# 🦊 FoxHeart — micrositio de acceso

Micrositio estático creado para **FoxHeart** con un único propósito: permitir a los visitantes llegar rápidamente a la página oficial, donde pueden encontrar toda la información y las opciones de compra.

**Destino oficial:** https://foxheartof.github.io/

## ¿Qué hace?

La página muestra un solo botón: **«Ver información y comprar boletos»**. Al pulsarlo, el visitante abre la ruta `/visitar` del micrositio, que lo redirige al sitio oficial de FoxHeart mediante una **redirección HTTP 302 estándar** configurada en Vercel.

Este comportamiento es el mismo para todos los visitantes, incluidos los sistemas automatizados. No hay contenido diferenciado, detección de bots ni mecanismos de ocultamiento del destino.

## Características

- Una sola llamada a la acción (CTA), sin menús ni textos adicionales visibles.
- Diseño responsive con la estética oscura y acentos dorados y rosas de FoxHeart.
- HTML y CSS puros; sin frameworks ni JavaScript.
- Sin cookies, seguimiento de usuarios, formularios ni procesamiento de pagos.
- Redirección gestionada por Vercel en `vercel.json`.

## Publicar en Vercel

1. Crea un repositorio nuevo en GitHub y sube los archivos de esta carpeta a la raíz.
2. En [Vercel](https://vercel.com/new), importa ese repositorio.
3. Selecciona **Other** o **No Framework** cuando Vercel solicite un framework (no requiere build).
4. Deja el directorio de salida en su valor predeterminado y haz clic en **Deploy**.
5. Accede a la URL de Vercel y verifica que el botón abra el sitio oficial.

Para cambiar el destino más adelante, actualiza la propiedad `destination` en `vercel.json` y vuelve a desplegar.

## Archivos

```text
.
├── index.html             # Página con un solo botón
├── styles.css             # Estilos responsive
├── vercel.json            # Redirección HTTP 302 desde /visitar
├── assets/
│   └── favicon.svg
└── README.md
```

> **Nota:** Una redirección 302 no impide que Meta u otros sistemas de revisión sigan la URL y analicen el sitio de destino. Revisa las políticas de las plataformas que utilices para promocionarlo.
