---
fecha: 2024-11-14
tags:
  - 4toSemestre
  - 4toSemestre/SISBD
keywords: 
---
# 3 SISBD - Conceptos de Base de Datos

¿la idea de estas clases iniciales es que nosotros podamos hablar un mismo idioma? Supongo está hablando sobrevenir leyendo los temas con anterioridad

# Conceptos básicos
Como técnicos se deben manejar conceptos claros

- El valor de los datos, es el conocimiento que se puede extraer
- El valor de los datos es la información que contiene
- La estructura para su almacenamiento

El valor de los datos es uno de los activos más importantes de las organizaciones. Porque es la información es lo más valioso que tenemos.

En las org podemos perder edificios, cosas tangibles y las recuperamos de pronto de alguna manera. PERO si se pierde la información o no se resguarda de forma adecuada eso sí va doler.
Es la materia prima para la toma de decisiones operativas y estratégicas, es lo que guía los procesos de todos tipos. Por tanto, es el componente estratégico de las organizaciones

En resumida las decisiones deben ser con base en lo más componente de todo, los datos

La informacion sisé trata, se cuida y se analiza esta se convierte en un ente estratégico. El ente que debe hacer todo este proceso es el informático. Somos aquellas personas que estamos trabajando con datos

En este aspecto vamos a iniciar a conocer como debemos tratar los datos y hacia donde se enfocan. 

## Datos
Distintos tipos de organizaciones lo necesitan. Todas las organizaciones necesitan los distintos tipos de información
Compañía de seguros, bancos, financieras, fabricas, proveedores, distribuidores. Sus actividades están guiados por los datos

Antes había un paradigma un **tabo** que invertir en la parte estrategica es un gasto. Ahora es visto como un ente estratégico para mejorar en competitividad y efectividad

♥ ESTRATEGIA DE SIU? es el que conversa con los entes superiores y tiene el valor de decir si ustedes invierten aqui tienen estos beneficios, seremos aquellas personas que orienten al resto de gerentes para que los productos sean mejorados

___

¿DATOS O INFORMACION?
Que es un dato
- Es una representacion simbolica, el dato como tal no tiene significado
- Ejemplo: 2011 es un año?, uncodigo de materia? es una extesion para telefono? un dato como tal no tiene significado

Para que este dato tenga significado debe pasar por un procesoy al hacerlo se vuelve información

Informacion
- Son datos procesados e interpretables. Una informacion dice algo
- Tienen significado (semantica)
- Eejemplo: El codigo de la asignatura de BD es 1713

PROCESO DE LOS DATOS PARA INFO
Paso por un proceso donde se unieron caracteristicas similares por cierta interpretacion de un ALGO que tiene como objetivo comun, TODO tiene un objetivo comun, que es representar una asignatura, la representacion de esa asignatura tiene esos datos y se volvio ESA informacion

___
# VISION DE LOS DATOS

Abstraccion de datos
Para que el sistema sea util debe recuperar los datos eficientemente

Nivel fisico
El nivel mas bajo de abstraccion describe como se almancena realmente los datos, Nivel fisico describe detalle estructuras de datos complejas de bajo nivel, repositorios, discos etc

nivel logico
Describe que datos se almacenan en la BD y que relaciones existen entre ellos
se hablan de otra cosa como mas tratada, este curso SE ORIENTA POR AQUI, en el nivel logico estaremos

Nivel de vista
Nivel mas alto de abstraccion que describe solo parte de la BD de datos mas completa un tratamiento mas alto para la toma de decisiones, porque solo parte? porque se escoge de toda la informacion se escoga cual nos sirve y cual visualizamos para la toma de decisioens
Se habla del cuadro de mando integral o el score, o los visualizadores y se manejan de busnisess intel y se usan para la mejroa de toma de decisiones

 ![](https://i.imgur.com/UgOB87b.png)

**ESTO SALDRAN EN LA PRUEBA**

# QUE ES UNA BD
Que concepto nos dicen los autores

Algunos podrian pensar que son solo datos almacenados en una PC como una planilla de datos

Una base de datos es un **conjunto de datos estructurados** y definidos a traves de un proceso de un proceso especifico (clasificacion, organizacion y archivado), **que busca evitar la redundancia**, y que almacenara en aglun medio de almacenamiento masico como un disco

El concepto mas importante tambien es la evitar la redundancia, apoyados en ciertas normas o estrategias de diseño de BD tratamos de evitar esta redundancia.

Hablamos de BD relacionales hacia donde nos orientamos
Si hablamos de BD NO relacionales este tipo de estructuras les interesa la redundancia, 

Porque debemos en BD relaciones? es porque debemos tener implementacioens en rempresas para manejar datos relacionales
Por ejemplo, piensalo, en un banco si se diseña con redundancia la informacion, que podria estar sucediendo si no se controla? se tendra duplicacion de depositos, transacciones etc caos
Estas BD tratan de solucionar eso pero ciertamente TIENEN UN LIMITE

Tiene un crecimiento vertical de INFO son cosas muy estructuradas en cambio las NO SQL tienen un BD horizontal y no son tan rigidas, esto se ira viendo de apoco

___
# Para que sirve una BD

## Ejemplo de H2

Este ingeniero pregunta sobre conceptos para ver que tan definido tenemos los conceptos, despues los comparamos con los relaes

ALmacena gran numero de informacion de forma organizada para su futura consulta, realizacionde busquedas, nuevo ingreso de datos, etc

Todo esto lo permite realizar de una forma rapida y simple desde un ordenador

El otro concepto de gestion de la informacion en una BD ese ES UN GESTOR DE BD, ese es otra vaina

![](https://i.imgur.com/5Q6k7K1.png)

La inconsistencias de datos pasa por no tener el tratamiento adecuado de datos

La concurrencia puede ser el caso de un banco, por ejemplo se tiene en una tabla las cuentas corrientes, imaginese los clientes todos a la vez los clientes estan leyendo y tal vez grabando nueva informacion entonces como se controla esta concurrencia? ahi viene la importancia de BD, tiene procesos internos que permiten manejar sin problema concurrencia

Porque usar BD
- Org. de la informacion
    - Definicion central de datos
    - abstraccion de datos
    - Mutiples vistas de los datos
    - Almacenamiento de datos y progamas
- PROG. de la BD
    - Separacion entre programas y datos
    - Control de retrcciones de integridad
    - Estandarizacion de omdelos y lenguajes
- Explotacion de la BD
    - Datos compartidos (info en varios sitios)
    - Control de concurrencia
    - Seguridad y recuperacion ante fallas (tlodavia se trabaja en esto aunque estamos retrasados, si llevamos todo el negocio a la nube si tenemos AWS ellos se encargan de esto)
    - Datos persistentens en modelos avanzados

ya no existen los data sets que son los q adminstran la informacion y que solo ocupaban espacio y dinero eso se ta quedando fuera, todos los ERP estan ahora en la nube 

El inge tiene bien vista el proceso en la nube

# Sistema Gestor de BD
- Los SGBD Se lo puede penasr como uan capa de software que controla todos los accesos a la BD
- todas las apps que usa interactuan con un conjunto de programas aglutinados en lq uese denomina el SGBD
- El DBMS puede implementar instrucciones dadas por los distintos usuarios
- Las instrucciones se agrupan minimamente en : DLL (lenguajes de definciion de datos) y DML (lenguaje de manipulacion de datos) aunque tambien suele concerse al DCL (lenguaje control de datos)


- Seguridad
- Alta disponibilidad
- COncurrencia
- Lenguaje de programacion
SIno no se habla de un gestor

gestores de BD
MySQL, Progress, Oracle

Si se tiene almacenado un monton de datos y se quiere que se recomiende la mejor solucion de un gestor de bd
Regularmente se recomienda lo que mas conocen, lo primero que hay que responder es estar intelignete de donde se encuentra, el perfil de la empres,a su proyeccion a futuro, se estudia la planificacion estrg. de la empresa 

En este momento se puede manejar con MYSQL pero segun delante por el crecimiento se puede comprar oracle

Esto es una parte importante que se debe tener en cuenta, inteligensiarse con el perfil de la empresa

Apoyarnos de las herramientas que nos permitan tomar decisiones. " EL CUADRANTE DE GARTNER 2024 gestores de BD"

Son estudios que se realizan a las empresas dependiendo de lo que buscan 

para que una empresa en oracle o mysql se encuentre como lider debe haber pasado ciertos procesos
- mejores ventas
- soporte
- presencia en empresas
- confiabilidad
- etc etc

Se posicionan como lideres en este cuadrante, de ahi viene la respuesta, a donde se enfoca la compra, hacia los lideres?

![](https://i.imgur.com/IpmLQo7.png)

Tal ves se puede hacer una busqueda para aquellos GBD para aquellos que son libres 

> [!consejo]
> Estos son hechos con estudios mediante el tiempo esti nos ayuda muchisimo en auditorias, cuando nos cuestionen nuestras decisiones nos podemos sustentar de estos estudios y estar actualizados

___
# TALLER
coño otro trabajo
El taller esta subido en la plataforma
