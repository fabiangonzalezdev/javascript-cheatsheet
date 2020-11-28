# Cheatsheet + Documentación Javascript💻

¿Este es un cheatsheet mas de python? No. Este cheatshet tambien contiene un wiki con la documentación mas importante de python acá:
[Wiki Documentación Python](https://github.com/fabiansato/javascript-cheatsheet/wiki "Documentación Python")

------------------------------
## Tipos de variables
#### tres tipos de datos: 

```javascript
numericos, booleanos, textos
```

#### Asignacion de variables
```javascript
numero = 10
```



#### Datos booleanos
```javascript
Valor = True
Valor = False
```

### entrada de datos 
```javascript
nombre = input("mensaje al usuario")
```
el input te lo guarda como cadena
entonces podemos asingnar el tipo antes de poner el input
```javascript
numero = int(input("ingresar un numero"))
```
cambiar el float por el tipo de variable, int, float string o boolean

------------------------------
## Mostrar datos por pantalla
#### Imprimir un string
```javascript
print("hola mundo")
```

#### salto de linea 
```javascript
\n
```

#### imprimir el tipo de variable
```javascript
print(type(nombrevariable))
```

#### mostrar int o float
Si ponemos un valor entero (int) ej 10 , un valor flotante (float) 10.5
ingresar comillas simples dentro de comillas dobles:
```javascript
variable = "la verdad o 'la verdad'"
```


### Separadores en print
Podemos separar internamente datos con la palabra clave "sep=" y terminar con "end="
```javascript
print(1, 2, 3, sep=', ', end='. ')
print(4, 5, 6, sep=' * ', end='.')
```


#### concatener
```javascript
print ("el resultado es: ",resultado)
colcamos unca coma para concatenar
```

#### tipado dinamico
podemos almacenar diferentes tipos de variables
```javascript
valor = 20
print(valor)
valor = "Sato"
print (valor)
```

#### comentarios

```javascript
# esto es un comentario 
''' comentario multilinea
esto es un comentario multinea ***
```
----------------------------------------
### operadores aritmeticos

```javascript
suma +
resta -
multiplicar *
dividir /
division entero (redondeado para abajo // 
modulo (que vamos a divir el resto de la division) %
exponenciacion  **
```

ejemplo:
```javascript
2**3 * (5/2 + (6*5))
```

#### prioridad de los operadores aritmeticos
```javascript
1. parentesis ()
2. exponenciacion **
3. multiplicacion, division, modulo *, / , %, NOT
4. suma y resta +, -, AND
5.  >, <, ==, >=, <=, !=, or 
```

----------------------------------------
### Operadores relacionales
se utilizan para establecer una relacion entre 2 valores
compara estos valores entre si y esta comparacion produce 
un resultado de certeza o falsedad (verdaderos o falsos)
tienen el mismo nivel de su evaluacion
los operadores relacionales tienen menor prioridad que los aritmeticos
```javascript
> mayor que
< menor que
>= mayor o igual que
<= menor o igual que
!= diferente (distinto que)
== igual 
```
ejemplo:
```javascript
resultado = 10 < 20
print (resultado)
```
nos mostrarà verdero o falso.

----------------------------------------
### operadores logicos
*permiten construir expreciones logicas y se obtiene como resultados booleanos
and && (perador de multiplicacion logica)
or  || (oeperador de suma logica)
not

#### operando AND

valor1 | AND | valor2  | Resultado
------------ | ------------- |------------- |------------- |
TRUE | AND | TRUE  | TRUE
TRUE | AND | FALSE  | FALSE
FALSE | AND | TRUE  | FALSE
FALSE | AND | FALSE  | FALSE


_Solamente basta un false para que el resultado sea false_

#### operando OR

valor1 | AND | valor2  | Resultado
------------ | ------------- |------------- |------------- |
TRUE | AND | TRUE  | TRUE
TRUE | AND | FALSE  |  TRUE
FALSE | AND | TRUE  | TRUE
FALSE | AND | FALSE  | FALSE

_Solamente es falso cuando ambos son false false (0 y 0)_


#### Operador de NOT negacion.
```javascript
not(true) = false
not(false) = true 
```

#### Prioridad de los operadores logicos

1. NOT
2- AND
3- OR 


Ejemplo:
```javascript
((a>b) or (a<c))and((a==c) or (a>=b))
```

aqui tenemos que pensarlo 
Es muy bueno para hacer matematica discreta.


--------------------------------
## Operadores de asignacion
a = 5 
a += 5 #suma en asignaciòn.
a -= 2 #resta en asignacion
a *= 8 #multiplacion en asignacion
a /= 9 #division en asignacion 
a **=8 #potencia en asignicacion
a %=6 #modulo de la asignicion 
valores que sirven para acortar el código.

-----------------------------
### salidas de datos
```javascript
print("hola",nombre,"tienes: ",edad,"años")
```
con funciones:
```javascript
print("hola {} tienes {} años".format(nombre,edad)
```
otra forma desde las ultimas actualizaciones de python:
```javascript
print(f"Hola {nombre} tienes {edad} años")
```



----------------------------
### CONDICIONALES
#### Condicionales (If, else)
```javascript
if resultado == 0:
contenido
else:
contenido del else
```

_podemos haer los valores aparte_
ej:
```javascript
vota=edad>=18 and edad<=70 and distancia<=500
if vota:
sasasa
else:
```



#### Condicionales (While)
```javascript
while(i<=n):
    suma=suma+i
    #print(i,suma)
    i=i+1
```


#### Condicionales (FOR)
Se coloca for _variable_ in range (_valor minimo_,_valor maximo_,_sumadevariable_)

```javascript
for i in range (1,11,2):
```
El antarior codigo es for variable _i_ en el rango de iniciacion en 1, hasta 11 con salteos de 2. El último numero no se incluye.

### Condicional for range(min_value, max_value)
función range(min_value, max_value) genera una secuencia con números min_value , min_value + 1 , ..., max_value - 1 . El último número no está incluido. 


### Forma reducida de range () 
Se realiza de la siguiente manera range(max_value) , en cuyo caso min_value se establece implícitamente en cero:
```javascript
for i in range(3):
    print(i)
# 0
# 1
# 2
```

### De esta manera, podemos repetir algunas acciones varias veces:
```javascript
for i in range(2 ** 2):
    print('Hello, world!')
```

#### Ejemplo de secuencia vacia
```javascript
for i in range(-5):
    print('Hello, world!')
```


#### Secuencia decreciente
Para iterar sobre una secuencia decreciente, podemos usar una forma extendida de range () con tres argumentos: range(start_value, end_value, step) . Cuando se omite, el paso es implícitamente igual a 1. Sin embargo, puede ser cualquier valor distinto de cero. El ciclo siempre incluye start_value y excluye end_value durante la iteración:
```javascript
for i in range(10, 0, -2):
    print(i)
# 10
# 8
# 6
# 4
# 2
```
----------------------------
###  MANEJO DE ARCHIVOS

Abrir archivo de lectura : 
```javascript
f = open("fichero.txt") 
```
Abrir archivo de lectura : 
```javascript
f = open("fichero.txt", "r") 
```

Abrir archivo para escribir desde cero : 
```javascript
f = open ("fichero.txt", "w") 

Abrir archivo para añadir al final :
```javascript
f = open ("fichero.txt", "a") 
```
⚠️ Recordar siempre al terminar de utilizar un archivo tanto para lectura o escritura cerrarlo.
 No hacerlo puede traer problemas para poder utilizarlo luego.

Simplemente basta llamar a 
```javascript
f.close() 
```
Donde f es la variable en donde se almacenó el archivo 
```javascript
(ejemplo, f = open("fichero.txt", "r") )
```

#### Leer de un archivo
Para leer del archivo, podemos usar las funciones f.readlines() y f.readline() 
Lectura de todo el archivo de golpe : 
```javascript
datos = f.readlines() 
(datos es una lista con todos los elementos del archivo)
```
Lectura de una línea completa : 
```javascript
dato = f.readline() 
```
(dato es una cadena con la primer línea del archivo)

#### funciones para conocer donde está el cursor en
el archivo y para ubicarlo en otro lugar
```javascript
archivo.tell() 
archivo.seek() 
```

#### funciones con write
```javascript
función f.write(“texto”)
f = open("arch.txt","w")
f.write("Esto es un archivo de texto\n");
f.write("Generado con python\n");
f.write("no es hermoso?\n")
f.close()
```

-----------------------------
### BIBLOTECAS
#### biblioteca import math
```javascript
import math
math.sqr(numero) #raiz cuadrada
math.exp(1) #exponente
math.pi #pi
math.log(2) #logaritmo

"*"*10 ##multiplica por 10 el contenido de una cadena
```

----------------------------
### Biblioteca Random
Debemos importar la biblioteca para utilizar sus funciones de trabajos aleatorios.
```javascript
import random
```
uso de biblioteca:
```javascript
random.randrange(inico,fin,paso)
random.randint(inicio,fin)

```
ejemplo
```javascript
import random
w=random.randrange(1,100,2)
print("w es:",w)

```
ejemplo con for range
```javascript
for i in range(3):
	w=random.randrange(1,100,2)
	print("w es:",w)
    # Por cada iteración obtiene un numero impar  aleatorio entre 1 y 99 .
Eventualmente podrían llegar a repetirse los números

```
```javascript
import random
w=random.randint(inicio,fin)
# Devuelve un entero aleatorio entre inicio y fin incluyendo los extremos.

```

----------------------------
### FUNCIONES
#### Funciones integradas
sirven para hacer conversiones entre tipos de datos
```javascript
n = int(10)
n = float(10)
n = str("10")
n = bin(1)
n = hex(10F)
n = int("010",2) #convierte un binario a entero
n = int("0xa",16) #convierte un numero hexa en base 16 a int
n = abs(-8) #devuelve un balor absoluto de -8
n = round (5.6) #lo redondea al numero entero mas cercano
n = len("fabian") #muestra cuantas caracteres tiene el string
```



---------------------------------
### Strings de caracteres
#### separa caracter a caracter
```javascript
for character in 'hello':
    print(character)

```
tamaño del caracter:
```javascript
a="Hola Mundo"
len(a)
```

Recorrer una cadena:
```javascript
a="mi cadena"

for caracter in a:
    print(caracter)

```
otra forma:
a="mi cadena"
```javascript
for caracter in a:
    print(caracter, end="")
```


-----------------------------
### FUNCIONES
```javascript
de f NOMBRE( LISTA DE PARAMETROS ) :
SENTENCIAS
```
ejemplo:
```javascript
de f mostrarGuion ( ) :
pr int ( "-" , end="" )
```

Pasar variables por argumentos:
```javascript
argumento = "Nunca digas nunca."
imprimirDosVeces ( argumento )
```


-----------------------------
### LISTAS (strings)
cracion de listas:
```javascript
lista = [7; 3; 4; 6; 10]
```
longitud de lista:
```javascript
len(lista)
```
agregar un elemento al final de la lista:
```javascript
lista:append(2)
```
quitar elementos de la lista:
```javascript
lista.pop(3)
#quita el tercer elemento de la lista empezando por 0
```
mostrar toda la lista por pantalla:
```javascript
print(lista)
```

Recorrer listas:
```javascript
animales = [''gato'', ''perro'', ''raton'']
i = 0
#forma 1
while (i < len(animales)):
print(animales[i])
i = i + 1
#forma 2
for i in range(len(animales)):
print (animales[i])
#forma 3
for elemento in animales:
print (elemento)
```


-----------------------------
### MATRICES (arrays)
Las matrices en Python son listas de listas.
se escriben así:
```javascript
[lista0, lista1,...,listaN]
```
ejemplo:
```javascript
numeros = [[1,2,4],[4,3,2],[9,8,7],[6,4,3],[5,6,8]]
	print(numeros[0][2]) # imprime 4
	print(numeros[3][0]) # imprime 6
	print(numeros[4][3]) # error
```
También podemos imprimir la matriz entera:
````javascript
print(numeros)
print(numeros[2])
```
saber la longitud de una variable
```javascript
longitud = len(numeros)
print (longitud) #imprime 5
print(len(numeros[2])) #imprime 3
```
Agregar datos a un array
```javascript
#por ejemplo
numeros[2].append(5) 
agrega un 5 al final de la lista 2
```

quitar datos en un array:
```javascript
numeros[3].pop(1) 
elimina la posición 1 de la lista 3
```


