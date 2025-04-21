# 📘 MÓDULO SEMANA 3: Bucles e Iteraciones en JavaScript

> 🧠 **Objetivo de Aprendizaje:**
>  Comprender y aplicar de forma sólida las estructuras de control de flujo mediante bucles: `for`, `while`, y `do...while`, empleando problemas reales, contextos aplicados y casos de estudio.

> 🛠️ **Herramienta:** Node.js (usando consola)

## 🔧 Instrucción previa obligatoria para usar `readline-sync`

Enlace --: https://www.npmjs.com/package/readline-sync

Antes de ejecutar cualquier ejemplo que incluya la línea:

```javascript
const readline = require("readline-sync");
```

💥 Debes ejecutar en tu terminal el siguiente comando:

```bash
npm install readline-sync
```

## 🛠️ Instrucciones paso a paso para ejecutar cualquier ejemplo con Node.js:

1. **Crea un archivo JavaScript**, por ejemplo:
    `ejemplo1.js`
2. **Copia el código del ejemplo dentro del archivo**
3. **Abre tu terminal** y navega a la carpeta donde se encuentra el archivo:

```bash
cd ruta/a/tu/carpeta
```

1. **Instala la dependencia** (solo una vez por proyecto):

```bash
npm install readline-sync
```

1. **Ejecuta el archivo con Node.js:**

```bash
node ejemplo1.js
```

### 📦 Tip adicional para proyectos organizados

Si estás trabajando varios ejercicios:

```bash
mkdir semana1-bucles
cd semana1-bucles
npm init -y
npm install readline-sync
```

Luego puedes ir creando archivos `.js` por cada ejercicio y reutilizar el módulo instalado.

## 🧩 Sección 1: Fundamentos de los Bucles en JavaScript

### ¿Qué es un bucle?

Un bucle permite **repetir instrucciones** hasta que se cumple una condición determinada.

## 🧪 EJEMPLOS PRÁCTICOS

### ✅ 1. Bucle `for`: **Mostrar múltiplos de 5**

```javascript
// Múltiplos de 5 del 1 al 50
for (let i = 1; i <= 50; i++) {
  if (i % 5 === 0) {
    console.log(i);
  }
}
```

🧠 *¿Qué está pasando?*

El bucle `for` recorre del 1 al 50. Solo imprime aquellos números que sean divisibles por 5 (múltiplos de 5).

### ✅ 2. Bucle `while`: **Simular carga de batería**

```javascript
let carga = 0;

while (carga < 100) {
  carga += 20;
  console.log(`Batería cargando... ${carga}%`);
}
```

🧠 *¿Qué está pasando?*

El bucle se repite mientras la batería esté por debajo del 100%. Se simula un proceso repetitivo real como cargar un celular.

### ✅ 3. Bucle `do...while`: **Validar PIN de acceso (3 intentos)**

```javascript
const pinCorrecto = "1234";
let intentos = 0;
let acceso = false;

const readline = require("readline-sync");

do {
  const pin = readline.question("Introduce el PIN: ");
  intentos++;

  if (pin === pinCorrecto) {
    console.log("✅ Acceso permitido");
    acceso = true;
  } else {
    console.log("❌ PIN incorrecto. Intento", intentos);
  }

} while (!acceso && intentos < 3);

if (!acceso) {
  console.log("🚫 Cuenta bloqueada por intentos fallidos.");
}
```

🧠 *¿Qué está pasando?*

Se simula una situación real de seguridad: ingreso de PIN. El usuario tiene solo 3 intentos. Este bucle **siempre se ejecuta al menos una vez**, lo cual es ideal para este tipo de validaciones.

## 💼 CASO DE ESTUDIO: Supermercado Automatizado

> Simulación de un sistema que calcula el total de productos ingresados por el usuario hasta que decide terminar la compra.

```javascript
const readline = require("readline-sync");

let total = 0;
let seguirComprando;

do {
  const precio = parseFloat(readline.question("💲 Precio del producto: "));
  total += precio;

  seguirComprando = readline.question("¿Deseas ingresar otro producto? (s/n): ");

} while (seguirComprando.toLowerCase() === "s");

console.log("🧾 Total a pagar: $" + total.toFixed(2));
```

🎯 *Aplicación real*: Simula una caja registradora.

## ✍️ GUÍA PASO A PASO: Crear tu Propio "Sistema de Conteo de Estudiantes"

### 💡 Enunciado:

Queremos contar cuántos estudiantes se han registrado para una actividad extracurricular. El proceso termina cuando el usuario ingresa "fin".

### 🔨 Código:

```javascript
const readline = require("readline-sync");

let contador = 0;
let nombre;

do {
  nombre = readline.question("👤 Ingrese el nombre del estudiante (o escriba 'fin'): ");
  
  if (nombre.toLowerCase() !== "fin") {
    contador++;
  }

} while (nombre.toLowerCase() !== "fin");

console.log(`👨‍🎓 Total de estudiantes registrados: ${contador}`);
```

### 📌 Paso a paso explicado:

1. Usamos `readline-sync` para obtener datos desde consola
2. Creamos una variable `contador` para acumular cuántos estudiantes se registran
3. El bucle `do...while` asegura que al menos se pida un nombre
4. Terminamos cuando se escribe `"fin"`
5. Mostramos el total registrado