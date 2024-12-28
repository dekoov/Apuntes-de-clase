---
fecha: 2024-12-05
tags:
  - 4toSemestre
  - 4toSemestre/SISBD
keywords: 
---
## Resumen


___
# 6 SISBD - 

Continuación de la clase anterior

## Tipos de Atributos
![](https://i.imgur.com/6GRR3fp.png)

Son aquellos que nos ayudan a calificar la entidad

Estos pueden existir varios: entre ellos el compuesto

Cuando por ejemplo se identifica en el requerimiento de tener que abrir esa info. para mayor detalle en almacenamiento,

Por ejemplo abrir la dirección en componentes basados en la norma ISO

Ese atributo compuesto es la concatenacion de valores componentes

Otro tambien son los atributos derivados
Cuando se almacena o identifica los atributos de una entidad, muchas veces puede estar cayendo en algo mal practico

La edad de una persona, se puede poner como tipo de dato fecha,

![](https://i.imgur.com/3qmEJxn.png)

Si se le pone tipo entero se quema esa información, si se le pone tipo fecha va cambiando con el sistema y eso no nos dara ningun inconveniente 

Otra mala practica es la factura, la entidad factura tiene el precio unitario del producto, el total del producto aqui y el valor total de compra, este v alor total de compra es un atributo derivado, porque se puede calcular de otra forma, esto es un error o redundancia

![](https://i.imgur.com/3Ljjqf0.png)

Monovalorados valor para cada entidad

;Multivalorados, mas de un valor para la misma entidad, por ejemplo poner la nacionalidad de una pelicula, puede que existan varios paises que estan diversos en esa nacionalidad

Como se puede controlar este tipo de limites por el momento se mencioan que existen pero es mucho mas sencillo manejarlos con el case

## Atributos opcionales

![](https://i.imgur.com/f16qt7v.png)

Aparecen en el diseño en el momento que se le pone a un atributo null, no es buena practica debido que la informacion que esta recolectado debe ser completa, se requiere para alguna situacino posterior

Caso de empleado, atributo altura no ha sido tomada, y como no se ha tomado la de todos los empleados, se puede dejar altura como un valor opcional

Pero si la intencion posterior esta info. usarla con el sistema medico de la institucion altura puede ser importante, SE DEBE TRATAR DE COLOCAR LA INFO LO MAS PRONTO PARA QUE LA MISMA BD SEA COMPLETA

## Atributos clave

![](https://i.imgur.com/LSEo5DP.png)

Nos ayuda a identificar una instancia sea distinta de otra en la entidad

Pongamos que el atributo clave de un empleado unico es su cedula porque esta no se va a repetir para dos empleados diferentes, sea un atributo que nos ayude a identificar de modo unica

Si este es subrayado se da a entender que esta es una llave primaria
EN otras notaciones no se le subraya sino el ovalo esta completamente pintado

### Caracteristicas

![](https://i.imgur.com/j6VILXW.png)

Puede estar formado po varios atributos, esta se las llamara claves compuestas

CUando se esta obligado a formar una llave compuesta?
Cuando una persona esta trayendo datos de otro sistema de personas, la llave primaria es la cedula, sin embargo encontro llaves celular repetida, se puede perder informacion entonces se buscan dos atributos que se pueda llegar a una llave compuesta y que puede ser el atributo clave

Un tipo de entidad puede ser mas de una clave candidata, clave candidata es diferente de clave principal

Estas son las que podrian llegar a ser en algun momento una clave primaria


## Tipos de entidades
Debiles
![](https://i.imgur.com/jt7kILO.png)

Una entidad debil es alguien que depende de otra

Un empleado - polizas

Porque se le llamaria a poliza una entidad debil? que pasa con la poliza si en algun momento el empleado desaparece. ESTA DESAPARECE, por tanto es DEBIL

para que un conjunto de entidades debiles sea signifitica debe ser parte de un conjunto de relaciones UNO A MUCHOS

Volviendo un empleado como tiene varios polizas, por tanto se cumple la relacion uno a varios, una ploliza pertenece a 1 y solo 1 empelado

![](https://i.imgur.com/71a7A10.png)


Diagrama de la izquierda una ciudad es parte de un estado, por tanto se lo diagrama con DOBLE LINEA por tanto es entidad debil


## ENTEIDADE DEBILES

![](https://i.imgur.com/9myHzGe.png)

Mira que la entidad fuerte tiene la llave primaria numero de cuenta y transaccion no esa es la clave para entender esto

las entidades debiles no pueden ser idenitificas de manera unicap or si solas necesitan de una entidad fuerte para completar su identificacion para compeltar su identificacion esto se logra mediante una clave compuesta

Va a hereder la llave PRIMARIA DE LA ENTIDAD FUERTE

![](https://i.imgur.com/bR4pXrv.png)

## EJEMPLO

![](https://i.imgur.com/dLDxOyY.png)

## IDENITIFICAR ENTIDADES DEBILES

![](https://i.imgur.com/pzQRNBR.png)


## SUPER CLAVE
![](https://i.imgur.com/AuQO45q.png)

Imagina que tienes la tabla empleados con los atributos,

CUales serian superclaves, podrian ser la combinacion de ID y de nombre o apellidos

## DIFERENCIAS ENTRE SUPERCLAVE Y CLAVE CANDAIDATA

![](https://i.imgur.com/sktLesy.png)

Superclave, va mucho mas alla por cierto que suceda algun probleman en el futuro, esta puede tener id nombre apellido y puede que no se este poniendo nombre 

La candidata es una superclave minima no contiene ningun atributo innecesario

## Libro de donde salio el material

![](https://i.imgur.com/k4egwt2.png)

## Inicio del Taller

Categoria, informacion, conceptual data

Poner nombre al modelo: conceptual medico

Se procede a mostrar la interfaz junto a la derecha los iconos de diseño, se asersiora que la parte superior tenemos los sub menu, file, edit, etc

en el pestaña MODEL > Modelo ER MERISE en model options

Cuando se diagrama, este sera el plano del diseño, entonces vamos a poner un nombre a nuestro plano,

al dar doble lcic en la entidad en la pestaña de atributo 

Mandatorio es cuando este atributo cuando se ingrese un nuevo empleado, necesariamente se deba ingresar la cedula

Pero tambien se puede decir llave primaria, entonces TODA llave primaria debe ser mandatorio

El que dice DESPLIEGUE es porque se desea que se muestre en el diagrama

El tipo de character se recomienda para valores pequeños como 1 digito, variable character lllega hasta 64 bits y long character hasta 128 para almacenar cadenas mas grandes

Todo nuevo empleado que se ingrese tendra que ser mandatorio con su nobmre cedula y


Pensemos que se quiere almacenar la info. de el momento que se dan de alta los empleados en cierto departamento

Se requiere por lo tanto las fechas en que ingreso el empleado

Vamos a tomar la cardinalidad y como el empleado puede tambien ir cambiando de darptamentos
![](https://i.imgur.com/x5e0g2F.png)

Pero esto en el tiempo, entonces se creo una relacion varios a varios, esto hay que romperlo

Se quita la relacion varios a varios

![](https://i.imgur.com/OMiU1B1.png)

Buscamos la herramienta association link,

Le damos atributos
Fecha de ingreso
Fecha de salida

Este atributo es correspondiente tanto a dep y emple. porque es corresponidnete porque el mo,ento que un empleado lo hace atraves de una fecha de un departamento 

Aparece cuando existe una transaccionalidad enrre entidades cuando son relaciones varios a varios

Identificamos los atributos que son parte de ambas

Contralmos la fecha donde se da de alta un empleado, entonces como sep uede mucho tiene muchas fechas de ingreso y de salida, se hace mediante un control de atributos varios avarios, el icono del asociacion link

Este case va pokito mas alla de lresto nos ayuda a leer y mejorar la interpretacion de varios a varios con la finalidad va un paso mas atras aqui existe una transaccionalidad, en otros case se puede dejar con la relacion varios a varios y el lo rompe en el modelo logico pero depue los nos tocara poner los atributos 

Check model o F4, quitamos paquetes damos OK y no problemas

Vamos a continuar las siguientes fases, 

Tools, model options, esta en NOtacion E/R Merise, un click en check  en domain atrribute check en check rules y mandatory

Esto sucede cuando posiblemente puso o borro alguna cosa y borro un historico?????

Doble click en atributo 8