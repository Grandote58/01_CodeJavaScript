![logo](https://github.com/Grandote58/Laravel_Magic/blob/main/Img/LogoGR58_1.png)

# 🚀 **Ejercicios Prácticos de Introducción a JavaScript**

Estos ejercicios están diseñados para reforzar el aprendizaje sobre **variables, tipos de datos y operaciones básicas en JavaScript**. Se recomienda realizarlos en **Visual Studio Code** y ejecutarlos con **Node.js**.

## **Ejercicio 1: Presentación Personal**

**Enunciado:**
Crea un programa que almacene tu nombre, edad y país en variables y luego las muestre en la consola con un mensaje de presentación.

### **Pasos a seguir:**

1. Crea un archivo `presentacion.js`.
2. Declara variables para el **nombre**, **edad** y **país**.
3. Usa `console.log()` para imprimir el mensaje.
4. Ejecuta el programa con `node presentacion.js`.

### **Código en JavaScript:**

```javascript
let nombre = "Carlos";
let edad = 17;
let pais = "México";

console.log("¡Hola! Mi nombre es " + nombre + ", tengo " + edad + " años y soy de " + pais + ".");
```

------

## **Ejercicio 2: Suma de Dos Números**

**Enunciado:**
Escribe un programa que sume dos números y muestre el resultado en la consola.

### **Pasos a seguir:**

1. Crea un archivo `suma.js`.
2. Declara dos variables con números.
3. Suma los valores y almacena el resultado en otra variable.
4. Muestra el resultado en la consola.

### **Código en JavaScript:**

```javascript
let numero1 = 8;
let numero2 = 5;
let suma = numero1 + numero2;

console.log("La suma de", numero1, "y", numero2, "es:", suma);
```

## **Ejercicio 3: Multiplicación de Dos Números**

**Enunciado:**
Crea un programa que multiplique dos números y muestre el resultado.

### **Código en JavaScript:**

```javascript
let num1 = 7;
let num2 = 3;
let resultado = num1 * num2;

console.log("El resultado de la multiplicación es:", resultado);
```

------

## **Ejercicio 4: Calculando el Perímetro de un Cuadrado**

**Enunciado:**
Escribe un programa que calcule el **perímetro de un cuadrado** dado el valor de su lado.

### **Código en JavaScript:**

```javascript
let lado = 5;
let perimetro = lado * 4;

console.log("El perímetro del cuadrado es:", perimetro);
```

## **Ejercicio 5: Transformación de Grados Celsius a Fahrenheit**

**Enunciado:**
Convierte una temperatura en grados Celsius a Fahrenheit usando la fórmula:

 💡 `F = (C × 9/5) + 32`

### **Código en JavaScript:**

```javascript
let celsius = 25;
let fahrenheit = (celsius * 9/5) + 32;

console.log(celsius + "°C equivalen a " + fahrenheit + "°F.");
```

------

## **Ejercicio 6: Determinar el Año de Nacimiento**

**Enunciado:**
Escribe un programa que calcule el año de nacimiento de una persona con base en su edad actual.

### **Código en JavaScript:**

```javascript
let edad = 16;
let añoActual = 2024;
let añoNacimiento = añoActual - edad;

console.log("Tu año de nacimiento es:", añoNacimiento);
```

## **Ejercicio 7: Precio Final con Descuento**

**Enunciado:**
Calcula el precio final de un producto aplicando un **descuento del 20%**.

### **Código en JavaScript:**

```javascript
let precioOriginal = 100;
let descuento = precioOriginal * 0.2;
let precioFinal = precioOriginal - descuento;

console.log("El precio final con descuento es:", precioFinal);
```

## **Ejercicio 8: Verificar si un Número es Par o Impar**

**Enunciado:**
Escribe un programa que determine si un número ingresado es par o impar.

### **Código en JavaScript:**

```javascript
let numero = 15;

if (numero % 2 === 0) {
    console.log("El número", numero, "es par.");
} else {
    console.log("El número", numero, "es impar.");
}
```



## **Ejercicio 9: Intercambiar Valores de Dos Variables**

**Enunciado:**
Intercambia los valores de dos variables sin introducir nuevos valores manualmente.

### **Código en JavaScript:**

```javascript
let a = 5;
let b = 10;

console.log("Antes: a =", a, "y b =", b);

let temp = a;
a = b;
b = temp;

console.log("Después: a =", a, "y b =", b);
```

## **Ejercicio 10: Operaciones con Cadenas de Texto**

**Enunciado:**
Concatena dos cadenas de texto y muestra el resultado en mayúsculas.

### **Código en JavaScript:**

```javascript
let texto1 = "Hola";
let texto2 = "Mundo";

let resultado = (texto1 + " " + texto2).toUpperCase();
console.log(resultado);
```

------

## **Ejercicio 11: Calcular la Hipotenusa de un Triángulo**

**Enunciado:**
Dado un triángulo rectángulo con catetos `a` y `b`, calcula la hipotenusa usando **el teorema de Pitágoras**.

### **Código en JavaScript:**

```javascript
let a = 3;
let b = 4;
let hipotenusa = Math.sqrt((a * a) + (b * b));

console.log("La hipotenusa es:", hipotenusa);
```

## **Ejercicio 12: Determinar si un Número es Positivo o Negativo**

### **Código en JavaScript:**

```javascript
let numero = -10;

if (numero >= 0) {
    console.log("El número es positivo.");
} else {
    console.log("El número es negativo.");
}
```

------

## **Ejercicio 13: Cálculo del Área de un Círculo**

### **Código en JavaScript:**

```javascript
const PI = 3.1416;
let radio = 6;
let area = PI * (radio * radio);

console.log("El área del círculo es:", area);
```

------

## **Ejercicio 14: Conversión de Horas a Minutos y Segundos**

### **Código en JavaScript:**

```javascript
let horas = 2;
let minutos = horas * 60;
let segundos = minutos * 60;

console.log(horas + " horas equivalen a " + minutos + " minutos o " + segundos + " segundos.");
```



## **Ejercicio 15: Verificar si un Año es Bisiesto**

### **Código en JavaScript:**

```javascript
let año = 2024;

if ((año % 4 === 0 && año % 100 !== 0) || año % 400 === 0) {
    console.log(año, "es un año bisiesto.");
} else {
    console.log(año, "no es un año bisiesto.");
}
```

### 📢 **¡Felicitaciones! Ahora tienes 15 nuevos ejercicios para mejorar tu lógica en JavaScript. 🚀**



## **Ejercicio 16: Convertir Metros a Kilómetros**

**Enunciado:**
Escribe un programa que convierta una distancia en **metros** a **kilómetros**.

### **Pasos a seguir:**

1. Crea un archivo `conversion.js`.
2. Declara una variable con una distancia en metros.
3. Convierte la distancia a kilómetros (`1 km = 1000 m`).
4. Muestra el resultado en la consola.

## **Ejercicio 17: Determinar si un Número es Múltiplo de 5**

**Enunciado:**
Escribe un programa que verifique si un número es **múltiplo de 5**.

### **Pasos a seguir:**

1. Declara una variable con un número.
2. Usa el operador **módulo (%)** para verificar si el número es divisible por 5.
3. Muestra el resultado en la consola.

## **Ejercicio 18: Contar Caracteres de un Texto**

**Enunciado:**
Crea un programa que cuente cuántos caracteres tiene una palabra o frase.

### **Pasos a seguir:**

1. Declara una variable con un texto.
2. Usa la propiedad `.length` para contar los caracteres.
3. Muestra el resultado en la consola.

## **Ejercicio 19: Comparar Dos Números**

**Enunciado:**
Escribe un programa que compare dos números e indique cuál es mayor, menor o si son iguales.

### **Pasos a seguir:**

1. Declara dos variables con números.
2. Usa estructuras condicionales (`if-else`) para compararlos.
3. Muestra el resultado en la consola.

## **Ejercicio 20: Calcular el IVA de un Producto**

**Enunciado:**
Escribe un programa que calcule el **precio final de un producto con IVA** (Impuesto al Valor Agregado).

📌 **Supongamos que el IVA es del 19%**.

### **Pasos a seguir:**

1. Declara una variable con el precio del producto.
2. Calcula el IVA multiplicando por **0.19**.
3. Suma el IVA al precio original.
4. Muestra el precio final en la consola.



## 📢 **¡Listo! Ahora tienes 5 ejercicios más para practicar JavaScript. 🚀💡**









