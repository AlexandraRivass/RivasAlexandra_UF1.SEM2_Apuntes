## Apuntes de Markown, Github y HTML- Alexandra Rivas
>## Markdown
## Introducción a Markdown

En esta lección se ofrece una introducción a Markdown, un lenguaje de marcado con sintaxis en texto plano para generar textos con formato. Descubrirás el porqué se utiliza, cómo dar formato a los archivos de Markdown y cómo obtener una vista previa en la web de los documentos formados con Markdown.

Dado que las lecciones de The Programming Historian en español deben ser enviadas como archivos Markdown, hemos incluido ejemplos específicos de PH en la medida de lo posible. Espero que esta guía sea útil si estás considerando contribuir con una lección en este sitio.

## ¿Qué es Markdown?

Markdown es un formato de texto creado en 2004 por **John Gruber**.  
Tiene dos significados principales:
1. Una forma sencilla de **escribir texto con formato** (negritas, listas, títulos, etc.) usando solo caracteres de texto plano.  
2. Una herramienta en **Perl** que convierte archivos Markdown en **HTML**.

En esta lección se estudia la primera acepción: aprender a escribir con la **sintaxis de Markdown**.

Los archivos Markdown son **texto plano**, lo que los hace:
* Compatibles con casi cualquier dispositivo o sistema.
* Más duraderos y fáciles de abrir con el paso del tiempo.
* Legibles directamente, sin necesidad de programas especiales.

Además, muchas plataformas (como **GitHub** o los generadores de sitios estáticos) pueden convertir Markdown a **HTML** automáticamente.  
También existen herramientas como **Pandoc**, que permiten **convertir Markdown a otros formatos** de documento.

--------
## Encabezados

Los encabezados se usan para crear títulos y subtítulos.  
Se definen con el símbolo `#`. Cuantos más `#` uses, más pequeño será el título.
Ejemplo:
```md
# Título 1
## Título 2
### Título 3 
#### Título 4
```
__Se visualiza así:__
# Título 1  
## Título 2  
### Título 3  
#### Título 4

--------------
## Sintaxis general: 

Sirven para aplicar formato visual al texto.  
Se usan asteriscos o guiones bajos para cursiva y negrita.

__Se visualiza así:__
```md
Esto está en __negrita__
Esto está en **negrita** también 

Esto está en _cursiva_
Esto está en *cursiva*

Y ambos es __*TEXTO*__
```
Esto está en __negrita__
Esto está en **negrita** también 

Esto está en _cursiva_
Esto está en *cursiva*

Y ambos es __*TEXTO*__

-------
## Listas

#### Listas ordenadas

Para agregar listas ordenadas en Markdown debes agregar un número seguido de un punto, un espacio y el elemento de la lista. La lista no debe estar ordenada numéricamente, pero debe comenzar por el número

```md
1. Primer elemento
2. Segundo elemento
3. Tercer elemento
```
__Se visualiza así:__

1. Primer elemento
2. Segundo elemento
3. Tercer elemento

#### Listas desordenadas
Para agregar listas no ordenadas en Markdown debes agregar un guion -, un signo más + o un asterisco * delante de los elementos de la lista:

```md
1. Elemento 1
    * Elemento desordenado 1.1
    - Elemento desordenado 1.2
2. Elemento 2
    + Elemento desordenado 2.1
    * Elemento desordenado 2.2
```
__Se visualiza así:__

1. Elemento 1
    * Elemento desordenado 1.1
    - Elemento desordenado 1.2
2. Elemento 2
    + Elemento desordenado 2.1
    * Elemento desordenado 2.2
------
### Links o enlaces
Añadir enlaces a una publicación, más que común, hoy en día es algo casi obligatorio. Con Markdown tendrás varias formas de hacerlo.
#### Enlaces internos
Son los enlaces de toda la vida. Como su nombre indica, se encuentran en línea con el texto.

Se crean escribiendo la palabra o texto enlazada entre [] corchetes, y el link en cuestión entre () paréntesis.
```md
[enlace en línea](https://www.google.com)
```

__Se visualiza así:__
[enlace en línea](https://www.google.com)

------
### Imágenes
Se pueden referir las imágenes mediante el uso de !, seguido de un texto alternativo entre corchetes, seguido a su vez por el URL de la imagen y un título opcional entre comillas. Esto no se representará como texto en tu documento pero te permitirá incluir la imagen en la visualización de una página en HTML.

```md
  ![alt text](./imagenes/img_markdown/img_ejemplo.jpg "Imagen de loro de ejemplo")   

```
__Se visualiza así:__


![alt text](./imagenes/img_markdown/img_ejemplo.jpg "Imagen de loro de ejemplo")   


------
### Tablas
Para crear una tabla en GitHub, usa barras verticales | para separar columnas y guiones entre los encabezados y el resto del contenido de la tabla. 
Dado que las barras verticales son sólo estrictamente necesarias entre columnas, puedes usarlas en los extremos de la tabla para darle una vista más acabada. 
Las celdas pueden tener contenido de cualquier extensión, y no es necesario que las barras verticales estén alineadas verticalmente entre sí.

 ```md
| Encabezado 1 | Encabezado 2 | Encabezado 3 |
| --------- | --------- | --------- |
| renglón 1, columna 1 | renglón 1, columna 2 | renglón 1, columna 3|
| renglón 2, columna 1 | renglón 2, columna 2 | renglón 2, columna 3|
| renglón 3, columna 1 | renglón 3, columna 2 | renglón 3, columna 3|
```
__Se visualiza así:__

| Encabezado 1 | Encabezado 2 | Encabezado 3 |
| --------- | --------- | --------- |
| renglón 1, columna 1 | renglón 1, columna 2 | renglón 1, columna 3|
| renglón 2, columna 1 | renglón 2, columna 2 | renglón 2, columna 3|
| renglón 3, columna 1 | renglón 3, columna 2 | renglón 3, columna 3|

Para especificar la alineación del contenido de cada columna se pueden agregar dos puntos :al renglón de los encabezados como sigue:
 ```md
| Alineado-izquierda | Centrado | Alineado-derecha |
| :-------- | :-------: | --------: |
| Manzanas | rojo | 5000 |
| Plátanos | amarillo | 75 |
```
__Se visualiza así:__
| Alineado-izquierda | Centrado | Alineado-derecha |
| :-------- | :-------: | --------: |
| Manzanas | rojo | 5 |
| Plátanos | amarillo | 25 |
------

### Fragmentos de código (snippets)
Representar fragmentos de código en forma distinta al resto del documento es una buena práctica que lo hace más legible. La escritura de código se representa generalmente a espacio sencillo. Dado que Markdown no distingue las tipografías involucradas, representamos los fragmentos de código encerrados entre dos signos de acento grave `. Por ejemplo: `<br/>`. Cuando queremos representar un bloque completo de código lo debemos encerrar entre dos líneas de tres acentos graves. En la ventana de vista previa de StackEdit esto se representará como una caja de texto sombreada y escrita a espacio seguido.

Ejemplo HTML
```html
<html>
    <head>
        <title>Título del sitio Web</title>
    </head>
    <body>
    </body>
</html>
```
Ejemplo de código JavaScript
```js
console.log("Hello world!")
```

------







