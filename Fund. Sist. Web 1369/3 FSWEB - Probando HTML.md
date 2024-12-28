---
fecha: 2024-11-11
tags:
  - 4toSemestre
  - 4toSemestre/FSWEB
keywords: 
share_link: https://share.note.sx/whg5550o#1aEwjKNpHcKD8TWcI1O9ZSDLXOSUXbCBESqx0bymOug
share_updated: 2024-12-27T22:28:17-05:00
---
# 3 FSWEB - Probando HTML

# Introducción

Tener instalado los componentes básicos en Visual Studio para poder trabajar los ejercicios con HTML5

Dios santo está instalando un poco de plug-ins en Visual Studio Code de un poco de cosas que no tengo idea que mierda dañar mi perfil de VS Code con todo eso aaaaaa

# Info. de etiquetas

**ESTRUCTURA BÁSICA**
Al ingresar `html` en VS Code se despliega un snippet para generar las etiquetas básicas para la estructura de la página

De forma básica tenemos las cabeceras `head` y el cuerpo `body`.

**HEAD**
Por lo general en las cabeceras aparece el título de la pestaña de la página y otras etiquetas llamadas `<meta>` que son los metadatos o las directivas que el navegador debe saber de la página web

UTF8 es un estándar que sirve básicamente para los caracteres esto nos especifica los caracteres de la página

la etiqueta `<title>` sirve para modificar el título que aparezca en la pestaña de la página web en el navegador pondremos "título pestaña"

Anda creando un archivo  `pagina1.html` en donde empieza a explicar lo siguiente 

`viewport` Significa cuando se está realizando aplicaciones web un principio básico es que ==se puede reproducir una página en una computadora o teléfono o televisor o tablet==. Al poner viewport significa que el ancho y alto va a tomar el 100% del dispositivo así sea móvil o PC se adapta se agranda

**BODY**
Dentro del body ponemos el contenido de nuestra página

Una etiqueta para tamaños que se suelen utilizar son `<h1>` para títulos y si se va elevando el número se va achicando el texto, así para tener "subtítulos"

```html
<body>
    <h1> hola pagina 1 etiqueta h1</h1>
    <h2> hola pagina 1 etiqueta h2</h2>
    <h3> hola pagina 1 etiqueta h3</h3>
    <h4> hola pagina 1 etiqueta h4</h4>
</body>
```

**ATRIBUTOS**
Estas etiquetas tienen atributos un montón, por ejemplo `<style>`, dentro de este se puede poner color por ejemplo:

```
style ="color: red;"
```

Si hasta ahí guardamos y cargamos 

![|350](https://i.imgur.com/Ysoh2PZ.png)

Dijimos que íbamos a seguir el tutorial de "W3School"

==Cada una de las etiquetas pueden tener atributos== por ejemplo la etiqueta ``<img>`` tiene como atributo `<src>`

Ahora vamos a agregar etiquetas para irnos familiarizando.
Porque lo primero que va a poner de imagen es una imagen de Karol G

`<img src="karol.jpg" width=200" height="50">`

![](https://i.imgur.com/ae4Fvv6.png)

También le pusimos atributos de tamaño jasdlkajwd sin estos atributos de tamaño. La imagen se coloca en su tamaño por defecto

No olvides poner la imagen dentro de la misma carpeta en donde está nuestro archivo "HTML"

**RESUMEN Y RECOMENDACIONES**
Una página tiene dos partes fundamentales:
- Head (las directivas y las cabeceras que dan orden en el navegador, bibliotecas y todo lo que es el comportamiento)
- Body (es el cuerpo del programa, la parte que podemos ver)

Creamos una segunda página de nombre `pagina2.html`

Si quisiéramos ver las etiquetas básicas de HTML podemos ver en W3School párrafos estilos etc. Ahora vamos a utilizar la IA como herramienta pedagógica, nojodas va a usar ChatGPT

Escribe: 100 etiquetas básicas de HTML5 con etiqueta, descripción y 1 ejemplo de cada una
y ahí nos está poniendo todas las etiquetas básicas que sería bonito memorizar, pero que miércoles son muchas todas diferentes

**ESTILOS EN HTML**
Generaremos una nueva página para probar estilos, la generamos con nombre "pagina3.html"
y nada nomas anda probando colores y etiquetas de título

Cada vez que hablamos de estilos podemos hablar de 3 uno de ellos es ==in-line==, que significa en la misma línea estos son estilos en línea

![](https://i.imgur.com/9O6PwcK.png)

Así mismo como se tiene al título con estilos se puede dar atributos y estilos al body

```html
<body style="background-color: aquamarine">
```

![](https://i.imgur.com/lGX6j9o.png)

Este tipo de combinación hace referencia a la segunda propiedad, como funciona CSS es un conjunto de instrucciones

```
propiedad : atributo
```

![](https://i.imgur.com/ePEw1XQ.png)

**SINTAXIS**
![|500](https://i.imgur.com/63J0Cn0.png)

En esta ocasión ya no vamos a colocar las líneas de estilo "in-line" ahora las vamos a poner en `<head>` dentro de un bloque de código "`<stiyle>`"

![|450](https://i.imgur.com/GJTr5QK.png)

Ahora al declarar una etiqueta `<p>` no tendrá nada será simple, pero el estilo sigue presente en el encabezado

![|450](https://i.imgur.com/6XlWlT0.png)

 *c fue laluz