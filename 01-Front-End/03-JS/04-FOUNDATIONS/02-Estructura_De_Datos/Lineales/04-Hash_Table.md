# Hash table

Permiten crear una lista de valores en par-clave. De este modo podremos retornar un valor a partir de su “contraseña” que tendremos de antemano. En otras palabras, una Hash Function le asignará un valor único a una variable, para que podamos obtenerla más tarde. (Esto está asociado a la encriptación). 

```js
class HashTable { // [{key: value}]
  constructor() {
    this.numderoDeCasilleros = 35;
    this.arreglo = []; 
  }

  // Saber en que POSICIÓN debo guardar el valor:
  hash(key){ // calcula el número de casillero en donde se guardará el valor con su 'key'
      let suma = 0;
      for(let i = 0; i < key.length; i++){ 
          suma += key.charCodeAt(i); // 'i' suma cada valor numérico por letra
      }
      let casillero = suma % this.numeroDeCasilleros;
      return casillero;
  }
  
  // Guardar un valor:
  set(key, value){ 
      if(!this.buckets[this.hash(key)]){ // cuando el casillero (arreglo) está vacío, para tener más sub casilleros
          this.buckets[this.hash(key)] = {} // le metemos un objeto para buscar más fácil a través de la propiedad (key) el valor
      }
      this.buckets[this.hash(key)][key] = value; // accede al casillero (arreglo) y anda a la clave que tengas (key) y ahí guarda el valor
  }

  // Busco si la información existe en esa posición
  get(key){
      return this.buckets[this.hash(key)][key]; // retorname el valor que busco
  }

  hasKey(key){
      let booleanos = this.buckets[this.hash(key)][key] ? true : false; // si existe retorna true sino false
      return booleanos; 
  }
}