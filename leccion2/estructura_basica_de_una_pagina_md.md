# Estructura básica de una página

Primero me gustaría hacer una pequeña aclaración sobre terminología que voy a usar, diferenciaremos:
- **Página web**: a una página individual dentro de un sitio web (p.e: [rauljimenez.info/contacto]( view-source:http://rauljimenez.info/contacto))
- **Sitio web (o web)**: como el conjunto de todas las páginas en las que podemos navegar dentro de un mismo dominio (p.e: [rauljimenez.info](http://rauljimenez.info) es un sitio web que incluye: [rauljimenez.info/experiencia](http://rauljimenez.info/experiencia/), [rauljimenez.info/contacto](http://rauljimenez.info/contacto), etc).

Dicho esto, toda *página web* que hagamos en HTML5 debe tener una estructura inicial similar a la siguiente:

```html
<!DOCTYPE html>
<html lang="es">
<head>
	<meta charset="UTF-8">
	<title>Título de la página</title>
</head>
<body></body>
</html>
```

A continuación explicamos la función que cumple cada etiqueta:

* ```<!DOCTYPE html>```: indicar al navegador que el código HTML en el que está escrita la página es en la versión 5, osea que es HTML5. [+info](http://www.w3.org/TR/2011/WD-html5-20110525/syntax.html#the-doctype)
* ```<html lang="es">... </html>```: indica la raíz del documento y **todas** las etiquetas deben estar incluidas dentro. Además se especifica el idioma en el que está escrita, *es* = Español ([+idiomas](http://www.iana.org/assignments/language-subtag-registry/language-subtag-registry)).
* ```<head> ... </head>```: se usa para envolver otras etiquetas que ofrecen información principalmente a: el navegador, a los buscadores y a otras páginas (como pueden ser redes sociales, etc). La información especificada dentro del *head* no se muestra *dentro*<sup>1</sup> de la página web que ve el usuario.
* ```<meta charset="UTF-8">```: indica al navegador qué tipo de caracteres contiene la página. Para especificar cuál de [todos los disponibles](http://www.iana.org/assignments/character-sets/character-sets.xhtml) usamos el atributo charset con el valor [UTF-8](http://tools.ietf.org/html/rfc3629) podremos crear contenido en la mayoría de los sistemas de escritura: español, inglés, francés, etc.
* ```<title> ... </title>```: indica el título de nuetra página. Este se muestra en: la pestaña del navegador, el enlace que indexan los buscadores, etc.
* ```<body> ... </body>```: contiene todo el contenido visible por el usuario *dentro* de nuestra página.
 
Observa que la etiqueta *html* contiene dos hijas: *head* y *body*, esto **obligatoriamente es así en todas las páginas**.

<small>Aclaraciones:</small><br>
<small>1. Cuando digo **dentro** me refiero al contenido de la página, lo que no incluye la pestaña del navegador ni la barra de direcciones.</small><br>