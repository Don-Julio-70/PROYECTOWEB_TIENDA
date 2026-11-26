# PROYECTOWEB_TIENDA

Repositorio para aprender a hacer páginas web profesionales con la ayuda de Claude.

## DIAMOND LUXURY STORE

Sitio estático (solo HTML y CSS, sin frameworks ni JavaScript) de una tienda multimarca
de ropa, zapatos y accesorios. Está pensado primero para celular.

### Cómo ver el sitio: GitHub Pages

GitHub Pages publica gratis los archivos de este repositorio como una página web con su
propia dirección, que puedes abrir desde cualquier celular o computador.

**Activarlo (una sola vez):**

1. En GitHub, entra al repositorio y abre **Settings** (Configuración).
2. En el menú de la izquierda, entra a **Pages**.
3. En **Build and deployment → Source**, elige **Deploy from a branch**.
4. En **Branch**, elige `main` y la carpeta `/ (root)`. Pulsa **Save**.
5. Espera uno o dos minutos y recarga la página de Settings → Pages. Arriba aparece
   el enlace del sitio.

**Dirección del sitio:**

<https://don-julio-70.github.io/PROYECTOWEB_TIENDA/>

**Ten en cuenta:**

- Pages publica lo que está en la rama `main`. Mientras los cambios estén en un pull
  request sin fusionar, no aparecen en el sitio. Cada vez que algo llega a `main`, GitHub
  vuelve a publicar solo en uno o dos minutos.
- Pages es gratis porque el repositorio es público. Si lo vuelves privado, se necesita
  un plan de pago.
- En Pages, las mayúsculas y minúsculas importan: `Zapatos.html` y `zapatos.html` son
  archivos distintos. Escribe los enlaces exactamente igual que el nombre del archivo.

**Para verlo en tu computador mientras editas:** abre `index.html` con doble clic en el
navegador y recarga (`F5`) cada vez que guardes un cambio.

### Archivos

| Archivo | Qué es |
|---|---|
| `index.html` | Portada: banner, categorías, productos destacados y beneficios |
| `ropa.html` | Categoría Ropa |
| `zapatos.html` | Categoría Zapatos |
| `accesorios.html` | Categoría Accesorios |
| `producto.html` | Ficha de las Zapatillas Aurora con el selector de talla |
| `css/estilos.css` | Todos los estilos, divididos en 11 secciones con un índice al inicio |
| `img/*.svg` | Logo e ilustraciones de relleno. Cámbialas por fotos reales |

### Límites conocidos (es una demo)

- El botón **Agregar al carrito** no guarda nada: hace falta JavaScript o un servidor.
- Solo existe la ficha de las Zapatillas Aurora. Es la única tarjeta de producto que es
  enlace; las demás se activarán cuando tengan su propia ficha.
- La cabecera y el pie de página están copiados en cada página. Si cambias el menú,
  cámbialo en todos los archivos `.html`.
- Las marcas (Nórdika, Casa Ferro, Vellani, Costa Alba, Horalia) son inventadas.
