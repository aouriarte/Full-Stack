# Introducción

Son la manera de organizar nuestros datos en la programación. Están:

## Built-in

Son las incorporadas:

- Integer
- Float
- Character
- Pointer

## User Defined

Las definidas por el usuario son:

### Arrays

Ya vimos los arreglos. También son una estructura nativa de JavaScript en la que se ordena una serie de elementos entre corchetes y separados por comas.

```js
ARRAY = ["Hola", 245, false, 325, "Ejemplos"];
```

     Index:  0 | 1 | 2 | 3 | 4
             H | E | L | L | O

     Adress: H -> 0x23451
             E -> 0x23452
             L -> 0x23453
             L -> 0x23454
             O -> 0x23455


Cada elemento de un arreglo tiene una dirección a al que el intérprete accede directamente. Se pueden agregar y sacar elementos al comienzo y al final del arreglo.

---

### Set

Es parecido a los arreglos, solo que crea un nuevo objeto sin que se repita sus valores. Es un constructor. Es para cualquier tipo de dato.

```js
var arreglo = [1,2,3,4,,1,3,1,7,5]
var set1 = new Set(arreglo)
console.log(set1); // Set {1,2,3,4,7,5} 
```

También tiene distintos métodos:

```js
var arr = [1, 2, 5, 4, 7, 7, 2, 4, 6];

var comp = new set(arr);
//[1, 2, 5, 4, 7, 6]

comp.add("Hola");
//[1, 2, 5, 4, 7, 6, "Hola"]
```

---

### Listas

#### **Lineales:**

- Stacks (Pilas)
- Queues (Colas)
- LinkedList (Listas enlazadas)

#### **No Lineales:**

- Trees (Árboles)
- Graphs (Gráficos)

---

### Files
