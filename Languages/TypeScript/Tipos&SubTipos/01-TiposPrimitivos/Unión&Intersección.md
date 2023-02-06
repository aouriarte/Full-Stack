# Tipos de Unión e Intersección

TypeScript proporciona opciones más avanzadas para declarar tipos. Permiten controlar situaciones en las que un tipo se compone de _dos o más tipos posibles_.

## Tipos de Unión

Un tipo de **unión** describe un valor que puede ser uno de entre varios tipos. Restringen la asignación de valores a los tipos especificadosEsto puede ser útil cuando no tenga controlado un valor (por ejemplo, los valores de una biblioteca, una API o una entrada de usuario).

Un tipo de unión usa la barra vertical o pleca `|` para separar cada tipo.

```ts
let multiType: number | boolean;
multiType = 20; //* Valid
multiType = true; //* Valid
multiType = "twenty"; //* Invalid
```

Con las [restricciones de tipos](../00-Tipos/01-Tipos%26SubTipos.md), puede trabajar fácilmente con una variable de un tipo de unión.

```ts
function add(x: number | string, y: number | string) {
  if (typeof x === "number" && typeof y === "number") {
    return x + y;
  }
  if (typeof x === "string" && typeof y === "string") {
    return x.concat(y);
  }
  throw new Error("Parameters must be numbers or strings");
}
console.log(add("one", "two")); //* Returns "onetwo"
console.log(add(1, 2)); //* Returns 3
console.log(add("one", 2)); //* Returns error
```

> En este ejemplo, la función `add` acepta dos valores que pueden ser `number` o `string`. Si ambos valores son tipos numéricos, los agrega. Si ambos son tipos de cadena, los concatena. De lo contrario, genera un error.

---

## Tipos de Intersección

Un tipo de **intersección** combina dos o más tipos para crear uno que tiene todas las propiedades de los tipos existentes.

Un tipo de intersección usa el símbolo `&` para separar cada tipo.

Los tipos de intersección se usan con mayor frecuencia con las [interfaces](../01-Tipos%26SubTipos/04-TiposDeObjeto.md).

```ts
interface Employee {
  employeeID: number;
  age: number;
}
interface Manager {
  stockPlan: boolean;
}

type ManagementEmployee = Employee & Manager;
let newManager: ManagementEmployee = {
  employeeID: 12345,
  age: 34,
  stockPlan: true,
};
```

> En este ejemplo se definen dos interfaces, `Employee` y `Manager`, y luego se crea un tipo de intersección llamado `ManagementEmployee` que combina las propiedades en ambas interfaces.
