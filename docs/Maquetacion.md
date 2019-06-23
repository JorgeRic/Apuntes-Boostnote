# MAQUETACION
## Position
La propiedad position marca donde ha de verse cada elemento en el screen
Por defecto se inicia con la propiedad position static, pero hay más tipos
### Position relative
Con esta propiedad podemos modificar la posición inicial de cada elemento con los valores left, right, bottom y top (valores negativos y postivos en px)
```
#nombre{ position: relative;
         left: px;
         top: px;
         right: px;
         bottom: px;
        }
```
### Position absolute
Pone al elemento deseado fuera del flufo de la pagina
Una vez declarada esta propiedad, la posición y el tamaño quedan determinados a priori en relación al elemento que lo contiene
Utiliza los valores left, right, bottom y top (valores negativos y positivos)
El tamaño del elemento se determina por height y width
```
#nombre{ position: absolute;
         left: px;
         top: px;
         right: px;
         bottom: ;
        }
```
Cuando dos o más elementos se superponen en la pantalla, podemos utilizar la propiedad z-index con un valor numerico ordenado en cada uno de ellos para determinar cual se verá sobre el otro.
El valor más alto seráel que aparecerá por encima del resto
### Position fixed
El elemento al que se le de esta propiedad aparecerá siempre en el mismo sitio en la pantalla (aunque se haga scroll)
```
#nombre{ position: fixed;     
        }
```
Podemos ajustar eltamoño del elemento con los valores right, left, top y bottom
Si imprimimos la pantalla y tiene varias hojas, el lemento con esta propiedad aparecerá en todas y siempre en el sitio en el que lo hayamos puesto
## Posicionamiento flotante (float)
Saca del flujo a un elemento y nos permite que el texto envuelva al elemento afectado
Junto con la propiedad float, siempre se ha de aplicar la propiedad witdh para determinar el ancho del elemento
Hay tres tipos: float: left, float: right y none
Si queremos dividir la pagina en dos columnas utilizamos la propiedad float de esta forma:
```
#columna izq { float: left;
              width: px;              
              }
#columna izq { margin-left: px;          
              }
```
Si queremos ver la pagina dividida en dos columnas pero con cabecera y pie de pagina haremos
```
#contenedor{ width: 100%;
             margin: 0 auto;
            }
#cabecera{ clear: left;
         }
#cuadro1{ float: left;
          width: px;
         }
#cuadro2{ margin-left: px;
         }
#pie{ clear: left;
    }
```
Si queremos ver la pantalla dividida en tres columnas deberemos:
```
#contenedor{ width: 100%;
             margin: 0 auto;
            }
#cabecera{ clear: left;
         }
#cuadro1{ float: left;
          width: px;
         }
#cuadro2{ margin-left: px;
         }
#cuadro3{ float: rigth;
         }    
#pie{ clear: left;
    }
```
Para que esto se vea correctamente en la pantalla deberemos crearlos en HTML como:
```
<div id="cuadro1"></div> 
<div id="cuadro3"></div> 
<div id="cuadro2"></div> 
```
## Desbordamiento (overflow)
en caso de que un elemento no quepa en el cuadro creado podemos arreglarlo a traves de la propiedad overflow
Esta propiedad tiene cuatro valores:
###### visible
Es la opcion automatica. el contenido que no cabe se sale del cuadro
###### hidden
Lo que no cabe en el elemento queda oculto
###### auto
Muestra una barra scroll en el elemento solo cuando el contenido es mayor al cuadro
###### scroll
Muestra una barra scroll en el elemento aunque no sea necesario
