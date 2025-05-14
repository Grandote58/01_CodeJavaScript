# 🧪 PRÁCTICA 01 - DESTACADAS: **Gestión de Clientes en Lista de Espera**

## **"Administrando mi fila 🧍‍♂️🧍‍♀️: Manejo de listas con Arrays"**

### 🎯 Objetivos de Aprendizaje:

- Comprender cómo se utiliza un **array** para almacenar datos de forma secuencial.
- Aplicar los métodos `.push()` y `.pop()` para **agregar** y **eliminar elementos** del array.
- Relacionar los conceptos con un **contexto real**: la gestión de una fila de espera de clientes en una tienda o sistema de atención.

### 🧠 Descripción de la práctica:

El estudiante simulará un sistema de **turnos**, donde podrá:

- Ingresar nuevos clientes en una lista
- Atender al último cliente ingresado
- Ver la lista actualizada de clientes en espera

### 💻 Código de la práctica:

```javascript
const readline = require("readline-sync");

let filaDeEspera = [];

let opcion;

do {
  console.log("\n📋 MENÚ");
  console.log("1. ➕ Agregar cliente");
  console.log("2. ➖ Atender último cliente");
  console.log("3. 📄 Ver lista de espera");
  console.log("4. 🚪 Salir");

  opcion = readline.question("Selecciona una opción: ");

  switch (opcion) {
    case "1":
      const cliente = readline.question("Nombre del cliente: ");
      filaDeEspera.push(cliente);
      console.log(`✅ ${cliente} ha sido agregado a la lista.`);
      break;

    case "2":
      if (filaDeEspera.length > 0) {
        const atendido = filaDeEspera.pop();
        console.log(`🧑‍⚕️ Atendiendo a: ${atendido}`);
      } else {
        console.log("❌ No hay clientes en la lista.");
      }
      break;

    case "3":
      console.log("📃 Lista actual:");
      filaDeEspera.forEach((c, i) => {
        console.log(`${i + 1}. ${c}`);
      });
      break;

    case "4":
      console.log("👋 Cerrando sistema...");
      break;

    default:
      console.log("❌ Opción inválida.");
  }

} while (opcion !== "4");
```

### ✅ Al finalizar la práctica el estudiante:

✔️ Comprenderá el funcionamiento básico de un array y cómo simular **estructuras dinámicas** (como una fila o cola).

✔️ Dominará los métodos `.push()`, `.pop()` y `.forEach()` para manipular datos reales.

✔️ Aplicará la lógica de programación a un **caso de uso cotidiano**, integrando entrada del usuario, lógica condicional y estructura repetitiva.

✔️ Estará listo para crear sistemas más complejos como listas de tareas, pedidos, asistentes virtuales o formularios dinámicos.

# 🧪 PRÁCTICA 2: **Encuesta de Opinión Exprés 🗣️📊**

## **"Voz del público: Analizando respuestas con Arrays"**

### 🎯 Objetivos de Aprendizaje:

- Reforzar el uso de **arrays de cadenas** (`string`) para almacenar información dinámica.
- Aplicar métodos como `.push()`, `.length`, y `.forEach()` para analizar datos.
- Simular una situación real de **recopilación de encuestas** y procesamiento de resultados.

### 💻 Código de la práctica:

```javascript
const readline = require("readline-sync");

let respuestas = [];
let respuesta;

console.log("📝 ENCUESTA: ¿Qué opinas de nuestro servicio?");

do {
  respuesta = readline.question("Escribe tu opinión o escribe 'fin' para terminar: ");
  if (respuesta.toLowerCase() !== "fin") {
    respuestas.push(respuesta);
  }
} while (respuesta.toLowerCase() !== "fin");

console.log("\n📊 RESULTADOS:");
console.log(`Total de respuestas: ${respuestas.length}`);

respuestas.forEach((resp, index) => {
  console.log(`${index + 1}. "${resp}"`);
});
```

### ✅ Al finalizar la práctica el estudiante:

✔️ Sabrá cómo **almacenar texto de usuarios** de forma dinámica usando `.push()`
 ✔️ Practicará `.length` para obtener cantidad de elementos
 ✔️ Usará `.forEach()` para mostrar datos en consola con formato
 ✔️ Relacionará arrays con **aplicaciones reales**: encuestas, formularios, feedbacks

# 🧪 PRÁCTICA 3: **Control de Temperatura 🌡️🔥**

## **"Monitoreo climático: Registrando temperaturas con JavaScript"**

### 🎯 Objetivos de Aprendizaje:

- Usar arrays numéricos para **almacenar y analizar datos físicos** (temperatura).
- Aplicar `.push()`, `.splice()` y bucles para capturar y modificar registros.
- Comprender cómo manejar una lista dinámica con valores numéricos reales.

### 💻 Código de la práctica:

```javascript
const readline = require("readline-sync");

let temperaturas = [];

for (let i = 1; i <= 5; i++) {
  let temp = parseFloat(readline.question(`🌡️ Ingresa la temperatura del día ${i}: `));
  temperaturas.push(temp);
}

console.log("\n📊 Temperaturas registradas:");
console.log(temperaturas);

// Corrección opcional de temperatura
let corregir = readline.question("\n¿Deseas corregir una temperatura? (s/n): ");

if (corregir.toLowerCase() === "s") {
  let indice = parseInt(readline.question("¿Qué día quieres corregir? (1-5): ")) - 1;
  let nuevaTemp = parseFloat(readline.question("🌡️ Nueva temperatura: "));
  temperaturas.splice(indice, 1, nuevaTemp);
}

console.log("\n📋 Temperaturas finales:");
temperaturas.forEach((t, i) => {
  console.log(`Día ${i + 1}: ${t}°C`);
});
```

### ✅ Al finalizar la práctica el estudiante:

✔️ Aprenderá a trabajar con **arrays numéricos reales**
 ✔️ Usará `.splice()` para **corregir valores** en una posición específica
 ✔️ Integrará entrada del usuario, control de flujo y manipulación de datos
 ✔️ Conectará la programación con una **aplicación científica o meteorológica**