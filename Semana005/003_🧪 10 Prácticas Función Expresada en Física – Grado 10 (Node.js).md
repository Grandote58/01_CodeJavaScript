# 🧪 **10 Prácticas: Función Expresada en Física – Grado 10 (Node.js)**

> 📘 Todas las funciones aquí son **expresadas**, es decir, se almacenan en variables y no se pueden invocar antes de su declaración.

### ✅ Prerrequisitos para todas las prácticas

```python
npm install readline-sync
```

Y al inicio de cada archivo `.js`:

```javascript
const readline = require("readline-sync");
```

## 1️⃣ **Conversión de m/s a km/h (Function Expression)**

📘 Fórmula: `km/h = m/s * 3.6`

```javascript
const convertirVelocidad = function (velMs) {
  return velMs * 3.6;
};

let velMs = parseFloat(readline.question("🚀 Velocidad en m/s: "));
console.log(`🏎️ Velocidad en km/h: ${convertirVelocidad(velMs)} km/h`);
```

## 2️⃣ **Cálculo de presión**

📘 Fórmula: `Presión = Fuerza / Área`

```javascript
const calcularPresion = function (fuerza, area) {
  return fuerza / area;
};

let f = parseFloat(readline.question("💪 Fuerza (N): "));
let a = parseFloat(readline.question("🟦 Área (m²): "));
console.log(`🧯 Presión: ${calcularPresion(f, a)} Pa`);
```

## 3️⃣ **Conversión de calorías a Joules**

📘 Fórmula: `1 cal = 4.184 J`

```javascript
const caloriasAJoules = function (cal) {
  return cal * 4.184;
};

let cal = parseFloat(readline.question("🔥 Energía en calorías: "));
console.log(`⚡ Energía en Joules: ${caloriasAJoules(cal).toFixed(2)} J`);
```

## 4️⃣ **Ley de Hooke: Fuerza elástica**

📘 Fórmula: `F = k * x`

```javascript
const fuerzaElastica = function (k, x) {
  return k * x;
};

let constante = parseFloat(readline.question("🧷 Constante elástica (N/m): "));
let estiramiento = parseFloat(readline.question("📏 Estiramiento (m): "));
console.log(`💪 Fuerza elástica: ${fuerzaElastica(constante, estiramiento)} N`);
```

## 5️⃣ **Velocidad final en caída libre**

📘 Fórmula: `vf = g * t` (g = 9.8 m/s²)

```javascript
const velocidadFinal = function (tiempo) {
  const g = 9.8;
  return g * tiempo;
};

let tiempo = parseFloat(readline.question("⏱️ Tiempo de caída (s): "));
console.log(`🌍 Velocidad final: ${velocidadFinal(tiempo)} m/s`);
```

## 6️⃣ **Tiempo de caída libre desde cierta altura**

📘 Fórmula: `t = sqrt(2h / g)`

```javascript
const tiempoCaida = function (altura) {
  const g = 9.8;
  return Math.sqrt((2 * altura) / g);
};

let altura = parseFloat(readline.question("🗼 Altura (m): "));
console.log(`⏳ Tiempo de caída: ${tiempoCaida(altura).toFixed(2)} s`);
```

## 7️⃣ **Cálculo de densidad**

📘 Fórmula: `densidad = masa / volumen`

```javascript
const calcularDensidad = function (masa, volumen) {
  return masa / volumen;
};

let masa = parseFloat(readline.question("⚖️ Masa (kg): "));
let volumen = parseFloat(readline.question("🧪 Volumen (m³): "));
console.log(`🧊 Densidad: ${calcularDensidad(masa, volumen)} kg/m³`);
```

## 8️⃣ **Trabajo realizado por una fuerza**

📘 Fórmula: `Trabajo = F * d`

```javascript
const trabajoMecanico = function (fuerza, distancia) {
  return fuerza * distancia;
};

let fuerza = parseFloat(readline.question("💪 Fuerza (N): "));
let distancia = parseFloat(readline.question("📏 Distancia (m): "));
console.log(`🔧 Trabajo: ${trabajoMecanico(fuerza, distancia)} J`);
```

## 9️⃣ **Energía potencial gravitacional**

📘 Fórmula: `Ep = m * g * h`

```javascript
const energiaPotencial = function (masa, altura) {
  const g = 9.8;
  return masa * g * altura;
};

let masa = parseFloat(readline.question("⚖️ Masa (kg): "));
let altura = parseFloat(readline.question("📏 Altura (m): "));
console.log(`🏔️ Energía potencial: ${energiaPotencial(masa, altura)} J`);
```

## 🔟 **Energía cinética**

📘 Fórmula: `Ec = 0.5 * m * v²`

```javascript
const energiaCinetica = function (masa, velocidad) {
  return 0.5 * masa * velocidad ** 2;
};

let masa = parseFloat(readline.question("⚖️ Masa (kg): "));
let velocidad = parseFloat(readline.question("🚗 Velocidad (m/s): "));
console.log(`⚡ Energía cinética: ${energiaCinetica(masa, velocidad)} J`);
```

### 🎓 ¿Qué aprende el estudiante?

| Competencia                      | Desarrollada mediante...                |
| -------------------------------- | --------------------------------------- |
| Comprensión de funciones         | Uso de funciones expresadas en JS       |
| Aplicación de fórmulas físicas   | Codificación de expresiones algebraicas |
| Lógica y resolución de problemas | Input → procesamiento → output          |
| Pensamiento computacional        | Modularización del código               |