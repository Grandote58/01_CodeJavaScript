# 📘 EJERCICIOS GUIADOS 

**Condicionales en JavaScript sin funciones**

 💻 Ejecutar con `Node.js` usando `node ejercicioX.js`

### ✅ EJERCICIO 01: Determina si un número es impar

📌 Si el número no es divisible entre 2, imprime `"Es impar"`

```javascript
const numero = 7;

if (numero % 2 !== 0) {
  console.log("Es impar");
}
```

### ✅ EJERCICIO 02: Verifica si alguien tiene acceso premium

📌 Si `tipoUsuario` es `"premium"`, muestra "Bienvenido usuario premium".

```javascript
const tipoUsuario = "premium";

if (tipoUsuario === "premium") {
  console.log("Bienvenido usuario premium");
}
```

### ✅ EJERCICIO 03: Indica si hay cupos disponibles

📌 Si el número de cupos es **mayor a cero**, muestra "Cupos disponibles", si no "Curso lleno".

```javascript
const cupos = 0;

if (cupos > 0) {
  console.log("Cupos disponibles");
} else {
  console.log("Curso lleno");
}
```

### ✅ EJERCICIO 04: Valida si el día es laboral

📌 Si el día es `"lunes"`, `"martes"`, `"miércoles"`, `"jueves"` o `"viernes"`, imprime "Día laboral"

```javascript
const dia = "domingo";

if (
  dia === "lunes" ||
  dia === "martes" ||
  dia === "miércoles" ||
  dia === "jueves" ||
  dia === "viernes"
) {
  console.log("Día laboral");
} else {
  console.log("Fin de semana");
}
```

### ✅ EJERCICIO 05: Muestra si una persona tiene derecho a votar

📌 Edad mínima para votar: 16 años

```javascript
const edad = 14;

if (edad >= 16) {
  console.log("Puede votar");
} else {
  console.log("No puede votar");
}
```

### ✅ EJERCICIO 06: Evalúa si hay clima favorable

📌 Si la temperatura está entre 20 y 30 (inclusive), imprime "Clima ideal para salir".

```javascript
const temperatura = 24;

if (temperatura >= 20 && temperatura <= 30) {
  console.log("Clima ideal para salir");
} else {
  console.log("Mejor quedarse en casa");
}
```

### ✅ EJERCICIO 07: Clasifica el puntaje de un juego

📌 Según el puntaje:

- 100 → "Perfecto"
- 50 a 99 → "Buen intento"
- Menos de 50 → "Sigue practicando"

```javascript
const puntaje = 75;

if (puntaje === 100) {
  console.log("Perfecto");
} else if (puntaje >= 50) {
  console.log("Buen intento");
} else {
  console.log("Sigue practicando");
}
```

### ✅ EJERCICIO 08: Verifica si el año es bisiesto (simplificado)

📌 Si el año es divisible entre 4, muestra "Es año bisiesto"

```javascript
const anio = 2024;

if (anio % 4 === 0) {
  console.log("Es año bisiesto");
} else {
  console.log("No es año bisiesto");
}
```

### ✅ EJERCICIO 09: Comprueba si un estudiante puede obtener beca

📌 Si su nota es mayor a 90 y tiene menos de 20 años

```javascript
const nota = 95;
const edad = 18;

if (nota > 90 && edad < 20) {
  console.log("Puede obtener la beca");
} else {
  console.log("No cumple con los requisitos");
}
```

### ✅ EJERCICIO 10: Evalúa si el nombre de usuario es válido

📌 Si el `username` no está vacío, imprime "Nombre válido"

```javascript
const username = "juan123";

if (username !== "") {
  console.log("Nombre válido");
} else {
  console.log("Nombre inválido");
}
```

### ✅ EJERCICIO 11: Verifica si un usuario está conectado

📌 Si `conectado === true`, muestra "En línea"

```javascript
const conectado = false;

if (conectado) {
  console.log("En línea");
} else {
  console.log("Desconectado");
}
```

### ✅ EJERCICIO 12: Clasifica el peso de un paquete

📌 Muestra:

- < 5kg → “Ligero”

- 5-20kg → “Mediano”

- > 20kg → “Pesado”

```javascript
const peso = 10;

if (peso < 5) {
  console.log("Ligero");
} else if (peso <= 20) {
  console.log("Mediano");
} else {
  console.log("Pesado");
}
```

### ✅ EJERCICIO 13: Validación de login simple

📌 Si el usuario y contraseña coinciden, permite el acceso.

```javascript
const usuario = "admin";
const contraseña = "1234";

if (usuario === "admin" && contraseña === "1234") {
  console.log("Acceso concedido");
} else {
  console.log("Acceso denegado");
}
```

### ✅ EJERCICIO 14: Determina si un número está fuera de un rango

📌 Muestra “Fuera de rango” si el número **no está** entre 1 y 100

```javascript
const numero = 150;

if (numero < 1 || numero > 100) {
  console.log("Fuera de rango");
} else {
  console.log("Dentro del rango");
}
```

### ✅ EJERCICIO 15: Identifica el trimestre del año

📌 Según el mes, imprime el trimestre correspondiente

```javascript
const mes = 5;

if (mes >= 1 && mes <= 3) {
  console.log("Primer trimestre");
} else if (mes >= 4 && mes <= 6) {
  console.log("Segundo trimestre");
} else if (mes >= 7 && mes <= 9) {
  console.log("Tercer trimestre");
} else if (mes >= 10 && mes <= 12) {
  console.log("Cuarto trimestre");
} else {
  console.log("Mes inválido");
}
```