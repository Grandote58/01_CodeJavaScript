# 👉 Aprende a usar `readline` y operadores lógicos en JavaScript

## 👩‍🏫 OBJETIVO GENERAL

- Comprender cómo capturar datos desde consola con `readline` en Node.js.
- Utilizar operadores lógicos `AND`, `OR`, y `NOT` para crear condiciones complejas.
- Aplicar este conocimiento en ejemplos prácticos y reales.

## 🧠 CONTENIDO

1. ¿Qué es `readline`?

2. Configuración básica en Node.js

3. Sintaxis de operadores lógicos

4. Ejemplos con `&&`, `||`, `!`

5. Ejercicios guiados + soluciones

   

## 1️⃣ ¿QUÉ ES `readline`?

El módulo `readline` permite a los programas de Node.js **recibir texto del usuario por consola**, de forma similar a cómo funcionan los formularios web, pero desde terminal.

✅ Es muy útil para actividades prácticas con entrada de datos.

## 2️⃣ CONFIGURACIÓN BÁSICA DE `readline`

### 📦 Paso a paso

```javascript
// Paso 1: Importamos readline
const readline = require("readline");

// Paso 2: Creamos una interfaz
const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
});

// Paso 3: Hacemos una pregunta
rl.question("¿Cuál es tu nombre? ", (respuesta) => {
  console.log("Hola, " + respuesta + "!");
  rl.close(); // ¡Cierra después de recibir la respuesta!
});
```

📌 Para ejecutar:
 Guarda como `ejemplo.js` y corre con:

```bash
node ejemplo.js
```

## 3️⃣ OPERADORES LÓGICOS EN JAVASCRIPT

| Operador | Significado | Ejemplo         | Resultado |
| -------- | ----------- | --------------- | --------- |
| `&&`     | Y (AND)     | `true && false` | `false`   |
| `        |             | `               | O (OR)    |
| `!`      | Negación    | `!true`         | `false`   |

## 4️⃣ EJEMPLOS PRÁCTICOS CON `readline` Y OPERADORES LÓGICOS

### ✅ EJEMPLO 1: Verificar edad Y nacionalidad

📌 El usuario solo puede votar si tiene **18 años o más** **y** es de nacionalidad `"colombiana"`.

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("Ingresa tu edad: ", (edad) => {
  readline.question("Ingresa tu nacionalidad: ", (nacionalidad) => {
    if (edad >= 18 && nacionalidad === "colombiana") {
      console.log("Puedes votar 🗳️");
    } else {
      console.log("No puedes votar");
    }
    readline.close();
  });
});
```

### ✅ EJEMPLO 2: Entrada válida si tiene tarjeta O dinero

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("¿Tienes tarjeta? (sí/no): ", (tarjeta) => {
  readline.question("¿Tienes efectivo? (sí/no): ", (dinero) => {
    if (tarjeta === "sí" || dinero === "sí") {
      console.log("Puedes ingresar 🛒");
    } else {
      console.log("No puedes ingresar");
    }
    readline.close();
  });
});
```

### ✅ EJEMPLO 3: Validar si NO tiene bloqueos

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("¿Tu cuenta está bloqueada? (sí/no): ", (bloqueada) => {
  if (!(bloqueada === "sí")) {
    console.log("Acceso permitido ✅");
  } else {
    console.log("Acceso denegado ❌");
  }
  readline.close();
});
```

## 🧪 EJERCICIOS GUIADOS CON `readline` + LÓGICA

### ✅ EJERCICIO 1: Verifica si puedes ver una película

📌 Si tiene más de 13 años **y** permiso de los padres.

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("Edad: ", (edad) => {
  readline.question("¿Tienes permiso de tus padres? (sí/no): ", (permiso) => {
    if (edad >= 13 && permiso === "sí") {
      console.log("Puedes ver la película 🎬");
    } else {
      console.log("No puedes verla");
    }
    readline.close();
  });
});
```

### ✅ EJERCICIO 2: Acceso solo si es alumno o profesor

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("Rol (alumno/profesor/externo): ", (rol) => {
  if (rol === "alumno" || rol === "profesor") {
    console.log("Acceso autorizado");
  } else {
    console.log("Acceso denegado");
  }
  readline.close();
});
```

### ✅ EJERCICIO 3: Verificar disponibilidad de un producto

📌 Si el stock **no** está en cero.

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("Cantidad disponible: ", (cantidad) => {
  if (!(cantidad == 0)) {
    console.log("Producto disponible 📦");
  } else {
    console.log("Producto agotado");
  }
  readline.close();
});
```

## 🎯 CONCLUSIONES

✅ El módulo `readline` te permite crear experiencias interactivas desde consola.
 ✅ Los operadores lógicos permiten controlar múltiples condiciones al mismo tiempo.
 ✅ Combinarlos permite crear programas **reales y dinámicos**.