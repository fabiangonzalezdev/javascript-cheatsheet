# Cheatsheet + Documentación Javascript💻

¿Este es un cheatsheet mas de Javascript? No. Este cheatshet tambien contiene un wiki con la documentación mas importante de python acá:
[Wiki Documentación Javascript](https://github.com/fabiansato/javascript-cheatsheet/wiki "Documentación de Javascript")

------------------------------
# Introducción a los conceptos básicos de JavaScript
------------------------------
## Condiciones
Javascript es case-sensitive
Javascript es flexible, una variable puede ser int, luego string etc

## Mostrar datos por pantalla
La función ```console.log(<mensaje /  variables / funciones>)``` muestra un mensaje por consola /  variables / funciones

## Adjuntar javascript
podemos ponerlo en el mismo html como
```html
<script>
  aca va el codigo
</script
```
o podemos agregarlo a otro archivo con src
  
```html
  <script src="codigo.js"></script>
```

---------------------------------
### Comentarios

Hay 2 tipos de comentarios:
```javascript
// este es un comentario de una sola línea
```
otro tipo:
```javascript
/*
Esto es un comentario de varias líneas linea 1
linea 2
linea 3 Ultima linea!
*/
```

------------------------------
# Variables en JS
------------------------------

## Variables
### Tipo de variables
En javascript podemos encontrar este tipo de variables:
```javascript
Numericas, strings, arrays, booleans
```

### Carga de variables
tipo var (Se puede asignar con '' o con "") (es valida fuera del for)
```javascript
var nombre = 'juan';
```

tipo let (Se puede asignar con '' o con "") (solo es valido en un fragmento de codigo, ejemplo dentro solo de un for)
```javascript
let nombre = 'juan';
```

tipo const (Se asigna una vez pero no se puede volver a asignar:
```javascript
const nombre = 'juan';
```

booleanos (true o false | 1 o 0):
```javascript
var esbooleano = true;
```
Javascript permite cambiar de tipos de variables y eso hay que tener cuidado! Podemos tener una variable en string y cambiarla a numerica!

---------------------------------
### Carga de vectores
Podemos cargar info de un vector así:
```javascript
var meses = ['Enero', 'Febrero', 'Marzo', 'Abril', 'Mayo', 'Junio', 'Julio', 'Agosto', 'Septiembre', 'Octubre', 'Noviembre', 'Diciembre']; //vector con cantidad de meses

```
Podemos cargar vectores vacios:
```javascript
var meses = []; 
```
Todos los indices de los vectores empiezan en 0.

## agregar item al vector
```javascript
vector.push(i);
```

## buscar datos de un vector y eliminarlos
se crea una funcion que se llama:
```javascript
function removeritem(arr, item) {
    let i;
    while ((i = arr.indexOf(item)) !== -1) {
        arr.splice(i, 1);
    }


}
```


------------------------------
# Estructura de datos en JS
------------------------------
## Estructura IF:

```javascript
If (<condiciones>) {
// Código a ejecutar cuando se cumplen las condiciones
} else {
// Código a ejecutar cuando NO se cumple alguna de las condiciones
}
```

## Bucle FOR
```javascript
for(let contador=1; contador<=10; contador++) { 
console.log(contador);
}
```

## Bucle While
```javascript
var contador = 1; 
while(contador<=10) {
console.log(contador);
contador++;
}
```

## Funciones
```javascript
function sumar(valor1, valor2) { 
return valor1 + valor2;
}
```
y llamamos la funcion asi:
```javascript
var total = sumar(10,20); 
console.log(total);
```
diferencias de llamar a una funcion con () y sin ()
```javascript
      function unaFuncion(){
      console.log("Esto es una funcion");
      return 10;
      }

      console.log("LLamamos a la funcion SIN () y nos dá como resultado: " + unaFuncion);
     console.log("LLamamos a la funcion con () y nos dá como resultado: " + unaFuncion());
    console.log("Vemos como al mandar funciones en javascript con () nos devuelve el return")
```

------------------------------
# Operadores Ternarios
------------------------------
```javascript
a ? b : c;
```
Donde "a" es la condición luego ? "b" es la opción a realizar si la condición es verdadera y ;"c" si la condición es falsa.

------------------------------
# Introducción y manejo del DOM
------------------------------
## Árbol de nodos:

<img src="https://fabiansato.github.io/imagenes/javascript-nodos2.gif">

## Tipos de nodos creados:
```html
●	Document, nodo raíz del que derivan todos

●	Element, cada una de las etiquetas. Único nodo que puede contener atributos y del que pueden derivar otros nodos.

●	Attr, se define uno para cada par atributo=valor

●	Text, contiene el texto encerrado por una etiqueta

●	Comment, representa los comentarios incluidos en la página.
```
## Hay 3 funciones para acceder directamente a un nodo:
```javascript
getElementsByTagName(nombreEtiqueta)
getElementsByClassName(nombreAtributo)
getElementById(id)
```

## ** Crear un nodo
-------------------------

Recordar que cada elemento genera 2 nodos. 4 pasos:
1.	Creación de un nodo de tipo Element que represente al elemento.
2.	Creación de un nodo de tipo Text que represente el contenido del elemento.
3.	Añadir el nodo Text como nodo hijo del nodo Element.
4.	Añadir el nodo Element a la página,en forma de nodo hijo del nodo correspondiente al lugar en el que se quiere insertar el elemento.

## Implica utilizar 3 funciones DOM:

●	`createElement(etiqueta):` crea un nodo de tipo Element que representa al elemento cuya etiqueta se pasa como parámetro.
●	`createTextNode(contenido):` crea un nodo de tipo Text que almacena el
contenido textual de los elementos.
●	`nodoPadre.appendChild(nodoHijo)`: añade un nodo como hijo de otro nodo. Se debe utilizar al menos dos veces con los nodos habituales: en primer lugar se añade el nodo Text como hijo del nodo Element y a continuación se añade el nodo Element como hijo de algún nodo de la página.


Ejemplo para la creación de un párrafo
```javascript
// Crear nodo de tipo Element
var parrafo = document.createElement("p");

// Crear nodo de tipo Text
var contenido = document.createTextNode("Hola Mundo!");

// Añadir el nodo Text como hijo del nodo Element 
parrafo.appendChild(contenido);

// Añadir el nodo Element como hijo de la página 
document.body.appendChild(parrafo);
```
## Eliminar un nodo
Afortunadamente, eliminar un nodo del árbol DOM de la página es mucho más sencillo que añadirlo. En este caso, solamente es necesario utilizar la función  `removeChild(nodo)` que debe ser invocada desde el elemento padre. Para acceder al padre de un nodo: `nodoHijo.parentNode`
```javascript
var parrafo = document.getElementById("provisional");
parrafo.parentNode.removeChild(parrafo);
```

```html
<p id="provisional">...</p>
```

## eliminar contenido de un nodo

```javascript
    for (let e = 0; e < 21; e++) {
        if (parrafo.hasChildNodes()) {
            parrafo.removeChild(parrafo.firstChild);
        }
    }
```
## Seleccionar datos de un elemento y mostrar sus modulos
```javascript
var enlace = document.getElementById("enlace");
alert(enlace.href); // muestra http://www...com
```
```html
<a id="enlace" href="http://www...com">Enlace</a>
```
Vemos como tomanos el id del enlace y mostramos su href

ejemplo con imagenes:
```javascript
var imagen = document.getElementById("imagen");
alert(imagen.style.margin);
```
```html
<img id="imagen" style="margin:0; border:0;" src="logo.png" />
```

## Para propiedades CSS con nombre compuesto, se accede eliminando los guiones (-).
```javascript
●	font-weight → fontWeight
●	line-height → lineHeight
●	border-top-style → borderTopStyle
●	list-style-image → listStyleImage
```



## QuerySelector

Permite recorrer el documento de una forma más fácil que las opciones anteriores, pudiendo utilizar los selectores CSS.

```javascript
document.querySelector(‘<selector CSS>’);
document.querySelector(‘.menu’); 
document.querySelector(‘#id-principal .clase-secundaria’);

```

Retorna solo la primer ocurrencia
pero...

### QuerySelectorAll

Retorna todas las ocurrencias
```javascript
document.querySelectorAll(‘<selector CSS>’);
```


ejemplo con uso:

```javascript
let elem1 = document.querySelector('#nombreid');
let elem2 = document.querySelector('.clase'); //solo trae la primer clase que matchea
let elem3 = document.querySelectorAll('.clase'); //trae todas las clases que matchea
```
## obtener valores de inputs (formularios)
podemos obtener los valores del imput poniendo `variable.value`
```javascript
let nombre = document.querySelector('#nombre');
                console.log('el usuario hizo click', nombre.value);
```
#### Class

Modificar el class desde JS

Cambio de las clases de un elemento (respuesta de getElementById, querySelector, etc) 
```javascript
elemento.className = ‘nueva-clase-css’;
```

#### Agregar class

Agregar una clase CSS a un elemento 
```javascript
elemento.classList.add(‘nueva-clase-css’);
```

#### Eliminar un class
Eliminar una clase CSS a un elemento 
```javascript
elemento.classList.remove(‘clase-css-a-borrar’);
```

# Eventos


●	`onClick`: se produce cuando el usuario hace click sobre una etiqueta HTML (por ejemplo un botón)

●	`onChange`: se produce cada vez que el usuario cambia el contenido de una etiqueta del tipo input (y abandona el campo de entrada)

●	`onFocus`: se produce cada vez que el usuario ingresa a una etiqueta del tipo input

●	`onSubmit`: se produce cuando el usuario envía un formulario

●	`onScroll`: que se produce cada vez que el usuario se desplaza en la página (siempre y cuando exista un desplazamiento de la barra de scroll lateral)



## OnClick Ejemplo
```html
<script>
function presionoBoton() { alert('Presiono botón');
}
</script>
<body>
...
<button onClick="presionoBoton()">Botón</button>
...
</body>
```
Cuando el usuario hace click sobre Botón, se muestra un alerta con el mensaje “Presionó botón”.

## Onchange ejemplo

```html
<script>
function cambioInput() { console.log("Cambio el valor");
}
</script>
<body>
...
<input type="text" onChange="cambioValor()">
...
</body>
```

### Onfocus ejemplo

```html
<script>
function accedioAlElemento() { console.log("Accedió al elemento");
}
</script>
<body>
...
<input type="text" onFocus="accedioAlElemento()">
...
</body>
```

### Onsubmit ejemplo:

```html
<script>
function envioFormulario() { console.log('Envio formulario');
}
</script>
<body>
...
<form onsubmit="envioFormulario()">
...
</form>
...
</body>
```


##Parámetros a los eventos
Cuando se produce un evento, también tenemos la posibilidad de acceder al contexto del mismo (en donde se ejecutó el mismo). Por ejemplo:
●	El input en el cual se produjo el evento, y al valor

●	El formulario en el cual se produjo el submit

●	El botón que fue presionado

## Onchange ejemplo:

```html
<script>
function cambioValor(e) {
console.log("Cambio el valor del input y ahora es " + e.target.value);
}
</script>
<body>
...
<input type="text" onChange="cambioValor(event)">
...
</body>
```

## OnSubmit y preventDefault() Ejemplo:

```html
<script>
function envioFormulario(e) { console.log('Envio formulario'); e.preventDefault();

}
</script>
</head>
<body>
<form onsubmit="envioFormulario(event)">
<input type="text">
<button type="submit">Enviar</button>
</form>
```

------------------------------
# JSON
------------------------------

crear un array con un json interno en un array:

```javascript
    const productos = [ 
        { 
            id:1,
            name: "Moto g"

        }
        {
            id: 2,
            name: "Moto X"

        }
    ]
 ```
------------------------------
# Clases  
------------------------------
Declaración de clases:
 ```Javascript
 class Rectangulo {
  constructor(alto, ancho) {
    this.alto = alto;
    this.ancho = ancho;
  }
}
 ```
En primer lugar necesitas declarar tu clase y luego acceder a ella


Expreciones de clases:
 ```javascript
// Anonima
let Rectangulo = class {
  constructor(alto, ancho) {
    this.alto = alto;
    this.ancho = ancho;
  }
};

console.log(Rectangulo.name);
// output: "Rectangulo"

// Nombrada
let Rectangulo = class Rectangulo2 {
  constructor(alto, ancho) {
    this.alto = alto;
    this.ancho = ancho;
  }
};
console.log(Rectangulo.name);
// output: "Rectangulo2"
 ```
 
 
 ## Métodos prototipo:
  ```javascript
 class Rectangulo {
  constructor (alto, ancho) {
    this.alto = alto;
    this.ancho = ancho;
  }
  // Getter
  get area() {
     return this.calcArea();
   }
  // Método
  calcArea () {
    return this.alto * this.ancho;
  }
}

const cuadrado = new Rectangulo(10, 10);

console.log(cuadrado.area); // 100
 ```
 
 ## Métodos estáticos
La palabra clave static define un método estático para una clase. Los métodos estáticos son llamados sin instanciar su clase y no pueden ser llamados mediante una instancia de clase
 ```
class Punto {
  constructor ( x , y ){
    this.x = x;
    this.y = y;
  }

  static distancia ( a , b) {
    const dx = a.x - b.x;
    const dy = a.y - b.y;

    return Math.sqrt ( dx * dx + dy * dy );
  }
}

const p1 = new Punto(5, 5);
const p2 = new Punto(10, 10);
 ```
## "Boxing" con prototipos y métodos estáticos
Cuando un método estático o método del prototipo es llamado sin un valor para "this" (o con "this" como booleano, cadena, número, undefined o null), entonces el valor de "this" será undefined dentro de la funciona llamada
 ```javascript
class Animal {
  hablar() {
    return this;
  }
  static comer() {
    return this;
  }
}

let obj = new Animal();
obj.hablar(); // Animal {}
let hablar = obj.hablar;
hablar(); // undefined

Animal.comer() // class Animal
let comer = Animal.comer;
comer(); // undefined
 ```
 
 ## Subclases con extends
 La palabra clave extends es usada en declaraciones de clase o expresiones de clase para crear una clase hija.
 
  ```javascript
 class Animal {
  constructor(nombre) {
    this.nombre = nombre;
  }

  hablar() {
    console.log(this.nombre + ' hace un ruido.');
  }
}

class Perro extends Animal {
  hablar() {
    console.log(this.nombre + ' ladra.');
  }
}
 ```
 
 ## También se pueden extender las clases tradicionales basadas en funciones:
  ```javascript
  function Animal (nombre) {
  this.nombre = nombre;
}
Animal.prototype.hablar = function () {
  console.log(this.nombre + 'hace un ruido.');
}

class Perro extends Animal {
  hablar() {
    super.hablar();
    console.log(this.nombre + ' ladra.');
  }
}

var p = new Perro('Mitzie');
p.hablar();
   ```
   
   Fijarse que las clases no pueden extender objectos regulares (literales). Si se quiere heredar de un objecto regular, se debe user    ```Object.setPrototypeOf():   ```:
   ```javascript
   var Animal = {
  hablar() {
    console.log(this.nombre + 'hace ruido.');
  }
};

class Perro {
  constructor(nombre) {
    this.nombre = nombre;
  }
  hablar() {
    console.log(this.nombre + ' ladra.');
  }
}

Object.setPrototypeOf(Perro.prototype, Animal);

var d = new Perro('Mitzie');
d.hablar();
   ```
   
   ## Especies
   Quizás se quiera devolver objetos Array derivados de la clase array MyArray. El patron species permite sobreescribir constructores por defecto.

Por ejemplo, cuando se usan metodos del tipo map() que devuelven el constructor por defecto, se quiere que esos métodos devuelvan un objeto padre Array, en vez de MyArra
 ```javascript
class MyArray extends Array {
  // Sobre escribe species sobre el constructor padre Array
  static get [Symbol.species]() { return Array; }
}

var a = new MyArray(1,2,3);
var mapped = a.map(x => x * x);

console.log(mapped instanceof MyArray); // false
console.log(mapped instanceof Array);   // true
 ```
 
 ## Llamadas a súperclases con super
 La palabra clave super es usada para llamar funciones del objeto padre.
  ```javascript
 class Gato {
  constructor(nombre) {
    this.nombre = nombre;
  }

  hablar() {
    console.log(this.nombre + ' hace ruido.');
  }
}

class Leon extends Gato {
  hablar() {
    super.hablar();
    console.log(this.nombre + ' maulla.');
  }
}
 ```
 
 ## Mix-ins
 Subclases abstractas or mix-ins son plantillas de clases. Una clase ECMAScript solo puede tener una clase padre, con lo cual la herencia multiple no es posible. La funcionalidad debe ser proporcionada por la clase padre.
  ```javascript
 var calculatorMixin = Base => class extends Base {
  calc() { }
};

var randomizerMixin = Base => class extends Base {
  randomize() { }
};
 ```
 
 Una clase que use este método puede ser escrita tal que así:
  ```javascript
 class Foo { }
class Bar extends calculatorMixin(randomizerMixin(Foo)) { }
 ```
