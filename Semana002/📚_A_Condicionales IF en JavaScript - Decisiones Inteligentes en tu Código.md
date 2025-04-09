# 📚 **Condicionales IF en JavaScript - Decisiones Inteligentes en tu Código**

## 🎯 OBJETIVO DEL MÓDULO

Que el estudiante:

- Comprenda el uso y sintaxis del condicional `if` en JavaScript.
- Aplique condicionales simples, múltiples (`if...else`, `else if`) y anidadas.
- Emplee ejemplos prácticos para la toma de decisiones en programas reales.
- Interprete diagramas de flujo que representen estructuras condicionales.

## 📦 CONTENIDO DEL MÓDULO

1. Introducción a las Condicionales
2. `if` simple
3. `if...else`
4. `if...else if...else`
5. Condicionales anidadas
6. Prácticas guiadas (con diagramas)
7. Proyecto Mini: Clasificador de edad
8. Evaluación de conceptos
9. Recomendaciones para profundizar

## 1️⃣ INTRODUCCIÓN A LAS CONDICIONALES

Las condicionales permiten que nuestros programas **tomen decisiones**, igual que lo hacemos los humanos:

> *"Si está lloviendo, entonces llevo paraguas. Si no, salgo sin él."*

En código:

```javascript
if (estaLloviendo) {
  console.log("Lleva paraguas ☔");
} else {
  console.log("No necesitas paraguas 😎");
}
```

## 2️⃣ `if` SIMPLE

La estructura más básica:

```javascript
if (condición) {
  // Código que se ejecuta si la condición es verdadera
}
```

🔍 **Ejemplo práctico 1: Validar mayoría de edad**

```javascript
const edad = 20;

if (edad >= 18) {
  console.log("Eres mayor de edad ✅");
}
```

🧠 **Diagrama de flujo:**

```
[Inicio]
   |
[edad >= 18?]
   | Sí
   V
["Mayor de edad"]
```

------

## 3️⃣ `if...else`

Nos permite tomar una **alternativa** si la condición no se cumple.

```javascript
if (condición) {
  // si es verdadero
} else {
  // si es falso
}
```

🔍 **Ejemplo práctico 2: Entrada a una fiesta**

```javascript
const tieneInvitacion = false;

if (tieneInvitacion) {
  console.log("Puedes entrar 🎉");
} else {
  console.log("Lo siento, necesitas una invitación 🚫");
}
```

🧠 **Diagrama de flujo:**

```css
[Inicio]
   |
[tieneInvitacion?]
  / \
Sí  No
|     \
["Entrar"] ["No pasar"]
```

------

## 4️⃣ `if...else if...else`

Cuando hay múltiples condiciones que queremos evaluar:

```javascript
const nota = 85;

if (nota >= 90) {
  console.log("Excelente 🏆");
} else if (nota >= 70) {
  console.log("Aprobado ✅");
} else {
  console.log("Reprobado ❌");
}
```

------

## 5️⃣ CONDICIONALES ANIDADAS

Una condicional **dentro de otra**. Útiles para decisiones más complejas.

🔍 **Ejemplo práctico 3: Clasificación por edad y género**

```javascript
const edad = 22;
const genero = "femenino";

if (edad >= 18) {
  if (genero === "femenino") {
    console.log("Eres una mujer adulta");
  } else {
    console.log("Eres un hombre adulto");
  }
} else {
  console.log("Eres menor de edad");
}
```

🧠 **Diagrama de flujo (resumen):**

```css
[Inicio]
   |
[edad >= 18?]
  / \
Sí   No
|     \
[genero === "femenino"?]  ["Menor de edad"]
   / \
  Sí  No
 /     \
["Mujer adulta"] ["Hombre adulto"]
```

## 6️⃣ PRÁCTICA GUIADA

> 🔧 **Caso real: Sistema de acceso a una aplicación bancaria**

- Si el usuario está **logueado**, mostrar el saldo.
- Si **no está logueado**, mostrar un mensaje de error.

```javascript
const estaLogueado = true;

if (estaLogueado) {
  console.log("Tu saldo es $1,000 💰");
} else {
  console.log("Debes iniciar sesión para ver tu saldo 🔒");
}
```

------

## 7️⃣ MINI PROYECTO: Clasificador de Edad

🎯 **Objetivo**: Construir un programa que clasifique edades.

```javascript
function clasificarEdad(edad) {
  if (edad < 13) {
    return "Niño";
  } else if (edad < 18) {
    return "Adolescente";
  } else if (edad < 60) {
    return "Adulto";
  } else {
    return "Adulto mayor";
  }
}

console.log(clasificarEdad(8));    // Niño
console.log(clasificarEdad(16));   // Adolescente
console.log(clasificarEdad(30));   // Adulto
console.log(clasificarEdad(70));   // Adulto mayor
```

## 8️⃣ EVALUACIÓN

### 📝 Preguntas de reflexión:

1. ¿Qué pasa si no coloco `else`?
2. ¿Qué ocurre si no uso `{}`?
3. ¿Es posible combinar múltiples condiciones usando `&&` o `||`?

### ✅ Ejercicio evaluado:

Completa el siguiente código para que imprima si un número es **positivo**, **negativo** o **cero**:

```javascript
const numero = -5;

// tu código aquí
```

✅ Respuesta esperada:

```javascript
if (numero > 0) {
  console.log("Positivo");
} else if (numero < 0) {
  console.log("Negativo");
} else {
  console.log("Cero");
}
```

## 9️⃣ RECOMENDACIONES FINALES

- Usa condicionales para evitar errores y validar datos.
- Lee tu código como si fuera una historia: "Si pasa esto, entonces haz aquello".
- Prueba con distintos valores y observa los resultados.