# Notas SASS #

### Importar archivos: ###

`@import "nombre_archivo.scss"`


### Variables: ###

`$color-font: #555;`


### Anidaciones: ###

~~~
.btn{
	display: inline-block;
	color: #fff;
	background-color: #333;
	border-radius: 5px;

	.btn__icon{
		font-size: 24px;
	}

	.btn--info{
		background-color: skyblue;
	}
}
~~~


### Mixins ###

Los mixins permiten definir estilos reutilizables en toda la hoja de estilos.
Se definen con la directiva **@mixin** seguida del nombre del mixin

Los mixins se incluyen en las hojas de estilos mediante la directiva **@include** seguida del nombre del mixin y opcionalmente por una lista de argumentos.

**Ejemplo:**
~~~
@mixin max-width($max-width: 800px) {
	max-width: $max-width;
	margin-left: auto;
	margin-right: auto;
}

.container{
	@include max-width(1200px);
}

section{
	@include max-width(800px);
	background-color: #333;
	padding: 15px;
}
~~~


### Content ###

Nos permite incluir un bloque de contenido dentro de un mixin.

**Entrada:**

~~~
@mixin respond-to($width){
  @media only screen and (min-width: $width){
    @content;
  }
}

section{
  background-color: skyblue;
  @include respond-to(800px){
    background-color: teal;
  }
}
~~~

**Salida:**

~~~
section {
  background-color: skyblue;
}

@media only screen and (min-width: 800px) {
  section {
    background-color: teal;
  }
}
~~~



<br><br>
## Estructura de proyectos ##

**style.scss**

~~~
// Librerias, settings y variables
@import'lib/_variables.sass'

// Elementos base
@import'_tablas.sass'
@import'base/_botones.sass'
@import'base/_tipografia.sass'

// Components
@import'components/_grids.sass'

// Esto va de último
@import'components/_utilities.sass'
~~~


**_variables.scss**

~~~
// Branding colors

$color-brand: #ea83ee
$color-secondary: rgb(219, 216, 121)

$color-black: rgb(0,0,0)
$color-darkblack: #4d4d4d
$color-grey: #bfbfbf
$color-white: rgb(255,255,255)

// Texturas
$color-alert: rgb(252,228,207)
$color-error: rgb(218,79,73)
$color-info: rgb(66,104,221)
$color-success: rgb(91,183,91)


// Tipografía
$basefont: 'Quicksand', sans-serif
$basefontsize: 16px

$buttoncolor: $color-white
$buttonbackgroundcolor: $color-brand
~~~


<br><br><br>
### Enlaces de interes ###

[BEM](http://getbem.com/introduction/) <br>
[SASS Meister](https://www.sassmeister.com/) <br>