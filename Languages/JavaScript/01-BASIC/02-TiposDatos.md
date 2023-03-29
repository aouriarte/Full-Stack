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

- `toString`

Convierte los elementos a una 'string':

```js
var numero = 123;
numero.toString(); // '123'
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

## Compuestos

Se accede a la referencia del valor.
Los veremos más adelante por separado, pero son los siguientes:

- `object = {}`
- `array = []`
- `function(){}`
- `Class{}`
- etc.

## JavaScript Avanzado

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

- Tabla de igualdades:

```js
6 / "3"                                     //2
"2" * "3"                                   //6
4 + 5 + "px"                                //9px
"$" + 4 + 5                                 //$45
"4" - 2                                     //2
"4px" - 2                                   //NaN
7 / 0                                       //Infinity
{}[0]                                       //undefined
parseInt("09")                              //9
5 && 2                                      //2
2 && 5                                      //5
5 || 0                                      //5
0 || 5                                      //5
[3]+[3]-[10]                                //23
3>2>1                                       //false
[] == ![]                                   //true
true                                        //1
false                                       //0
```

### Valor y Referencia

- **Valor:** Los _datos primitivos_ son los que se pasan por valor `=` .

Por ejemplo: En este caso estamos pasando variables por valor. Al comienzo **a** y **b** son distintas. Luego **a** se hace **“fotocopia”** de **b** y adquiere su valor. Si luego cambiamos el valor de **b**, el valor de **a** se seguirá manteniendo igual, ya que mantiene independencia:

```js
var a = 3;
var b = 5;
a = b;
//  5 = 5

b = 324;
a = 5;
```

- **Referencia:**
  Los NO primitivos (objetos, arreglos o funciones en variables) se pasan por **referencia**, como que se copia.

Por ejemplo: En este caso primero creamos un objeto, y luego definimos un nuevo objeto que es igual al primero. Cuando al primero le agregamos la propiedad Edad, esta se agregará automáticamente a la segunda:

```js
var obj = {Nombre: "Alexis", Apellido: "Uriarte"};
var newObj = obj;

obj.Edad = 21;
// obj = {Nombre: "Alexis", Apellido: "Uriarte", Edad: 21}

<newObj>
{Nombre: "Alexis", Apellido: "Uriarte", Edad: 21};
```

> En ese caso hay un **“reflejo”** de los cambios que hagamos en cualquiera de las variables.
