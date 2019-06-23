# FLEXBOX
Creamos un contenedor a traves de un div en el que dentro van varios contenedores

```
<div id="contenedor">
  <div id="cuadro1"></div>
  <div id="cuadro2"></div>
  <div id="cuadro3"></div>
  ....
</div>
```
Los divs interiores se redimensionana en ancho y largo automaticamente dependienedo de su contenido
## propiedades aplicadas al contenedor
#### flex-direction
Puede ser de 4 tipos:
###### row
Los cuadros se agrupan de izquierda a derecha
Es la que sale por defecto
###### row-reverse
Los cuadros se agrupan de derecha a izquierda
###### column
Los cuadros se agrupan en columna del primero al ultimo
###### column-reverse
Los cuadros van uno debajo del otro del último al primero
```
#contenedor{ display: flex;
             flex-direction: row/ row-reverse/ column /column-reverse;
            }
```
#### justify-content
###### flex-start
Los cuadros aparecen pegados unos a otros al principio del cuadro
Sale por defecto
###### flex-end
Los cuadros aparecen pegados unos a otros al final del cuadro
###### flex-center
Los cuadros aparecen pegados unos a otros en el centro del cuadro
###### space-betwen
Los cuadros ocupan todo el espacio disponible dejando el mismo hueco entre ellos.
No deja espacios ni al principio ni al final
###### space-around
Los cuadros ocupan todo el espacio disponible dejando el mismo espacio entre ellos.
Deja este mismo espacio al principio y al final
```
#contenedor{ display: flex;
             flex-direction: row/ row-reverse/ column /column-reverse;
             justify-content: flex-start/ flex-end/ flex-center/ space-betwen/ space-around;
            }
```
#### align-items
###### strecht
Los items ocupan todo el largo o el ancho del cuadro(dependiendo del flex-direction establecido).
Salvo que hayamos determinado un witdh y un height, es lo que aparece por defecto
###### flex-start
Los items se agrupan a la izquierda del cuadro
###### flex-end
Los items se agrupan a la derecha del cuadro
###### center
Los items se agrupan en el centro del cuadro
```
#contenedor{ display: flex;
             flex-direction: row/ row-reverse/ column /column-reverse;
             justify-content: flex-start/ flex-end/ flex-center/ space-betwen/ space-around;
             align-items: strescht/ flex-start/ flex-end/ center;
            }
```
#### flex-wrap
###### wrap
Cuando los items son muchos y no caben en el cuadro, podemos usar esta propiedad para que los items se agrupen en diferentes filas
###### nowrap
Los items se agrupan siempre en el eje principal y en una sola linea
Es la que aparece por defecto
```
#contenedor{ display: flex;
             flex-direction: row/ row-reverse/ column /column-reverse;
             justify-content: flex-start/ flex-end/ flex-center/ space-betwen/ space-around;
             align-items: strescht/ flex-start/ flex-end/ center;
             flex-wrap: wrap/ nowrap;
            }
```
##### flex-flow
Esta propiedad resume las propiedades flex-direction y flex-wrap
Los atributos serian: row-wrap / row-nowrap / row-reverse wrap/ row-reverse nowrap/ column-wrap / column-nowrap / column-reverse wrap / column-reverse nowrap
## Propiedades aplicadas a los items
##### flex-grow
Utilizando esta propiedad damos un ancho determinado al item
Solo admite valores enteros positivos
Si aplicamos el fle-grow a todos los items, todos tendrán el mismo ancho
##### flex-shrink
Cuando los items ocupan todo el ancho o el largo del contenedor (dependiendo del flex-direction del cuadro), comienza a contraerse para poder caber
Aplicando esta propiedad en uno o varios items hacemos que estos no pierdan su alto o ancho original
La medida por defecto de todos es 1, por lo que debemos aplicar siempre el valor 0
##### flex-basis
Se utiliza para ponerle medida al item
Si el flex-direction del contenedor es row, representa el witdh
Si el flex-direction del contenedor es column, representa el height
Se puede utilizar en %, px o em
#### flex
Estas tres propiedades pueden reducirse en una uilizando la propiedad flex
```
#cuadro1 { flex: numero (susutituye el flex-grow) numero 0 - 1(sustituye al flex-shrink) % px em (sustituye al flex-basis)
         }
```
##### order
Los items aparecen siempre en el mismo oreden en el que los creamos en HTML
Si queremos cambiar ese orden debemos crear la propiedad order en el item en todos los items
Estableceremos un valor numerico en el que queremos que aparezcan en la pantalla
##### align-self
Determinamos el espacio que ocupa cada item en el contenedor
Hay varios tipos
###### auto
Es el que aparece por defecto
###### flex-start
El item aparece en la parte superior o izquierda, dejando el espacio en la otra parte
###### flex-end
El item aparece en la parte inferior o derecha, dejando el margen en la otra parte
###### center
Deja un margen arriba y abajo, o a la izquierda y la derecha. Depende del contenido
###### strescht
El item ocupa todo el ancho o el largo del contenedor, dependiendo del flex direction
```
#cuadro1 { flex-grow: valor numerico (determina el ancho del item);
          flex-shrink: valor numerico(0-1)(evita que un item se contraiga por falta de espacio);
          flex-basis: valor numerico en %, em o px(Ponemos medida al item);
          flex: (sustituye a los tres primeros);
          order: (determina el orden visual en el que queremos que se vean en pantalla);
          align-self: (determina el espacio que ocupa cada item en el contenedor);
         }
```
          

