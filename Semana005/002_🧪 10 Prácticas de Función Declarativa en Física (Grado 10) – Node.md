# 🧪 **10 Prácticas de Función Declarativa en Física (Grado 10) – Node.js**

📌 **Objetivo transversal:** Aplicar funciones declarativas en JavaScript para resolver situaciones problema del área de física, fomentando el razonamiento lógico y el aprendizaje significativo a través de la programación.

### ✅ Prerrequisitos

Instala `readline-sync` una vez:

```bash
npm install readline-sync
```

Y en cada práctica importa al inicio:

```javascript
const readline = require("readline-sync");
```

## 1️⃣ **Calcular la velocidad media**

📘 Fórmula: `velocidad = distancia / tiempo`

```javascript
function calcularVelocidad(distancia, tiempo) {
  return distancia / tiempo;
}

let distancia = parseFloat(readline.question("📏 Distancia recorrida (m): "));
let tiempo = parseFloat(readline.question("⏱️ Tiempo empleado (s): "));

console.log(`🚀 Velocidad media: ${calcularVelocidad(distancia, tiempo)} m/s`);
```

## 2️⃣ **Conversión de grados Celsius a Kelvin**

📘 Fórmula: `K = °C + 273.15`

```javascript
function celsiusAKelvin(celsius) {
  return celsius + 273.15;
}

let temp = parseFloat(readline.question("🌡️ Temperatura en °C: "));
console.log(`🔥 Temperatura en Kelvin: ${celsiusAKelvin(temp)} K`);
```

## 3️⃣ **Calcular la aceleración**

📘 Fórmula: `a = (vf - vi) / t`

```javascript
function calcularAceleracion(vf, vi, tiempo) {
  return (vf - vi) / tiempo;
}

let vi = parseFloat(readline.question("🔰 Velocidad inicial (m/s): "));
let vf = parseFloat(readline.question("🏁 Velocidad final (m/s): "));
let t = parseFloat(readline.question("⏳ Tiempo (s): "));

console.log(`💨 Aceleración: ${calcularAceleracion(vf, vi, t)} m/s²`);
```

## 4️⃣ **Calcular la fuerza**

📘 Fórmula: `F = m * a`

```javascript
function calcularFuerza(masa, aceleracion) {
  return masa * aceleracion;
}

let masa = parseFloat(readline.question("⚖️ Masa (kg): "));
let aceleracion = parseFloat(readline.question("💨 Aceleración (m/s²): "));

console.log(`💪 Fuerza resultante: ${calcularFuerza(masa, aceleracion)} N`);
```

## 5️⃣ **Calcular el trabajo realizado**

📘 Fórmula: `Trabajo = Fuerza * Distancia`

```javascript
function calcularTrabajo(fuerza, distancia) {
  return fuerza * distancia;
}

let fuerza = parseFloat(readline.question("💪 Fuerza (N): "));
let distancia = parseFloat(readline.question("📏 Distancia (m): "));

console.log(`🔧 Trabajo realizado: ${calcularTrabajo(fuerza, distancia)} J`);
```

## 6️⃣ **Calcular energía cinética**

📘 Fórmula: `Ec = 0.5 * m * v²`

```javascript
function energiaCinetica(masa, velocidad) {
  return 0.5 * masa * velocidad ** 2;
}

let masa = parseFloat(readline.question("⚖️ Masa (kg): "));
let velocidad = parseFloat(readline.question("🚗 Velocidad (m/s): "));

console.log(`⚡ Energía cinética: ${energiaCinetica(masa, velocidad)} J`);
```

## 7️⃣ **Calcular energía potencial gravitacional**

📘 Fórmula: `Ep = m * g * h` (con g = 9.8 m/s²)

```javascript
function energiaPotencial(masa, altura, gravedad = 9.8) {
  return masa * gravedad * altura;
}

let masa = parseFloat(readline.question("⚖️ Masa (kg): "));
let altura = parseFloat(readline.question("📏 Altura (m): "));

console.log(`🏔️ Energía potencial: ${energiaPotencial(masa, altura)} J`);
```

## 8️⃣ **Calcular densidad**

📘 Fórmula: `densidad = masa / volumen`

```javascript
function calcularDensidad(masa, volumen) {
  return masa / volumen;
}

let masa = parseFloat(readline.question("⚖️ Masa (g): "));
let volumen = parseFloat(readline.question("🧪 Volumen (cm³): "));

console.log(`🧊 Densidad: ${calcularDensidad(masa, volumen)} g/cm³`);
```

## 9️⃣ **Conversión de m/s a km/h**

📘 Fórmula: `km/h = m/s * 3.6`

```javascript
function msAKmh(velocidad) {
  return velocidad * 3.6;
}

let velocidad = parseFloat(readline.question("🚀 Velocidad en m/s: "));
console.log(`🏎️ Velocidad en km/h: ${msAKmh(velocidad)} km/h`);
```

## 🔟 **Conversión de Joules a calorías**

📘 Fórmula: `1 cal = 4.184 J`

```javascript
function joulesACalorias(joules) {
  return joules / 4.184;
}

let energia = parseFloat(readline.question("⚡ Energía en Joules: "));
console.log(`🔥 Energía en calorías: ${joulesACalorias(energia).toFixed(2)} cal`);
```

### 🎓 ¿Qué habilidades desarrolla el estudiante?

| Habilidad                      | Aplicación en la práctica                |
| ------------------------------ | ---------------------------------------- |
| Lógica matemática              | Fórmulas físicas implementadas           |
| Lectura y escritura de código  | Sintaxis de funciones y tipos de datos   |
| Pensamiento computacional      | Entrada, procesamiento y salida de datos |
| Aprendizaje interdisciplinario | Física + Programación                    |