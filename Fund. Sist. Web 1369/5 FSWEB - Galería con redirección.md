---
fecha: 2024-11-25
tags:
  - 4toSemestre
  - 4toSemestre/FSWEB
keywords: 
share_link: https://share.note.sx/ynqjtgjd#o9IiMIP6ctZucwPk3/yJy11wD2np5INYxAEBPbdj2XQ
share_updated: 2024-12-27T22:29:05-05:00
---
# 5 FSWEB - Galería con redirección

El objetivo 1 del día de hoy es crear una página web sobre galería de artistas
Ella nos va a conectar por cada artista hay un enlace y un botón para descargar

![](https://i.imgur.com/oB4l87H.png)
Así se debería ver

## Creación
La etiqueta es ``img`` y tiene atributos en rojo

```html
<html>
<body>
    <h2>HTML Image</h2>
    <img src="pic_trulli.jpg" alt="Trulli" width="100" height="100">
</body>
</html>
```

Se tiene la etiqueta de la imagen, el atributo ``src`` que es la dirección de la imagen, el alto y ancho es `height` y `width` respectivamente

Si esto se lo lleva a otro código se necesita la dirección única de nuestra imagen junto con su nombre y su respectiva extensión

Por ejemplo en este caso es Karol G. Se necesita ver el nombre y la extensión de la imagen

Teniendo esto en cuenta realizamos nuestra página

```html
<!DOCTYPE html>
<html>
<body>
    <h2>HTML Image</h2>
    <img src="karol.jpg" alt="Trulli" width="200" height="200">
    <img src="karolina.jpg" alt="Trulli" width="200" height="200">
    <img src="michelle.jpg" alt="Trulli" width="200" height="200">
</body>
</html>
```

![](https://i.imgur.com/uQ3h90Y.png)

Ahora vamos a crear una etiqueta "a" para redireccionar al link que deseemos
```html
<a href="https://www.karolgmusic.com/">Sitio de Karol</a>
```

![](https://i.imgur.com/oefKpGC.png)

Al hacer clic se va a la página web de Karol G oficial

¿Como podemos hacer para que la IMAGEN redireccione a un enlace?
Entonces hacemos

```html
<a href="https://www.karolgmusic.com/">
    <img src="karol.jpg" alt="Trulli" width="200" height="200">
</a>
```

Hacemos lo mismo para las demás imágenes

```html
<!DOCTYPE html>
<html>
<body>

    <h2>HTML Image</h2>
    <a href="https://www.karolgmusic.com/">
        <img src="karol.jpg" alt="Trulli" width="200" height="200">
    </a>
    <a href="https://www.espe.edu.ec">
        <img src="karolina.jpg" alt="Trulli" width="200" height="200">
    </a>
    <a href="https://www.teleamazonas.com">
        <img src="michelle.jpg" alt="Trulli" width="200" height="200">
    </a>
    
</body>
</html>
```

___

La primera imagen debe estar adentro de un contenedor un `<div>` y le pones un atributo en este caso será `id="row"`
Dentro de este `<div>` colocaremos otro, con el atributo `id="colums"`

![](https://i.imgur.com/MaAbh3n.png)

Hagamos de cuenta que no queremos que se vaya hacia abajo entonces lo ponemos en el primer `<div>` con ID `colum`

![](https://i.imgur.com/AFNDEXO.png)
`
![](https://i.imgur.com/FO12aIl.png)

Primer deber una galería de imágenes con enlaces en cada una de sus imágenes de un tema diferente yo que se algún concesionario de autos y se descarga el catálogo de autos