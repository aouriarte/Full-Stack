# Tipos de Datos

## Primitivos

Son datos que no son un objeto y no tienen métodos. Se accede directamente al valor.

### **Strings**

Es una cadena de carácteres, que se define entre comillas dobles `""` o simples `''`.

```js
var mascota = "perro";
```

- `.length`

La propiedad de `String` representa la longitud de una cadena:

```js
var name = "Alexis";
name.length; //6
```

- `parseInt()`

Retorna números enteros. Sirve para _parsear_ una "string" e intentar obtener un valor numérico.

```js
var s = "1234";
var m = parseInt(s); //1234

var a = 3.15;
var b = parseInt(a); //3
```

### **Numbers**

Son números, puede ser positivos o negativos. Van sin conmillas.

```js
var edad = 20;
```

- `parseFloat()`

El número siempre se interpreta como decimal.

```js
var s = 3.15;
var o = parseFloat(s); //3.15
```

### **Boolean**

Usamos `falso` o `true` . Representan números binarios `0` o `1` .

```js
let mayorDeEdad = true;
```

### **null**

Denota valor nulo.

```js
let País = null;
```

### **undefined**

Una _variable_ a la que no se le ha asignado valor, o no se ha declarado en absoluto (no se declara, no existe) son de tipo `undefined` .

```js
var x;
console.log(x); // undefined
```

### **NaN**

Es un valor que representa _Not-A-Number_ (No es un número).

```js
"4px" - 2; // NaN
```

> Hay más pero los veremos luego, ya que son más complejos.

---

## Compuestos

Se accede a la referencia del valor.
Los veremos más adelante por separado, pero son los siguientes:

- `object = {}`
- `array = []`
- `function(){}`
- `Class{}`
- etc.

---

## Avanzado:

### Coerción de Datos

Permite tomar un dato como otro para desarrollarlo o ejecutarlo:

```js
"2" + "3"; // '23'
"2" + 3; // '23'

"2" * "3"; // 6
"2" * 3; // 6
```

> Con Number forzamos un cambio de dato a tipo número:

```js
Number("3"); // devuelve el número 3. Obvio!
Number(false); // devuelve el número 0. mini Obvio.
Number(true); // devuelve el número 1. menos mini Obvio.
Number(undefined); // devuelve `NaN`. No era obvio, pero tiene sentido.
Number(null); // devuelve el nuḿero 0. WTFFFF!!! porqueeEE no debería ser `NaN`??
```

### Valor y Referencia

Los valores primitivos son los que se pasan por **valor** `=` .

Los NO primitivos se pasan por **referencia**, como que se copia.
