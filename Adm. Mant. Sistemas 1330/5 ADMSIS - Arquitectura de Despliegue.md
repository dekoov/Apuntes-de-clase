---
fecha: 2024-11-28
tags:
  - 4toSemestre
  - 4toSemestre/ADMSIS
keywords: 
share_link: https://share.note.sx/wziymxry#FY/mezon8us0NTE+gRkZwc8iBvusqB/2dXvio2rns1E
share_updated: 2024-12-27T00:45:42-05:00
---
## Resumen:

___
# 5 ADMSIS - Arquitectura de Despliegue

De arquitecturas en forma general se nos viene a la cabeza un diseño que nos permite modelar o representar algo que se desea construir.

Dentro de las infraestructuras hay varios elementos, y tanto para el hardware y software se realizan diagramas para saber como realizar la implementación

Para la implementación de cableado estructurado en un edificio, el Ingeniero encargado debe presentar documentación y ahí se presentan los diagramas de red, como está estructurado internamente ese cableado.

Si se desea presentar o vender un desarrollo de software también se presenta la arquitectura como están conectados los nodos

Siempre para cualquier proyecto que hagamos ya sea hardware o software necesitamos dibujar diseñar la arquitectura

Cuando se quiere implementar un base de datos todo se parte desde el diseño, primero de diagrama un concepto de la base de datos un dibujo, y después se siguen los diferentes modelos hasta llegar al físico para la implementación

## Arquitecturas de despliegue

Estos muestran las relaciones físicas de los distintos nodos que componen un sistema y el reparto de los componentes sobre dichos nodos. La vista de despliegue representa la disposición de las instancias de componentes de ejecución en instancias de nodos conectados por enlaces de comunicación.

Dentro de la teoría estamos haciendo una convergencia de todo lo que hemos visto antes, hardware, software, medios de comunicación.

Un nodo es un recurso de ejecución tal como un computador, un dispositivo o memoria. Los estereotipos permiten precisar la naturaleza del equipo:
- Dispositivos
- Procesadores
- Memoria


![](https://i.imgur.com/Vrm1wFw.png)


**OTRA DEFINICIÓN**

![](https://i.imgur.com/5YjWUgE.png)

Los nodos pueden ser dispositivos físicos, pero también los podemos ver desde la perspectiva de software y están unidos por medios de comunicación

![](https://i.imgur.com/6jsarn9.png)

Ejemplo de diagrama de despliegue

Corresponda a una arquitectura de un Cajero ATM

Aquí está la representación de los nodos
- El nodo cajero (procesador, RAM)
- Sus componentes
    - Lector de tarjetas
    - Impresora de recibo
    - Dispositivo de registro
    - Dispensador de dinero
    - Pantalla
    - Teclado
    - Interfaz de Red (Conexión de red T-1)
- Se comunica con otra interfaz de red
- Servidor de red de cajeros (reemplazable)

Siempre que se presenten proyectos sobre todo en el trabajo integrado, normalmente se hacen ya sea implementaciones de algún tipo de infraestructura o propuestas de implementaciones o planes o algún desarrollo. Casi siempre **van a tener que dibujar arquitectura** dibujar la conexión de los elementos que están proponiendo

### Arquitectura de Network Node Manager i (NNMi)

Potente herramienta de gestión de redes que permite monitorear el estado de la red en tiempo real desde una única localización identificando rápidamente los problemas y creando un preciso mapa de los dispositivos de red

![](https://i.imgur.com/ZZCe7wx.png)

Esta es una herramienta de monitoreo de red, en conceptos generales

El hecho de instalarla como tal es muy complicado por los recursos necesarios

El software empresarial es muy costoso por su calidad

Dependiendo de lo que queramos representar en estas arquitecturas están representados por nodos. Lo que veremos aquí vamos a analizar una arquitectura particular que es la de que presenta esta herramienta de software NNMi.

![](https://i.imgur.com/mOjkh0M.png)

Captura antigua de la interfaz de la herramienta

- Parte izquierda tenemos funcionalidades para poder gestionar y monitorear la red
    - Características
- Podemos ver características de los nodos
- Monitoreo del CPU

Qué tipos de arquitectura podemos implementar usando esta herramienta

![](https://i.imgur.com/lUZPbVG.png)

Mapeo de la red usando la herramienta junto con la identificando de problemas analizando también los protocolos

#### Características
- Implementación automática para fallos de la red, disponibilidad de gestión (identifica los nodos conectados a la red junto con sus características)
- Gestión de cambios y configuración
- Incrementa la productividad del operador a través de un diseño intuitivo gestionado a través de excepciones (facilita la vida de los administradores de red)
- Consolida el mapa de red gestionando más de 10000 nodos de forma automática en su versión NNMi Standard Edition y más de 30000 en su versión NNMi Extended Edition (Septiembre, 2021) (Nodos son además obviamente PC, portátil, teléfonos, impresoras, AP generales)
- Facilita la resolución de problemas en tiempo récord, incrementando la escalabilidad y la automatización de tareas
- Reducción del tiempo de administración de la red

**TIPOS DE IMPLEMENTACIONES**

*1.ª IMPLEMENTACIÓN*

![](https://i.imgur.com/77AvehK.png)

Todo parte de un diagrama, y ese se debe representar físicamente, esta herramienta ofrece 3 tipos de arquitectura para su implementación

Esto depende de un análisis profundo y muchos factores, los recursos, tamaño de la empresa, factor económico de la empresa, etc.

La más sencilla es la "Implementación de servidor único (SS)"

Modelo simple instalado en un único servidor se encuentra empaquetado con una base de datos embebida que se instala en el mismo servidor

Esta base de datos va a ir almacenando el monitoreo de la red



![](https://i.imgur.com/EuL9K3U.png)

Nada más en el gráfico nos damos cuenta de que ahora se representa una base de datos

"Clúster de Alta Disponibilidad"
Esta habilita minimizar el tiempo de inactividad en el evento de fallo de aplicación en la creación de un clúster de sistemas redundantes

Existe un servidor activo y uno en standby si en algún momento el servidor principal deja de estar activo por algún problema de la red o problema de energía

El servidor en standby permitirá que la red se siga gestionando y va a manejar los nodos

![](https://i.imgur.com/m5O5ZlK.png)

Esta es una implementación de dos servidores donde se puede obtener el beneficio de un clúster de gran disponibilidad sin tener que instalar ningún software adicional

En el primer gráfico tenemos la ejemplificación de un fallo de la aplicación con una base de datos embebida

En la 1.ª implementación la BD se instala en el mismo servidor aquí está esa misma implementación tanto para el servidor activo como para el Standby, cada uno tiene la BD embebida

En la segunda gráfica ahora se representa un fallo en la aplicación no tiene una BD embebida esta externa montada con el sistema Oracle y dos servidores, uno activo y uno en standby, es costosa por los recursos que implica la instalación y los servidores activos y en standby

___

Otro ejemplo de Implementación

Revisamos la arquitectura de un cajero y un sistema de monitoreo de red ahora revisaremos el NPS

![](https://i.imgur.com/l4N0a1o.png)

Esta es normalmente una implementación que ofrece Microsoft con un servidor proxy del Servicio de usuario de autenticación remota

![](https://i.imgur.com/ORkhnG5.png)

En la parte superior tenemos los dispositivos finales que nos permite conectar a los servidores

Tenemos los servidores, y estos permiten la conexión permiten la transferencia de datos

Tenemos un switch, AP un servidor VPN

Tenemos un servidor NPS RADIUS junto con su base de datos tiene SQLServer por la comptabilidad, junto con un servidor de Directorio Activo

## Lectura Recomendada
![](https://i.imgur.com/e9alpnI.png)


De los ejemplos vistos deben dibujar a mano, tomar foto y enviar por WhastApp a Michell, el mejor tendra una actuación en clase

Dibujar a mano la arquitectura que podria tener las maquinas para (todo el sistema de maquinas) que tiene el metro

Maquinas que tiene desde que el usuario entra
Para la compra de pasaje
El como pasa

Tanto de hadrware como sofftware y los medios de comunicación, para la arquitectura de despliegue de un sistema de metro

Ganadores:
- Juan Albarracin
- Carlos Guanoluisa
- Keila Galeano
- Bruno Tobar

___

## Plataformas de Software y Hardware

![](https://i.imgur.com/xXV30qM.png)

Lo que hicimos fue una abstracción logica, cuando se entrega un desarrollo de software se debe entregar
- Diagramas de usuario
- Casos de uso
- Maquetado de interfaces
- Manuales de usuario
- Manuales de administración

Los procesos cuando piden un desarrollo de software las empresas tiene sus procesos definidos, requisitos funcionales y no funcionales

Todo esto le permite al equipo de desarrollo formar este sistema de acuerdo a los requerimientos de los clientes

### Diferenciar Software

Esta es la clasificacion mas solida para DIFERENCIAR SOFTWARE

![](https://i.imgur.com/H4V3poX.png)

- El software de aplicación ha sido desarrollado para un aspecto en particular por ejemplo
    - Editores de texto: desarrollado exclusivamente para editar texto
    - Hojas de calculo
    - Presentaciónes (Power Point)
    - WhatsApp
    - Exploradores Web
    - Zoom
- El software de sistema es uno mucho mas complejo y engloba gran parte de los sistemas operativos
    - Windows (todas sus versiones)
    - Windows Server (todas sus versiones)
    - Android
    - iOS
    - Linux (todas las distribuciones)

Clasificación ENFOCADA EN LICENCIAS

![](https://i.imgur.com/tF9kosS.png)

La contraloría general de estado tiene especialistas en administración, jurisprudencia e informática Ellos suelen ir a las empresas para trabajar durante 2 meses revisando que todo en la empresa se esté gestionando y adquirido de manera legal

Por ejemplo el documento del POA en donde si se quiere hacer una implementación debe estar plasmado aquí, como eso incurrió un gasto un presupuesto del estado para instituciones públicas son objetos de auditorias

Si una empresa se desea ahorrar (o falta de conocimiento) adquiero o descargo o instalo software crackeado por ejemplo (Windows Pirata) eso es algo muy grave dentro de las instituciones públicas, ellos van a pedir licencias contrato y si ella corresponde a cada una de las máquinas en la red

Existen 3 tipos de servicios principales y modelos en cuanto a computacion en la nube
- Software as a Service
    - Google Docs (toda su ofimatica)
- Infraestructura as Service
    - Contratar servidores fisicos pero acceso virtual
- Platform as a Service
    - Tenemos todo el ambiente y herramientas junto con las conexiones

Modelos en Computación en la Nube
- Publico
- Privado
- Hibrido

Por el hecho de que se pueda copiar y pegar software no signiifica que pueda usarse, existen las auditorias para evitar eso

Si tenemos nuestras herramientas para el desarrollo de TICS de la empresa, que bien, pero si no tenemos debemos justificar [[3 ADMSIS - Infraestructura TI]] porque no podemos hacerlo internamente y buscar en la cartera de MINTEL y pasar por varios filtros para a la final adquirir

**DEFINICIÓN**

![](https://i.imgur.com/thNEAY0.png)

**CLASIFICACION SEGUN EL TIPO DE LICENCIA**

- Software de Aplicacion
- Software de sistema

Tambien se puede por tipo de licencia

![](https://i.imgur.com/TMo7B8D.png)

En la teoría de la materia se puede analizar esto y si no se entiende algo pueden consultar

**¿Quién decide "QUE" y "COMO" se usara e instalar el software adecuado para llevar a cabo las operaciones dentro del centro de datos?**

¿De donde sale el POA? Para adquirir cualquier tecnología de la empresa?

==SIEMPRE SALE DEL DEPARTAMENTO DE TI==


La dirección financiera quiere adquirir un sistema financiero, quien es el que administra los procesos, crea los proyectos, analista. Todo esto lo realiza el DEPARTAMENTO DE TI, la dirección financiera sabe lo que quiere, pero NO SABE COMO APLICARLO

### Ventajas Software Libre
- Económico
    - Bajo nulo o coste de los productos libres permiten proporcionar a las PYMES servicios y ampliar sus infraestructuras sin que se vean mermados sus intentos de crecimiento por no poder hacer frente al pago de grandes cantidades de dinero en licencias
- Libertad de uso y redistribución
    - Las licencias de software libre existentes permiten la instalación de software tantas veces y en tantas maquians quieras
- Requisitos de hadrware menores  y durabilidad de las soluciones
    - Existen casos documentados que demuestran que las soluciones de libre tienen sus requisitos de hardware menor y por lo tanto son baratas de implementar
    - Hay que hacer un analisis profundo analizando varios factores con metodologias estandares etc porque las cosas no se implementa por inercia ni improvisando
- Fomento de la libre compentencia al basarse en servicios y no licencias
    - ![](https://i.imgur.com/vGVmASe.png)
    - Lo más costoso es la gestión, el conocimiento, hay muy pocas personas que tienen implementar, gestionarlo y continuar usando el sistema.
    - Hace varios años en uno de los gobiernos anteriores había decretos en donde se exigía a las empresas públicas a usar Software libre, las empresas que antes usaban Windows (acostumbrados y conocimiento general) ahora de un momento para otro debieran usar Ubuntu y ofimática Open Source fue una transición muy complicada *No funciono*
- Independencia del proveedor
    - Garantiza independencia con respecto al proveedor gracias a la disponibilidad del codigo fuente. Cualquier empresa o profesional, con los conocimientos adecuados, puede seguir ofreciendo desarrollo o servicios para la aplicación
- Adaptación del Software
    - Permite personalizar gracias al hecho que se dispone del codigo fuente los programas tanto como sea necesario hasta que cubran exactamente alguna necesidad.
- Metodos simples y uninificados de gestión de software
    - ![](https://i.imgur.com/tRSMODb.png)
- Sistema en expansión
    - Las ventajas especialmente económica que aportan las soluciones libres a muchas empresas y a aportaciones de la comunidad han permitido constante crecimiento de software libre hasta superar en ocasiones como en el de los servidores web, al mercado propietario


> [!bug]
> En las siguiente clase vamos a ver las desventajas del software libre

El taller grupal se debe hablar sobre las mejoras practicsa normas estandares para infraestructuras de TI

Las cosas no se improvisan entonces para gestionar esto hemos aprendido estas normas y estandares de mejores practicas

Cada equipo debe cubrir 3 de los siguientes temas:

![](https://i.imgur.com/XW5L7we.png)

Se debe grabar, se debe ver el rostro en linea con tiempo real pero se debe tener la camara encendida 

La presentación la transforman a PDF y esa se carga, en el comentario de la actividad se sube el enlace que tenga en algo en la Nube, pero se necesita ver que SE USO UNA APLICACIÓN COLABORATIVA