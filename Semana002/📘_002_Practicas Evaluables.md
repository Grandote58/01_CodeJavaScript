# 📘 Practicas Evaluables 

**Condicionales en JavaScript con `if`, `else`, `else if`, condicionales anidadas.**

## ✅ Ejercicio 1: Verifica si un número es positivo

📌 Crea un programa que imprima "Positivo" si el número es mayor a cero.

```javascript
const numero = 5;

// Escribe tu condicional aquí
```

## ✅ Ejercicio 2: Comprueba si un número es par

📌 Muestra “Es par” si el número es divisible entre 2.

```javascript
const numero = 8;

// Tu condicional
```

## ✅ Ejercicio 3: ¿Puedes entrar al cine?

📌 Si la edad es mayor o igual a 18, imprime “Bienvenido al cine para adultos”.

```javascript
const edad = 20;

// Escribe aquí
```

## ✅ Ejercicio 4: Verifica si un número es cero

📌 Si el número es igual a 0, imprime “El número es cero”.

```javascript
const numero = 0;

// Escribe aquí
```

## ✅ Ejercicio 5: Clasifica la temperatura

📌 Dado un número, clasifica así:

- Menor a 10 → "Hace frío"
- Entre 10 y 25 → "Clima agradable"
- Mayor a 25 → "Hace calor"

```javascript
const temperatura = 22;

// Usa if...else if...else
```

## ✅ Ejercicio 6: Verifica si alguien tiene acceso

📌 Usa dos variables: `usuarioLogueado` y `tienePermiso`

- Si ambas son verdaderas, imprime "Acceso concedido"
- Si no, "Acceso denegado"

```javascript
const usuarioLogueado = true;
const tienePermiso = false;

// Usa if con && lógico
```

## ✅ Ejercicio 7: Clasifica a una persona por edad

📌 Imprime:

- Menor a 13 → Niño
- 13 a 17 → Adolescente
- 18 a 64 → Adulto
- 65 o más → Adulto mayor

```javascript
const edad = 67;

// Escribe los condicionales necesarios
```

## ✅ Ejercicio 8: ¿Hay descuentos?

📌 Si el cliente es mayor de 60 o menor de 12, imprime "Descuento aplicado"

```javascript
const edad = 11;

// Usa || para combinar condiciones
```

## ✅ Ejercicio 9: Verifica calificación académica

📌 Muestra:

- 90 o más → “Sobresaliente”
- 70 a 89 → “Aprobado”
- Menos de 70 → “Reprobado”

```javascript
const nota = 78;

// Escribe los condicionales necesarios

```

## ✅ Ejercicio 10: Validación de contraseña

📌 Si la contraseña es igual a `"admin123"`, imprime “Acceso autorizado”.

```javascript
const contraseña = "admin123";

// if con comparación de strings
```

## ✅ Ejercicio 11: Comparación de dos números

📌 Dados dos números, imprime el mayor. Si son iguales, muestra "Son iguales".

```javascript
const num1 = 8;
const num2 = 12;

// Escribe los condicionales necesarios
```

## ✅ Ejercicio 12: Verifica si hay stock de producto

📌 Si la cantidad es mayor que 0, imprime "Producto disponible", de lo contrario, "Agotado".

```javascript
const stock = 0;

// Escribe los condicionales necesarios
```

## ✅ Ejercicio 13: Condicional anidada para calificaciones

📌 Si la calificación es válida (entre 0 y 100), evalúa:

- > = 90: “Excelente”

- > = 75: “Muy bien”

- > = 50: “Regular”

- Menor de 50: “Insuficiente”

❗ Si no está entre 0 y 100, imprime "Calificación inválida"

```javascript
const calificacion = 101;

// Usa una condicional dentro de otra
```

## ✅ Ejercicio 14: Clasificador de colores primarios

📌 Si el color es `"rojo"`, `"azul"` o `"amarillo"` muestra "Color primario", si no "Color no primario".

```javascript
const color = "verde";

// if con varias condiciones
```

## ✅ Ejercicio 15: Evalúa si se puede conducir

📌 Si la persona tiene más de 18 años **y** tiene licencia (`tieneLicencia === true`), imprime “Puedes conducir”.

```javascript
const edad = 19;
const tieneLicencia = true;

// Escribe los condicionales necesarios
```

# 📋 RECOMENDACIONES FINALES PARA LOS ESTUDIANTES

- Antes de probar tu código, **lee la lógica como si fuera una historia**.
- Ejecuta tu script en la terminal con `node ejercicioX.js`.
- Haz pruebas con **diferentes valores** para verificar todos los caminos posibles del condicional.
- Tómate tu tiempo, reflexiona sobre el "¿por qué?" de cada respuesta.