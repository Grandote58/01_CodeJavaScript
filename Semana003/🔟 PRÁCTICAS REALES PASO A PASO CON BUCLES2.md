## ✅ PRE-REQUISITO GENERAL

```bash
npm install readline-sync
```

Y recuerda importar al inicio de cada práctica:

```bash
const readline = require("readline-sync");
```

## 🔟 NUEVAS PRÁCTICAS CON BUCLES (Nivel Intermedio)

### 🧪 Práctica 11: **Simulador de entrada al cine**

**Objetivo:** Verificar edad de varios usuarios y permitir acceso solo a mayores de edad.

```javascript
let cantidad = parseInt(readline.question("🎟️ ¿Cuántas personas van a ingresar? "));
let permitidos = 0;

for (let i = 1; i <= cantidad; i++) {
  let edad = parseInt(readline.question(`Edad de la persona ${i}: `));
  if (edad >= 18) {
    console.log("✅ Acceso permitido");
    permitidos++;
  } else {
    console.log("🚫 Acceso denegado");
  }
}

console.log(`🔢 Total admitidos: ${permitidos}`);
```

### 🧪 Práctica 12: **Repetidor de frases**

**Objetivo:** Pedir una frase y repetirla N veces (útil en chatbots).

```javascript
let frase = readline.question("🗣️ Escribe una frase: ");
let repeticiones = parseInt(readline.question("🔁 ¿Cuántas veces deseas repetirla? "));

for (let i = 1; i <= repeticiones; i++) {
  console.log(`${i}. ${frase}`);
}
```

### 🧪 Práctica 13: **Simulador de carga de productos**

**Objetivo:** Cargar productos a una bodega hasta llenar un límite de peso.

```javascript
let pesoTotal = 0;
let producto;

do {
  let peso = parseFloat(readline.question("⚖️ Peso del producto en kg: "));
  pesoTotal += peso;
  producto = readline.question("¿Agregar otro producto? (s/n): ");
} while (producto.toLowerCase() === "s");

console.log(`📦 Peso total de carga: ${pesoTotal} kg`);
```

### 🧪 Práctica 14: **Verificador de números primos en un rango**

**Objetivo:** Mostrar los números primos entre 1 y 100.

```javascript
console.log("🔢 Números primos del 1 al 100:");

for (let num = 2; num <= 100; num++) {
  let esPrimo = true;

  for (let i = 2; i <= Math.sqrt(num); i++) {
    if (num % i === 0) {
      esPrimo = false;
      break;
    }
  }

  if (esPrimo) {
    console.log(num);
  }
}
```

### 🧪 Práctica 15: **Gestor de gastos personales**

**Objetivo:** Registrar montos de gastos hasta que se decida detener.

```javascript
let gasto;
let total = 0;

do {
  gasto = parseFloat(readline.question("💸 Ingrese un gasto (o 0 para finalizar): "));
  if (gasto > 0) total += gasto;
} while (gasto > 0);

console.log(`🧾 Gasto total del día: $${total.toFixed(2)}`);
```

### 🧪 Práctica 16: **Encuesta de satisfacción (escala 1 a 5)**

**Objetivo:** Registrar respuestas y mostrar promedios.

```javascript
let respuestas = 0;
let suma = 0;

do {
  let opinion = parseInt(readline.question("📝 Califica de 1 (malo) a 5 (excelente), o 0 para salir: "));
  if (opinion >= 1 && opinion <= 5) {
    suma += opinion;
    respuestas++;
  }
} while (suma === 0 || readline.keyInYN("¿Registrar otra respuesta?"));

if (respuestas > 0) {
  console.log(`📊 Promedio: ${(suma / respuestas).toFixed(2)} de 5`);
} else {
  console.log("❌ No se registraron respuestas válidas.");
}
```

### 🧪 Práctica 17: **Generador de secuencia Fibonacci**

**Objetivo:** Mostrar los primeros N términos de la secuencia de Fibonacci.

```javascript
let n = parseInt(readline.question("🔢 ¿Cuántos términos de Fibonacci quieres ver? "));
let a = 0, b = 1;

console.log("🔁 Secuencia Fibonacci:");
for (let i = 0; i < n; i++) {
  console.log(a);
  let siguiente = a + b;
  a = b;
  b = siguiente;
}
```

### 🧪 Práctica 18: **Simulador de progreso de descarga**

**Objetivo:** Simular visualmente una barra de progreso con `while`.

```javascript
let progreso = 0;

while (progreso <= 100) {
  console.log(`📥 Descargando... ${progreso}%`);
  progreso += 10;
}
console.log("✅ Descarga completada.");
```

### 🧪 Práctica 19: **Verificador de número palíndromo**

**Objetivo:** Comprobar si un número ingresado se lee igual al revés.

```javascript
let numero = readline.question("🔁 Ingresa un número: ");
let invertido = numero.split('').reverse().join('');

if (numero === invertido) {
  console.log("✅ Es un número palíndromo");
} else {
  console.log("❌ No es un número palíndromo");
}
```

### 🧪 Práctica 20: **Buscador de palabras clave en una lista**

**Objetivo:** Buscar cuántas veces aparece una palabra clave en una lista.

```javascript
const frases = [
  "Me encanta programar en JavaScript",
  "JavaScript es muy poderoso",
  "Aprendí bucles con JavaScript",
  "Amo la pizza 🍕",
  "Programar en JavaScript es divertido"
];

let palabraClave = readline.question("🔍 Palabra a buscar: ");
let contador = 0;

for (let frase of frases) {
  if (frase.toLowerCase().includes(palabraClave.toLowerCase())) {
    contador++;
  }
}

console.log(`✅ La palabra '${palabraClave}' aparece en ${contador} frases.`);
```

### 🧪 Práctica 21:  Identifica que hacen los siguientes códigos

```javascript
var readlineSync = require('readline-sync');
 
// Wait for user's response.
var userName = readlineSync.question('May I have your name? ');
console.log('Hi ' + userName + '!');
 
// Handle the secret text (e.g. password).
var favFood = readlineSync.question('What is your favorite food? ', {
  hideEchoBack: true // The typed text on screen is hidden by `*` (default).
});
console.log('Oh, ' + userName + ' loves ' + favFood + '!');
```

----

```javascript
var readlineSync = require('readline-sync');
if (readlineSync.keyInYN('Do you want this module?')) {
  // 'Y' key was pressed.
  console.log('Installing now...');
  // Do something...
} else {
  // Another key was pressed.
  console.log('Searching another...');
  // Do something...
}
```

-----

```javascript
var readlineSync = require('readline-sync'),
  animals = ['Lion', 'Elephant', 'Crocodile', 'Giraffe', 'Hippo'],
  index = readlineSync.keyInSelect(animals, 'Which animal?');
console.log('Ok, ' + animals[index] + ' goes to your room.');
```

-----

```javascript
var readlineSync = require('readline-sync'),
  MAX = 60, MIN = 0, value = 30, key;
console.log('\n\n' + (new Array(20)).join(' ') +
  '[Z] <- -> [X]  FIX: [SPACE]\n');
while (true) {
  console.log('\x1B[1A\x1B[K|' +
    (new Array(value + 1)).join('-') + 'O' +
    (new Array(MAX - value + 1)).join('-') + '| ' + value);
  key = readlineSync.keyIn('',
    {hideEchoBack: true, mask: '', limit: 'zx '});
  if (key === 'z') { if (value > MIN) { value--; } }
  else if (key === 'x') { if (value < MAX) { value++; } }
  else { break; }
}
console.log('\nA value the user requested: ' + value);
```

## 🔚 CONCLUSIÓN

Estas 10 nuevas prácticas están enfocadas en:

- 🔁 Repetición de acciones en contextos reales
- 🧠 Aplicaciones significativas y creativas
- 💬 Interacción fluida con el usuario vía consola
- 🛠️ Ejecución directa en Node.js