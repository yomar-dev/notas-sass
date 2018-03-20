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
