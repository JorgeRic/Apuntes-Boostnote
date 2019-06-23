# CSS3
## Sombreado de imagenes y textos
### Sombra exterior
Permite definir a un objeto en una pagina
box-shadow: 10 px(posicionamiento horizontal), 10 px(posicionamiento vertical), 10px (radio de desenfoque) color;
Si el posicionamiento horizontal es positivo la sombra esta a la derecha. Si es negativo a la izquierda
si el posicionamiento vertical es positivo la sombra esta por debajo, si es negativo esta por encima
El radio de desenfoque marca como veremos el color. A más numeración más borroso se vera
### Sombras multiples
Si queremos que el objeto tenga dos sombras debemos hacer lo mismo, pero con un elemento doble
box-shadow: 10 px(posicionamiento horizontal), 10 px(posicionamiento vertical), 10px (radio de desenfoque) color,
            10 px(posicionamiento horizontal), 10 px(posicionamiento vertical), 10px (radio de desenfoque) color;
Tantas como queramos
### Sombra interior
Si queremos que la sombra sea interior debemos añadir el atributo inset
box-shadow: inset 10 px(posicionamiento horizontal), 10 px(posicionamiento vertical), 10px (radio de desenfoque) color;
### Sombra con transparencia
Si queremos añadir un grado de transparencia a la sombra hacemos:
box-shadow: 10 px, 10 px, 10px rgb(nº de color, nº de color o 0, nº de color o 0, grado de transparencia);
El grado de transparencia se mide del 0 al 1 (numeros decimales)
### Sombreado de texto
Para poder crear una sombra en un texto y no en todo un elemento podemos utilizar esta propiedad:
text-shadow: 10 px(posicionamiento horizontal), 10 px(posicionamiento vertical), 10px (radio de desenfoque) color;
Si el posicionamiento horizontal es positivo la sombra esta a la derecha. Si es negativo a la izquierda
si el posicionamiento vertical es positivo la sombra esta por debajo, si es negativo esta por encima.
Podemos crearmultiples sombras:
text-shadow: 10 px(posicionamiento horizontal), 10 px(posicionamiento vertical), 10px (radio de desenfoque) color,
             10 px(posicionamiento horizontal), 10 px(posicionamiento vertical), 10px (radio de desenfoque) color;
Tantas como queramos
## Transformaciones 2D
Propiedades:
#### Transform: rotate
Sirve para inclinar un elemento
El grado de inclinacion se determina por el numero de deg
```
.nombre{transform: rotate(nº deg)};
#nombre{transform: rotate(nº deg)};
```
Si el numero es positivo se inclina a la derecha
Si es negativo se inclina a la izquierda
#### Transform-origen
Permite cariar el punto fijo central
```
.nombre{transform-origen: left-top / left-bottom / right-top / right-bottom};
#nombre{transform-origen: left-top / left-bottom / right-top / right-bottom};
```
#### Transform-scale
Nos permite agrandar o reducir el tamaño del elemento
```
.nombre{transform-scale:(nº,nº)};
#nombre{transform-scale:(nº,nº)};
```
El primer numero hace referencia al alto. El segundo al ancho
Los numero van del 0 al 2(de origen aparece el 1). Admite decimales
#### Transform-traslate
Nos permite mover el elemento
```
.nombre{transform-traslate(x px, y px)};
#nombre{transform-traslate(x px, y px)};
```
con x nos movemos a la derecha(numero positivo) o la derecha (numero negativo)
con y nos movemos hacia arriba(numero positivo) o hacia abajo (numero negativo)
#### Transform-skew
Nos permite torcer el elemento
```
.nombre{transform-skew(x-horizontal deg, y-vertical deg)};
#nombre{transform-skew(x-horizontal deg, y-vertical deg)};
```
#### Aplicacion conjunta
Podemos aplicarlas todas mediante:
```
.nombre{transform-rotate(xdeg) scale(nº, nº) traslate(x px, y px) skew(x-horizontal deg, y-vertical deg)};
```
## Opacity
Propieda que nos permite ver los elementos con una determinada opacidad
```
.nombre{opacity: nº del 0 al 1 de forma decimal)};
```
Por defecto la opacidad es 1
## Multiples columnas
Cuando queremos que un texto se vea dentro de un elemento con distintas columnas, podemos utilizar la propiedad 'column-count' y el numero de columnas que queremos que se vean
```
.nombre{columnt-count: nº de columnas};
```
#### columnas dinamicas
Sirve para determinar el ancho de cada una de las columnas:
```
.nombre{columnt-count: nº de columnas;
        column-width: ancho en px;
};
```
La cantidad de las columnas dependerá del texto que tenga cada columna y del texto que hayamos establecido.
Si no hay un heigth establecido, este se creará por defecto adaptado al texto 
#### separación entre columnas
Podemos establecer la separación entre columnascon la propiedad column-grap
```
.nombre{columnt-count: nº de columnas;
        column-width: ancho en px;
        column-grap: medida en px;
};
```
#### bordes entre columnas
Podemos establecer lineas entre columnas con la propiedad column-rule y los atributos grosor, tipo y color
```
.nombre{columnt-count: nº de columnas;
        column-width: ancho en px;
        column-grap: medida en px;
        column-rule: grosor (en px) tipo(solid, doubled, dashed,...) color;
};
```
## Imagenes de fondo
Podemos insertar varias imagenes de fondo en un mismo elemento
```
.nombre{background-image: url('nombre.jpg'), url('nombre.jpg')
        background-repeat: repeat/no-repeat;
        background-position: 100%(x) 100%(y);(posicion eje de coordenadas);
        background-position: 50%(x) 50%(y);(posicion eje de coordenadas);
};
```
El tamaño de la imagen debe ser más pequeño que el del elemento
La primera imagen que pongamos es la que quedará sobre las demás
Utilizamos tantos % como imagenes hayamos puesto
x en 0 es a la izquierda, y en 0 es arriba
Propiedades:
#### background-size
Marca el tamaño de la imagen
Podemos utilizar % o cualquier otra unidad de medida
```
.nombre{background-image: url('nombre.jpg'), url('nombre.jpg')
        background-repeat: repeat/no-repeat;
        background-position: 100%(x) 100%(y);(posicion eje de coordenadas);
        background-position: 50%(x) 50%(y);(posicion eje de coordenadas);
        background-size: 50% 50%;
        cackground-size: 30% 30%;
};
```
background-size: La primera medida hace referencia al ancho, la segunda al alto.
Si queremos dejar la medida original ponemos background-size: auto auto;
## Transiciones de una propiedad (transition: propiedad tiempo)
Nos permite cambiar una propiedad en un elemento de manera gradual y por un tiempo determinado
La aplicamos en un elemento principal, pero solo tiene efecto si existe un elemento secundario(hover)
```
.nombre{witdh: x xp;
        heigth: x xp
        color: red;
        transition: width tiempo(s);   
                    color tiempo;
                    height tiempo;
};
.nombre: hover{width: x + 100px;
               height: x + 100px;
               color: ...;
};
```
El tiempo es en segundos.
Propiedades de las transiciones:
###### ease 
Es la que aparece por defecto
Comienzo lento, acelera y termina lenta
###### linear
Igual velocidad de principio a fin
###### ease-in
Comienxo lento
###### ease-out
Final lento
###### ease-in-out
Comienzo y final lento
```
transition: propiedad tiempo(s) ease / linear / ease-in / ease-out - ease-in-out;
```
###### tiempo de demora
Podemos aplicar un tiempo de demora.
La propiedad se aplica el tiempo de demora que nosotros establezcamos
```
transition: propiedad tiempo(s) de transicion ease / linear / ease-in / ease-out - ease-in-out tiempo(s) de demora;
```
## Animaciones
Nos permite cambiar las propiedades que queramos en un elemento al abrir una pagina
```
.nombre{ position: relative;
         animation-name: nombre de la animación;
         animation-duration: tiempo en segundos;
         color, background-color, width, height,...
}
@keyframes nombre de la animación{
from{color, background-color, width, height,...}
to{color, background-color, width, height,...}
}
```
Las propiedades que queramos aplicar han de ponerse en los tres sitios
#### Propiedades
###### animation-itineration-count: nº de veces o infinitive
sirve para determinar el numero de animaciones que queremos que se repitan
###### animation-direction: normal o alternative
Normal es la que aparece por defecto. La animación se repite una y otra vez desde el principio
alternative es la que una vez realizada, vuelve al principio de nuevo de forma animada
###### animation-timing-function:
Hay varias clases: 
ease - comienza lento, avanza rapido y termina lenta
linear - misma velocidad de princio al final
ease-in - comienzo lento
ease-out - finaliza lento
ease-in-out - comienza y termina rapido
###### animation-delay: tiempo en segundos(s)
tiempo de demora para que se inicie la animación
###### animation-played-state: running or paused
Running es la que aparece por defecto
### Complejidad
Podemos utilizar más keyframes para hacer animaciones más complejas
```
.nombre{ position: relative;
         animation-name: nombre de la animación;
         animation-duration: tiempo en segundos;
         color, background-color, width, height,...
}
@keyframes nombre de la animación{
0%{color, background-color, width, height,...}
25%{color, background-color, width, height,...}
50%{color, background-color, width, height,...}
100%{color, background-color, width, height,...}
}
```