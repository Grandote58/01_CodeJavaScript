# Práctica — Zapatería **PasoFino** (HTML5 + Bootstrap + CSS)

> **Nivel:** Intermedio
>  **Duración estimada:** 60–90 min
>  **Producto final:** Mini‑sitio multi‑página de zapatería (index, catálogo y contacto)

## 🎯 Nombre del proyecto

### **PasoFino — Calzado & Estilo**

## 🧭 Objetivo de aprendizaje

Diseñar y maquetar un mini‑sitio **multi‑página** para una tienda de zapatos utilizando **HTML5**, **Bootstrap 5** y **CSS** personalizado, incorporando componentes reutilizables (navbar/footer), grillas responsivas y un **catálogo filtrable** básico con JavaScript. 🥿👞🧦

## 🧱 Requisitos previos

- Editor de código (VS Code)
- Navegador moderno
- Conexión a internet (CDN Bootstrap e íconos)

## 🗂️ Crea adecuadamente la Estructura de archivos (cada página individual)

```css
pasofino-zapateria/
├─ index.html              # Home: héroe + destacados + CTA
├─ productos.html          # Catálogo de zapatos con filtro de búsqueda
├─ contacto.html           # Formulario de contacto con validación Bootstrap
├─ assets/
│  ├─ css/
│  │  └─ styles.css
│  ├─ img/
│  │  ├─ hombre1.jpg
│  │  ├─ mujer1.jpg
│  │  ├─ deportivo1.jpg
│  │  └─ casual1.jpg
│  └─ js/
│     └─ main.js          # Datos del catálogo + render y filtro
└─ README.md               # Instrucciones breves (opcional)
```

> 💡 **Tip:** Usa imágenes libres y nómbralas claro. Mantén rutas relativas consistentes.

## 🧪 Criterios de evaluación (rúbrica breve)

- **Estructura (20%)**: árbol de archivos correcto, rutas funcionales.
- **Maquetación (30%)**: uso de grid, cards, navbar, utilities de Bootstrap.
- **Estilos (20%)**: personalización en `styles.css` con coherencia visual.
- **Funcionalidad (15%)**: filtro de búsqueda en catálogo (JS) y validación en contacto.
- **Accesibilidad/UX (15%)**: alt en imágenes, jerarquías claras, contraste adecuado.

## ✅ Guía de práctica (paso a paso)

1. Crea la carpeta **`pasofino-zapateria/`** y su estructura.
2. Copia los archivos de ejemplo y ajusta **marca, textos e imágenes**.
3. Verifica **navegación** entre páginas desde la navbar.
4. En **productos**, prueba el **buscador** por nombre o categoría.
5. En **contacto**, valida el formulario (errores al dejar campos vacíos).
6. Personaliza la **paleta** y tipografías en `styles.css`.
7. Entrega: sube a GitHub/host estático o comparte carpeta comprimida. 📦

## 🔗 Fragmentos comunes: Navbar & Footer (guía)

Todas las páginas comparten la misma **navbar** y **footer**. Mantén los enlaces:

- Inicio → `index.html`
- Productos → `productos.html`
- Contacto → `contacto.html`

## 📄 `index.html`

```html
<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>PasoFino — Inicio</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.css" rel="stylesheet">
  <link rel="stylesheet" href="assets/css/styles.css">
</head>
<body>
  <!-- Navbar -->
  <nav class="navbar navbar-expand-lg bg-light border-bottom sticky-top">
    <div class="container">
      <a class="navbar-brand fw-bold" href="index.html">👟 PasoFino</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#nav" aria-controls="nav" aria-expanded="false" aria-label="Menú">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="nav">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item"><a class="nav-link active" href="index.html">Inicio</a></li>
          <li class="nav-item"><a class="nav-link" href="productos.html">Productos</a></li>
          <li class="nav-item"><a class="nav-link" href="contacto.html">Contacto</a></li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- Hero -->
  <header class="py-5 bg-hero text-white">
    <div class="container text-center">
      <h1 class="display-5 fw-bold">Da el paso con estilo ✨</h1>
      <p class="lead">Calzado para todas las ocasiones: deportivo, casual y ejecutivo.</p>
      <a href="productos.html" class="btn btn-warning btn-lg mt-3">Ver catálogo</a>
    </div>
  </header>

  <!-- Destacados -->
  <section class="py-5">
    <div class="container">
      <h2 class="mb-4">Colecciones destacadas 🏷️</h2>
      <div class="row g-4">
        <div class="col-12 col-md-4">
          <div class="card h-100">
            <img src="assets/img/deportivo1.jpg" class="card-img-top" alt="Zapatillas deportivas">
            <div class="card-body d-flex flex-column">
              <h5 class="card-title">Deportivo</h5>
              <p class="card-text">Amortiguación y ligereza para tu entrenamiento diario.</p>
              <a href="productos.html#cat-deportivo" class="btn btn-outline-primary mt-auto">Explorar</a>
            </div>
          </div>
        </div>
        <div class="col-12 col-md-4">
          <div class="card h-100">
            <img src="assets/img/casual1.jpg" class="card-img-top" alt="Zapatos casuales">
            <div class="card-body d-flex flex-column">
              <h5 class="card-title">Casual</h5>
              <p class="card-text">Comodidad y estilo para el día a día.</p>
              <a href="productos.html#cat-casual" class="btn btn-outline-primary mt-auto">Explorar</a>
            </div>
          </div>
        </div>
        <div class="col-12 col-md-4">
          <div class="card h-100">
            <img src="assets/img/hombre1.jpg" class="card-img-top" alt="Zapatos formales hombre">
            <div class="card-body d-flex flex-column">
              <h5 class="card-title">Formal</h5>
              <p class="card-text">Acabados premium para eventos y oficina.</p>
              <a href="productos.html#cat-formal" class="btn btn-outline-primary mt-auto">Explorar</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- CTA -->
  <section class="py-5 bg-light border-top">
    <div class="container text-center">
      <h3>Envíos a todo el país 📦</h3>
      <p class="mb-3">Pagos seguros, cambios fáciles y atención personalizada.</p>
      <a href="contacto.html" class="btn btn-primary">Contáctanos</a>
    </div>
  </section>

  <!-- Footer -->
  <footer class="py-4 bg-dark text-white-50">
    <div class="container text-center small">© 2025 PasoFino · Zapatería & Estilo</div>
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
  <title>PasoFino — Productos</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.css" rel="stylesheet">
  <link rel="stylesheet" href="assets/css/styles.css">
</head>
<body>
  <nav class="navbar navbar-expand-lg bg-light border-bottom sticky-top">
    <div class="container">
      <a class="navbar-brand fw-bold" href="index.html">👟 PasoFino</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#nav" aria-controls="nav" aria-expanded="false" aria-label="Menú">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="nav">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item"><a class="nav-link" href="index.html">Inicio</a></li>
          <li class="nav-item"><a class="nav-link active" href="productos.html">Productos</a></li>
          <li class="nav-item"><a class="nav-link" href="contacto.html">Contacto</a></li>
        </ul>
      </div>
    </div>
  </nav>

  <main class="py-5">
    <div class="container">
      <div class="d-flex flex-column flex-md-row align-items-md-center justify-content-between gap-3 mb-4">
        <h1 class="mb-0">Catálogo 👞</h1>
        <div class="input-group w-auto">
          <span class="input-group-text"><i class="bi bi-search"></i></span>
          <input id="search" class="form-control" type="search" placeholder="Buscar por nombre o categoría...">
        </div>
      </div>

      <div class="row g-4" id="product-list">
        <!-- Render dinámico desde main.js -->
      </div>

      <hr class="my-5">
      <div class="text-center text-muted small">Filtra por categoría con anclas:
        <a id="cat-deportivo" href="#" onclick="filterBy('deportivo')">deportivo</a> ·
        <a id="cat-casual" href="#" onclick="filterBy('casual')">casual</a> ·
        <a id="cat-formal" href="#" onclick="filterBy('formal')">formal</a>
      </div>
    </div>
  </main>

  <footer class="py-4 bg-dark text-white-50">
    <div class="container text-center small">© 2025 PasoFino · Zapatería & Estilo</div>
  </footer>

  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
  <script src="assets/js/main.js"></script>
  <script>
    document.addEventListener('DOMContentLoaded', () => {
      renderCatalog('product-list');
      const input = document.getElementById('search');
      input.addEventListener('input', (e) => filterBy(e.target.value));
    });
  </script>
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
  <title>PasoFino — Contacto</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.css" rel="stylesheet">
  <link rel="stylesheet" href="assets/css/styles.css">
</head>
<body>
  <nav class="navbar navbar-expand-lg bg-light border-bottom sticky-top">
    <div class="container">
      <a class="navbar-brand fw-bold" href="index.html">👟 PasoFino</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#nav" aria-controls="nav" aria-expanded="false" aria-label="Menú">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="nav">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item"><a class="nav-link" href="index.html">Inicio</a></li>
          <li class="nav-item"><a class="nav-link" href="productos.html">Productos</a></li>
          <li class="nav-item"><a class="nav-link active" href="contacto.html">Contacto</a></li>
        </ul>
      </div>
    </div>
  </nav>

  <main class="py-5">
    <div class="container">
      <h1 class="mb-4">¡Hablemos! 📬</h1>
      <div class="row g-4">
        <div class="col-md-6">
          <form class="needs-validation" novalidate>
            <div class="mb-3">
              <label for="name" class="form-label">Nombre</label>
              <input type="text" class="form-control" id="name" required>
              <div class="invalid-feedback">Por favor, ingresa tu nombre.</div>
            </div>
            <div class="mb-3">
              <label for="email" class="form-label">Correo</label>
              <input type="email" class="form-control" id="email" required>
              <div class="invalid-feedback">Ingresa un correo válido.</div>
            </div>
            <div class="mb-3">
              <label for="subject" class="form-label">Asunto</label>
              <input type="text" class="form-control" id="subject" required>
              <div class="invalid-feedback">Escribe un asunto.</div>
            </div>
            <div class="mb-3">
              <label for="msg" class="form-label">Mensaje</label>
              <textarea class="form-control" id="msg" rows="5" required></textarea>
              <div class="invalid-feedback">Cuéntanos en qué podemos ayudarte.</div>
            </div>
            <button class="btn btn-primary" type="submit"><i class="bi bi-send"></i> Enviar</button>
          </form>
        </div>
        <div class="col-md-6">
          <div class="p-4 bg-light rounded-3 h-100">
            <h5 class="fw-bold">Nuestra tienda</h5>
            <p class="mb-1">Av. Paso 456 — Ciudad Calzado</p>
            <p class="mb-1">Horario: L‑S 9:00–19:00 | D 10:00–16:00</p>
            <p class="mb-0">Tel: (xxx) xxx‑xxxx</p>
          </div>
        </div>
      </div>
    </div>
  </main>

  <footer class="py-4 bg-dark text-white-50">
    <div class="container text-center small">© 2025 PasoFino · Zapatería & Estilo</div>
  </footer>

  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
  <script>
  // Validación Bootstrap
  (() => {
    'use strict';
    const forms = document.querySelectorAll('.needs-validation');
    Array.from(forms).forEach(form => {
      form.addEventListener('submit', event => {
        if (!form.checkValidity()) {
          event.preventDefault();
          event.stopPropagation();
        }
        form.classList.add('was-validated');
      }, false);
    });
  })();
  </script>
</body>
</html>
```

## 🧵 `assets/css/styles.css`

```css
:root{
  --brand:#0d6efd; /* azul bootstrap */
  --accent:#FFC107; /* ámbar para CTA */
  --ink:#212529;
}

body{ font-family: system-ui, -apple-system, "Segoe UI", Roboto, Ubuntu, "Helvetica Neue", Arial; }

.navbar-brand{ letter-spacing:.5px; }

.bg-hero{
  background: linear-gradient(45deg, rgba(0,0,0,.55), rgba(0,0,0,.4)), url('../img/mujer1.jpg') center/cover no-repeat;
}

.btn-warning{ background-color: var(--accent); border-color: var(--accent); }
.btn-warning:hover{ filter: brightness(.9); }

.card img{ object-fit: cover; height: 200px; }

footer{ margin-top: 3rem; }
```

## 🧠 `assets/js/main.js`

```javascript
// Datos del catálogo (personaliza nombres, precios e imágenes)
const PRODUCTS = [
  { id: 1, name: 'Runner Pro', category: 'deportivo', price: 199900, img: 'assets/img/deportivo1.jpg' },
  { id: 2, name: 'Urban Soft', category: 'casual', price: 149900, img: 'assets/img/casual1.jpg' },
  { id: 3, name: 'Oxford Elite', category: 'formal', price: 259900, img: 'assets/img/hombre1.jpg' },
  { id: 4, name: 'Luna Comfort', category: 'casual', price: 169900, img: 'assets/img/mujer1.jpg' },
];

function formatCOP(value){
  return new Intl.NumberFormat('es-CO', { style:'currency', currency:'COP', maximumFractionDigits:0 }).format(value);
}

function renderCatalog(containerId, query=''){
  const container = document.getElementById(containerId);
  if(!container) return;
  const q = query.trim().toLowerCase();
  const filtered = PRODUCTS.filter(p => !q || p.name.toLowerCase().includes(q) || p.category.toLowerCase().includes(q));
  const html = filtered.map(p => `
    <div class="col-12 col-sm-6 col-lg-3">
      <div class="card h-100">
        <img src="${p.img}" alt="${p.name}" class="card-img-top"/>
        <div class="card-body d-flex flex-column">
          <span class="badge text-bg-light align-self-start mb-2">${p.category}</span>
          <h5 class="card-title">${p.name}</h5>
          <p class="card-text text-muted">Ergonomía y durabilidad para cada paso.</p>
          <div class="mt-auto d-flex align-items-center justify-content-between">
            <span class="fw-bold">${formatCOP(p.price)}</span>
            <a class="btn btn-sm btn-primary" href="contacto.html"><i class="bi bi-chat-dots"></i> Consultar</a>
          </div>
        </div>
      </div>
    </div>`).join('');
  container.innerHTML = html || `<div class="text-center text-muted">No se encontraron resultados 🤔</div>`;
}

function filterBy(q){
  renderCatalog('product-list', q);
}

// Inicialización común
document.addEventListener('DOMContentLoaded', () => {
  // Si existe el contenedor, renderiza catálogo por defecto
  if(document.getElementById('product-list')){
    renderCatalog('product-list');
  }
});
```

## 🧭 Mini‑retos (eLearning)

1. **Agrega 4 productos nuevos** (sandalia, bota trekking, mocasín, zapatilla canvas) con sus imágenes.
2. **Crea una banda de promociones** en `index.html` (usa `alert` y `badge`).
3. **Añade filtros por botones** (deportivo/casual/formal) encima del buscador.
4. **Accesibilidad:** revisa `alt` en imágenes y contrastes (prueba Lighthouse).
5. **Estilo propio:** cambia paleta en `styles.css` y agrega `:hover` en cards.
6. **Extra:** agrega paginación simple (mostrar 8 por página) o etiquetas de talla.

## 🆘 Solución de problemas

- Si no carga el **catálogo**, revisa que `main.js` esté enlazado y la ruta `assets/img/...` sea correcta.
- Si la **navbar** no navega, verifica `href` relativos.
- Si la **validación** no funciona, confirma `novalidate` y el script de Bootstrap.

## 🏁 Cierre

¡Excelente trabajo! Construiste un sitio multi‑página con **Bootstrap**, integraste un **catálogo filtrable** y aplicaste buenas prácticas de maquetación. 🎉 Personaliza la marca, publica y comparte tu resultado. 🚀