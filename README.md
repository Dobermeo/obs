# obs



## Tipos de datos

Person:

- Tipos de datos en js ejemplos

ChatGPT:

- En JavaScript, los tipos de datos son las distintas categorías de valores que pueden ser utilizadas para representar información en un programa. Algunos de los tipos de datos más comunes en JavaScript son los siguientes, junto con ejemplos de cada uno:

1. Números (Number): Representa valores numéricos, ya sean enteros o decimales.

```javascript

let edad = 30;
let precio = 19.99;
```

1. Cadenas de texto (String): Representa una secuencia de caracteres, encerrada entre comillas simples o dobles.

```javascript

let nombre = "Juan";
let mensaje = 'Hola, ¿cómo estás?';
```

1. Booleanos (Boolean): Representa un valor verdadero (true) o falso (false).

```javascript

let esMayorDeEdad = true;
let esEstudiante = false;
```

1. Arreglos (Array): Representa una colección ordenada de elementos, que pueden ser de cualquier tipo de dato, incluyendo otros arreglos.

```javascript

let numeros = [1, 2, 3, 4, 5];
let frutas = ["manzana", "naranja", "plátano"];
```

1. Objetos (Object): Representa una colección de propiedades, donde cada propiedad tiene un nombre y un valor asociado. Los valores pueden ser de cualquier tipo de dato, incluyendo otros objetos y funciones.

```javascript

let persona = {
  nombre: "Ana",
  edad: 25,
  esEstudiante: true
};
```

1. Null: Representa la ausencia intencional de un valor.

```javascript

let valorNulo = null;
```

1. Undefined: Representa una variable que ha sido declarada pero no ha sido asignada con un valor.

```javascript

let variableNoDefinida;
console.log(variableNoDefinida); // Output: undefined
```

1. Funciones (Function): Representa un bloque de código que puede ser ejecutado cuando es invocado.

```javascript

function sumar(a, b) {
  return a + b;
}
```

1. Símbolos (Symbol): Representa un valor único e inmutable que puede ser utilizado como una clave para propiedades de objetos.

```javascript

const simbolo = Symbol("descripcion");
```

Estos son algunos de los tipos de datos más utilizados en JavaScript. Cabe mencionar que JavaScript es un lenguaje de tipado dinámico, lo que significa que las variables pueden cambiar de tipo de dato durante la ejecución del programa. Por ejemplo, una variable que contiene un número puede luego asignarse con una cadena de texto.


