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
	`(*)`: Cero o más veces
	`(?)`: Cero o una sola vez delimitador
	`(+)`: una o más veces.
	`[a-z]?` : Esto es que puede estar una sola vez o no estar una letra minuscula de la (a) a la (z).
	`\d*`: Esto es que puede estar muchas veces o no estar un digito.
	`\d+`: Esto es que puede estar muchas veces o una sola vez un digito.
	csv1,csv2,csv3,csv4,csv5
	`.*,`: trae todo antes de la ,
	`.+?,`: match minimo
1. Los contadores `{1,4}`
	`\d{2,4}[\.\- ]?`: de 2 a 4 digitos que pueden estar seguidos de un . o - o espacio vacio
1. Las clases predefinidas 
	`\w`, todas las palabras con letras y numeros `\W` lo contrario
	`\d`, todos los numeros `D` lo conntrario `\d?\d` 
	`\s` todos los espacios `S` lo contrario
	…
1. Las clases construidas `[a-zA-Z0-9]`
1. Not `^`, su uso y sus peligros (lo contrario al match anticlases)
	`\d\d\D\d\d` 2 digitos separados por algo que no sea un digito seguidos por dos digitos
	`[^0-9]` todo lo que no sea un numero
1. El caso de `()` agrupar y aectar al grupo
	`(p.s)?to` : Hace que resultado contenga ['pasto ', 'pisto ', 'to ']
1. El caso de `?` como delimitador
	`.+?,`: match minimo
	`(\d{2}\W?){3}` dos digitos separados por algo que no sea una letra (teléfonos)
1. Principio (`^`) y final de línea  (`$`)
	`^(\w+,){2,10}\w+$` inicia con una palabra que puede tener letra o numero entre 2 y 10 caracteres y termina con otra palabra
1. Expresiones comunes:
  1. mails
		`@[\w\.\-]{3,}\.\w{2,5}`: @mail.com 
		`[\w\._]{5,30}\+?[\w]{0,10}@[\w\.\-]{3,}\.\w{2,5}`: esto.es_un.mail+complejo@mail.com
	1. URLS
		`https?:\/\/[\w\-\.]+\.\w{2,5}\/?\S*$` https://www.instagram.com/p/\\\BXB4zsUlW5Z/?taken-by=beco.mx
  1. teléfonos
		`^\+?(\d{2,3}[.-\s]?){2,2}\d+[#pe]?\d*$`: +845-938-938 039-038-938#123
  1. logs
		`^\[LOG.*\[LOG\].*user:@\w+?\]\s.*$`: [LOG DATA] [LOG] [user:@celismx] Did something
  1. nombres
		`^([A-ZÁÉÍÓÚÑ][a-záéíóúñ]+\s?){3,4}$`: Miguel Ignacio Rodríguez Álvarez
  1. locaciones 
		`^-?(\d{1,3}\.\d{6,6},\s?){2,2}\d{4,4}\.?\d{2,2}$`: -99.205581, 19.429652,2275.10
		`^-?\d{1,3}\s\d{1,2}'\s\d{2,2}.\d{2,2}"[WE],\s?-?\d{1,3}\s\d{1,2}'\s\d{2,2}.\d{2,2}"[NS]$`: -34 54' 32.00"E, -3 21' 67.00"S
    1. [what three words](https://what3words.com/)
1. Búsqueda y reemplazo
	`^\d+::(.+)\((\d+)\)::.+$` : 1::Toy Story (1995)::Adventure|Animation|Children|Comedy|Fantasy `$1. $2` :  Toy Story . 1995
1. Procesadores de texto
1. `grep` y `find` desde consola
1. Regex en
  1. PHP
  1. Javascript
  1. Python
  1. Perl (aunque se burlen)
