# 📘**Arreglos (Arrays) y Métodos Básicos**



> 🧠 **Objetivo de Aprendizaje:**
>  El estudiante comprenderá qué es un arreglo, cómo declararlo, acceder a sus elementos y manipularlo usando los métodos más comunes (`push`, `pop`, `shift`, `unshift`, `slice`, `splice`, `indexOf`, `includes`, `length`, `forEach`).

## 🧩 1. ¿Qué es un Array? 🔢

Un **array (arreglo)** es una estructura que **almacena múltiples valores** en una sola variable.

📦 Imagina una caja de herramientas con compartimentos:

 Cada compartimento tiene un elemento con su propia **posición (índice)**, empezando desde el **0**.

```javascript
let frutas = ["🍎 Manzana", "🍌 Banana", "🍇 Uvas"];
console.log(frutas);  // ["🍎 Manzana", "🍌 Banana", "🍇 Uvas"]
```

## 🧩 2. Acceder a los elementos de un Array 🎯

Para obtener un valor específico, usamos su **índice**:

```javascript
let frutas = ["🍎 Manzana", "🍌 Banana", "🍇 Uvas"];
console.log(frutas[0]);  // 🍎 Manzana
console.log(frutas[2]);  // 🍇 Uvas
```

## 🧩 3. Métodos básicos para **modificar** arrays 🛠️

### 📌 `push()` → Agrega un elemento al final

```javascript
let colores = ["🔴", "🟢"];
colores.push("🔵");
console.log(colores);  // ["🔴", "🟢", "🔵"]
```

### 📌 `pop()` → Elimina el último elemento

```javascript
colores.pop();
console.log(colores);  // ["🔴", "🟢"]
```

### 📌 `unshift()` → Agrega al inicio

```javascript
colores.unshift("🟡");
console.log(colores);  // ["🟡", "🔴", "🟢"]
```

### 📌 `shift()` → Elimina el primero

```javascript
colores.shift();
console.log(colores);  // ["🔴", "🟢"]
```

## 🧩 4. Métodos para trabajar con partes del Array 🧩

### 📌 `slice(inicio, fin)` → Devuelve una **copia parcial**

```javascript
let numeros = [10, 20, 30, 40, 50];
let mitad = numeros.slice(1, 4);  // 20, 30, 40
console.log(mitad);
```

⚠️ **No modifica** el array original.

### 📌 `splice(inicio, cantidad)` → **Quita o reemplaza** elementos

```javascript
numeros.splice(2, 1);  // Quita 1 elemento desde índice 2
console.log(numeros);  // [10, 20, 40, 50]
```

## 🧩 5. Otros métodos útiles 🤓

### 📌 `indexOf()` → Encuentra la posición de un valor

```
jsCopiarEditarlet nombres = ["Ana", "Luis", "Pedro"];
console.log(nombres.indexOf("Luis"));  // 1
```

### 📌 `includes()` → Verifica si un valor existe

```javascript
console.log(nombres.includes("Pedro"));  // true
```

### 📌 `.length` → Cuenta elementos

```javascript
console.log(nombres.length);  // 3
```

## 🧩 6. Recorrer un Array con `for` y `forEach()` 🔁

### 🔁 Usando `for`

```javascript
let animales = ["🐶", "🐱", "🐰"];

for (let i = 0; i < animales.length; i++) {
  console.log(`Animal ${i + 1}: ${animales[i]}`);
}
```

### 🔁 Usando `.forEach()`

```javascript
animales.forEach((animal, index) => {
  console.log(`Animal ${index + 1}: ${animal}`);
});
```

## 🧠 SÍNTESIS VISUAL DE MÉTODOS

| Método       | Acción                         |
| ------------ | ------------------------------ |
| `push()`     | Agrega al final                |
| `pop()`      | Elimina el último              |
| `shift()`    | Elimina el primero             |
| `unshift()`  | Agrega al inicio               |
| `slice()`    | Extrae parte (no modifica)     |
| `splice()`   | Elimina / reemplaza (modifica) |
| `indexOf()`  | Devuelve posición de elemento  |
| `includes()` | Verifica si existe             |
| `length`     | Cuenta elementos               |

