# Practicas Evaluables: Uso de `readline` en JavaScript

> **🎓 Nivel:** Principiante
>  **🧑‍💻 Herramienta:** Node.js (ejecutar con `node ejercicioX.js`)
>  **📦 Modalidad:** Completa el código
>  **🎯 Objetivo:** Aprender a solicitar entrada por consola y usarla en estructuras condicionales básicas



## ✅ EJERCICIO 1: Tu nombre por consola

📌 Completa el siguiente código para que pregunte el nombre del usuario y lo salude.

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("_________________________", (nombre) => {
  console.log("Hola, " + ______________________ + "!");
  ______________________
});
```

## ✅ EJERCICIO 2: Validar si un número es mayor a 10

📌 Pide un número por consola. Si es mayor a 10, muestra "Es mayor a 10".

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("Ingresa un número: ", (numero) => {
  numero = _______________________;
  if (_____________________) {
    console.log("Es mayor a 10");
  }
  readline.close();
});
```

## ✅ EJERCICIO 3: Comprobar si una persona puede votar

📌 Solicita la edad. Si tiene 18 o más, puede votar.

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("¿Cuál es tu edad?: ", (edad) => {
  edad = parseInt(edad);
  
  if (_____________________) {
    console.log("Puedes votar 🗳️");
  } else {
    _______________________
  }

  readline.close();
});
```

## ✅ EJERCICIO 4: Verifica acceso con usuario y contraseña

📌 Si el usuario es `admin` y la clave es `1234`, muestra “Acceso concedido”.

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("Usuario: ", (usuario) => {
  readline.question("Contraseña: ", (clave) => {
    if (_____________________ && _____________________) {
      console.log("Acceso concedido ✅");
    } else {
      console.log("Acceso denegado ❌");
    }
    readline.close();
  });
});
```

## ✅ EJERCICIO 5: Clasifica una nota

📌 Pide una nota entre 0 y 100. Si es mayor a 90, imprime "Excelente".

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("Ingresa tu nota: ", (nota) => {
  nota = ______________________;

  if (nota > 90) {
    ______________________
  }

  ______________________
});
```

## ✅ EJERCICIO 6: Color primario

📌 Solicita un color. Si es rojo, azul o amarillo, muestra “Color primario”.

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("Ingresa un color: ", (color) => {
  if (_____________________ || _____________________ || _____________________) {
    console.log("Color primario 🎨");
  } else {
    console.log("No es color primario");
  }
  readline.close();
});
```

## ✅ EJERCICIO 7: ¿Eres estudiante?

📌 Pregunta si el usuario es estudiante. Si responde “sí”, muestra un mensaje de bienvenida.

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("¿Eres estudiante? (sí/no): ", (respuesta) => {
  if (_____________________) {
    console.log("¡Bienvenido estudiante! 🎓");
  }
  readline.close();
});
```

## ✅ EJERCICIO 8: Edad para ingresar a una discoteca

📌 Si la persona tiene 21 o más, puede ingresar.

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("Edad: ", (edad) => {
  edad = ______________________;

  if (_____________________) {
    console.log("Puedes ingresar 🎉");
  } else {
    ______________________
  }

  ______________________
});
```

### **✅ EJERCICIO 9: Saludo personalizado**

**Instrucción:** Solicita el nombre del usuario e imprime “Hola, [nombre]”.

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

// COMPLETA AQUÍ ↓
readline.question("____________________", (nombre) => {
  console.log("Hola, " + ___________________);
  readline._____________________;
});
```

📝 Resultado esperado:

```
Hola, Juan
```

------

### **✅ EJERCICIO 10: Suma de dos números**

**Instrucción:** Solicita dos números, súmalos e imprime el resultado.

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("Número 1: ", (num1) => {
  // COMPLETA AQUÍ ↓
  readline._________________("Número 2: ", (num2) => {
    let suma = ____________________;
    console.log("La suma es: " + suma);
    readline.____________________;
  });
});
```

📝 Resultado esperado:

```javascript
Número 1: 3
Número 2: 4
La suma es: 7
```

------

### **✅ EJERCICIO 11: Validar mayoría de edad**

**Instrucción:** Si edad >= 18, mostrar "Mayor de edad"

```
javascriptCopiarconst readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("¿Cuál es tu edad? ", (edad) => {
  // COMPLETA AQUÍ ↓
  if (__________________________) {
    console.log("Eres mayor de edad");
  } else {
    console.log("Eres menor de edad");
  }
  _______________________;
});
```

------

### **✅ EJERCICIO 12: Verifica acceso al sistema**

**Instrucción:** Usuario debe ingresar su contraseña. Si es `"admin123"`, se permite el acceso.

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("Contraseña: ", (clave) => {
  // COMPLETA AQUÍ ↓
  if (clave === "______________") {
    console.log("Acceso permitido");
  } else {
    console.log("Acceso denegado");
  }
  readline._____________________;
});
```

### **✅ EJERCICIO 13: ¿Puedes entrar al evento?**

**Instrucción:** Solo puede entrar si tiene más de 15 años y ha comprado entrada.

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("Edad: ", (edad) => {
  readline.question("¿Compraste entrada? (sí/no): ", (entrada) => {
    // COMPLETA AQUÍ ↓
    if (edad > 15 && entrada === "_________") {
      console.log("Puedes entrar 🎫");
    } else {
      console.log("No puedes entrar");
    }
    readline.____________________;
  });
});
```

### **✅ EJERCICIO 14: Detectar número par o impar**

**Instrucción:** Detecta si el número ingresado es par o impar.

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("Ingresa un número: ", (numero) => {
  numero = _____________________;
  if (numero % 2 === 0) {
    console.log("Es par");
  } else {
    console.log("Es impar");
  }
  readline._________________;
});
```

### **✅ EJERCICIO 15: ¿Es alumno o profesor?**

**Instrucción:** El sistema solo permite acceso a `"alumno"` o `"profesor"`.

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("¿Cuál es tu rol?: ", (rol) => {
  // COMPLETA AQUÍ ↓
  if (rol === "alumno" || ____________________) {
    console.log("Acceso permitido");
  } else {
    console.log("Acceso denegado");
  }
  readline._____________________;
});
```

### **✅ EJERCICIO 16: Clasificador de temperatura**

**Instrucción:**

- < 15: "Frío"

- 15 a 25: "Templado"

- > 25: "Calor"

```javascript
const readline = require("readline").createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.question("Temperatura actual (°C): ", (temp) => {
  temp = ___________________;

  // COMPLETA AQUÍ ↓
  if (temp < 15) {
    console.log("Frío ❄️");
  } else if (temp <= 25) {
    console.log("Templado 🌤️");
  } else {
    console.log("Calor ☀️");
  }

  _________________________;
});
```







