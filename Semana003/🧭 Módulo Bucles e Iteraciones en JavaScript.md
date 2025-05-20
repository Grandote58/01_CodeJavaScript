# 🧭 Módulo: **Bucles e Iteraciones en JavaScript**

📌 **Objetivo general**: Comprender y aplicar los bucles `for`, `while`, y `do...while` para ejecutar tareas repetitivas de forma eficiente. Al finalizar, serás capaz de crear ciclos controlados que ahorran tiempo y código, con ejemplos interactivos que usan template literals para visualizar los resultados.

## 📄 LECCIÓN 1: **Template Literals: Imprime con estilo**

### 🎯 Objetivo:

Aprender a utilizar los **template literals** (plantillas literales) para crear salidas más legibles en consola y mejorar la comprensión de la lógica de iteración.

### 🧠 ¿Qué son los template literals?

Los template literals son una forma moderna de crear cadenas de texto. Se escriben con **backticks** (```) en lugar de comillas.

✅ Ventajas:

- Permiten interpolación: `${expresion}`
- Pueden abarcar múltiples líneas
- Más legibles y ordenadas

### 📌 Ejemplo simple:

```javascript
const nombre = "Juan";
const edad = 17;

console.log(`Hola, mi nombre es ${nombre} y tengo ${edad} años.`);
```

⏬ Salida en consola:

```bash
Hola, mi nombre es Juan y tengo 17 años.
```

### ✨ Aplicación en bucles:

```javascript
for (let i = 1; i <= 3; i++) {
  console.log(`📌 Iteración número: ${i}`);
}
```

⏬ Salida:

```javascript
📌 Iteración número: 1
📌 Iteración número: 2
📌 Iteración número: 3
```

## 📄 LECCIÓN 2: **El bucle for: repite con control total**

### 🎯 Objetivo:

Aprender a usar el bucle `for` para repetir instrucciones con un número exacto de veces.

### 🧠 ¿Qué es `for`?

Un bucle `for` se usa cuando sabes cuántas veces necesitas repetir algo. Tiene tres partes:

```javascript
for (inicio; condición; actualización) {
  // código a repetir
}
```

### 📌 Ejemplo práctico: contar del 1 al 5

```javascript
for (let i = 1; i <= 5; i++) {
  console.log(`🔁 Contando: ${i}`);
}
```

⏬ Salida:

```bash
🔁 Contando: 1
🔁 Contando: 2
🔁 Contando: 3
🔁 Contando: 4
🔁 Contando: 5
```

### 💡 Ejercicio guiado:

🔨 Crea una tabla de multiplicar del 2:

```javascript
for (let i = 1; i <= 10; i++) {
  console.log(`2 x ${i} = ${2 * i}`);
}
```

⏬ Salida esperada:

```bash
2 x 1 = 2
2 x 2 = 4
...
2 x 10 = 20
```

## 📄 LECCIÓN 3: **El bucle while: repite mientras algo sea verdadero**

### 🎯 Objetivo:

Comprender y aplicar el bucle `while` para repetir acciones mientras una condición se mantenga verdadera.

### 🧠 ¿Cómo funciona `while`?

```javascript
while (condición) {
  // se repite si la condición es true
}
```

⚠️ ¡Cuidado! Si nunca se vuelve falsa, puede causar un bucle infinito.

### 📌 Ejemplo práctico: contar hasta que una variable llegue a 5

```javascript
contador = 1;

while (contador <= 5) {
  console.log(`📈 Subiendo el contador: ${contador}`);
  contador++;
}
```

⏬ Salida:

```bash
📈 Subiendo el contador: 1
📈 Subiendo el contador: 2
...
📈 Subiendo el contador: 5
```

### 💡 Ejercicio guiado:

🔨 Cuenta regresiva desde 5 a 1:

```javascript
let cuenta = 5;

while (cuenta >= 1) {
  console.log(`⏳ Cuenta regresiva: ${cuenta}`);
  cuenta--;
}
```

## 📄 LECCIÓN 4: **El bucle do...while: ejecuta primero, evalúa después**

### 🎯 Objetivo:

Utilizar `do...while` para asegurarse de que un bloque de código se ejecute al menos una vez.

### 🧠 ¿Cómo funciona `do...while`?

```javascript
do {
  // se ejecuta una vez antes de evaluar la condición
} while (condición);
```

### 📌 Ejemplo práctico: pedir confirmación

```javascript
let intentos = 0;
let clave;

do {
  clave = "1234"; // simulación de ingreso de clave
  console.log(`🔐 Intento número ${++intentos}`);
} while (clave !== "1234");
```

⏬ Salida:

```bash
🔐 Intento número 1
```

### 💡 Ejercicio guiado:

🔨 Simula un dado que lanza hasta obtener un 6

```javascript
let dado;

do {
  dado = Math.ceil(Math.random() * 6);
  console.log(`🎲 Resultado del dado: ${dado}`);
} while (dado !== 6);

console.log(`🎉 ¡Sacaste un 6!`);
```

⏬ Posible salida:

```bash
🎲 Resultado del dado: 3
🎲 Resultado del dado: 4
🎲 Resultado del dado: 6
🎉 ¡Sacaste un 6!
```

## 📌 RESUMEN VISUAL DE BUCLES

| Tipo de Bucle | ¿Cuándo usarlo?                    | Evalúa antes o después |
| ------------- | ---------------------------------- | ---------------------- |
| `for`         | Repeticiones conocidas             | Antes                  |
| `while`       | Condición dinámica o indeterminada | Antes                  |
| `do...while`  | Ejecutar mínimo una vez            | Después                |



# 🎮 Mini Juego: **¡Adivina el número secreto!**

📌 **Objetivo de aprendizaje**:

- Aplicar bucles (`while`, `do...while`)
- Usar `Math.random()` y `template literals`
- Reforzar lógica condicional y control de flujo

## 🧩 INTRODUCCIÓN DEL JUEGO

> El sistema elegirá un número secreto al azar entre 1 y 10.
>  El jugador debe adivinarlo. Si falla, el sistema dará pistas.
>  ¡Tienes 5 intentos! Al final, ganás o perdés.

## 📁 Paso 0: Prepara tu entorno

1. Asegúrate de tener Node.js instalado (`node -v`)
2. Crea un archivo llamado `adivinaNumero.js`

## 🧱 Paso 1: Importar módulos necesarios

```javascript
const readline = require('readline');
```

Este módulo permite leer entradas del teclado (estándar en Node.js).

## 🧱 Paso 2: Configura la interfaz de entrada

```javascript
const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout
});
```

Esto nos permitirá pedir datos al usuario desde la terminal.

## 🧠 Paso 3: Define el número secreto y otras variables

```javascript
const numeroSecreto = Math.ceil(Math.random() * 10);
let intentos = 0;
const maxIntentos = 5;
```

## 🔁 Paso 4: Función principal del juego

Creamos una función que se ejecuta recursivamente hasta acertar o agotar intentos.

```javascript
function jugar() {
  rl.question(`🔢 Adivina un número del 1 al 10 (Intento ${intentos + 1}/${maxIntentos}): `, (respuesta) => {
    const intentoUsuario = Number(respuesta);
    intentos++;

    if (intentoUsuario === numeroSecreto) {
      console.log(`🎉 ¡Felicidades! Adivinaste el número secreto: ${numeroSecreto}`);
      rl.close();
    } else if (intentos >= maxIntentos) {
      console.log(`💥 ¡Agotaste tus intentos! El número era: ${numeroSecreto}`);
      rl.close();
    } else {
      const pista = intentoUsuario < numeroSecreto ? "📈 Es más alto" : "📉 Es más bajo";
      console.log(`❌ Incorrecto. ${pista}`);
      jugar(); // Llamada recursiva para el siguiente intento
    }
  });
}
```

## 🟢 Paso 5: Inicia el juego

```javascript
console.log("🎮 ¡Bienvenido al juego Adivina el Número!");
jugar();
```

## 🧪 Código completo listo para ejecutar:

```javascript
// archivo: adivinaNumero.js
const readline = require('readline');

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout
});

const numeroSecreto = Math.ceil(Math.random() * 10);
let intentos = 0;
const maxIntentos = 5;

function jugar() {
  rl.question(`🔢 Adivina un número del 1 al 10 (Intento ${intentos + 1}/${maxIntentos}): `, (respuesta) => {
    const intentoUsuario = Number(respuesta);
    intentos++;

    if (intentoUsuario === numeroSecreto) {
      console.log(`🎉 ¡Felicidades! Adivinaste el número secreto: ${numeroSecreto}`);
      rl.close();
    } else if (intentos >= maxIntentos) {
      console.log(`💥 ¡Agotaste tus intentos! El número era: ${numeroSecreto}`);
      rl.close();
    } else {
      const pista = intentoUsuario < numeroSecreto ? "📈 Es más alto" : "📉 Es más bajo";
      console.log(`❌ Incorrecto. ${pista}`);
      jugar(); // sigue jugando
    }
  });
}

console.log("🎮 ¡Bienvenido al juego Adivina el Número!");
jugar();
```

## 🧠 REFLEXIÓN Y EXTENSIONES

- ¿Qué pasa si cambias el rango a 1-100?

- ¿Puedes guardar los intentos en un arreglo y mostrarlos al final?

  



# 🎯 Mini Juego Gamificado: **¡Escape del Laberinto!**

> Un clásico reinventado: estás atrapado en un laberinto y tienes que encontrar la salida moviéndote por coordenadas. El objetivo es llegar a la posición secreta antes de agotar tus pasos.

## 🎮 Objetivo de Aprendizaje:

- Reforzar el uso de bucles `while`, condiciones y operadores
- Implementar lógica de estado y movimiento
- Mejorar lectura de inputs y salidas con `template literals`
- Aplicar funciones y diseño de juego modular

## ⚙️ Mecánica del Juego

- Eres un aventurero en un mapa de 5x5.
- Inicias en la posición `(0, 0)` (esquina superior izquierda).
- Tienes 10 pasos para encontrar la posición secreta (la salida).
- Puedes moverte con comandos: `N`, `S`, `E`, `O`.
- El sistema te da retroalimentación visual de tu posición.
- ¡Si llegas a la meta antes de agotar los pasos, ganas!

## ✅ Paso 0: Crear el archivo del juego

Crea un archivo en tu proyecto:

```bash
escapeLaberinto.js
```

## ✅ Paso 1: Importar el módulo readline

```javascript
const readline = require('readline');
```

## ✅ Paso 2: Configurar la interfaz de entrada

```javascript
const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout
});
```

## ✅ Paso 3: Definir variables del juego

```javascript
const maxFilas = 5;
const maxColumnas = 5;
const maxMovimientos = 10;

let posicion = { fila: 0, columna: 0 };
const salida = { fila: Math.floor(Math.random() * maxFilas), columna: Math.floor(Math.random() * maxColumnas) };
let movimientos = 0;
```

## ✅ Paso 4: Función para mostrar la posición del jugador

```javascript
function mostrarPosicion() {
  console.log(`📍 Estás en la posición: (${posicion.fila}, ${posicion.columna})`);
}
```

## ✅ Paso 5: Función para verificar si ganaste

```javascript
function verificarVictoria() {
  return posicion.fila === salida.fila && posicion.columna === salida.columna;
}
```

## ✅ Paso 6: Función para mover al jugador

```javascript
function mover(direccion) {
  switch (direccion.toUpperCase()) {
    case 'N':
      if (posicion.fila > 0) posicion.fila--;
      else console.log('⛔ No puedes moverte más al norte.');
      break;
    case 'S':
      if (posicion.fila < maxFilas - 1) posicion.fila++;
      else console.log('⛔ No puedes moverte más al sur.');
      break;
    case 'E':
      if (posicion.columna < maxColumnas - 1) posicion.columna++;
      else console.log('⛔ No puedes moverte más al este.');
      break;
    case 'O':
      if (posicion.columna > 0) posicion.columna--;
      else console.log('⛔ No puedes moverte más al oeste.');
      break;
    default:
      console.log('❓ Dirección inválida. Usa N, S, E u O.');
  }
}
```

## ✅ Paso 7: Función principal del juego

```
function jugar() {
  if (verificarVictoria()) {
    console.log(`🎉 ¡Has escapado del laberinto en ${movimientos} movimientos! La salida estaba en (${salida.fila}, ${salida.columna}).`);
    rl.close();
    return;
  }

  if (movimientos >= maxMovimientos) {
    console.log(`💀 Te perdiste en el laberinto. La salida estaba en (${salida.fila}, ${salida.columna}).`);
    rl.close();
    return;
  }

  mostrarPosicion();
  rl.question(`🔀 Movimiento #${movimientos + 1}/${maxMovimientos} - Elige dirección (N/S/E/O): `, (direccion) => {
    mover(direccion);
    movimientos++;
    jugar();
  });
}
```

## ✅ Paso 8: Iniciar el juego

```javascript
console.log("🧭 ¡Bienvenido a ESCAPE DEL LABERINTO!");
console.log("🎯 Llega a la salida en 10 movimientos o menos.");
console.log("📌 Movimientos válidos: N (norte), S (sur), E (este), O (oeste)");
jugar();
```

## 🧪 Código completo para copiar y pegar

```javascript
// archivo: escapeLaberinto.js
const readline = require('readline');

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout
});

const maxFilas = 5;
const maxColumnas = 5;
const maxMovimientos = 10;

let posicion = { fila: 0, columna: 0 };
const salida = {
  fila: Math.floor(Math.random() * maxFilas),
  columna: Math.floor(Math.random() * maxColumnas)
};
let movimientos = 0;

function mostrarPosicion() {
  console.log(`📍 Estás en la posición: (${posicion.fila}, ${posicion.columna})`);
}

function verificarVictoria() {
  return posicion.fila === salida.fila && posicion.columna === salida.columna;
}

function mover(direccion) {
  switch (direccion.toUpperCase()) {
    case 'N':
      if (posicion.fila > 0) posicion.fila--;
      else console.log('⛔ No puedes moverte más al norte.');
      break;
    case 'S':
      if (posicion.fila < maxFilas - 1) posicion.fila++;
      else console.log('⛔ No puedes moverte más al sur.');
      break;
    case 'E':
      if (posicion.columna < maxColumnas - 1) posicion.columna++;
      else console.log('⛔ No puedes moverte más al este.');
      break;
    case 'O':
      if (posicion.columna > 0) posicion.columna--;
      else console.log('⛔ No puedes moverte más al oeste.');
      break;
    default:
      console.log('❓ Dirección inválida. Usa N, S, E u O.');
  }
}

function jugar() {
  if (verificarVictoria()) {
    console.log(`🎉 ¡Has escapado del laberinto en ${movimientos} movimientos! La salida estaba en (${salida.fila}, ${salida.columna}).`);
    rl.close();
    return;
  }

  if (movimientos >= maxMovimientos) {
    console.log(`💀 Te perdiste en el laberinto. La salida estaba en (${salida.fila}, ${salida.columna}).`);
    rl.close();
    return;
  }

  mostrarPosicion();
  rl.question(`🔀 Movimiento #${movimientos + 1}/${maxMovimientos} - Elige dirección (N/S/E/O): `, (direccion) => {
    mover(direccion);
    movimientos++;
    jugar();
  });
}

console.log("🧭 ¡Bienvenido a ESCAPE DEL LABERINTO!");
console.log("🎯 Llega a la salida en 10 movimientos o menos.");
console.log("📌 Movimientos válidos: N (norte), S (sur), E (este), O (oeste)");
jugar();
```