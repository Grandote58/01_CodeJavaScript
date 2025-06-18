# **🎬 *“¡Funciona Función! Aprende a Dominar Funciones y Tablas como un Pro”***

## 🎯 **OBJETIVOS DE APRENDIZAJE DE LA SEMANA:**

Al finalizar esta semana, los estudiantes serán capaces de:

- Comprender la estructura y utilidad de las funciones en JavaScript.
- Diferenciar entre funciones declarativas, funciones expresadas y funciones flecha.
- Aplicar funciones para modularizar código y evitar repetición.
- Utilizar funciones con parámetros y retorno de datos.
- Implementar `console.table()` para mostrar estructuras de datos complejas en formato visual.
- Generar, procesar y mostrar información en tabla a partir de estructuras como arrays y objetos.

# 📘 **SECCIÓN 1: CONCEPTO Y USO DE FUNCIONES EN JAVASCRIPT**

## ✅ ¿Qué es una función?

Una **función** es un bloque de código que puedes reutilizar. Sirve para organizar tu programa y no repetir instrucciones una y otra vez.

## 🔍 ¿Para qué se usan las funciones?

- Para **reutilizar código**.
- Para dividir el programa en **tareas pequeñas** (modularidad).
- Para **organizar la lógica** y facilitar el mantenimiento.
- Para hacer que tu código sea más **legible** y **profesional**.

# 📂 **TIPOS DE FUNCIONES EN JAVASCRIPT**

Las funciones son **bloques de código reutilizables** que realizan una tarea específica. JavaScript permite declarar funciones de distintas formas, cada una con sus características y ventajas. Aquí las conocerás todas 🧑‍🏫.

## 1️⃣ **🧱 Función Declarativa (Function Declaration)**

📌 **Sintaxis tradicional**. Se define con la palabra clave `function` y puede llamarse **antes o después** de su declaración.

### 📘 Ejemplo:

```javascript
function saludar(nombre) {
  console.log(`👋 ¡Hola, ${nombre}!`);
}

saludar("Ana");
```

✅ **Ventajas:**

- Puede usarse antes de que aparezca en el código gracias al *hoisting*.
- Muy clara y explícita para principiantes.

🔍 **Úsala cuando:** Necesites declarar funciones reutilizables de forma clara en cualquier parte del archivo.

## 2️⃣ **📦 Función Expresada (Function Expression)**

📌 Se **asigna a una variable**. El nombre puede ser opcional, pero normalmente se usa una función anónima.

### 📘 Ejemplo:

```javascript
const despedir = function(nombre) {
  console.log(`👋 Adiós, ${nombre}`);
};

despedir("Carlos");
```

⚠️ **Cuidado:** Solo puedes llamarla **después** de que ha sido definida (no tiene *hoisting*).

✅ **Ventajas:**

- Se puede usar como argumento o retornar desde otra función.
- Flexibilidad para funciones anónimas o dinámicas.

🔍 **Úsala cuando:** Quieras crear funciones internas, callbacks o lógica encapsulada.

## 3️⃣ **🚀 Función Flecha (Arrow Function)**

📌 Sintaxis moderna y compacta introducida en **ES6**. Ideal para funciones simples y expresiones.

### 📘 Ejemplo:

```javascript
const sumar = (a, b) => {
  return a + b;
};

console.log(`🧮 Resultado: ${sumar(5, 3)}`);
```

🧩 También puede escribirse en **una sola línea** si solo retorna un valor:

```javascript
const cuadrado = x => x * x;
console.log(`📐 Cuadrado: ${cuadrado(4)}`);
```

⚠️ **Nota importante:**

- No tiene su propio `this`, lo que la hace ideal para funciones dentro de objetos o clases.

✅ **Ventajas:**

- Más concisa, legible y elegante.
- Ideal para programación funcional y callbacks (como en `.map`, `.filter`, etc.).

🔍 **Úsala cuando:** Necesites funciones rápidas, especialmente en funciones de orden superior.



## 📊 COMPARATIVA VISUAL

| Tipo de Función     | ¿Tiene nombre? | ¿Tiene hoisting? | Sintaxis moderna | Usa `this` propio |
| ------------------- | -------------- | ---------------- | ---------------- | ----------------- |
| Declarativa         | ✅ Sí           | ✅ Sí             | ❌ No             | ✅ Sí              |
| Expresada           | ✅ Opcional     | ❌ No             | ❌ No             | ✅ Sí              |
| Función Flecha (=>) | ✅ Normalmente  | ❌ No             | ✅ Sí             | ❌ No              |