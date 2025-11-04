# 🥖 Práctica eLearning — Panadería **DulceRuta** (HTML5 + Bootstrap + CSS)

> **Nivel:** Intermedio (HTML5 + Bootstrap 5 + CSS + JS básico)
>  **Duración estimada:** 90–120 minutos
>  **Producto final:** Mini‑sitio multi‑página con carrito simple (localStorage)

## 🎯 Nombre del proyecto

**DulceRuta — Panadería & Café**

## 🧭 Objetivo de aprendizaje

Construir un mini‑sitio web multi‑página de una panadería utilizando **HTML5**, **Bootstrap 5** y **CSS** propio, con navegación coherente, componentes reutilizables y **carrito de compras básico** (localStorage) para afianzar maquetación, estilos y lógica frontal mínima. 🍰☕

## 🧱 Requisitos previos

- Editor de código (VS Code recomendado)
- Navegador actualizado
- Conexión a internet para CDNs de Bootstrap y los íconos

## 🗂️ Estructura de archivos (cada página individual)

```css
dulceruta-bakery/
├─ index.html              # Home: héroe + destacados + CTA
├─ productos.html          # Catálogo de productos
├─ carrito.html            # Carrito (render desde localStorage)
├─ contacto.html           # Formulario de contacto con validación
├─ assets/
│  ├─ css/
│  │  └─ styles.css
│  ├─ img/
│  │  ├─ pan1.jpg
│  │  ├─ pan2.jpg
│  │  ├─ torta1.jpg
│  │  └─ cafe1.jpg
│  └─ js/
│     ├─ main.js          # Productos + addToCart + contador
│     └─ carrito.js       # Render del carrito + totales
└─ README.md               # Instrucciones breves (opcional)
```

> 💡 **Tip:** coloca imágenes libres en `assets/img/` (puedes usar imágenes propias o de bancos gratuitos). Mantén nombres simples.

## 🧪 Criterios de evaluación (rubrica breve)

- **Estructura** (20%): árbol de archivos correcto, rutas relativas funcionales.
- **Maquetación** (25%): uso consistente de Bootstrap (grid, cards, navbar, utilities).
- **Estilos** (15%): `styles.css` con personalización sutil y coherente.
- **Funcionalidad** (25%): carrito (agregar, contar, listar, totalizar, vaciar).
- **Accesibilidad & UX** (15%): etiquetas alt, contraste, tamaños, focos, validación.

## ✅ Reto paso a paso

1. **Crea la carpeta** `dulceruta-bakery/` y su estructura.
2. **Copia y pega** los siguientes archivos en tu proyecto (ajusta textos/imágenes).
3. **Abre `index.html`** en el navegador y prueba la navegación completa.
4. **Agrega al carrito** desde `index.html`/`productos.html`; verifica el contador en la navbar.
5. **Abre `carrito.html`** y valida el total, el botón *Vaciar* y *Eliminar* por ítem.
6. **En `contacto.html`**, prueba la validación del formulario (HTML5 + Bootstrap).
7. **Personaliza** colores, logos, precios y descripciones en `styles.css` y `main.js`.

## 🔗 Fragmento común: Navbar & Footer (guía)

Todas las páginas comparten **navbar** y **footer** (copiados/pegados). Mantén los mismos enlaces:

- Inicio → `index.html`
- Productos → `productos.html`
- Carrito → `carrito.html`
- Contacto → `contacto.html`

## 📄 `index.html`

```html
<!doctype html>
</div>
<!doctype html>
<html lang="es">
<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title>DulceRuta — Inicio</title>
	<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
	<link href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.css" rel="stylesheet">
	<link rel="stylesheet" href="assets/css/styles.css">
	<meta name="description" content="Panadería y café artesanal — DulceRuta. Productos frescos y tostados cada día.">
</head>
<body>
<!-- Navbar -->
<nav class="navbar navbar-expand-lg navbar-light bg-light shadow-sm sticky-top">
	<div class="container">
		<a class="navbar-brand fw-bold" href="index.html">🥖 DulceRuta</a>
		<button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#nav" aria-controls="nav" aria-expanded="false" aria-label="Toggle navigation">
			<span class="navbar-toggler-icon"></span>
		</button>
		<div class="collapse navbar-collapse" id="nav">
			<ul class="navbar-nav ms-auto mb-2 mb-lg-0">
				<li class="nav-item"><a class="nav-link active" href="index.html">Inicio</a></li>
				<li class="nav-item"><a class="nav-link" href="productos.html">Productos</a></li>
				<li class="nav-item"><a class="nav-link position-relative" href="carrito.html">Carrito
					<span class="badge bg-danger rounded-pill position-absolute top-0 start-100 translate-middle" id="cart-count">0</span>
				</a></li>
				<li class="nav-item"><a class="nav-link" href="contacto.html">Contacto</a></li>
			</ul>
		</div>
	</div>
</nav>


<!-- Hero -->
<header class="py-5 bg-hero text-white">
	<div class="container">
		<div class="row align-items-center">
			<div class="col-md-7">
				<h1 class="display-5 fw-bold">Panadería & Café artesanal</h1>
				<p class="lead text-white-75">Sabor tradicional, ingredientes locales. Descubre nuestros productos destacados y llévate lo mejor a casa.</p>
				<p>
					<a href="productos.html" class="btn btn-warning btn-lg me-2">Ver productos</a>
					<a href="contacto.html" class="btn btn-outline-light btn-lg">Contacto</a>
				</p>
			</div>
			<div class="col-md-5 d-none d-md-block">
				<img src="assets/img/torta2.jpg" alt="Pan artesanal" class="img-fluid rounded-3 shadow-sm">
			</div>
		</div>
	</div>
</header>


<!-- Destacados -->
<section class="py-5">
	<div class="container">
		<h2 class="mb-4">Destacados de la semana ✨</h2>
		<div class="row g-4">
			<!-- Cards: reutilizamos el catálogo mínimo -->
			<div class="col-12 col-sm-6 col-lg-3">
				<div class="card h-100">
					<img src="assets/img/pan1.jpeg" class="card-img-top" alt="Pan artesanal">
					<div class="card-body d-flex flex-column">
						<h5 class="card-title">Pan campesino</h5>
						<p class="card-text">Corteza crujiente, miga suave. Ideal para el desayuno.</p>
						<div class="mt-auto d-flex align-items-center justify-content-between">
							<span class="fw-bold">$4.500</span>
							<button class="btn btn-sm btn-primary" onclick="addToCart(1)"><i class="bi bi-cart-plus"></i> Agregar</button>
						</div>
					</div>
				</div>
			</div>

			<div class="col-12 col-sm-6 col-lg-3">
				<div class="card h-100">
					<img src="assets/img/pan2.jpeg" class="card-img-top" alt="Croissant">
					<div class="card-body d-flex flex-column">
						<h5 class="card-title">Croissant</h5>
						<p class="card-text">Hojaldre mantequilloso perfecto para café.</p>
						<div class="mt-auto d-flex align-items-center justify-content-between">
							<span class="fw-bold">$3.200</span>
							<button class="btn btn-sm btn-primary" onclick="addToCart(2)"><i class="bi bi-cart-plus"></i> Agregar</button>
						</div>
					</div>
				</div>
			</div>

			<div class="col-12 col-sm-6 col-lg-3">
				<div class="card h-100">
					<img src="assets/img/torta.jpg" class="card-img-top" alt="Torta de chocolate">
					<div class="card-body d-flex flex-column">
						<h5 class="card-title">Torta de chocolate</h5>
						<p class="card-text">Cacao 70% con ganache cremoso. ¡Irresistible! 🍫</p>
						<div class="mt-auto d-flex align-items-center justify-content-between">
							<span class="fw-bold">$9.900</span>
							<button class="btn btn-sm btn-primary" onclick="addToCart(3)"><i class="bi bi-cart-plus"></i> Agregar</button>
						</div>
					</div>
				</div>
			</div>

			<div class="col-12 col-sm-6 col-lg-3">
				<div class="card h-100">
					<img src="assets/img/cafe.jpg" class="card-img-top" alt="Café de origen">
					<div class="card-body d-flex flex-column">
						<h5 class="card-title">Latte de la casa</h5>
						<p class="card-text">Café de origen colombiano, tostión media. ☕</p>
						<div class="mt-auto d-flex align-items-center justify-content-between">
							<span class="fw-bold">$5.500</span>
							<button class="btn btn-sm btn-primary" onclick="addToCart(4)"><i class="bi bi-cart-plus"></i> Agregar</button>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>


<!-- Footer -->
<footer class="py-4 bg-dark text-white-50">
	<div class="container text-center small">© 2025 DulceRuta · Panadería & Café · Hecho con ❤️ y Bootstrap</div>
</footer>


<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
<script src="assets/js/main.js"></script>
</body>
</html>
```

## 📄 `productos.html`

```html
<!doctype html>
<html lang="es">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>DulceRuta — Productos</title>
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
<link href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.css" rel="stylesheet">
<link rel="stylesheet" href="assets/css/styles.css">
</head>
<body>
<!-- Navbar -->
<nav class="navbar navbar-expand-lg navbar-light bg-light shadow-sm sticky-top">
<div class="container">
<a class="navbar-brand fw-bold" href="index.html">🥖 DulceRuta</a>
<button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#nav" aria-controls="nav" aria-expanded="false" aria-label="Toggle navigation">
<span class="navbar-toggler-icon"></span>
</button>
<div class="collapse navbar-collapse" id="nav">
<ul class="navbar-nav ms-auto mb-2 mb-lg-0">
<li class="nav-item"><a class="nav-link" href="index.html">Inicio</a></li>
<li class="nav-item"><a class="nav-link active" href="productos.html">Productos</a></li>
<li class="nav-item"><a class="nav-link position-relative" href="carrito.html">Carrito
<span class="badge bg-danger rounded-pill position-absolute top-0 start-100 translate-middle" id="cart-count">0</span>
</a></li>
<li class="nav-item"><a class="nav-link" href="contacto.html">Contacto</a></li>
</ul>
</div>
</div>
</nav>


<main class="py-5">
<div class="container">
<h1 class="mb-4">Nuestro catálogo 🍞🍰☕</h1>


<div class="row g-4" id="product-list">
<!-- Se llena dinámicamente desde main.js para reutilizar el catálogo -->
</div>
</div>
</main>


<footer class="py-4 bg-dark text-white-50">
<div class="container text-center small">© 2025 DulceRuta · Panadería & Café</div>
</footer>


<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
<script src="assets/js/main.js"></script>
<script>
// Render dinámico del catálogo en esta página
document.addEventListener('DOMContentLoaded', () => {
renderCatalog('product-list');
});
</script>
</body>
</html>
```

## 📄 `carrito.html`

```html
<!doctype html>
<html lang="es">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>DulceRuta — Carrito</title>
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
<link href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.css" rel="stylesheet">
<link rel="stylesheet" href="assets/css/styles.css">
</head>
<body>
<nav class="navbar navbar-expand-lg navbar-light bg-light shadow-sm sticky-top">
<div class="container">
<a class="navbar-brand fw-bold" href="index.html">🥖 DulceRuta</a>
<button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#nav" aria-controls="nav" aria-expanded="false" aria-label="Toggle navigation">
<span class="navbar-toggler-icon"></span>
</button>
<div class="collapse navbar-collapse" id="nav">
<ul class="navbar-nav ms-auto mb-2 mb-lg-0">
<li class="nav-item"><a class="nav-link" href="index.html">Inicio</a></li>
<li class="nav-item"><a class="nav-link" href="productos.html">Productos</a></li>
<li class="nav-item"><a class="nav-link active position-relative" href="carrito.html">Carrito
<span class="badge bg-danger rounded-pill position-absolute top-0 start-100 translate-middle" id="cart-count">0</span>
</a></li>
<li class="nav-item"><a class="nav-link" href="contacto.html">Contacto</a></li>
</ul>
</div>
</div>
</nav>


<main class="py-5">
<div class="container">
<h1 class="mb-4">Tu carrito 🧺</h1>


<div class="table-responsive">
<table class="table align-middle">
<thead>
<tr>
<th>Producto</th>
<th class="text-center">Precio</th>
<th class="text-center">Cantidad</th>
<th class="text-end">Subtotal</th>
<th></th>
</tr>
</thead>
<tbody id="cart-body">
<!-- Filas dinámicas -->
</tbody>
<tfoot>
<tr>
<td colspan="3" class="text-end fw-bold">Total</td>
<td class="text-end fw-bold" id="cart-total">$0</td>
<td></td>
</tr>
</tfoot>
</table>
</div>


<div class="d-flex gap-2 justify-content-end">
<a href="productos.html" class="btn btn-outline-secondary"><i class="bi bi-arrow-left"></i> Seguir comprando</a>
<button class="btn btn-danger" id="btn-empty"><i class="bi bi-trash"></i> Vaciar</button>
<button class="btn btn-success"><i class="bi bi-bag-check"></i> Finalizar compra</button>
</div>
</div>
</main>


<footer class="py-4 bg-dark text-white-50">
<div class="container text-center small">© 2025 DulceRuta · Panadería & Café</div>
</footer>


<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
<script src="assets/js/main.js"></script>
<script src="assets/js/carrito.js"></script>
</body>
</html>
```

## 📄 `contacto.html`

```html
<!doctype html>
<html lang="es">
	<head>
		<meta charset="utf-8">
		<meta name="viewport" content="width=device-width, initial-scale=1">
		<title>DulceRuta — Contacto</title>
		<meta name="description" content="Contacto — DulceRuta panadería y café. Envíanos tus dudas, pedidos o sugerencias.">
		<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
		<link href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.css" rel="stylesheet">
		<link rel="stylesheet" href="assets/css/styles.css">
	</head>
	<body>

		<!-- Navbar -->
		<nav class="navbar navbar-expand-lg navbar-light bg-light shadow-sm sticky-top">
			<div class="container">
				<a class="navbar-brand fw-bold" href="index.html">🥖 DulceRuta</a>
				<button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#nav" aria-controls="nav" aria-expanded="false" aria-label="Toggle navigation">
					<span class="navbar-toggler-icon"></span>
				</button>
				<div class="collapse navbar-collapse" id="nav">
					<ul class="navbar-nav ms-auto mb-2 mb-lg-0">
						<li class="nav-item"><a class="nav-link" href="index.html">Inicio</a></li>
						<li class="nav-item"><a class="nav-link" href="productos.html">Productos</a></li>
						<li class="nav-item"><a class="nav-link position-relative" href="carrito.html">Carrito
							<span class="badge bg-danger rounded-pill position-absolute top-0 start-100 translate-middle" id="cart-count">0</span>
						</a></li>
						<li class="nav-item"><a class="nav-link active" href="contacto.html">Contacto</a></li>
					</ul>
				</div>
			</div>
		</nav>


		<main class="py-5">
			<div class="container">
				<h1 class="mb-4">¡Hablemos! 📬</h1>

				<div class="row g-4">
					<div class="col-lg-6">
						<form id="contact-form" class="needs-validation" novalidate aria-label="Formulario de contacto">
							<div class="mb-3">
								<label for="name" class="form-label">Nombre</label>
								<input name="name" type="text" class="form-control" id="name" placeholder="Tu nombre" required aria-required="true">
								<div class="invalid-feedback">Por favor, ingresa tu nombre.</div>
							</div>

							<div class="mb-3">
								<label for="email" class="form-label">Correo</label>
								<input name="email" type="email" class="form-control" id="email" placeholder="nombre@ejemplo.com" required aria-required="true">
								<div class="invalid-feedback">Ingresa un correo válido.</div>
							</div>

							<div class="mb-3">
								<label for="msg" class="form-label">Mensaje</label>
								<textarea name="message" class="form-control" id="msg" rows="6" placeholder="Escribe tu mensaje..." required aria-required="true"></textarea>
								<div class="invalid-feedback">Cuéntanos en qué podemos ayudarte.</div>
							</div>

							<div class="d-flex gap-2">
								<button class="btn btn-primary" type="submit" aria-label="Enviar mensaje"><i class="bi bi-send me-1"></i> Enviar</button>
								<button class="btn btn-outline-secondary" type="reset">Limpiar</button>
							</div>
						</form>
					</div>

					<div class="col-lg-6">
						<div class="p-4 bg-light rounded-3 h-100">
							<h5 class="fw-bold">Nuestra tienda</h5>
							<p class="mb-1">Calle 123 #45‑67 — Ciudad Dulce</p>
							<p class="mb-1">Horario: L‑S 7:00–19:00 | D 8:00–14:00</p>
							<p class="mb-0">Tel: (xxx) xxx‑xxxx</p>
							<hr>
							<p class="small text-muted mb-0">También puedes escribirnos por redes o pasar a la tienda. Respuesta en <strong>24–48h</strong>.</p>
						</div>
					</div>
				</div>
			</div>
		</main>


		<footer class="py-4 bg-dark text-white-50">
			<div class="container text-center small">© 2025 DulceRuta · Panadería & Café</div>
		</footer>


		<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
		<script src="assets/js/main.js"></script>
		<script>
			// Bootstrap validation + friendly UX: show toast on successful submit and reset form
			(function(){
				'use strict';
				const form = document.getElementById('contact-form');
				if(!form) return;
				form.addEventListener('submit', function(event){
					event.preventDefault();
					event.stopPropagation();
					form.classList.add('was-validated');
					if(!form.checkValidity()) return;
					// Simular envío: mostrar toast y limpiar formulario
					if(typeof toast === 'function') toast('Mensaje enviado — Gracias 😊');
					form.reset();
					form.classList.remove('was-validated');
				}, false);
			})();
		</script>
	</body>
</html>
```

## 🧵 `assets/css/styles.css`

```css
:root{
--brand:#FCB900; /* dorado pan */
--brand-dark:#C48A00;
--ink:#212529;
--brand-contrast:#212529; /* color recomendado sobre el dorado */
}


body{ font-family: system-ui, -apple-system, "Segoe UI", Roboto, Ubuntu, "Helvetica Neue", Arial, "Noto Sans", "Apple Color Emoji","Segoe UI Emoji"; }


.navbar-brand{ letter-spacing:.5px; }


.bg-hero{
	background: linear-gradient(45deg, rgba(0,0,0,.55), rgba(0,0,0,.4)), url('../img/pan1.jpg') center/cover no-repeat;
	min-height: 320px;
	display: flex;
	align-items: center;
	padding: 3rem 0;
}


.btn-warning{
	background-color: var(--brand);
	border-color: var(--brand-dark);
	color: var(--brand-contrast);
}
.btn-warning:hover{
	background-color: var(--brand-dark);
	border-color: var(--brand-dark);
	color: #fff;
}
.btn-warning:focus-visible{
	outline: none;
	box-shadow: 0 0 0 .25rem rgba(196,138,0,0.22);
}


.card img{
	width: 100%;
	height: 180px;
	object-fit: cover;
	display: block;
}

/* Ajustes responsive: imágenes menos altas en móviles */
@media (max-width: 576px){
	.card img{ height: 140px; }
	.bg-hero{ min-height: 260px; padding: 2rem 0; }
}


footer{ margin-top: 3rem; }

/* Enfoque accesible para enlaces y botones */
.nav-link:focus-visible,
.btn:focus-visible{
	outline: none;
	box-shadow: 0 0 0 .15rem rgba(33,37,41,0.12);
}
```

## 🧠 `assets/js/main.js`

```javascript
// Catálogo base (puedes personalizar)
// Datos de ejemplo: listado mínimo de productos usados en las páginas
const PRODUCTS = [
	{ id: 1, name: 'Pan campesino', price: 4500, img: 'assets/img/pan1.jpg' },
	{ id: 2, name: 'Croissant', price: 3200, img: 'assets/img/pan2.jpg' },
	{ id: 3, name: 'Torta de chocolate', price: 9900, img: 'assets/img/torta1.jpg' },
	{ id: 4, name: 'Latte de la casa', price: 5500, img: 'assets/img/cafe1.jpg' }
];

// Utilidades de almacenamiento del carrito (localStorage)
function getCart(){
	try{
		return JSON.parse(localStorage.getItem('cart')) || {};
	}catch(e){
		return {};
	}
}

function saveCart(cart){
	try{
		localStorage.setItem('cart', JSON.stringify(cart));
	}catch(e){
		// Silenciar error de almacenamiento (por ejemplo en modo privado)
	}
	// Mantener contador de carrito actualizado tras cualquier cambio
	if(typeof updateCartCount === 'function') updateCartCount();
}

function addToCart(id){
	const cart = getCart();
	cart[id] = (cart[id] || 0) + 1;
	saveCart(cart);
	toast('Producto agregado 🧺');
}


function removeFromCart(id){
const cart = getCart();
if(cart[id]){ delete cart[id]; saveCart(cart); }
}


function clearCart(){ saveCart({}); }


function cartCount(){
const cart = getCart();
return Object.values(cart).reduce((a,b)=>a+b,0);
}


function updateCartCount(){
const el = document.getElementById('cart-count');
if(el) el.textContent = cartCount();
}


function formatCOP(value){
return new Intl.NumberFormat('es-CO', { style:'currency', currency:'COP', maximumFractionDigits:0 }).format(value);
}


function findProduct(id){
return PRODUCTS.find(p => p.id === Number(id));
}


// Render dinámico del catálogo (productos.html)
function renderCatalog(containerId){
const container = document.getElementById(containerId);
if(!container) return;
const html = PRODUCTS.map(p => `
<div class="col-12 col-sm-6 col-lg-3">
<div class="card h-100">
<img src="${p.img}" alt="${p.name}" class="card-img-top"/>
<div class="card-body d-flex flex-column">
<h5 class="card-title">${p.name}</h5>
<p class="card-text text-muted">Artesanal y fresco todos los días.</p>
<div class="mt-auto d-flex align-items-center justify-content-between">
<span class="fw-bold">${formatCOP(p.price)}</span>
<button class="btn btn-sm btn-primary" onclick="addToCart(${p.id})"><i class="bi bi-cart-plus"></i> Agregar</button>
</div>
</div>
</div>
</div>`).join('');
container.innerHTML = html;
}


// Mini toast sin dependencias (utilidad sencilla)
function toast(msg){
const t = document.createElement('div');
t.className = 'toast align-items-center text-bg-dark border-0 position-fixed bottom-0 end-0 m-3 show';
t.role = 'alert';
t.style.zIndex = 1080;
t.innerHTML = `<div class="d-flex"><div class="toast-body">${msg}</div><button type="button" class="btn-close btn-close-white me-2 m-auto" data-bs-dismiss="toast" aria-label="Close"></button></div>`;
document.body.appendChild(t);
setTimeout(()=> t.remove(), 2200);
}


// Inicializar contador al cargar cualquier página
document.addEventListener('DOMContentLoaded', updateCartCount);
```

## 🧮 `assets/js/carrito.js`

```javascript
function renderCart(){
const body = document.getElementById('cart-body');
const totalEl = document.getElementById('cart-total');
const cart = getCart();
let total = 0;
const rows = Object.entries(cart).map(([id, qty]) => {
const p = findProduct(id);
if(!p) return '';
const subtotal = p.price * qty;
total += subtotal;
return `
<tr>
<td>
<div class="d-flex align-items-center gap-3">
<img src="${p.img}" alt="${p.name}" width="64" height="64" style="object-fit:cover;border-radius:8px">
<div>
<div class="fw-semibold">${p.name}</div>
<small class="text-muted">ID: ${p.id}</small>
</div>
</div>
</td>
<td class="text-center">${formatCOP(p.price)}</td>
<td class="text-center">
<div class="btn-group btn-group-sm" role="group">
<button class="btn btn-outline-secondary" onclick="decrease(${p.id})">-</button>
<span class="btn btn-light disabled">${qty}</span>
<button class="btn btn-outline-secondary" onclick="increase(${p.id})">+</button>
</div>
</td>
<td class="text-end">${formatCOP(subtotal)}</td>
<td class="text-end">
<button class="btn btn-sm btn-outline-danger" onclick="removeItem(${p.id})"><i class="bi bi-x"></i></button>
</td>
</tr>`;
}).join('');


body.innerHTML = rows || `<tr><td colspan="5" class="text-center text-muted">Tu carrito está vacío 🧺</td></tr>`;
totalEl.textContent = formatCOP(total);
}


function increase(id){
const cart = getCart();
cart[id] = (cart[id]||0) + 1;
saveCart(cart);
renderCart();
}


function decrease(id){
const cart = getCart();
if(cart[id]){
cart[id] = cart[id] - 1;
if(cart[id] <= 0) delete cart[id];
saveCart(cart);
renderCart();
}
}


function removeItem(id){
const cart = getCart();
if(cart[id]) delete cart[id];
saveCart(cart);
renderCart();
}


document.addEventListener('DOMContentLoaded', () => {
renderCart();
const btnEmpty = document.getElementById('btn-empty');
if(btnEmpty) btnEmpty.addEventListener('click', () => { clearCart(); renderCart(); });
});
```

## 🧭 Pasos y mini‑retos

1. **Clona la estructura** y reemplaza textos con tu identidad de marca (nombre, dirección, horarios).
2. **Agrega 4 productos nuevos** en `main.js` (pan integral, galletas, cheesecake, capuccino) con sus precios e imágenes.
3. **Crea una sección “Promociones”** al final de `index.html` con una *alert* y dos *cards* de oferta.
4. **Accesibilidad:** agrega `alt` descriptivos a todas las imágenes (revisa Lighthouse si puedes).
5. **Estilo propio:** cambia la paleta en `styles.css` manteniendo buen contraste.
6. **Validación:** en `contacto.html`, marca campos como requeridos y prueba mensajes de error.
7. **Reflexión final:** ¿qué mejorarías del flujo de compra? ✍️

## 🧩 Extensiones opcionales (para nota extra)

- **Paginación** en `productos.html` o filtro por categoría (panes / pasteles / bebidas).
- **Persistencia del formulario** de contacto (guardar borrador en localStorage).
- **Modo oscuro** con toggle que cambie variables CSS.

## 🆘 Solución de problemas

- Si la **navbar no navega**, revisa las **rutas relativas** (`href="productos.html"`, etc.).
- Si el **contador** no cambia, confirma que `main.js` está **después** de Bootstrap y que no hay errores en la consola.
- Si no ves imágenes, valida la ruta `assets/img/archivo.jpg`.

## 🏁 Cierre

¡Listo! Has construido un sitio multi‑página con **Bootstrap 5**, integrando un **carrito funcional** y buenas prácticas de maquetación. 🎉 Ahora personaliza el branding y sube tu práctica a GitHub/Classroom si aplica. 💻🚀