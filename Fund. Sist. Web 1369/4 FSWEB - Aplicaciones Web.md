---
fecha: 2024-11-18
tags:
  - 4toSemestre
  - 4toSemestre/FSWEB
keywords: 
share_link: https://share.note.sx/kwm9uhcj#Jtu64JRE32WxDFCvysIO2etS67g6kMx2GzMXnlBtsDA
share_updated: 2024-12-27T22:28:44-05:00
---
# 4 FSWEB - Aplicaciones Web

![](https://i.imgur.com/eqgclTX.png)

HTML puede ser la estructura de la casa está basado en etiquetas, en cambio,
CSS es el diseño y está basado en formato
JavaScript está basado en la funcionalidad operaciones lógicas o matemáticas, maneja de archivos base de datos la parte que da interactividad a las anteriores 

## HTML
![](https://i.imgur.com/sOecSPm.png)

Un lenguaje de etiquetas basado en estas marcas de lenguaje, reside en dos partes head y body. Observemos que etiqueta que se abre se debe cerrar `<head> </head>` 

Tenemos `<h1>` que son los encabezados `<P>` que son los párrafos y estamos viendo nomas cosas generales

- Describe la estructura de una pagina web
- Consta de serie de elementos
- Los elementos HTML le dicen al navegador como mostrar el contenido
- Los elementos HTML etiqueta fragmentos de contenido como "este es un encabezado" "este es un párrafo" 

## CSS
![](https://i.imgur.com/JpPI6ki.png)

Es un lenguaje basado en formato para diseño, tenemos una instrucción que referencia a un componente de HTML y de ahí partimos con un diseño

Todas las etiquetas h1 serán de tal color y tales características

Dentro de HTML y CSS decimos que pueden ser inline, internal o external

- CSS significa hojas de Estilo en cascada
- Describe como se deben mostrar los elementos HTML en la pantalla en papel o en otros medios
- CSS salva un montón de tiempo, ya que puede controlar el lay out de la página
- Puede tener efecto o aplicabilidad en 
    - Inline: es la misma línea de código
    - Internal: en bloque interno de código
    - External: en 1 archivo externo


### CSS Inline
![](https://i.imgur.com/lmhb4S5.png)

h1 son etiquetas para especificar encabezados y son diferencias en tamaños siendo h1 la más grande

### CSS Internal
![](https://i.imgur.com/ymgCUvM.png)

## JS Lenguajes de scripting (JavaScript)
![](https://i.imgur.com/n1FlTgB.png)

Puede ser JavaScript o cualquier otro lenguaje de scripting. Es uno de los lenguajes más usados para lado del cliente por ejemplo un lenguaje cliente es lo que vamos a ver

También comparte paradigma POO y Javascript tiene más de 800 APIS y todos están basados en Programacion Orientada a Objetos y con un concepto moderno de programación sincrónica y asincrónica con paradigma web,

Los bloques de código también pueden ser inline, internal y external

Cuando veamos JavaScript veremos el concepto del DOM todo un árbol de contenidos de HTML

___
## Ejemplo practico
Cada programa que hagamos en clase deberemos nombrarlo con referencia interesante para que nos pueda ayudar el W3School y parecida TutorialPoint en HTML 

Creemos un archivo llamado pagina1.html vamos a hacer una página que tenga un título un párrafo y una imagen


dentro del head ponemos entre algunas cosas el título de la pestaña y cabeceras con información para el navegador

`<text-align: center;>`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Titulo Ventana</title>
</head>
<body>
    <h1>Titulo Grande</h1>
    <h2>Titulo mediano</h2>
    <h6>Titulo pequeño</h6>
    <p><font size="42" color="red">Este es un parrafo que contiene información</font></p>
    <p id="parrafo1" style="color: cyan; background-color: yellow;">Este es un parrafo 1 que contiene información</p>
    <p id="parrafo1" style="color: red; background-color: green;">Este es un parrafo 2 que contiene información</p>
    <p id="parrafo3" style="color: blue; font-size:50;">Este es un parrafo 3 que contiene información</p>
</body>
</html>
```

```html
<!DOCTYPE html>
<html>
<head>
    <title>artistas</title>
</head>
<body>
    <h2>Galeria de Artistas</h2>
    <img src="brunis.jpg" alt="Bruno Mars" width="200" height="200">
    <img src="karol.jpg" alt="Bruno Mars" width="200" height="200">
</body>
</html>
```

Miércoles 1 pm reunión para el proyecto en la Espe se puede conectar también virtualmente si alguien le interesa se puede apoyar