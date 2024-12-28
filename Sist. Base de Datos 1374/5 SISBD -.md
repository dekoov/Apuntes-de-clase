---
fecha: 2024-11-28
tags:
  - 4toSemestre
  - 4toSemestre/SISBD
---

````col
```col-md
## Keywords


```
```col-md
## Resumen


```
````

# 5 SISBD - 

## Recapitulación

Las tangibles las que podemos palpar las que son objetos del mundo real

Intangibles que aparecen dentro de cierta característica y aparece de una transacción forman parte del problema que vamos a resolver

Dentro de estas entidades tenemos los atributos. Estos nos permiten identificar de forma única una entidad, estas tienen que ser propias de ella

No pueden existir atributos de otras entidades atributos de otras entidades

# Modelamiento de Base de Datos

En esta clase nos centraremos en continuar con los otros componentes mas perfeccionando en el modelo conceptual

Nos apoyaremos posteriormente de un Caso para el diseño, hasta entonces vamos a hacerlo de forma manual, que sera **EN ESTA Y OTRA CLASE MAS**

Usaremos Power Designer

## Tipos de Relaciones Uno a Uno
- Es una asociación en que una instancia de una entidad se puede asociar, cuando mucho con una instancia de la otra entidad y viceversa (la relación también es obligatoria en ambas direcciones)

- aparece cuando un registro de la tabla A solo puede relacionarse con 1 registro de la tabla 

La instancia se le reconoce como una especie de registro, entidad formada por todos los atributos

Se toma una instancia de un extremo con el otro y ellas deben ser una sola?

![](https://i.imgur.com/5l1NFou.png)

1 paciente tiene 1 historia clinica

Tener presente la forma de diagramar la linea, para relacionar que se relaciona solo con uno se atraviesa con una linea vertical al extremo

Le corresponde una y solo una historia clínica

A esta historia clínica le pertenece a uno y solo un paciente

![](https://i.imgur.com/lmc2Lps.png)

**CARDINALIDAD**

Esta se obtiene visualizando la forma de relación de los extremos 1:1

**EJEMPLO**
Se habrá una relación entre entidad PAÍS y entidad BANDERA

![](https://i.imgur.com/P31Q3Ik.png)

En este caso es DEBE, de forma obligada, a un país LE PERTENECE de forma obligada una bandera y a la bandera LE CORRESPONDE un país
## Relaciones Uno a Uno (OPCIONAL)

Suponga el diseño de una BD para un distribuidor de automóviles. Este **PUEDE** entregar autos a algunos empleados, vendedores, para que los conduzca por cierto tiempo

En este caso la palabra PUEDE es clave

El empleado PUEDE (Es abierto es un círculo) la línea representa el máximo de 1 y el mínimo 0

![](https://i.imgur.com/5Wa6Prc.png)

Esto por el momento no lo visualizamos, pero cuando trabajamos con modelos de IA, Machine Learning, Modelos Relacionales Avanzados.

Este tipo de diagramación es valiosísima 

Por ejemplo en el ejemplo de la bandera se puede dejar un registro de una bandera en blanco y eso nos puede ocasionar errores en el registro

Si es que un experto no usa correctamente este lenguaje, se debe captar esto y asesorar para que el software sea eficiente

## Relaciones Uno a Varios

Se presenta en una asociacion entre dos entidades en que cualqueir instancia de la primera entidad se asocia con una o mas instancias de la segunda, y cualqueir instancia de la segunda entidad se asocia con cuando mucho una instancia de la primera

![](https://i.imgur.com/n0UF91J.png)

Una persona que tiene UNO o VARIOS automoviles

Se le conoce tambien como la pata de gallo

![](https://i.imgur.com/ZE2WiBE.png)

La cardinalidad es 1:N

Otras formas de diagramar

![](https://i.imgur.com/p6nQcK0.png)


## Relaciones Varios a Varios

![](https://i.imgur.com/tk36zlk.png)

Entre persona y materias

Un estudiante cursa UNA o VARIAS materias

Y del otro extremo, Esta materia es CURSADA por UNA o VARIAS personas

![](https://i.imgur.com/xQaxFpd.png)

Este tipo se recomienda hacer un analisis para TRATAR en lo posible de romper, si es que no se logra romper en el diseño conceptual

En el diseño logico va lograr omper esto, va a crear una tabla intermedia entre persona y materia y ABSORBERÁ la llave primaria de la entidad de la izquierda, y la llave primaria de la entidad de la derecha

En el diseño conceptual cuando se topa este tipo de relaciones aparecen atributos compartidos tanto a personas como a materias

LA FECHA DE MATRÍCULA es ello lo que este atributo le corresponde a AMBAS ENTIDADES en este caso

![](https://i.imgur.com/UIZVluB.png)

Este rombo que esta diagramado es una relacion con UN ATRIBUTO COMPARTIDO entre dos entidades, esta rompe la relacion varios a varios

Se puede tener uno o los que sean de atributos relacionales

la tabla intermedia absorve como atributos la cédula de persona, el codigo de la materia y la fecha mencionada

De est amanera rompe las relaciones varios a varios

![](https://i.imgur.com/7vn92fM.png)
Una matricula es cursada por una o varias personas, y una matricula es cursada por una o varias materias

## Relaciones Recursivas
Son asociaciones entre instancias de entidades del mismo tipo: Uno a Uno, uno a Varios , Variso a varios

![](https://i.imgur.com/UBIIg4I.png)

Cuando en una empleada se tiene empleados muchos, se dice que de los empleados hay ciertos que supervisan a otros.

NO CREAREMOS una entidad aparte que diga supervisor, sino crearemos una entidad aparte recursiva en donde se especifique esto

1 Empleado es supervisado por 1 nada mas q 1 supervisor
1 Supervisor puede supervisar 1 o Varios Empleados

# Taller

**ENTIDADES NO TANGIBLES**
Servicio
Diagnostico


**HOSPITAL**
Codigo_Hospital (Clave Primaria)
Nombre
Dirección
Telefono

**SALA**
Codigo_Sala (Clave Primaria)
Codigo_Hospital (Clave Foranea)
Capacidad

**MEDICO**
ID_Médico (clave primaria)
Nombre
Especialidad
Código_Hospital (clave foránea)

**LABORATORIO**
ID_Laboratorio (clave primaria)
Nombre
Dirección
Teléfono

**PACIENTE**
ID_Paciente (clave primaria)
Nombre
Fecha_Nacimiento
Género
Código_Sala (clave foránea)

*DIAGNOSTICO* PACIENTE A DIAGNOSTICO
ID_Diagnóstico (clave primaria)
Descripción
Fecha_Diagnóstico
ID_Paciente (clave foránea)

*SERVICIO* (Intermedio entre **LABORATORIO - HOSPITAL**)
ID_Servicio (clave primaria)
Descripción
Fecha_Servicio
Código_Hospital (clave foránea)
ID_Laboratorio (clave foránea)

*ATENCION* (Intermedio entre **PACIENTE - MEDICO**)
ID_Atención (clave primaria)
Fecha_Atención
ID_Paciente (clave foránea)
ID_Médico (clave foránea)