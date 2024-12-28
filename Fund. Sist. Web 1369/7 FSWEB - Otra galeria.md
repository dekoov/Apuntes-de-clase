---
fecha: 2024-12-09
tags:
  - 4toSemestre
  - 4toSemestre/FSWEB
keywords: 
share_link: https://share.note.sx/nb87o0l9#N8zcbScLIFpSMXtcXOQD8zQCslZqCxT88WC/6PlkfLo
share_updated: 2024-12-27T22:29:29-05:00
---
## Resumen


___
# 7 FSWEB - Otra galeria 

Próxima semana evaluación de Fundamentos de Sistemas Web
## Objetivo
El objetivo es la interacción entre los 3 componentes
- HTML
- CSS
- JAVASCRIPT

## Ejemplos
Todo lo que hacemos se convertira en un arbol de contenidos que llamamos DOM (Documento Object Model)

```html
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <!--CSS Internal-->
    <style>
        body{
            background-color: cyan;
        }
    </style>
</head>
<body>
    <p style="color: red; background-color: burlywood;">AUTOS</p>
    <img src="../img/auto1.jpg" width="200" height="300"> <br>
    <p>AUTOS 1</p>
    <p>AUTOS 2</p>
    <p style="color: green; background-color: rgb(82, 94, 68);">Autos</p>
</body>
</html>
```

![](https://i.imgur.com/atv8WOC.png)

Basicamente CSS es lo mas importante el concepto de interacción

- External CSS
    - Desde un archivo "estilo.css" externo al documento html
- Internal CSS
    - Embebido dentro de la cabezera como una etiqueta `<style>` en html
- Inline CSS
    - Embebido dentro de cada etiqueta como atributo `style=" "` html

```html
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <!--CSS Internal-->
    <style>
        body{
            background-color: cyan;
        }
    </style>
</head>
<body style="background-color: yellow;"> <!Superposición!>
    <p style="color: red; background-color: burlywood;">AUTOS</p>
    <img src="../img/auto1.jpg" width="200" height="300"> <br>
    <p>AUTOS 1</p>
    <p>AUTOS 2</p>
    <p style="color: green; background-color: rgb(82, 94, 68);">Autos</p>
</body>
</html>
```

![](https://i.imgur.com/wqXnwWk.png)

## Ejemplo CSS External

Creamos un archivo `estilos1.css` donde escribimos el codigo CSS de nuestra página web

- Son páginas que tiene código de estilos
- Afectan a todos los elementos html
- CSS Cascada Style Sheets
- Describe el comportamiento de los elementos html desplegados en pantalla
- Los estilos se graban y se pueden usar diferentes capas

```css
body {
    background-color: lightblue;
} 

h1 {
    color: white;
    text-align: center;
}

p {
    font-family: verdana;
    font-size: 20px;
    text-align: right;
}
```

Comando para agregar una hoja de estilos external:
```html
<link rel="stylesheet" href="../css/estilos.css>
```


```html
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="../cs/estilos1.css">
    <!--CSS Internal-->
    <style>
        body{
            background-color: cyan;
        }
    </style>
</head>
<body style="background-color: yellow;"> <!Superposición!>
    <p style="color: red; background-color: burlywood;">AUTOS</p>
    <img src="../img/auto1.jpg" width="200" height="300"> <br>
    <p>AUTOS 1</p>
    <p>AUTOS 2</p>
    <p style="color: green; background-color: rgb(82, 94, 68);">Autos</p>
</body>
</html>
```

Para la tarea de la pagina web esta bien enviar el archivo .zip de todo el directorio

El Ing. se puso a editar el codigo de CSS Layout de una ventana de HTML

![](https://i.imgur.com/lES4mF6.png)
