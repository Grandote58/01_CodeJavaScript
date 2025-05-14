

# 🧪 PRÁCTICA 

Aquí tienes **tres prácticas para cada uno de los métodos básicos de los arrays** en JavaScript (`push`, `pop`, `shift`, `unshift`, `slice`, `splice`, `indexOf`, `includes`, `length`, `forEach`), usando **números**, **cadenas**, y **booleanos**, explicadas de forma clara y aplicadas a contextos del mundo real 🌎.

## 🧰 MÉTODO: `push()` → **Agrega al final**

### ✅ Ejemplo 1 - Número 🔢

**Contexto:** Registro de temperaturas del día

```javascript
let temperaturas = [22, 24, 21];
temperaturas.push(25);
console.log(temperaturas); // [22, 24, 21, 25]
```

🧠 *Agrega una nueva temperatura al final de la lista.*

### ✅ Ejemplo 2 - Cadena 📝

**Contexto:** Añadir nuevo cliente a lista de espera

```javascript
let clientes = ["Ana", "Luis"];
clientes.push("Carlos");
console.log(clientes); // ["Ana", "Luis", "Carlos"]
```

🧠 *Cliente que llegó se pone al final de la fila.*

### ✅ Ejemplo 3 - Booleano ✅❌

**Contexto:** Registrar asistencia a clase

```javascript
let asistencia = [true, false, true];
asistencia.push(true);
console.log(asistencia); // [true, false, true, true]
```

🧠 *Se registra que un nuevo estudiante asistió.*

## 🧰 MÉTODO: `pop()` → **Elimina el último**

### ✅ Ejemplo 1 - Número 🔢

**Contexto:** Última calificación fue errónea

```javascript
let notas = [10, 9, 8];
notas.pop();
console.log(notas); // [10, 9]
```

🧠 *Se elimina la calificación equivocada.*

### ✅ Ejemplo 2 - Cadena 📝

**Contexto:** Se va el último de la fila

```javascript
let fila = ["Pedro", "Juan", "Sofía"];
fila.pop();
console.log(fila); // ["Pedro", "Juan"]
```

🧠 *La última persona ya fue atendida.*

### ✅ Ejemplo 3 - Booleano ✅❌

**Contexto:** El último dato de entrega de tareas no fue válido

```javascript
let entregas = [true, true, false];
entregas.pop();
console.log(entregas); // [true, true]
```

🧠 *Se corrige quitando el último valor.*

## 🧰 MÉTODO: `shift()` → **Elimina el primero**

### ✅ Ejemplo 1 - Número 🔢

**Contexto:** Primer pedido ya fue entregado

```javascript
let pedidos = [1201, 1202, 1203];
pedidos.shift();
console.log(pedidos); // [1202, 1203]
```

🧠 *Se retira el primer pedido atendido.*

### ✅ Ejemplo 2 - Cadena 📝

**Contexto:** Se despacha el primer producto

```javascript
let productos = ["Laptop", "Tablet", "Monitor"];
productos.shift();
console.log(productos); // ["Tablet", "Monitor"]
```

🧠 *Primer producto fue entregado.*

### ✅ Ejemplo 3 - Booleano ✅❌

**Contexto:** Primer estado de revisión ya no importa

```javascript
let revisiones = [false, true, true];
revisiones.shift();
console.log(revisiones); // [true, true]
```

🧠 *Eliminamos una revisión vieja.*

## 🧰 MÉTODO: `unshift()` → **Agrega al inicio**

### ✅ Ejemplo 1 - Número 🔢

**Contexto:** Nuevo turno llegó primero

```javascript
let turnos = [102, 103];
turnos.unshift(101);
console.log(turnos); // [101, 102, 103]
```

🧠 *Se agrega al principio de la cola.*

### ✅ Ejemplo 2 - Cadena 📝

**Contexto:** Agregar nueva noticia importante

```javascript
let noticias = ["Noticias locales", "Deportes"];
noticias.unshift("⚠️ Última hora");
console.log(noticias); // ["⚠️ Última hora", "Noticias locales", "Deportes"]
```

🧠 *Se inserta como la primera noticia.*

### ✅ Ejemplo 3 - Booleano ✅❌

**Contexto:** Registrar si una sesión fue grabada

```javascript
let sesionesGrabadas = [true, true];
sesionesGrabadas.unshift(false);
console.log(sesionesGrabadas); // [false, true, true]
```

🧠 *La primera sesión no fue grabada, se anota.*

## 🧰 MÉTODO: `slice()` → **Extrae una parte del array**

### ✅ Ejemplo 1 - Número 🔢

**Contexto:** Obtener primeras 3 calificaciones

```javascript
let notas = [10, 9, 8, 7, 6];
let primeras = notas.slice(0, 3);
console.log(primeras); // [10, 9, 8]
```

🧠 *Extraemos sin modificar el original.*

### ✅ Ejemplo 2 - Cadena 📝

**Contexto:** Mostrar primeras tareas asignadas

```javascript
let tareas = ["HTML", "CSS", "JS", "React"];
let intro = tareas.slice(0, 2);
console.log(intro); // ["HTML", "CSS"]
```

🧠 *Ideal para mostrar “nivel inicial” sin alterar.*

### ✅ Ejemplo 3 - Booleano ✅❌

**Contexto:** Revisar primeras 2 asistencias

```javascript
let asistencia = [true, false, true];
let primeras = asistencia.slice(0, 2);
console.log(primeras); // [true, false]
```

🧠 *Copiamos datos sin modificar la lista original.*

## 🧰 MÉTODO: `splice()` → **Quita o reemplaza elementos**

### ✅ Ejemplo 1 - Número 🔢

**Contexto:** Corregir nota equivocada en índice 2

```javascript
let notas = [10, 9, 0];
notas.splice(2, 1, 8);  // cambia 0 por 8
console.log(notas); // [10, 9, 8]
```

🧠 *Se reemplaza directamente el valor.*

### ✅ Ejemplo 2 - Cadena 📝

**Contexto:** Eliminar producto obsoleto

```
let inventario = ["Mouse", "Teclado", "Disquete"];
inventario.splice(2, 1);
console.log(inventario); // ["Mouse", "Teclado"]
```

🧠 *Remueve elemento en una posición específica.*

### ✅ Ejemplo 3 - Booleano ✅❌

**Contexto:** Corregir entrega que se marcó mal

```javascript
let entregas = [true, false, false];
entregas.splice(1, 1, true);
console.log(entregas); // [true, true, false]
```

🧠 *Reemplaza un dato booleano mal ingresado.*