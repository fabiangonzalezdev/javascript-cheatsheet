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
Se dividen en 2 tipos:
Tipos primitivos
y
Tipos de objeto (a su vez se dividen en 4):
  1-Predefinidos
| 2-Definidos por el programador/usuarios
  3-Arrays
  4-Objetos especiales
  
## Variables
### Tipo de variables primitivas

```javascript
String
Number
Boolean
Null
Undefied
```
### Tipo de variables OBJETO (predefinidas de javascript):
```javascript
Date (fechas) 
RegExp (expresiones regulares) 
Error 
```


### Tipo de variables OBJETO (definidos por el programador / usuario): 
```javascript
Funciones simples 
Clases 
```
### Tipo de variables OBJETO (ARRAYS): 
```javascript
Serie de elementos o formación tipo vector o matriz 
```

### Tipo de variables OBJETO (OBJETOS ESPECIALES): 
```javascript
objeto global 
objeto prototipo 
```
---------------------------
## Funciones
Existen dos tipos de funciones:
1)declarativas
2) de expresión

funciones declarativas:
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
Un ejemplo de una función de expresión sería: 
```javascript
var suma = function(a,b){return a+b;} 
```

### Tipo de variables OBJETO (predefinidas de javascript):
```javascript
Date (fechas)
RegExp (expresiones regulares)
Error
```

### Tipo de variables OBJETO (definidos por el programador / usuario):
```javascript
Funciones simples
Clases
```
### Tipo de variables OBJETO (ARRAYS):
```javascript
Serie de elementos o formación tipo vector o matriz
```

### Tipo de variables OBJETO (OBJETOS ESPECIALES):
```javascript
objeto global
objeto prototipo
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


---------------------------
## Scope
Existen dos tipos de Scope: 

• Scope Global: lo que está en global no puede acceder a lo que está en local. 

• Scope Local: lo que está en local puede acceder a lo que está en global. 


---------------------------
## Hoisting
El Hoisting es un proceso donde el compilador aun no carga la declaración de la variable y esta misma se toma como undifined.
```javascript
saludo(); 
 
function saludo() { 
console.log("Hola " + nombre); 
} 
 
var nombre = "Fabian Sato"; 
```
En ecmascript 6 para arriba esto no sucede ya que tenemos las declaraciones de variables con const y let 

---------------------------
## Coercion
Coerción es la forma en la que podemos cambiar un tipo de valor a otro, existen dos tipos de coerción: 

Coerción implícita = es cuando el lenguaje nos ayuda a cambiar el tipo de valor. 

Coerción explicita = es cuando obligamos a que cambie el tipo de valor. 
---------------------------
## Valores: Truthy y Falsy 
```javascript
 

//Ejemplos en los que Boolean devuelve Falso: 
Boolean(0); //false 
Boolean(null); //false 
Boolean(NaN); //false 
Boolean(undefined); //false 
Boolean(false); //false 
Boolean(""); //false 
 
//Ejemplos en los que Boolean devuelve verdadero: 
Boolean(1); //true para 1 o cualquier número diferente de cero (0) 
Boolean("a"); //true para cualquier caracter o espacio en blanco en el string 
Boolean([]); //true aunque el array esté vacío 
Boolean({}); //true aunque el objeto esté vacío 
Boolean(function(){}); //Cualquier función es verdadera también 
Boolean(-1); // true 

 
```
---------------------------
##  Asignación, Comparación y Aritméticos. 
Operador de asignación:
```javascript
__________________________
= | operador de asignacion 
__________________________

```
Operador de comparación:
```javascript
__________________________
== | Igual que
__________________________
=== | Estrictamente igual que contenido y tipo de datos
__________________________
> or >= or >== | Mayor o mayor igual que
__________________________
< or <= or <== | Menor o menor igual que
__________________________
!= or !== | Diferente que
__________________________
```

Operador aritmetico:
```javascript
__________________________
+ | Operador de suma, tambien se utiliza para concatenar dos cadenas de texto
__________________________
- | Operador de resta
__________________________
* | Operador de multiplicación
__________________________
/ | Operador de división
__________________________
% | Operador de Modulo
__________________________
** | Operador de potenciación
__________________________
```

Operadores Logicos:
```javascript
__________________________
! | Not (niega un valor)
__________________________
&& | AND
__________________________
|| | OR
__________________________
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

} else if(codincion) {
// Código a ejecutar cuando NO se cumple alguna de las condiciones y una condicion extra
}
```

------------------------------
# Operadores Ternarios
------------------------------
```javascript
a ? b : c;
```
Donde "a" es la condición luego ? "b" es la opción a realizar si la condición es verdadera y ;"c" si la condición es falsa.


------------------------------
## SWITCH
```javascript
 switch(condicion) {
    case '1': 
    return CONDICIOES
    break
    
    case '2': 
   return CONDICIOES
    break
    
    case '3': 
   return CONDICIONES
    break
    
    default: //valor
   return CONDICIONES
  }
}

}
```
------------------------------
# Array
------------------------------
Un Array es un tipo de estructura de datos, objeto. Puede guardar datos distintos dentro, guarda los datos en forma de lista. 

Podemos cargar info de un vector así:
```javascript
var meses = ['Enero', 'Febrero', 'Marzo', 'Abril', 'Mayo', 'Junio', 'Julio', 'Agosto', 'Septiembre', 'Octubre', 'Noviembre', 'Diciembre']; //vector con cantidad de meses
```

Podemos cargar vectores vacios:
```javascript
var meses = []; 
```


metodos de arrays:

```javascript
array.lenght devuelve la longitud del array.  //ejemplo console.log(variable.lenght)

console.log(variable[0]); // acceder del index del elemento en posicion 0

array.push(nombrevariableNueva) agrega elementos al final de array. /

array.pop(nombrevariable) elimina un elemento del array. 

array.unshift(nombrevariable) agrega un elemento al array, pero lo agrega en primer lugar. 

array.shift(nombrevariableNueva) **elimina el elemento que está en el inicio del array. 

array.indexOf(variable) ** devuelve la posición de un elemento del array. 
```



Todos los indices de los vectores empiezan en 0.


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
-----------------
Loops (bucles/ciclos)  For y For...of 
-----------------

## Bucle FOR
```javascript
for(let contador=0; contador<=10; contador++) { 
console.log(contador);
}
```

Ejemplo con arrays:
```javascript
for(let i=0; array.lenght; i++) { 
console.log(array);
}
```



## Bucle FOR OF
```javascript
for(var array of arrays) { //recorre el array y "arrays" se crea como nuevo que es el indice de cada array
console.log(array);
}
```

## Bucle FOR IN
La instrucción for-in itera sobre todas las propiedades enumerables de un objeto que está codificado por cadenas (ignorando los codificados por Símbolos, incluidas las propiedades enumerables heredadas.
```javascript
const object = { a: 1, b: 2, c: 3 };

for (const property in object) {
  console.log(`${property}: ${object[property]}`);
}

// expected output:
// "a: 1"
// "b: 2"
// "c: 3"

```

## Bucle While
En el bucle itera solamente si se cumple una condición
```javascript
var contador = 1; 
while(contador<=10) {
console.log(contador);
contador++;
}
```


## Bucle do While
En do while si o si hace una acción por primera vez
```javascript
do {
    saludarEstudiante(estudiantes[i]);
    i++;
} while (i < estudiantes.length)


```

------------------------------
# Objetos
------------------------------
Objetos: JS es un lenguaje que está diseñado en un paradigma de objetos. 

Ejemplo de Objeto: 
```javascript
var miAuto = { 
marca: "Toyota", 
modelo: "Corolla", 
año: 2020 
}
```

Ejemplo de objetos con funciones:
Objetos: JS es un lenguaje que está diseñado en un paradigma de objetos. 

Ejemplo de Objeto: 
```javascript
var miAuto = { 
marca: "Toyota", 
modelo: "Corolla", 
año: 2020 
DetalleDelAuto: function(){ // llamamos una funcion dentro del propio objeto 
Console.log(`Auto ${this.modelo} ${this.marca}`); //podemos llamar dentro del objeto 
} 
 
//llamamos al objeto:
MiAuto.detalleDelAuto();
```
------------------------------
# Objects Funcion constructora 
------------------------------
```javascript
function auto (MARCA, MODELO, ANNIO){ //funcion auto para guardar las variables
this.marca = MARCA; 
this.modelo = MODELO; 
this.annio = ANNIO; 
} 
var autos = []; //variable desde cero
for(let i = 0 ; i < 30 ; i++){  //carga 30 autos y guarda en cada variable
var marca = prompt("Ingresa la marca del auto"); 
var modelo = prompt("Ingresa el modelo del auto"); 
var annio = prompt("Ingresa el año del auto"); 
autos.push(new auto (marca, modelo, annio)); //guarda un nuevo ogjeto y lo guarda en un objeto auto con sus variables
} 
 
for(let i = 0 ; i < autos.length ; i++){ //bucle para iterar todos los objetos de autos.
console.log(autos[i]); 
} 
```

------------------------------
# Metodos de recorrido de arrays
------------------------------
 
RECORRER EL CONTENIDO DEL ARRAY:  
 - array.filter: filtra en base a validaciones (genera un nuevo array)  
```javascript
 

  Var nuevo = arrays.filter(function(variableparafiltrar){ 

Return array <= 300; // retornamos una condicion de una posicion del array 

} 
```
- array.map: regresa un atributo de los objetos (genera un nuevo array) 
```javascript


  Var nuevo = arrays.map(function(variableparafiltrar){ 

Return array,nombre // retornamos  una condicion (en este caso el nombre) 

} 

 ```

Ejemplo: 
 
```javascript
var articulos = [ 
{ nombre: '📱', precio: 1000 }, 
{ nombre: '💻', precio: 1500 }, 
{ nombre: '🖥', precio: 2000 }, 
{ nombre: '⌨️', precio: 100 }, 
{ nombre: '🖱', precio: 70 }, 
{ nombre: '🚗', precio: 30000 }, 
]; 
 
// Método Filter 
var articulosFiltrados = articulos.filter(function(articulo) { 
return articulo.precio <= 500; 
}); 
 
// Método Map 
var nombreArticulos = articulos.map(function(articulo) { 
return articulo.nombre; 
}); 
 
articulosFiltrados; 
// (2) [{…}, {…}] 
// 0: {nombre: "⌨️", precio: 100} 
// 1: {nombre: "🖱", precio: 70} 
 
nombreArticulos; // (5) ["📱", "💻", "🖥", "⌨️", "🚗"] 
```

------------------------------
# Recorriendo Arrays con .find(), .forEach() y .some() 
------------------------------
find() : Devuelve el primer elemento del array que cumpla con la condición dada 

foreach() : Ejecuta lo que le definamos una vez por cada elemento de nuestro array 

some() : Comprueba si al menos un elemento del array cumple con la condición que le damos 

filter() : Devuelve todos los elementos del array que cumplan con la condición dada 
 
```javascrfipt
var articulos = [
    { nombre: "Bici", costo: 3000 },
    { nombre: "TV", costo: 2500 },
    { nombre: "Libro", costo: 320 },
    { nombre: "Celular", costo: 10000 },
    { nombre: "Laptop", costo: 20000 },
    { nombre: "Teclado", costo: 500 },
    { nombre: "Audifonos", costo: 1700 },
];

//filter Genera un nuevo array
var articulosFiltrados = articulos.filter(function(articulo){
    return articulo.costo <= 500; //articulos con precio menor a 500 pesos
});

//map Ayuda a mapear ciertos elementos de los articulos, es necesario generar nuevo array
var nombreArticulos = articulos.map(function(articulo){
    return articulo.nombre;
});

//find Ayuda a encontrar algo dentro del array articulos
var encuentraArticulo = articulos.find(function(articulo){
    return articulo.nombre === "Laptop";
});

//forEach No es necesario generar nuevo array, se utiliza para realizar un recorrido de un array principal
articulos.forEach(function(articulo){
    console.log(articulo.nombre);
});

//some Se genera nuevo array, regresa un condición en Boolean
var articulosBaratos = articulos.some(function(articulo){
    return articulo.costo <= 700;
});


//Filter muestra el valor que agreguemos en una funcion externa
const ages = [32, 33, 16, 40];

const result = ages.filter(checkAdult);

function checkAdult(age) {
  return age >= 18;
}
```

------------------------------
# Eliminando elementos de un Array
------------------------------
AGREGAR El método .push() nos permite agregar uno o más elementos al final de un array.
```javascript

let numArray = [1,2,3,4,5]

function newNum(){
  numArray.push(6,7)
}

newNum()
```
QUITAR con Shift

// --- SHIFT --
elimina el primer contenido del array
```javascript
//Creamos el array
let array = [1,2,3,4,5]
console.log(array)

// Aplicamos .shift()
let shiftArray = array.shift()

//Revisamos. El output debe de ser [2,3,4,5]
console.log(array)
```
// --- POP--
elimina el ultimo contenido del array
```javascript
//Creamos el array
let array = [1,2,3,4,5]
console.log(array)

// Aplicamos .shift()
let shiftArray = array.pop()


//Revisamos. El output debe de ser [1,2,3,4]
console.log(array)
```





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
 
------------------------
widow.localation
---------------------
## Autoredirect de pagina en javascript
```javascript
<script type="text/javascript">
            window.location.href = "http://example.com"
        </script>
```

------------------------
Numeros aleatorios 
---------------------

```javascript
	functionaleatorio(min, max)
{
  returnMath.floor(Math.random()*(max- min+ 1)) + min;
}

```

----------------------
arrow functions
----------------------

var hello = 'Hola Gente'
let world = 'Hola mundo'
const holamundillo = 'hola mundillo'


```javascript
const funcionArrow = () => {
    console.log(hello);
    console.log(world);
    console.log (holamundillo);
}

funcionArrow();

```


