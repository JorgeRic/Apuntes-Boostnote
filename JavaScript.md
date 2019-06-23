# JAVASCRIPT
```
<!DOCTYPE html>
<html>
<head>
<title></title>
<meta charset="UTF-8">
<link rel="styleSheet" href="nombredelarchivo.css" type="text/css">
<script src="nombredelarchivo.js"></srcipt>
</head>
<body>
</body>
</html>
```
## Escribir comentarios
```
/* Entre estas figuras podemos escribir comentarios en CSS de más de dos lineas */
//Comentarios internos en una linea
```
## console.log / document.write
Podemos escribir texto de manera más eficaz así:
```
console.log(`texto deseado ${nombredelvar.nombredelkey}`)
Si hay dos cosas
console.log(`texto deseado ${nombredelvar.nombredelkey},${nombredelvar.nombredelkey}`)
```
## Arrays
Los arrays son colecciones ordenadas de valores dentro de un contenedor unico
Los arrays pueden contener otros arrays
```
var array = [5, 6, 'a'];
var array2 = [[5, 6, 'a'],[1, 6, 'g']];
```
Añadir elementos a un array
```
var array = [5, 6, 'a'];
arra.push(10); // Resultado var array = [5, 6, 'a', 10];
var array3 = [{name: 'Celia', edad: 28}, {name: 'Paco', edad: 25}];
array3.push[{name: 'Jose', edad: 40}] // 
Resultado array3 = [{name: 'Celia', edad: 28}, {name: 'Paco', edad: 25}, {name: 'Jose', edad: 40}];
```
Para filtrar los arrays utilizamos
```
var coches = ['seat', 'ford', 'citroen', 'bmw'];
var coches[0]   Nos devuelve 'seat'
Cuando el var esta compuesto por un conjunto de arrays
var coches = [['seat', 'ford', 'citroen', 'bmw'],['grande', 'pequeño', 'bonito']]
var coches[0][2]    Nos devolverá 'citroen'
El [0] hace referencia al primer array y [2] al numero de item que se encuentra en ese array
```
.filter
Podemos aplicarle la function .filter a cualquier array
```
var array = [5, 8, 9, 4]
Si queremos obtener los numeros pares
var array = [5, 8, 9, 4].filter(function(elemento){
return elemento %== 0
})
Devuelve array = [8,4]
Si queremos obtener los numeros los numeros mayores de 4
var array = [5, 8, 9, 4].filter(function(elemento){
return elemento > 4
})
Devuelve array = [5, 8, 9]
```
Estas dos funciones pueden encadenarse
```
var array = [5, 8, 9, 4].filter(function(elemento) {
return elemento !== 0
}).filter(function(elemento){
return elemento > 4
})
Devuelve 8

```
## String
caracter de un var que se encuentra encerrado en ' ' o " "
#### Metodos
###### length
Utilizando este metodo, conocemos el numero de strings que hay en un array
var nombre = ['Jorge', 'Rico']
nombre.length Nos devuelve 2
###### charAt
Retorna el caracter del indice especificado
var nombre = 'jorge rico'
nombre.charAt(0) Nos devuelve j
nombre.charAt(2) Nos devuelve r
Tener en cuenta que cuando debemos revisar el conjunto de los strings que forman un array deberemos hacer un for por todos sus elementos
###### indexOf
Devuelve el valor de la primera aparición de un valor especificado en una cadena
devuelve -1 si el valor especificado no esta en esa cadena
```
var array = [2, 8, 5, 8, 8]
array.indexOf(2)    Nos devuelve 0
array.IndexOf(6)    Nos deuelve -1
array.IndexOf(8)    Nos deuelve 1(posicion de la primera aparicion)

Tambien podemos pedirle que nos diga la posicion determinada de un valor que se repite
array.IndexOf(8(nombre del valor),2(cantidad de repeticiones deseada))    Nos deuelve 3
array.IndexOf(8,3)    Nos deuelve 4
```
Tener en cuenta que cuando debemos revisar el conjunto de los strings que forman un array deberemos hacer un for por todos sus elementos
###### toUpperCase( )
Convierte todos los caracteres del string en mayusculas
var nombre = nombre.toUpperCase()
###### toLowerCase( )
Convierte todos los caracteres del string en minusculas
var nombre = nombre.toLowerCase()
## Ordenes prioritarias
En el caso de darse varias operaciones, este es el orden de prioridades
1º operaciones entre parentesis ( )
2º operaciones exponenciales **  2**3 = 2*2*2
3º multiplicaciones *
4º divisiones /
5º sumas +
6º restas -

## Enlazar con una carpeta HTML
Seleccionamos un elemento HTML con Javascript seleccionando su atributo class o id
```
En HTML
<div class="nombre de clase"></div>
<div id="nombre de id"></div;
En Javascript
var nombre = document.getElementsByClassName('nombre de la clase');
var nombre = document.getElementById('nombre del id');
```
## Operadores logisticos
&& es igual a 'y'
|| es igual a 'o'
!== es ihual a distinto
## Estructura switch
Sirve para sustituir a 'if' 'else' en estructuras muy largas
```
swicht(nombre del var){
case'...' console.log('....');break;
case'...' console.log('....');break;
case'...' console.log('....');break;
default:console.log('.....')
}
```
## acumulador (while)
Si nos piden que ingresemos una cantidad de valores determinados podemos hacerlo utlizando el while
```
var x = 0;
while(x<= numero determinado){
car nombre = parseInt(prompt('texto'))
x = x + 1;
}
console.log(texto)
```
## do/while
Estructura repetitiva en la que se fija el tope de repeticiones a traves del while
El programa finaliza cuando cargamos un valor determinado
```
do{

}while(valor!==tope)
```
## switch
Sirve para sustituir en ciertas ocasiones al if / else
switch(nombre) {
case 'texto': console.log('texto'); break;
case 'texto': console.log('texto'); break;
case 'texto': console.log('texto'); break;
....
default: console.log('texto');break;
}

## Datos
Hay tres tipos:
-string: datos rodeados de comillas(listas)
-boleanos: verdadero o falso
-texto: datos sin comillas
## Random
Sirve para conseguir un numero aleatorio entre un numero determinado por nosotros
```
Math.random()*numero a elegir;
Si queremos que no nos devuelva decimales haremos
Math.floor(Math.random()*numero a elegir) o parseInt(Math.random()*numero a elegir)
```
## Convertir texto en lista(string)
Utilizaremos la funcion'split'
```
var texto="hola que tal"
function parseList(texto){
var lista=texto.split("");
var newList=[ ];
for(var i=0; i<lista; i++) {
newList.push(parseInt(lista[i]));
}
return newList;
}
```
## Resultados con decimales
En una funcion con return podemos fijar el numero de decimales de esta forma
return nombre.toFixed(numero de decimales deseado)
## Method
Hay varias propiedades
#### delete
Sirve para eliminar un elemento 
delete nombredelvar(posicion en la que se encuentra en el array)
Es mejor utilizr splice, ya que con delete su posición en el array aparecerá como indefinida
#### push
Sirve para añadir un nuevo item al final de la lista
nombredelvar.push('nuevo item', 'nuevo item',...)
#### pop
Elimina el último item en el string
nombredelvar.pop()
#### unshift
Añade items al principio del string
nombredelvar.unshift('nuevo elemento', 'nuevo elemento', ....)
#### shift
Elimina el primer item del string
nombredelvar.shift()
#### splice
Elimina y/o añade nuevos items en un string
nombredelvar.splice(valor numerico(determina la posicion en el arrya)), valor numerico(determina la cantidad de items a eliminar), 'nuevo elemento'(item o items a añadir en el string))
```
var nombre = ['a','b','c']
nombre.splite(numero(marca la posicion del string),numero(determina la cantidad de strings a eliminar),'nuevo string', 'nuevo string'....)
```
#### join
El metodo join encadena los strings de un array con el caracter que nosotros queramos
```
var cadena = [5,6,8,8]
var nombre = cadena.join('-'  / '<br>' / '---' / ....)
el resultado será nombre = [5-6-8-8]
Si no ponemos un caracter apareceran comas por defecto
```
#### includes
Hace una busqueda en un array y nos dice si existe un item determinado o parte de eĺ
var nombre=['item','item',....]
nombredelvar.includes('item buscado')
#### indexOf
Sirve para saber la posicion que ocupa un item en un array
nombredelvar.indexOf('nombredelitem')
En caso de que el item no se encuentre en la cadena nos devolverá -1
#### contact
Nos permite unir dos o más arrays
var nombre1 = ['1', '2'];
var nombre2 = ['3', '4'];
var nombre3 = nombre1.contact(nombrre2)
El resultado es nombre3 = ['1', '2', '3', '4']
si hay tres arrays hariamos nombre4 = nombre1.contact(nombre2, nombre3);
## Loops
#### while
Hace que la computadora haga un bucle a traves de la matriz una cantidad desconocida de veces
while(condicion){ }
#### for
Hace que la computadora haga un bucle a traves de la matriz una cantidad conocida de veces
for(var = 0 (condicion de inicio); i < matriz.length(condicion de parada); i++(va aumentando el bucle a traves de la matriz)){ }
Si queremos que el bucle sea al reves haremos:
```
for(var = matriz.length - 1(inicia el bucle desde el ultimo elemento); i>=0(condición de parada); i--(va reduciendo el bucle a traves de la matriz)){ }
```
Si queremos comparar dos matrices:
```
for(var i = 0; i < matriz1.length; i++){
    for(var j = 0; j < matriz2.length; i++){
    if(matriz1 === matriz2)
    console.log(matriz1) // Estos serán los items que coincidan en ambas matrices
    }
}
```
#### forEach
Sirve para sustituir al for
Ejecuta la funcion callback una vez para cada uno de los items presentes en un array en orden ascendente
Nos devuelve un resultado
```
var nombredelvar = ['5','4'];     
var suma = 0;
nombredelvar.forEach(function(nombredelelemento){
suma = suma+nombredelelemento;
})
Nos devuelve 9
```
#### map
Sirve para sustituir al for
Ejecuta la function callback una vez para cada uno de los items presentes en un array
Nos devuleve un array mediante un return
```
var nombredelvar = ['5,'4'];
var doble = nombredelvar.map(function(elemento){
return elemento*2;
})
Nos devuelve un array doble=['10','8']
```
