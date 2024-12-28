---
fecha: 2024-12-02
tags:
  - 4toSemestre
  - 4toSemestre/FSWEB
keywords: 
share_link: https://share.note.sx/amm0i8ik#8y87eL+B0n4zGlPg02FFJR7ugSjRNPHt4OF5cNDNOEE
share_updated: 2024-12-27T10:08:18-05:00
---
## Resumen


___
# 6 FSWEB - Galeria con DOM
## Document Object Model (DOM)
![](https://i.imgur.com/XBaSEQn.png)
Imagen sobre DOM

El `head` es todo lo que hace referencia a la cabecera
- Directivas
- Directrices
- Título
- Enlaces a metadatos
- Código tipo internal

Todo lo que se va haciendo en la página web se puede graficar con el DOM

En la página web #2 se tienen más cosas: 

- Una etiqueta `a` para direccionar a otra página
- Dentro del `head` tenemos un `title`
- Dentro del `body` tenemos: 
    - Los títulos `h1`, `h2`, etc.
- También tenemos el atributo `href` que nos enlaza a otra página web, se da el link

En la página web #4 tenemos ya la galería de imágenes
Tenemos atributos `style` e `inline` que afectan solo a esa línea por ejemplo al `h1`

```html
<h2 style="background-color:red;" id="tit2" name="tit2">
```

> [!important]
> Algo importante a tener en cuenta es la jerarquía de la página
> 
> Se lee como una cascada, o por capas, de arriba hacia abajo, el estilo que este abajo ganara relevancia

## Estilos en linea
![|450](https://i.imgur.com/QyMefg0.png)

![|450](https://i.imgur.com/erpuubW.png)

## Tablas
Ahora página 5 se hizo lo mismo pero mediante un contenedor, en este caso una tabla mediante etiqueta `table`

`tr` significa filas
`td` significa columnas

![|450](https://i.imgur.com/3XogoRB.png)

## Ejemplos

### pagina10.html
En este ejemplo estaremos haciendo la simple maquetación de una tabla para su posterior relleno

Dentro del documento tenemos:
- Al `html`

Y ese está contiene a dos
- `head`
- `body`

El atributo `alt` sirve para cuando la imagen no se carga tenga un mensaje alternativo explicando que debería haber ahí

```html
<html>
    <head>
    
    </head>
    <body>
        <h1> Galeria de Imagenes </h1>
        <a href="https://www.bmw.com.ec/es/index.html">concesionario
            <img src="bmw.jpg" alt="auto vmw" width="200" height="200">
        </a>
        <a href="https://www.mercedes-benz.com.ec">concesionario
            <img src="mercedes.png" alt="auto vmw" width="200" height="200">
        </a>
        
        <table border="3">
            <tr>
                <td> fila 1 columna 1 </td>
                <td> fila 2 columna 2 </td>
            </tr>
            <tr>
                <td> fila 2 columna 2 </td>
                <td> fila 2 columna 2 </td>
            </tr>
        </table>
        
    </body>
</html>
```

El DOM es un árbol de los elementos HTML

> [!attention] Atención
> Pequeña evaluacion entre semana muchas de esas preguntas esta en el W3School


### pagina11.html
Ya usando la tabla creada anteriormente estamos rellenando con imagenes que redireccionan a sitios web junto con titulos en la tabla

```html
<html>
    <head>
    
    </head>
    <body style="brackground-color:green;">
        <h1> Galeria de Imagenes </h1>
        
        <table border="3" style="background-color:yellow;">
            <tr>
                <td>
                    <a href="https://www.bmw.com.ec/es/index.html">
                        <img src="bmw.jpg" alt="auto vmw" width="200" height="200">
                    </a>
                </td>
                <td>
                    concesionario 1: BMW
                </td>
            </tr>
            <tr>
                <td>
                    <a href="https://www.mercedes-benz.com.ec">
                        <img src="mercedes.png" alt="auto vmw" width="200" height="200">
                    </a>
                </td>
                <td>
                    concesionario 2: MB
                </td>
            </tr>
        </table>
        
    </body>
</html>
```

### pagina12.html
Es lo mismo que la pagina anterior solo que ahora se movio la ubicación de los titulos y los titulos tambien redireccionan a sitios web

```html
<html>
    <head>
    
    </head>
    <body style="brackground-color:green;">
        <h1> Galeria de Imagenes </h1>
        
        <table border="3" style="background-color:yellow;">
            <tr>
                <td>
                    <a href="https://www.bmw.com.ec/es/index.html">
                    <img src="bmw.jpg" alt="auto vmw" width="200" height="200"></a>
                </td>
                <td>
                    <a href="https://www.mercedes-benz.com.ec">
                    <img src="mercedes.png" alt="auto vmw" width="200" height="200"></a>
                </td>
            </tr>
            <tr>
                <td>
                   <a href="https://www.bmw.com.ec/es/index.html">concesionario 1: BMW</a>
                </td>
                <td>
                    <a href="https://www.mercedes-benz.com.ec">concesionario 2: MB</a>
                </td>
            </tr>
        </table>
        
    </body>
</html>
```

#### Archivo DOM
![](https://i.imgur.com/YA9MYDH.png)
