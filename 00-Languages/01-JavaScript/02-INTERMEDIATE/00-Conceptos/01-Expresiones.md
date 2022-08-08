## Expresiones

Cómo dijimos arriba, una **expression** es cualquier pedazo de código _que pueda ser evaluado a un valor_. Justamente por esto, las vamos a usar en lugares donde JavaScript _espera un valor_. Por ejemplo, cómo cuando pasamos una expresión como argumento de una función.

Según la documentación de [MDN](https://developer.mozilla.org/es/docs/Web/JavaScript), las expresiones se pueden clasificar en las siguientes categorías:

### **Expresiones Aritméticas**

Son las expresiones que resuelven a un valor **numérico**:

```js
10;
1 + 10;
2 * 16;
```

### **Expresiones de Strings**

Son expresiones que resuelven a una **string**:

```js
"hola";
"hola" + " como va?";
```

### **Expresiones Lógicas**

Son expresiones que resuelven a un valor **booleano**:

```js
10 > 9;
11 === 2;
false;
```

### **Expresiones Primarias**

Son expresiones que se escriben por si mismas, y no utilizan ningún operador. Incluyen a valores literales, uso de variables, y algunos **keywords** de JS:

```js
"hola";
23;
true;
this; // hace referencia al keyword this
numero; // hace referencia a la variable numero
```

### **Expresiones de Asignación**

Cuando utilizamos el operador `=` hablamos de un _assigment expression_. Está expresión retorna el valor asignado:

```js
a = 1; // si probamos esto en la consola, vemos que retorna el valor 1.
var c = (a = 2); // vamos a ver que dentro de la variable c, está el valor retornado por la expresion `a = 2`
```

> Este es un caso muy particular, nótese que esta expresion retornar una valor, **pero a su vez hace algo**!! Ese algo, es guardar el valor a la derecha del signo `=` en la variable a la izquierda del signo `=`.
> Otra cosa a notar, es que si usamos el keyword `var` la expresión retorna `undefined`, es decir, no es lo mismo una asignación que una declaración de variables.

### **Expresiones con efectos secundarios (side effects)**

Son expresiones que al ser evaluadas retornan algo, pero a su vez tienen _un efecto secundario_ (incrementar un valor, etc...). Por ejemplo:

```js
contador++; //retorna el valor de contador e incrementa uno.
++contador; // incrementa el valor de contador y retorna el valor;

mult *= 2; // multiplica mult por dos, asigna ese valor a mult y retorna el valor;
```
