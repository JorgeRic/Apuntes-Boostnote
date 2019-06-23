# OBJETOS Y MATRICES
## Objetos
Es una coleccion compuesta por clave-valor (key-value)
key - es un string que identifica la propiedad de un objeto
value - es el contenido asociado a la clave indicada.
Solo puede haber un valor para cada clave
```javascript
var nombre = {key1: 'value1', key2: 'value2', ....}
```
Un array puede contener un conjunto de objetos
```
var nombre = [{key1: 'value1', key2: 'value2', ....},{key1: 'value1', key2: 'value2', ....},{key1: 'value1', key2: 'value2', ....}];
```
#### Acceso a los value
Se puede acceder a los keys de dos maneras
```
console.log(nombredelvar.key);
console.log(nombredelvar['key']);
```
#### Añadir keys en un objeto
```
nombredelvar.nuevakey = 'value';
nombredelvar['nuevakey'] = 'value'
```
#### Modificar un valor en una key
```
nombredelvar.keyquequeremos modificar = 'nuevovalue';
nombredelvar['keyquequeremosmodificar'] = 'nuevovalue'
```
#### Añadir objetos a un array con objetos
```
nombredelvar.push({key:value})
```
#### Eliminar keys
```
delete nombredelvar.keyaeliminar;
delete nombredelvar['keyaeliminar'];
```
#### Ver lista de keys o values
```
Object.keys(nombre del var)
Object.values(nombre del var)
```
#### Filtar objetos en un array con objetos
Para filtrar los bojetos de un array debemos utilizar la function filter
Utilizando esta funcion nos devolverá los objetos que cumplan la condicion solicitada a traves de un array
```
var personas = [{nombre: 'Juan', edad: 18}, {nombre: 'Paco', edad: 25}, {nombre: 'Maria', edad: 17}]
Si queremos filtrar las personas que sean mayores de 18 haremos
var mayores18 = personas.filter(function(persona) {
return persona.edad >= 18;
});
Esto nos devolverá [{nombre: 'Paco', edad: 25},{nombre:'Juan', edad: 18}]
```
Tambien podemos crear un filtro doble, triple, etc...
```
var personas = [{nombre: 'Juan', edad: 18, altura: 1.8}, {nombre: 'Paco', edad: 25, altura: 1.95}, {nombre: 'Maria', edad: 17, altura: 1.7}]
var nombre = personas.filter(function(persona){
return persona.edad > 18}).filter(function(persona){
return persona.altura>= 1.8
})
Esto nos devuelve [{nombre: 'Paco', edad: 25, altura: 1.95}]
```
Podemos filtrar a traves de una function
```
var personas = [{nombre: 'Juan', edad: 18, altura: 1.8}, {nombre: 'Paco', edad: 25, altura: 1.95}, {nombre: 'Maria', edad: 17, altura: 1.7}]
function filtrar(key,value){
return personas.filter(function(persona){ return persona[key] >= value})
}
console.log(filtrar('edad',18))
Esto nos devolverá [{nombre: 'Paco', edad: 25, altura: 1.8},{nombre:'Juan', edad: 18, altura: 1.95}]
```
Podriamos mejorar esta function utilizando más keys y values
```
var personas = [{nombre: 'Juan', edad: 18, altura: 1.8}, {nombre: 'Paco', edad: 25, altura: 1.95}, {nombre: 'Maria', edad: 17, altura: 1.7}]
function filtrar(key1, value1, key2, value2){
return personas.filter(function(persona){return persona[key1] >= value1 && persona[key2] >= value2});
}
console.log(filtrar('edad', 18, 'altura', 1.9))
Esto nos devolverá [{nombre: 'Paco', edad: 25, altura: 1.95}]
```
Aun podriamos crear un filtro sustitutendo el nombre del var
```
var personas = [{nombre: 'Juan', edad: 18, altura: 1.8}, {nombre: 'Paco', edad: 25, altura: 1.95}, {nombre: 'Maria', edad: 17, altura: 1.7}]
function filtrar(colection,key1, value1, key2, value2){
return colection.filter(function(elemento){return elemento[key1] >= value1 && elemento[key2] >= value2});
}
console.log(filtrar(personas (sin comillas), 'edad', 18, 'altura', 1.9))
Esto nos devolverá [{nombre: 'Paco', edad: 25, altura: 1.95}]
```
#### Eliminar objetos en un array con objetos
Para eliminar un objeto determinado o un grupo de objetos debemos utilizar la function filter
```
var personas = [{nombre: 'Juan', edad: 18}, {nombre: 'Paco', edad: 25}, {nombre: 'Maria', edad: 17}]
Si queremos eliminar a Juan haremos
personas = personas.filter(function(persona){
return persona.nombre!== 'Juan';
});

Esto nos devolverá 
personas = [{nombre: 'Paco', edad: 25}, {nombre: 'Maria', edad: 17}];
```
#### Crear objetos a partir de otros objetos
```javascript
Supongamos que tenemos dos arrays con objetos diferentes:
var fabricantes = [{nombre:'Seat', paisOrigen:'España',numeroModelos: 5}, {nombre: 'bmw', paisOrigen: 'Alemania', numeroModelos: 7}];
var motores = [{nombre:'Zar, paisOrigen:'Rusia',numeroModelos: 8}, {nombre: 'Cesar', paisOrigen: 'Italia', numeroModelos: 3}];
Si queremos crear un var de objetos nuevos hacemos:
var cocheNuevo = [];
var coche = [{referencia: 1, modelo: 'Toledo', fabricantes[0], motores[1]},{referencia: 2, modelos: 'Alicante', fabricantes[1], motores[0]}];
cocheNuevo.push(coche);
Si queremos hacer un nuevo modelo de un marca determinada, pero con un motor diferente haremos
var seat = fabricantes.filter(function(fabricante){
return fabricante.nombre === 'Seat';
})[0];
var zar = motores.filter(function(motor) {
return motor.nombre === 'Zar'[1];
})
```
var cocheNuevo2 = {referencia: 1, fabricante: seat, motor: zar, ....};
## Matrices
Son datos representados como filas y columnas
Podemos representar cosas como estructuras 3D y tableros de juego
Podemos acceder a los elementos de una matriz a traves de rows y cols
```
var texto = nombre de la matriz [      column
                  [valor1, valor2, valor3, ....],
 row              [valor1, valor2, valor3, ....],
                  [valor1, valor2, valor3, ....],
];
Para acceder al row hacemos: var row = texto[0 / 1 / 2 / 3....]
Para acceder al row y al column: var rowColumn = texto[0, 1 , ..][0, 1 ,2, ....]
```
#### Iteración en una matriz
Para poder hacer una iteración en una matriz, debemos hacer una doble iteración usando el for
```
En primer lugar haremos una iteración sobre la matriz usando su nombre del var
var matriz = [
['null', 'null', 'X'],
['null', 'null', 'null'],
['null', 'null', 'null']
];
for(var i = 0; i < matriz.length; i++) {
var row = matriz[i]
}
for(var j = 0; j < row.length; j++) {
var column = row[j]
}
if(colum ==='X'){
console.log('texto')
}
```

