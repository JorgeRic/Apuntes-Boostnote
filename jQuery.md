# jQuery
Sirve para interactura mejor con los elementos DOM
Es una librería, por lo que debemos ingresar este codigo en nuestra hoja HTML
Conviene ingresarlo dentro del body y al final
Ojo!!! El enlace entre la pagina Javascript y la de HTML siempre ha de ponerse a continuacion o dara error
```
<script src='https://code.jquery.com/jquery-3.1.0.min.js'></script>
<script src='main.js'></script>
</body>
```
Creamos una funcion
```
function main(){
}
Utilizando esta propiedad nuestro codigo Javascript no aparece hasta que se ejecute el DOM
$(document).ready(main);
Es una llamada de retorno
```
jQuery sustituye los elementos de selectores de CSS
```
Document.getElementByID('nombredelid'); por $('#nombre del id')
Document.getElementByClassName('#nombredelaclase'); por $('.nombredelaclase')
```
Para que esto tenga sentido, debemos llamar a los selectores de CSS en Javasript dentro de la function main
## Propiedades
Utilizar dentro de la function main
#### click
Podemos hacer que una function se jecute al hacer click
Ojo!!! La propiedad que queremos que se ejecute ha de estar dentro de la funcion click (que a su vez esta dentro de la function main)
```
$('.nombredelaclase').on('click' function() {
$(.nombredelaclase').show();
$('.nombredelaclase').toggle();
$('nombredelaclase').toggleClass('nombrecreadoenCSS');// No pueden ir juntos
$('nombredelaclase').slideToggle(tiempo en milisegundos);//No es compatible con toggle
$('nombredelaclase').text('texto deseado que queremos que aparezca al clickar el boton');
})
$('#nombredelid').on('click' function() {
$(.nombredelid').show();
$('.nombredelid).show(); 
$('nombredelid').toggleClass('nombrecreadoenCSS');// No pueden ir juntos
$('nombredelid').slideToggle(tiempo en milisegundos);//No es compatible con toggle
$('nombredelaid').text('texto deseado que queremos que aparezca al clickar el boton');
})
```
#### hide
Oculta el elemento
```
$('.nombredelaclase').hide();
$('.nombredelid).hide();
```
#### fadeIn
Hace que los elementos se desvanezcan en un tiempo determinado
Esta ligada a la propiedad hide
Por defecto es 400
```
$('.nombredelaclase').fadeIn(tiempo en milisegundos);
$('.nombredelid).fadeIn(tiempo en milisegundos);
```
#### show
Hace visible el elemento
Generalmente interactua con la propiedad click(va dentro de su funcion)
```
$('.nombredelaclase').show();
$('.nombredelid).show();
```
#### toggle
Dentro de la funcion 'click', funciona como un interruptor.
Visualiza o culta un elemento segun clickemos el boton
```
$('.nombredelaclase').toggle();
$('.nombredelid).toggle();
```
#### toggleClass
Actua dentro de la funcion click como la propiedad toggle, pero sirve para modificar el boton al pulsarlo
Debemos crear una clase especifica en CSS para que se apliquen las modificaciones deseadas (tamaño, color,....)
No es compatible con las propiedades toggle ni hide
```
$('.nombredelaclase').toggleClass('nombre de la clase que queremos utilizar en CSS');
$('.nombredelid).toggleClass('nombre de la clase que queremos utilizar en CSS');
```
#### slideToggle
Sirve para animar la entrada y salida de un elemento cuando haces 'click' sobre eĺ
Hace que el elemento desaparezca al pinchar o aparezca de nuevo
Puede combinarse con el hide(fuera de la funcion click, para que el elemento no aparezca al abrir la pagina y se muestre al pulsarla)
No es compatibel con toggle
```
$('.nombredelaclase').slideToggle(tiempo en milisegundos);
$('.nombredelid).slideToggle(tiempo en milisegundos);
```
## this
Dentro de una funcion con un nombre determinado nos permite sustituir ese nombre por this(sin las comillas)
```
$('.ejemplodenombre').on('click' function() {
$(this).toggle();
$(this).show();
....
})
```
## text
Nos permite poner un texto cuando alguien haga 'click'
Se pone dentro de la funcion click
```
$('.ejemplodenombre').on('click' function(){
$('.nombre' o this).text('texto que queremos que aparezca')
});
```












