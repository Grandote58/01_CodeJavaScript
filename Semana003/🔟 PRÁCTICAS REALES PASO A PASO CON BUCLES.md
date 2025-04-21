# 🔟 PRÁCTICAS REALES PASO A PASO CON BUCLES

### 🧪 Práctica 1: **Contador de estudiantes registrados**

**Objetivo:** Contar cuántos estudiantes se registran hasta que se escriba "fin".

```javascript
const readline = require("readline-sync");

let nombre;
let contador = 0;

do {
  nombre = readline.question("👤 Nombre del estudiante (o escribe 'fin' para terminar): ");
  if (nombre.toLowerCase() !== "fin") {
    contador++;
  }
} while (nombre.toLowerCase() !== "fin");

console.log(`✅ Total de estudiantes registrados: ${contador}`);
```

### 🧪 Práctica 2: **Cálculo de ahorro acumulado**

**Objetivo:** El usuario introduce cuánto ahorra por día hasta llegar o superar los $1000.

```javascript
const readline = require("readline-sync");

let total = 0;
let dias = 0;

while (total < 1000) {
  let ahorro = parseFloat(readline.question("💰 Ingrese cuánto desea ahorrar hoy: "));
  total += ahorro;
  dias++;
}

console.log(`🎉 Lograste ahorrar $${total.toFixed(2)} en ${dias} días.`);
```

### 🧪 Práctica 3: **Calculadora de promedio académico**

**Objetivo:** Calcular el promedio de N notas ingresadas por el usuario.

```
const readline = require("readline-sync");

let cantidad = parseInt(readline.question("📚 ¿Cuántas notas desea ingresar? "));
let suma = 0;

for (let i = 1; i <= cantidad; i++) {
  let nota = parseFloat(readline.question(`Ingrese nota ${i}: `));
  suma += nota;
}

let promedio = suma / cantidad;
console.log(`📊 Promedio final: ${promedio.toFixed(2)}`);
```

### 🧪 Práctica 4: **Verificador de contraseñas (3 intentos)**

**Objetivo:** Permitir 3 intentos para ingresar la contraseña correcta.

```javascript
const readline = require("readline-sync");

const password = "javascript123";
let intentos = 0;
let acceso = false;

do {
  let entrada = readline.question("🔐 Ingrese la contraseña: ");
  intentos++;

  if (entrada === password) {
    acceso = true;
    console.log("✅ Acceso concedido.");
  } else {
    console.log("❌ Contraseña incorrecta.");
  }

} while (!acceso && intentos < 3);

if (!acceso) {
  console.log("🚫 Cuenta bloqueada.");
}
```

------

### 🧪 Práctica 5: **Tablas de multiplicar dinámicas**

**Objetivo:** Generar la tabla de multiplicar para un número elegido.

```javascript
const readline = require("readline-sync");

let numero = parseInt(readline.question("🔢 Ingrese un número para ver su tabla de multiplicar: "));

for (let i = 1; i <= 10; i++) {
  console.log(`${numero} x ${i} = ${numero * i}`);
}
```

### 🧪 Práctica 6: **Simulador de turnos (cola de atención)**

**Objetivo:** Registrar nombres en una cola hasta que se escriba "fin".

```javascript
const readline = require("readline-sync");

let turno = 1;
let nombre;

do {
  nombre = readline.question("👤 Ingrese nombre (o escriba 'fin' para terminar): ");
  if (nombre.toLowerCase() !== "fin") {
    console.log(`🔔 Turno #${turno} - ${nombre}`);
    turno++;
  }
} while (nombre.toLowerCase() !== "fin");
```

### 🧪 Práctica 7: **Contador de pares e impares**

**Objetivo:** Ingresar 10 números y contar cuántos son pares e impares.

```javascript
const readline = require("readline-sync");

let pares = 0;
let impares = 0;

for (let i = 1; i <= 10; i++) {
  let num = parseInt(readline.question(`Ingrese el número ${i}: `));
  if (num % 2 === 0) {
    pares++;
  } else {
    impares++;
  }
}

console.log(`✅ Pares: ${pares}, Impares: ${impares}`);
```

### 🧪 Práctica 8: **Menú interactivo con bucle**

**Objetivo:** Crear un menú de opciones con `do...while`

```javascript
const readline = require("readline-sync");

let opcion;

do {
  console.log("\n📋 MENÚ:");
  console.log("1. Saludar");
  console.log("2. Decir hora");
  console.log("3. Salir");

  opcion = readline.question("Seleccione una opción: ");

  switch (opcion) {
    case "1":
      console.log("👋 ¡Hola, usuario!");
      break;
    case "2":
      console.log(`🕒 La hora es: ${new Date().toLocaleTimeString()}`);
      break;
    case "3":
      console.log("👋 Saliendo...");
      break;
    default:
      console.log("❌ Opción no válida.");
  }

} while (opcion !== "3");
```

### 🧪 Práctica 9: **Juego de adivinar el número**

**Objetivo:** El usuario intenta adivinar un número secreto.

```javascript
const readline = require("readline-sync");

const secreto = Math.floor(Math.random() * 100) + 1;
let intento;
let contador = 0;

do {
  intento = parseInt(readline.question("🎯 Adivina el número (1-100): "));
  contador++;

  if (intento < secreto) {
    console.log("📉 Demasiado bajo");
  } else if (intento > secreto) {
    console.log("📈 Demasiado alto");
  }

} while (intento !== secreto);

console.log(`🎉 ¡Correcto! Lo lograste en ${contador} intentos.`);
```

### 🧪 Práctica 10: **Simulación de encuesta**

**Objetivo:** Registrar respuestas (sí/no) y contar estadísticas.

```javascript
const readline = require("readline-sync");

let si = 0;
let no = 0;
let respuesta;

do {
  respuesta = readline.question("¿Te gusta programar? (s/n, escribe 'fin' para salir): ").toLowerCase();

  if (respuesta === "s") {
    si++;
  } else if (respuesta === "n") {
    no++;
  }

} while (respuesta !== "fin");

console.log(`📝 Resultados:\n👍 Sí: ${si}\n👎 No: ${no}`);
```

## 🧠 ¿Qué se trabaja con estas prácticas?



| Práctica                    | Lógica desarrollada                 |
| --------------------------- | ----------------------------------- |
| 1 - Registro de estudiantes | Control de flujo y entrada de datos |
| 2 - Ahorro acumulado        | Condicional con while               |
| 3 - Promedio de notas       | Ciclo for + operaciones             |
| 4 - Validación de login     | Seguridad básica                    |
| 5 - Tabla multiplicar       | Repetición controlada               |
| 6 - Turnos                  | Simulación de procesos              |
| 7 - Pares/Impares           | Clasificación y conteo              |
| 8 - Menú interactivo        | Programas tipo consola              |
| 9 - Juego del número        | Aleatoriedad + lógica               |
| 10 - Encuesta               | Entrada de datos y análisis         |