# CSS
```
<!DOCTYPE html>
<html>
<head>
<title></title>
<meta charset="UTF-8">
<link rel="styleSheet" href="nombredelarchivo.css" type="text/css">
</head>
<body>
</body>
</html>
```
## Escribir comentarios
```
/* Entre estas figuras podemos escribir comentarios en CSS */
```
## Eliminar margenes
Utilizando el selector universal en CSS, eliminamos margenes que salen automaticamente en HTML
```
*{margin:0
  padding:0}
```
## Estilos por medio de clases
Se crea cuando la regla de estilo es igual para muchos elementos
.nombredelaclase{....}
Se aplica en elementos enteros como img, h1, spam, p, ...
h1.nombre{.....}
```
En HTML <div class="nombre"> En CSS .nombre{....}
```
Si queremos aplicar dos clases a un mismo elemento
```
En HTML <etiqueta class='nombredelaclase nombredelaclase nombredela clase ....>'
```
## Estilos por medio de id
Solo podemos aplicar esta clase a un solo elemento en la pagina de HTML
```
En HTML <div id="nombre"> En CSS #nombre{.....}
```
## Principales propiedades en CSS

### Padding
Marca la distancia entre el contenido de del cuadro y su borde
Podemos resumirlo en padding: 5px(arriba) 5px(derecha) 5px(abajo) 5px(izquierda)
### Margin
Separa un elemento HTML de otro
Podemos resumirlo en margin: 5px(arriba) 5px(derecha) 5px(abajo) 5px(izquierda)
### Font-family
Marca el tipo de fuente de escritura
hay muchos tipos: Arial, Vergana, Roman, Impact, Georgia, Sans-serif/serif, Arial narrow, ....
Podemos poner varias por si el navegador no reconoce alguna de ellas
### Font-style
Marca el estilo de letra
Hay tres clases: normal(normal), italic(cursiva)y oblique(oblicua) 
### Font-weight
Marca la anchura de las letras
Hay tres clases: normal(normal), bold(con peso), poner manualmente el peso(font-weight: 100, 200, 300,...)
### Font-size
Marca el tamaño de las letras
Hay varias clases: xx-small, x-small, small, maedium, large, x-large, xx-large// smaller, larger
Lo normal es poner nosotros la medida en px(minimo 15px)
### Font-variant
Marca el tamaño de las letras mayusculas
Hay dos formas: normal(normal), small-caps(Reduce el tamaño)
##### Resumen de reglas
Todas estas reglas pueden resumirse de esta forma:
.nombre{font: bold(style) small-caps(variant) 15px(size) arial(family)}
#nombre{font: bold(style) small-caps(variant) 15px(size) arial(family)}
siempre sin comas
Los últimos font han de ser font-size y font-family
### Line-height
Marca la separación entre lineas
Lo normal es 1.5em.
### Letter-spacing
Marca la separación entre las letras de un texto
Se mide en px
### Word-spacing
Marca la separación entre palabras en un texto
Se mide en px
### Text-indent
Marca la separación del primer parrafo con respecto al margen
Puede ser positivo(10px) o negativo(-10px)
### Text-align
Marca la posición de un texto
Puede ser: left, right, center o justify
### Text-decoration
Hay varias formar de decorar un texto determinado:
none (se muestra sin decoración)
underline (subrayado)
overline (sobrerrayado)
blink (El texto parpadea)
line-through (tachado)
### Text-transform
Convierte el texto a letras mayusculas o minusculas
uppercase (Todo el texto en mayusculas)
lowercase (Todo el texxto en minusculas)
Capitalize (convierte a mayusculas la primera letra de cada palabra enel texto)
## Bordes
Pdemos crear bordes en todo el cuadro o en una parte(border-top, border-right, border-left o border-bottom)
Propiedades de los bordes:
### Border-width
Marca elancho de los bordes
### Border-style
Hay varios tipos:
none
solid
double
doted - El borde esta compuesto por puntos
dashes - El borde esta compuesto por rectangulos
inset - El borde esta compuesto por dos colores similares(más oscuro el borde izquierdo y superior y más claro el borde derecho e inferior)
outset - El borde esta compuesto por dos colores similares(más claro el borde izquierdo y superior y más oscuro el borde derecho e inferior)
groove - El borde esta compuesto por dos colores similares(más oscuro el de fuera y más claro el interior)
ridge - El borde esta compuesto por dos colores similares(más claro el de fuera y más oscuro el interior)
### Border-color
Marca el color de los bordes
#### Resumen de reglas
Podemos poner las tres propiedades de resumidas
.nombre{border: 5px(width) solid(style) red(color)}
#nombre{border: 5px(width) solid(style) red(color)}
En este orden y no separado por comas
### Border-radius
Permite crear esquinas redondeadas en los cuadros
No es necesario que exista un borde
Podemos aplicarlo a todo el cuadro (border-radius: 20px) o a una parte (border-top-radius: 20px, border-right-radius: 20px, .....)
### border-sizing: border-box
Al utilizar la propiedad border-sizing: border-box; Los distintos cuadros que estan dentro de un cuadro a su vez, se ordenan quedando ajustados dentro del primer cuadro.
Ya no tenemos que calcular la medida de los cuadros y añadirle las medidas de los bordes y del padding
La propiedad hace estos calculos solos
## Listas
Dentro del elelmento li podemos crear un em si queremos que lgodestaque
Propiedades relacionadas a listas:
### List-style-type
Marca la forma de enumerar los elementos li en una lista:
none
disc
circle
square
decila
lower-roman (numeros romanos)
upper-roman (numeros romanos)
lower-alfa (letras)
upper-alfa (letras)
### List-style-position
inside - En caso de que exista un list-style-tipe, quedará dentro del item
outside - En caso de que exista un list-style-tipe, quedaran fuera del item
### List-style-image
Nos permite crear un list-style-type con una imagen determinada:
list-style-image: url("imagendeseada.png/gif/jpg")
```
En HTML
<ul class="nombre">
  <li><em> texto</em></li>
  <li></li>
  ...
</ul>
```
## Fondos (background)
Existen varias propoiedades relacionadas al fondo de pantalla
### background-color
Marca el color del fondo
### background-image
Estable una imagen de fondo en la pagina o en la parte deseada
background-image: url("enlace deseado.jpg/gif/png")
Cuando utilizamos imagenes, podemos usar una seria de propiedades:
##### background-repeat
Puede ser: repeat - la imagen se repite varias veces en el fondo
           no-repeat - Solo se muestra la misma imagen en el fondo
##### background-position
Posicionas la imagen en la pantalla
Puede ser: top left, top center, top right, center right, center center, center left, botton right, botton center, botton left
Solo podemos sirve si utilizamos la propiedad background-repeat: no-repeat
##### background-attachment
Esta puede ser: fixed - La imagen queda fija a todo el fondo de la pantalla
                scroll - La imgen se mueve al bajar o subir la rueda del ratón
## Menu
Podemos crear un menu vertical (un elemento sobre otro):
```
En HTML
<div id="menu">
  <p><a href="http://nombredelapagina.com">texto</a></p>
  <p><a href="http://nombredelapagina.com">texto</a></p>
  ....
</div>
En CSS
menu{
    }
menu p{
      }
menu a{
      
      }
```
Podemos crear un menu horizontal (un elemento junto a otro) mediante ul o ol:
```
En HTML
<ul class="menu">
  <li><a href="http://nombredelapagina.com">texto</a></li>
  <li><a href="http://nombredelapagina.com">texto</a></li>
  ...
</ul>
En CSS
menu{
    }
menu a{
    }
menu li{float:left; - Es imprescindible poner esta propiedad
    }
```
## Tablas
Para centrar la tabla en la pagina debemos poner table {margin:0 auto;}
##### Propiedades de la table:
cellspacing, mide la distancia entre los bordes de los elementos (maximo 10)
cellpadding, mide la distancia entre los bordes y su contenido (maximo 10)
El tamaño de la tabla se fija mediante la propiedad width aplicado en le table
Por defecto el contenido de una celda se muestra centrado verticalmente y alineado horizontalmente a la izquierda
Esto lo podemos cambiar utilizandolas propiedades:
Modificacar horizontalmente propiedad align: center, right, left o justify (no en table)
Modificar verticalmente propiedad valign: midle, top, botton o justify
Si queremos que las primeras filas formen un encabezado utilizaremos el atributo thead. Si queremos destacar las ultimas el atributo tfood
Los bordes exteriores de una tabla se fijan mediante la propiedad border-collapse, y los atributos border-collapse: separate (la que sale por defecto) o border-collapse: collapse (sin borde exterior)

## Pseudoclases en el elemento a
Permiten variar un elemento dependiendo de donde se encuentre el ratón
:link - es el estado del elemento antes de que el cursor haga nada
:visited - Cambia el estado una vez hayamos hecho click sobre el elemento
:hover - Cambia el estado del elemento cuando el cursor esta sobre el elemento
:active - Cambia el estado del elemento cuando el cursor esta pulsado sobre el elemeneto
Para que funcione ha de respetarse siempre este orden: link, visited, hover, active
```
menu a: link{ } menu a: visited{ } menu a: hover{ } menu a: active{ }
```
## Pseudoelementos
A diferencia de las pseudoclases afectan solo a una parte del elemento y no a todo
##### La sintaxis es siempre con dos puntos ::
Hay cuatro clases:
  - first-letter
  Sirve para definir la primera letra sin necesidad de crear un spam
  p/h1/h3/li/...::first-letter {color:, font-size:, font-weight:, ....}
  - first-line
  sirve para definir la primera linea de un texto sin necesidad de crear un spam
   p/h1/h3/li/...::first-line {color:, font-size:, font-weight:, ....}
  - before
  sirve para añadir un caracter previo a un contenido determinado (puede sercualquier caracter: !, /, ?,...)
  p/ h1/ h3/ strong/ li/....::before {content:"caracter deseado"}
  - after
  sirve para añadir un caracter posterior a un contenido determinado (puede sercualquier caracter: !, /, ?,...)
  p/ h1/ h3/ strong/ li/....::after {content:"caracter deseado"}
### Selectores de hijos
Nos permiten aplicar a un elemento o a un conjunto de elementos
###### Selector de un tipo de elemento:
h1 { }   h1.nombre { }    h1#nombre { }
###### Selectores descendientes
Cuando se definen dos elementos
Los estilos se aplican solo al segundo elemento
h2 p { }   ul li { }    tr td { }
###### Selectores de hijos
Es muy similar al selector descendiente, pero se sustituye el espacio en blanco por >
h2>p { }    ul>li { }    tr>td { }
###### Selector de hermano adyacente
En este caso solo se aplica el estilo al primer elemento que viene inmediatamente despues del primer elemento
h2+p { } Solo se aplica al primer p que haya
ul+li { } Solo se aplica al primer li que haya en la lista
En zaso de que haya varios elementos iguales y pidamos un lemento+elemento
p+p { } El estilo se aplica a todos los elementos p, menos al primero
li+li { } El estilo se palica a todos los elementos li, menos al primero
###### Selector de hermano general
Permite seleccionar todos los elementos iguales que esten incluidosen el primer elemento
h2~p { }    ul~li { }

   
  


