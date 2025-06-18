# 🧪 **10 Prácticas de Funciones para Laberintos y Movimiento (Node.js)**

> 🧱 Nivel: Básico - Intermedio
>  💻 Herramienta: Node.js + readline-sync
>  🧠 Enfoque: Programación, lógica, orientación espacial y gamificación

### ✅ Prerrequisitos

```javascript
npm install readline-sync
```

Y al inicio de cada archivo:

```javascript
const readline = require("readline-sync");
```

## 1️⃣ **Mostrar coordenadas del jugador**

```javascript
const mostrarPosicion = () => {
  const posicion = { x: 0, y: 0 };
  console.log(`🧍 Estás en la posición (${posicion.x}, ${posicion.y})`);
};

mostrarPosicion();
```

🧠 *Objetivo:* Comprender coordenadas en el espacio 2D.

## 2️⃣ **Mover al jugador hacia la derecha**

```javascript
const moverDerecha = (pos) => {
  pos.x += 1;
  return pos;
};

let jugador = { x: 0, y: 0 };
jugador = moverDerecha(jugador);
console.log(`➡️ Te moviste a (${jugador.x}, ${jugador.y})`);
```

🧠 *Objetivo:* Crear una función que modifica estado.

## 3️⃣ **Movimiento con selección de dirección**

```javascript
const mover = (pos, direccion) => {
  if (direccion === "N") pos.y -= 1;
  if (direccion === "S") pos.y += 1;
  if (direccion === "E") pos.x += 1;
  if (direccion === "O") pos.x -= 1;
  return pos;
};

let pos = { x: 0, y: 0 };
const dir = readline.question("🧭 Dirección (N/S/E/O): ");
pos = mover(pos, dir.toUpperCase());
console.log(`📍 Nueva posición: (${pos.x}, ${pos.y})`);
```

🧠 *Objetivo:* Aplicar funciones con parámetros + lógica condicional.

## 4️⃣ **Simular varios movimientos seguidos**

```javascript
const mover = (pos, dir) => {
  if (dir === "N") pos.y--;
  if (dir === "S") pos.y++;
  if (dir === "E") pos.x++;
  if (dir === "O") pos.x--;
  return pos;
};

let pos = { x: 0, y: 0 };
for (let i = 1; i <= 3; i++) {
  const dir = readline.question(`🔄 Movimiento ${i} (N/S/E/O): `);
  pos = mover(pos, dir.toUpperCase());
}
console.log(`✅ Posición final: (${pos.x}, ${pos.y})`);
```

🧠 *Objetivo:* Uso de bucles y funciones con control de estado.

## 5️⃣ **Impedir salir del mapa 5x5**

```javascript
const mover = (pos, dir) => {
  const nueva = { ...pos };
  if (dir === "N") nueva.y--;
  if (dir === "S") nueva.y++;
  if (dir === "E") nueva.x++;
  if (dir === "O") nueva.x--;
  if (nueva.x < 0 || nueva.y < 0 || nueva.x >= 5 || nueva.y >= 5) {
    console.log("⛔ Movimiento inválido: fuera del laberinto");
    return pos;
  }
  return nueva;
};

let pos = { x: 2, y: 2 };
const dir = readline.question("🚶 Dirección (N/S/E/O): ");
pos = mover(pos, dir.toUpperCase());
console.log(`📍 Estás en (${pos.x}, ${pos.y})`);
```

🧠 *Objetivo:* Validar límites con funciones y condicionales.

## 6️⃣ **Crear función para imprimir el mapa**

```javascript
const imprimirMapa = (pos) => {
  for (let y = 0; y < 5; y++) {
    let fila = "";
    for (let x = 0; x < 5; x++) {
      fila += (x === pos.x && y === pos.y) ? "🧍 " : "⬜ ";
    }
    console.log(fila);
  }
};

let jugador = { x: 1, y: 2 };
imprimirMapa(jugador);
```

🧠 *Objetivo:* Visualización gráfica con lógica y bucles.

## 7️⃣ **Meta secreta: llegar a la salida**

```javascript
const mover = (pos, dir) => {
  if (dir === "N") pos.y--;
  if (dir === "S") pos.y++;
  if (dir === "E") pos.x++;
  if (dir === "O") pos.x--;
  return pos;
};

const meta = { x: 3, y: 2 };
let pos = { x: 0, y: 0 };

while (pos.x !== meta.x || pos.y !== meta.y) {
  const dir = readline.question("🧭 Mueve (N/S/E/O): ");
  pos = mover(pos, dir.toUpperCase());
  console.log(`📍 Estás en (${pos.x}, ${pos.y})`);
}

console.log("🎉 ¡Llegaste a la salida!");
```

🧠 *Objetivo:* Combinar funciones + bucles + lógica de comparación.

## 8️⃣ **Agregar muros en el mapa**

```javascript
const esMuro = (x, y) => {
  return (x === 2 && y === 1) || (x === 1 && y === 3);
};

let pos = { x: 1, y: 1 };
const mover = (pos, dir) => {
  let nueva = { ...pos };
  if (dir === "N") nueva.y--;
  if (dir === "S") nueva.y++;
  if (dir === "E") nueva.x++;
  if (dir === "O") nueva.x--;
  if (esMuro(nueva.x, nueva.y)) {
    console.log("🚧 ¡Hay un muro! No puedes pasar.");
    return pos;
  }
  return nueva;
};

const dir = readline.question("🧱 Dirección (N/S/E/O): ");
pos = mover(pos, dir.toUpperCase());
console.log(`📍 Posición: (${pos.x}, ${pos.y})`);
```

🧠 *Objetivo:* Funciones lógicas anidadas y validación de obstáculos.

## 9️⃣ **Registrar ruta completa del jugador**

```javascript
const mover = (pos, dir) => {
  if (dir === "N") pos.y--;
  if (dir === "S") pos.y++;
  if (dir === "E") pos.x++;
  if (dir === "O") pos.x--;
  return pos;
};

let pos = { x: 0, y: 0 };
let ruta = [`Inicio: (${pos.x}, ${pos.y})`];

for (let i = 0; i < 3; i++) {
  const dir = readline.question("➡️ Dirección (N/S/E/O): ");
  pos = mover(pos, dir.toUpperCase());
  ruta.push(`→ (${pos.x}, ${pos.y})`);
}

console.log("🧾 Ruta completa:");
console.log(ruta.join("\n"));
```

🧠 *Objetivo:* Almacenar historial con funciones y arrays.

## 🔟 **Desafío: función que detecta victoria y lo imprime bonito**

```javascript
const mover = (pos, dir) => {
  if (dir === "N") pos.y--;
  if (dir === "S") pos.y++;
  if (dir === "E") pos.x++;
  if (dir === "O") pos.x--;
  return pos;
};

const victoria = (pos, meta) => pos.x === meta.x && pos.y === meta.y;

let pos = { x: 0, y: 0 };
const meta = { x: 2, y: 2 };

while (true) {
  const dir = readline.question("🧭 Movimiento (N/S/E/O): ");
  pos = mover(pos, dir.toUpperCase());

  if (victoria(pos, meta)) {
    console.log(`🎊 ¡Victoria! Llegaste a (${meta.x}, ${meta.y})`);
    break;
  } else {
    console.log(`📍 Estás en: (${pos.x}, ${pos.y})`);
  }
}
```

🧠 *Objetivo:* Modularizar: mover, verificar, imprimir y finalizar.

## ✅ BONUS EDUCATIVO

Cada práctica permite al estudiante:

| Competencia clave        | Práctica aplicada                     |
| ------------------------ | ------------------------------------- |
| Pensamiento lógico       | Movimiento direccional y validaciones |
| Funciones en acción      | Modularización del código             |
| Orientación espacial     | Mapas, rutas y posiciones             |
| Programación interactiva | Entrada por teclado y ciclos de juego |