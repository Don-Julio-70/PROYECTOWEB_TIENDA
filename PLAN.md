# Plan: tienda multimarca estática (HTML + CSS)

> Estado: **aprobado y construido**. Nombre de la tienda: DIAMOND LUXURY STORE.
> Las preguntas 3 y 4 no se respondieron; se usaron las propuestas (Zapatos, zapatillas 36–43, pesos colombianos).
> Único cambio respecto al plan: en celular la cuadrícula muestra 2 productos por fila (no 1), como la mayoría de tiendas en línea.

## Estado actual del repositorio

El repositorio solo tiene un `README.md` de dos líneas, así que empezamos desde cero. No hay nada que reaprovechar ni que pueda entrar en conflicto.

## Tres límites que debes conocer

1. **Sin JavaScript, la página no puede comprar nada.** El selector de talla sí va a funcionar: se puede elegir una talla y se ve cuál está marcada, todo con HTML y CSS. Pero el botón "Agregar al carrito" no va a guardar nada, porque para eso hace falta JavaScript o un servidor. Queda como botón visual y se marca en el código.
2. **Imágenes.** No se usan fotos ni logos de marcas reales: tienen derechos de autor. Se hacen ilustraciones SVG sencillas y propias como relleno, que luego cambias por tus fotos.
3. **"Multimarca".** Se usan nombres de marcas inventados. Con marcas reales, la página parecería que las representa de verdad.

## Plan de archivos

```
PROYECTOWEB_TIENDA/
├── index.html          → Portada
├── categoria.html      → Listado de productos (ej. "Zapatos")
├── producto.html       → Ficha de producto con selector de talla
├── css/
│   └── estilos.css     → Todos los estilos, divididos en secciones comentadas
├── img/
│   ├── logo.svg
│   └── (5-6 ilustraciones SVG de producto: camiseta, zapato, bolso, etc.)
└── README.md           → Cómo abrir el sitio y qué hay en cada archivo
```

**Por qué una sola hoja de estilos y no varias:** para tres páginas, repartir el CSS en `base.css`, `componentes.css`, etc. es organizar de más. Te obliga a saltar entre archivos sin ganar nada. Un solo archivo bien dividido en secciones (variables, reset, cabecera, tarjetas, ficha, pie de página) se aprende y se mantiene mejor. Se divide cuando el proyecto crezca y de verdad haga falta.

## Contenido de cada página

| Página | Secciones |
|---|---|
| **Portada** | Cabecera con logo y menú (Ropa / Zapatos / Accesorios), banner principal, 3 tarjetas de categoría, 4 productos destacados, pie de página |
| **Categoría** | Misma cabecera, ruta de navegación ("Inicio › Zapatos"), título, cuadrícula de productos (1 columna en celular, 2 en tablet, 3-4 en escritorio) |
| **Producto** | Imagen, marca, nombre, precio, selector de talla, botón de compra, descripción y detalles |

## Decisiones técnicas

- **Primero el celular (mobile-first):** el CSS base está pensado para pantallas pequeñas, y con `@media` se agregan los cambios para pantallas grandes.
- **Selector de talla accesible:** `<fieldset>`, `<legend>` y botones de opción (`radio`) con estilo de "botón de talla". Funciona con teclado y con lectores de pantalla. Una talla agotada aparece tachada y no se puede elegir.
- **Menú en celular:** sin JavaScript no hay menú hamburguesa. Hacerlo con trucos de CSS sería frágil y poco accesible. En el celular el menú queda como una fila de 3 enlaces, que caben bien.
- **HTML semántico:** `header`, `nav`, `main`, `article` y `footer` en vez de `div` para todo.
- **Variables CSS** para colores y espacios, para cambiar la paleta en un solo lugar.

## Orden de trabajo

| # | Actividad | Importancia |
|---|---|---|
| 1 | Aprobar este plan y responder las preguntas de abajo | Crítica: sin esto no se empieza |
| 2 | Crear `estilos.css` (variables, reset, cabecera, pie) | Alta: es la base de las 3 páginas |
| 3 | Crear `index.html` | Alta |
| 4 | Crear `categoria.html` y los estilos de la cuadrícula | Alta |
| 5 | Crear `producto.html` y el selector de talla | Alta: es lo más difícil de lo pedido |
| 6 | Crear las ilustraciones SVG | Media: son de relleno |
| 7 | Revisar en tamaño celular y escritorio con capturas de pantalla | Alta: es la prueba de que se ve bien en el celular |
| 8 | Actualizar el README, hacer commit y push a `claude/fervent-davinci-71v625` | Media |
| 9 | Explicar cada archivo | Alta: es el objetivo de aprendizaje |

## Preguntas pendientes

1. **¿Apruebas la estructura?** Sobre todo la decisión de usar un solo archivo CSS.
2. **Nombre de la tienda.** Si no hay uno, se usa uno de relleno como "Vitrina".
3. **Categoría y producto de ejemplo.** Propuesta: **Zapatos** y unas **zapatillas con tallas 36–43**, porque el selector de talla se entiende mejor con números.
4. **Moneda y precios.** Propuesta: pesos colombianos (ej. `$189.900`).
