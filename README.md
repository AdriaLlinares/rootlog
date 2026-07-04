# rootlog — writeups (archivo único)

Todo el sitio está en un solo archivo: `rootlog.html`. No necesita servidor ni
internet. Las librerías (Markdown, resaltado, ZIP y el sanitizador de seguridad)
van dentro del archivo.

```
rootlog/
├── rootlog.html          ← ábrelo con doble clic
└── img/
    ├── team/
    └── year-of-the-rabbit/
```

## Cómo verlo
Doble clic en `rootlog.html`.

## Botón "+" (subir writeups)
Abajo a la derecha. Pulsa y **sube un `.zip`** con tu `.md` y sus imágenes:
detecta título/plataforma/SO/dificultad, lo revisas y se crea al momento.
Lo que subes se guarda **en tu navegador**; para publicarlo en la web, en el
writeup pulsa **"Copiar código para publicar"** y pega el bloque en el archivo.
(El "+" se puede ocultar en la web pública añadiendo `?public` a la URL.)

## Editar y eliminar
Dentro de cada writeup, arriba a la derecha:
- **Editar** (solo en los que subes tú): cambia datos y el Markdown.
- **Eliminar**: los que subes tú se borran; los de fábrica (Team, Year of the
  Rabbit) se ocultan en tu navegador. Para quitar uno de fábrica del sitio
  publicado, borra su bloque `<script type="text/markdown">` del archivo.

## Ampliar imágenes
Clic en cualquier imagen de un writeup para verla grande. Clic fuera o Esc cierra.

## Seguridad (si lo haces público)
- Todo el Markdown pasa por **DOMPurify**: elimina scripts, `onerror`, enlaces
  `javascript:`, etc. No puede ejecutar código en la página.
- Estático = sin servidor ni base de datos que atacar; GitHub sirve por HTTPS.
- El "+" no publica nada para el público: lo que sube un visitante solo queda en
  su propio navegador. Publicar de verdad = hacer commit al repo (solo tú, o
  quien tenga permiso de escritura).
- Riesgo real = el CONTENIDO: no publiques credenciales reales, IPs de sistemas
  ajenos, datos personales ni flags de máquinas activas (HTB/THM lo prohíben).
- Nunca metas un token de escritura de GitHub en el archivo (es público).

## Que otros publiquen (si quieres)
Recomendado con GitHub: **añádelos como colaboradores del repo** y activa
protección de rama + revisión de PR, así nada sale publicado sin tu visto bueno.
No requiere tocar el sitio.

## Subir a GitHub Pages
Sube `rootlog.html` (renómbralo a `index.html` para que sea la home) y la carpeta
`img/`. En *Settings → Pages* activa Pages sobre la rama `main`.

## Personalizar
Nombre/lema en `<h1 class="site-title">` y `.tagline`; colores en `:root`.
