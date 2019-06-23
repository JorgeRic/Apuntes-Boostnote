# HTML
```
<DOCTYPE html>
<html>
<head>
<title></title>
<meta charset="UTF 8">
</head>
<body>

</body>
</html>
```

## Elementos semanticos:
nav - Creamos un cuadro en la pagina que sirve para enlazar con otra pagina u otras partes dentro de la propia pagina
___
header - marca la cabecera de una pagina
Suele contener al nav
___
section - sirve para dividir la pagina en secciones. Cualquier cosa que incluya su propio encabezado
___
footer - indica el pie de la propia pagina o de una sección dentro de la porpia pagina
___
aside - representa una nota, un consejo o una explicación
___
article - representa una entrada independiente en un blog, revista, periodico, ... O partes independientes que cuentan con su propio titulo dentro de section

## Salto de linea
Para generar un salto de linea entre textos usamos:
```
<br>
```
## Creación de linea entre parrafos
```
<hr>
```
## Tipos de textos:
```
<h1></h1> Titulo principal
<h2></h2>
....
<h7></h7> Titulo menor
<p></p> Parrafo
<strong></strong> Mayor enfasis en la palabra o frase
<em></em> Texto en curiva que enfatiza su contenido
<mark></mark>El texto queda marcado como si pasases un rotulador sobre el
<small></small> Textos laterales con letra pequeña
<blockquote></blockquote>Es usado para insertar bloques de textoque citan a otro autor
<i></i> Texto en cursiva que sirve para designar textos en tono diferente o que contienen una definición
<b></b> Texto en negrita
<span></span> Con esta etiqueta englobamos textos que modificamos mediante CSS
```
## Hipervinculo:

Para ir a una pagina que se encuentra dentro del mismo archivo
```
<a href="nombre de la pagina que se encuentra dentro del mismo archivo.html">Texto</a>
```
Para ir a otra pagina web
```
<a href="http://www.pagina web a la que queremos ir.com">texto</a>
```
Para enviar mails
```
<a href="mailto: dirección mail.com">texto</a>
```
Podemos crear anclas en una pagina que al pulsarlas nos enviaran al lugar deseado de esa misma pagina(introduccion, una seccion determinada, un comentario,...)
```
<a href="#nombredelancla">texto</a>
Es necesario crear el ancla antes del punto al que queremos ir para que nos dirija al punto deseado
El punto al que queremos ir sería:
<h2 id ="#punto3">texto</h2>
```
Tambien podemos llamar a otro punto determiando que se encuentre dentro de otra pagina que este en nuestro archivo de una forma muy similar
```
<a href="pagina a la que queremos ir.html#nombredelancla">texto</a>
debemos de crear un <a name="nombredelancla"></a> antes del punto al que queremos ir en la pagina de nuestro archivo elegida
```
## Imagenes
Es una etiqueta de cierre automatico. Sin cierre 
Podemos insertar imagenes de cuatro formas:

Si la imagen esta dentro de la misma carpeta que nuestra pagina:
```
<img src="nombredelaimgen.jpg/png/gif" alt="definifición de la imagen">
```
Si la imagen esta en otra carpeta dentro de nuestro archivo:
```
<img src="nombredelacarpeta/nombredelaimagen" alt="definicion de la imagen">
```
Si la imagen esta en otro archivo:
```
<img src="../nombredelacarpeta/nombredelaimgen" alt="definicion de la imagen">
```
Si capturamos la imagen de otra pagina
```
<img src="http:// .....png/gif/jpg" alt="definicion de la imagen">
```
## Audio
Podemos reproducir archivos de audio a traves de:
```
<audio constrols autoplay loop autobuffer>
<source src="archivodesonido.ogg/.mp3/.wav/.au"
</audio>
```
Propiedades:
constrols - muestra la interface visual al visitante
autoplay - en caso de ponerse, reproduce el archivo automaticamente sin que exista intervención del visitante
loop - en caso de ponerse, el archivo se ejecuta una y otra vez
autobuffer - en caso de ponerse, el archivo no se ejecuta hasta que se haya cargado en el ordenador del visitante
## Video
Podemos reproducir archivos de video a traves de:
```
<video width="" height="" controls autoplay>
<sourse src="http://www.archivodeaudio.mp4/ogv"
</video>
```
Propiedades:
controls - muestra la interface visual al visitante
autoplay - en caso de ponerse, descarga reproduce el archivo de video automaticamente sin que exista intervención del visitante
## Hacer listas
Hay tres clases de listas:
Listas desordenadas:
```
<ul>
  <li></li>
  <li></li>
  ....
</ul>
```
Listas ordenadas:
```
<ol>
  <li></li>
  <li></li>
  ...
</ol>
Junto a cada uno de los items aparecerá de forma automatica un numero para que se tenga en cuenta el orden
```
Listas descriptivas:
```
<dl>
  <dt>Titulo a definir</dt>
  <dd>Explicación del titulo</dd>
  <dt>Titulo a definir</dt>
  <dd>Explicacion del titulo</dd>
</dl>
```
## Hacer tablas
Para crear tablas debemos utilizar las siguientes etiquetas:
```
<table>
<caption>Lo utilizamos solo si queremos incluir un titulo a la tabla</caption>
  <tr>Crea una fila
    <td>texto</td><td>texto</td><td>texto</td>...
    Si sustituimos el primer <td></td> por <th></th> creamos un encabezado
  </tr>
  <tr>Crea una fila
    <td>texto>/td><td>texto</td><td>texto</td>....
  </tr>
</table>
```
Podemos crear un encabezado en cada fila cambiando td por th
Para crear celdas que ocupen dos o mas espacios utilizamos la propiedad:
```
<td rowspan="numero de celdas que queremos ocupar a lo alto">
<td colspan="numero de celdas que queremos ocupar a lo ancho">
```


# Inputs
Cuando queremos que el visitante ingrese datos y estos se registren en el backend debemos crear las etiquetas input type dentro de la etiqueta form
### Label tag
Representa un titulo para todos los tipos de entrada
```
<form action="/some-url" mathod="post">
<label for="name">Name:</label>
<input type="text" id="name">
```
## Form tags
La etiqueta form es un elemento que representa un formulario
La tarea del form es tomar la informacion y enviarla a un servidor (backend)
#### Atributos del form
###### Action
Action apunta al servidor URL al que se enviará la información del formulario
```
<form action="nombre de la pagina que procesa los datos ingresados por el visitante en el servidor(ASP, PHP, JSP)"
  <input type="...">
</form>
```
### Tipos de inputs
###### text
```
<input type="text" name="" maxlength="valor numerico size="valor numerico">
```
Utilizando el atributo maxlength="valor numerico" determinamos un numero de caracteres maximos a ingresar
Utilizando el atributo size, determinamos el tamaño del cuadro visual
___
###### password
```
<input type="password" name=""maxlength="valor numerico size="valor numerico" >
```
Utilizando el atributo maxlength="valor numerico" determinamos un numero de caracteres maximos a ingresar
Utilizando el atributo size, determinamos el tamaño del cuadro visual
___
###### radio
```
<input type="radio" name="" value="Texto que aparece en el cuadro">
```
Ojo! Todos tienen que tener el mismo name
Nos permite elegir varias opciones, pero solo podremos marcar una
Añadiendo el atributo checked a uno de los input type aparecerá como valor predeterminado
___
###### checkbox
```
<label><input type="checkbox" name="Texto que aparece visualizado"></label>
```
Nos permite elegir dos o más opciones
Si añadimos el atributo checked a uno o más input type de los que hemos creado, esos ya aparecerán marcados por defecto
Si metemos el input dentro de una etiqueta label, al visitante le bastará con pinchar en cualquier parte del texto para que este aparezca como marcado
Si no ponemos esta etiqueta, tendrá que pulsar exclusivamente el cuadro que nos ofrece la pantalla para que se marque
___
###### mail
```
<input type="mail" name=""size="valor numerico" >
```
Sirve para enviar mails
Utilizando el atributo size, determinamos el tamaño del cuadro visual
___
###### url
```
<input type="url" name="" size="valor numerico">
```
Exclusivo para incluir direcciones web
Utilizando el atributo size, determinamos el tamaño del cuadro visual
___
###### date
```
<input type="date" "datetime-local "month" "week" "time" id="" name="">
```
Con este input el navegador abre automaticamente un cuadro en el que podemos elegir fecha, fecha-hora, mes, semana o día de la semana
___
###### color
```
<input type="color" name="" value="">
```
Con este input el navegador abre automaticamnete un cuadro en el que podremos elegir un color.
Si queremos que aparezca un color por defecto debemos de poner el atributo value y el color deseado.
___
###### number
```
<input type="number" name="" min="" max="">
```
Con este input el navegador abre un cuadro automaticamente en el que podremos elegir un numero.
al poner los atributos min y max podremos delimitar los numeros que queremos que aparezcan
___
###### textarea
```
<textarea rows="nº de filas" cols="nº de columnas">texto que se verá dentro del cuadro</textarea>
```
___
###### file
```
<input type="file" name="">
```
Nos permite enviar enviar archivos al servidor
Para que funcione ha de incluirse la etiqueta enctype dentro del form
___
###### select
```
<select name="" size="valor numerico">
  <optgroup label="nombre de la etiqueta">
    <option value="valor numerico" selected>Texto</option>
    <option value="valor numerico">Texto</option>
   ...
</select>
```
El atributo size en el select muestra al visitante a la pagina el mismo numero de options que nossotros hayamos puesto en el size. Es basicamente un atributo estetico.
Si añadimos el atributo selected a una de las options será que aparezca en primer lugar por defecto
Cuando existen muchas options y queremos clasificarlas, creamos la etiqueta optgroup label para dividir lasoptions en secciones
El visitante no puede pinchar esa opcion
Si queremos que el visitante pueda elegir más de una option debemos añadir el atributo multiple al select e incluir [] en el name
```
<select name="nombre determinado[]" size="valor numerico" multiple>
  <optgroup label="nombre de la etiqueta">
    <option value="valor numerico">Texto</option>
    <option value="valor numerico">Texto</option>
  </optgroup>
   ...
</select>
```
Para que el visitante pueda elegir varias options ha de mantener pulsado el boton "control"
___
###### submit
```
<input type="submit" value="texto que aparece dentro del cuadro">
```
Envia los datos al servidor que procesa la información
___
###### reset
```
<input type="reset" value="texto que aparece dentro del cuadro">
```
___
###### button
```
<input type="button" name="" value="texto que aparece dentro del cuadro">
```
Podemos insertar imagenes en los cuadros submit, reset y button sustituyendo los input type por button type
quedaría así
```
<button type="reset, button, submit" img src="archivodeimganen.jpg,gif,png">texto</button>
```
___
##### Agrupación de inputs
Cuando tenemos varios inputs (nombre + apellidos + DNI + comentarios + ...) y queremos agruparlos dentro de un cuadro debemos utilizar la etiqueta fielset
Podemos poner un titulo al cuadro añadiendo un legend
```
<fielset>
  <legend>Titulo</legend>
    <input type="" name="">
    <input type="" name="">
  </legend>
</fielset>
```
 
#### Propiedades de los inputs
Exiten propiedades que se pueden aplicar en el propio input type:
###### autofocus
El punto de pie de pagina irá directamente a este input
  ```
  <input type="text" name="nombre" autofocus>
  ```
###### placeholder
Es un texto que se visualiza dentro del cuadro a rellenar por el visitante de la pagina como una marca de agua
  ```
  <input type="text" name="nombre" placeholder="texto que queremos que se visualice">
  ```
###### required
Aplicamos este atributo a un input cuando exugimos que el visitante rellene este cuadro
Si no lo rellena, pero pulsa verificar, aparece un cuadro que le pide que lo rellene
  ```
<input type="text" name="nombre" required>
  ```
###### readonly
Mediante este atributo hacemos que los input type del tipo text, textarea y password sean exclusivamente para la lectura
No se pueden modificar
###### size
Valor numerico que qetermina el tamaño de los cuadros que se mostraran al visitante
Solo se puede utilizar con los input type text, password, mail y url
###### maxlength
Valor numerico que determina el numero maximo de caracteres que se pueden incluir
Solo sirve para los input type text y password
###### disabled
Añadiendo este atributo al input type, inhabilitamos el control pero no lo eliminamos
###### required pattern
Al aplicar este atributo exigimos un numero detrminado de caracteres(letras o numeros)
En caso de pedir un DNI sería:
  ```
  <input type="text" name="nombre" required pattern[0-9]{8}[a-z A-Z]{1}>
  ```
## Caracteres especiales:

Hay ciertos caracteres especiales que no podemos usar en htma por que el navegador los confundiria con las marcas usadas en html. Los más usados son:
```
< & lt; (todo junto)
> & gt; (todo junto);
& & amp; (todo junto);
€ € euro(todo junto);
```




