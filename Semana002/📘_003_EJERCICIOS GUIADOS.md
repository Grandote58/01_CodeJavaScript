# ⚙️ INSTRUCCIONES TÉCNICAS

- Ejecuta los ejercicios en Node.js
- Asegúrate de tener habilitado `readline` para entrada por consola
- Todos los ejemplos están listos para copiar y pegar en un archivo `.js`

# 📚 EJERCICIOS PRACTICOS

**Entrada por consola + condicionales `if`, `else`, `else if`, anidados**

### ✅ EJERCICIO 01: ¿Es mayor de edad?

📌 Solicita la edad del usuario y muestra si es mayor de edad (18+).

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("Ingresa tu edad: ", (edad) => {
  if (edad >= 18) {
    console.log("Eres mayor de edad ✅");
  } else {
    console.log("Eres menor de edad ❌");
  }
  readline.close();
});
```

------

### ✅ EJERCICIO 02: Verificar si un número es positivo, negativo o cero

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("Ingresa un número: ", (numero) => {
  numero = parseInt(numero);
  if (numero > 0) {
    console.log("Es positivo");
  } else if (numero < 0) {
    console.log("Es negativo");
  } else {
    console.log("Es cero");
  }
  readline.close();
});
```

### ✅ EJERCICIO 03: Acceso al sistema según rol

📌 Solicita el tipo de rol (`admin`, `editor`, `lector`) y muestra un mensaje diferente para cada uno.

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("Escribe tu rol (admin/editor/lector): ", (rol) => {
  if (rol === "admin") {
    console.log("Tienes acceso total al sistema");
  } else if (rol === "editor") {
    console.log("Puedes editar contenido");
  } else if (rol === "lector") {
    console.log("Solo puedes leer");
  } else {
    console.log("Rol no reconocido");
  }
  readline.close();
});
```

### ✅ EJERCICIO 04: ¿Puede conducir?

📌 Solicita edad y si tiene licencia (sí/no).

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("¿Cuál es tu edad?: ", (edad) => {
  readline.question("¿Tienes licencia? (sí/no): ", (licencia) => {
    if (edad >= 18 && licencia === "sí") {
      console.log("Puedes conducir 🚗");
    } else {
      console.log("No puedes conducir");
    }
    readline.close();
  });
});
```

### ✅ EJERCICIO 05: Calificación académica

📌 Ingresa la nota y clasifícala:

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("Ingresa tu calificación (0-100): ", (nota) => {
  nota = parseFloat(nota);

  if (nota >= 90) {
    console.log("Excelente");
  } else if (nota >= 70) {
    console.log("Aprobado");
  } else {
    console.log("Reprobado");
  }

  readline.close();
});
```

### ✅ EJERCICIO 06: ¿Color primario?

📌 Pregunta por un color y verifica si es primario.

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("Ingresa un color: ", (color) => {
  if (color === "rojo" || color === "azul" || color === "amarillo") {
    console.log("Es un color primario 🎨");
  } else {
    console.log("No es un color primario");
  }
  readline.close();
});
```

### ✅ EJERCICIO 07: Validación de usuario y contraseña

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("Usuario: ", (usuario) => {
  readline.question("Contraseña: ", (clave) => {
    if (usuario === "admin" && clave === "1234") {
      console.log("Acceso autorizado");
    } else {
      console.log("Acceso denegado");
    }
    readline.close();
  });
});
```

### ✅ EJERCICIO 08: Número dentro de rango

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("Ingresa un número (entre 1 y 100): ", (numero) => {
  numero = parseInt(numero);
  if (numero >= 1 && numero <= 100) {
    console.log("Número dentro del rango");
  } else {
    console.log("Número fuera del rango");
  }
  readline.close();
});
```

### ✅ EJERCICIO 09: Edad para categorías

📌 Categorías:

- <13: niño
- 13-17: adolescente
- 18-59: adulto
- 60+: adulto mayor

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("¿Qué edad tienes?: ", (edad) => {
  edad = parseInt(edad);
  if (edad < 13) {
    console.log("Niño");
  } else if (edad < 18) {
    console.log("Adolescente");
  } else if (edad < 60) {
    console.log("Adulto");
  } else {
    console.log("Adulto mayor");
  }
  readline.close();
});
```

------

### ✅ EJERCICIO 10: Día de la semana válido

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("Ingresa un día de la semana: ", (dia) => {
  if (
    dia === "lunes" ||
    dia === "martes" ||
    dia === "miércoles" ||
    dia === "jueves" ||
    dia === "viernes" ||
    dia === "sábado" ||
    dia === "domingo"
  ) {
    console.log("Día válido");
  } else {
    console.log("Día inválido");
  }
  readline.close();
});
```

### ✅ EJERCICIO 11: Evaluar si puede ingresar al club

📌 Edad mínima 21 años

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("Edad: ", (edad) => {
  if (edad >= 21) {
    console.log("Puedes ingresar al club 🎉");
  } else {
    console.log("No tienes edad suficiente");
  }
  readline.close();
});
```

### ✅ EJERCICIO 12: Temperatura para actividades

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("Temperatura en °C: ", (temp) => {
  temp = parseInt(temp);
  if (temp < 15) {
    console.log("Hace frío, abrígate ❄️");
  } else if (temp <= 25) {
    console.log("Clima agradable 😊");
  } else {
    console.log("Hace calor, mantente hidratado ☀️");
  }
  readline.close();
});
```

### ✅ EJERCICIO 13: Monto de compra con descuento

📌 Si la compra es mayor a $100, aplica 10% de descuento

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("Monto de compra: ", (monto) => {
  monto = parseFloat(monto);
  if (monto > 100) {
    const total = monto * 0.9;
    console.log("Descuento aplicado. Total a pagar: $" + total.toFixed(2));
  } else {
    console.log("Total a pagar: $" + monto);
  }
  readline.close();
});
```

### ✅ EJERCICIO 14: Verifica si el número es divisible entre 3 y 5

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("Ingresa un número: ", (num) => {
  num = parseInt(num);
  if (num % 3 === 0 && num % 5 === 0) {
    console.log("Es divisible entre 3 y 5");
  } else {
    console.log("No es divisible entre 3 y 5");
  }
  readline.close();
});
```