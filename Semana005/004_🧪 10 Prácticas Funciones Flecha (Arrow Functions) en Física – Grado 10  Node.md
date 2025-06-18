# 🧪 **10 Prácticas: Funciones Flecha (Arrow Functions) en Física – Grado 10 | Node.js**

> 📘 Las **arrow functions** (`=>`) permiten escribir funciones más compactas y modernas, ideales para cálculos rápidos y expresivos.

### ✅ Prerrequisitos (común para todos los ejercicios):

```javascript
npm install readline-sync
```

Y al inicio de cada archivo JS:

```javascript
const readline = require("readline-sync");
```

## 1️⃣ **Conversión de segundos a horas, minutos y segundos**

📘 Contexto: Conversión de tiempo para análisis cinemático.

```javascript
const convertirTiempo = segundos => {
  const horas = Math.floor(segundos / 3600);
  const minutos = Math.floor((segundos % 3600) / 60);
  const segRestantes = segundos % 60;
  return `${horas}h ${minutos}m ${segRestantes}s`;
};

let t = parseInt(readline.question("⏱️ Tiempo en segundos: "));
console.log(`🕒 Tiempo convertido: ${convertirTiempo(t)}`);
```

## 2️⃣ **Calcular velocidad angular**

📘 Fórmula: `ω = θ / t`

```javascript
const velocidadAngular = (angulo, tiempo) => angulo / tiempo;

let angulo = parseFloat(readline.question("🌀 Ángulo (rad): "));
let tiempo = parseFloat(readline.question("⏱️ Tiempo (s): "));
console.log(`🔄 Velocidad angular: ${velocidadAngular(angulo, tiempo)} rad/s`);
```

## 3️⃣ **Ley de Ohm: Calcular corriente**

📘 Fórmula: `I = V / R`

```javascript
const corriente = (voltaje, resistencia) => voltaje / resistencia;

let v = parseFloat(readline.question("🔌 Voltaje (V): "));
let r = parseFloat(readline.question("🧱 Resistencia (Ω): "));
console.log(`💡 Corriente: ${corriente(v, r)} A`);
```

## 4️⃣ **Calcular frecuencia**

📘 Fórmula: `f = 1 / T`

```javascript
const frecuencia = periodo => 1 / periodo;

let t = parseFloat(readline.question("🔄 Período (s): "));
console.log(`🎵 Frecuencia: ${frecuencia(t).toFixed(2)} Hz`);
```

## 5️⃣ **Calcular longitud de onda**

📘 Fórmula: `λ = v / f`

```javascript
const longitudOnda = (velocidad, frecuencia) => velocidad / frecuencia;

let v = parseFloat(readline.question("🌊 Velocidad de onda (m/s): "));
let f = parseFloat(readline.question("🎵 Frecuencia (Hz): "));
console.log(`📏 Longitud de onda: ${longitudOnda(v, f).toFixed(2)} m`);
```

## 6️⃣ **Convertir grados a radianes**

📘 Fórmula: `rad = grados * π / 180`

```javascript
const gradosARadianes = grados => (grados * Math.PI) / 180;

let grados = parseFloat(readline.question("📐 Ángulo en grados: "));
console.log(`🔁 Ángulo en radianes: ${gradosARadianes(grados).toFixed(4)} rad`);
```

## 7️⃣ **Calcular energía térmica**

📘 Fórmula: `Q = m * c * ΔT`

```javascript
const energiaTermica = (masa, calorEspecifico, deltaT) => masa * calorEspecifico * deltaT;

let m = parseFloat(readline.question("⚖️ Masa (kg): "));
let c = parseFloat(readline.question("🔥 Calor específico (J/kg°C): "));
let dT = parseFloat(readline.question("🌡️ Cambio de temperatura (°C): "));
console.log(`♨️ Energía térmica: ${energiaTermica(m, c, dT).toFixed(2)} J`);
```

## 8️⃣ **Calcular potencia eléctrica**

📘 Fórmula: `P = V * I`

```javascript
const potencia = (voltaje, corriente) => voltaje * corriente;

let v = parseFloat(readline.question("🔌 Voltaje (V): "));
let i = parseFloat(readline.question("⚡ Corriente (A): "));
console.log(`🔋 Potencia: ${potencia(v, i)} W`);
```

## 9️⃣ **Calcular índice de refracción**

📘 Fórmula: `n = c / v`

```javascript
const indiceRefraccion = (c, v) => c / v;

let c = 3e8; // velocidad de la luz en el vacío
let v = parseFloat(readline.question("💡 Velocidad en el medio (m/s): "));
console.log(`🔍 Índice de refracción: ${indiceRefraccion(c, v).toFixed(2)}`);
```

## 🔟 **Energía mecánica total**

📘 Fórmula: `Em = Ec + Ep`

```javascript
const energiaMecanica = (ec, ep) => ec + ep;

let ec = parseFloat(readline.question("⚙️ Energía cinética (J): "));
let ep = parseFloat(readline.question("🪨 Energía potencial (J): "));
console.log(`🛠️ Energía mecánica total: ${energiaMecanica(ec, ep)} J`);
```

## 🧠 **Reflexión pedagógica**

Estas prácticas permiten al estudiante:

| Competencia                     | Desarrollada mediante...                |
| ------------------------------- | --------------------------------------- |
| Dominio de funciones flecha     | Sintaxis moderna en JavaScript          |
| Aplicación de conceptos físicos | Fórmulas contextualizadas y programadas |
| Lógica matemática-computacional | Entrada → proceso → salida estructurada |
| Aprendizaje significativo       | Física aplicada a situaciones digitales |

