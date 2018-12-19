Regex
=====

## Presentación

Las Expresiones Regulares son una herramienta de búsqueda y manipulación de cadenas de caracteres increíblemente potente presente en **todos** los lenguajes de programación. Este curso busca llevar al alumno a entenderlas y darles un uso correcto dentro de sus diferentes aplicaciones.

Algunos puntos de este temario asumen un uso intermedio de la CLI, por lo que se recomienda el curso de "Línea de Comandos".

## Temario

1. Qué es y para qué sirven las expresiones regulares, por ejemplo `/^([a-z\.\+]{4,30})@([a-z\.]+)\.([\w]{2,5})$/`
1. Notas sobre el curso
1. El caracter `.` e introducción a los caracteres especiales y su escapado
1. Los delimitadores numéricos: 
	(*) : Cero o más veces
	(?): Cero o una sola vez
	(+): una o más veces.
	[a-z]? : Esto es que puede estar una sola vez o no estar una letra minuscula de la (a) a la (z).
	\d*: Esto es que puede estar muchas veces o no estar un digito.
	\d+: Esto es que puede estar muchas veces o una sola vez un digito.
	csv1,csv2,csv3,csv4,csv5
	.*,: trae todo antes de la ,
	.+?,: match minimo
1. Los contadores `{1,4}`
	\d{2,4}[\.\- ]?: de 2 a 4 digitos que pueden estar seguidos de un . o - o espacio vacio
1. Las clases predefinidas `\w`, `\d`, `\s` …
1. Las clases construidas `[a-zA-Z0-9]`
1. Not `^`, su uso y sus peligros
1. El caso de `?` como delimitador
1. Principio (`$`) y final de línea (`^`)
1. Expresiones comunes:
  1. mails
  1. teléfonos
  1. logs
  1. nombres
  1. locaciones
    1. [what three words](https://what3words.com/)
1. Búsqueda y reemplazo
1. Procesadores de texto
1. `grep` y `find` desde consola
1. Regex en
  1. PHP
  1. Javascript
  1. Python
  1. Perl (aunque se burlen)
