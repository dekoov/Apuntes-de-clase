---
fecha: 2024-11-14
tags:
  - 4toSemestre
  - 4toSemestre/ADMSIS
keywords: 
share_link: https://share.note.sx/tgg03s9s#4rNaqZnG/sLhKf7FZ6PpsLe6OmDmf5Bfj7p7xtXkVJQ
share_updated: 2024-12-27T22:23:18-05:00
---
## Resumen


___
# 3 ADMSIS - Infraestructura TI
## Introducción

Las presentaciones tienen carátula
- Título de presentación
- Nombres de los integrantes
- Grupo número tal

Debe ir una transparencia con tabla de contenido
- Se debe explicar esta transparencia con un poco de contexto
- La tercera diapositiva ya viene el contenido de contenido, aquí viene el tema y las explicaciones

Si se usa MÁS de una diapositiva para un tema se debe:
- En el título Hardware I, Hardware II, ... Hardware VI, etc.
- Existe una diapositiva obligatoria de Conclusiones
- Otra diapositiva obligatoria de Bibliografías

Temas cargados en el aula virtual se debe estudiar, para la prueba de esta asignatura que viene el día JUEVES

___
## [[Infraestructura de TI#Componentes de la infraestructura|Elementos Infraestructura de TI]]

La infraestructura se puede decir que está compuesta por grupos ==el primer grupo grande es el hardware, el otro grupo de elementos básicos es software, y las redes de comunicaciones,== aquí se menciona como se conectan todos los dispositivos incluido el centro de datos

**La [[Infraestructura de TI]] es parte de la [[Arquitectura de TI]], tener en cuenta esto**

### Definición

==La infraestructura comprende dispositivos físicos y software necesarios para la operacion empresarial,==, pero también se trata de un conjunto de servicios a lo largo y ancho de la empresa presupuestada. La dirección ejecutiva debe aprobar las propuestas del departamento de infraestructura de TI

A continuación una definición de libro:
ITIL define **como el conjunto de hardware, software, redes, instalaciones, recursos de datos y capacidades necesarias para el desarrollo, operacion, entrega, monitoreo y soporte de los servicios digitales**

> [!note]
> Los ingenieros o el personal NO FORMAN parte de la infraestructura de TI

### Componentes

**HARDWARE de TI:**
Incluye todos los dispositivos físicos en el entorno tecnológico de la organización
- Servidores
- Dispositivos de almacenamiento
- Access Points como
    - Computadoras
    - Teléfonos 
    - Tabletas

**SOFTWARE de TI:**
Engloba muchos elementos como
- Sistemas operativos
- Middleware
- Base de datos
- Servidores de aplicación
- CRM
- ERP
- CMS
- Herramientas de virtualización que facilitan el intercambio de datos y funcionalidad de apps

*EJEMPLO*
Por ejemplo una plataforma financiera, para la gestión del personal, un CRM para las relaciones con los clientes, 

## Arquitectura de Infraestructura
![](https://i.imgur.com/uxLmOk9.png)

*ANALOGÍA*
Un arquitecto al diseñar una casa empieza a poner la disposición de todo los cuartos de la casa. **Dentro de una empresa siempre se definen estrategias y objetivos.** 

Dentro de cada departamento de la org. También lo hacen, todas relacionadas de forma general con la empresa. 

Dependiendo tendremos diferentes servicios de infraestructura de TI, depende del negocio

*EJEMPLO REAL*

Por ejemplo para una empresa de venta de ropa, necesitará

- Un servicio para los proveedores
- Base de datos donde almacenarlos
- Tablas en la BD donde tener los contactos 
- Los empleados tendrán una intranet
- Una plataforma pare gestionar ventas
- Software para gestión de clientes 

### Dentro de la arquitectura
#### Servicios

Plataformas de cómputo
- Usadas para servicios de PC para conectar empleados, clientes y proveedores en un entorno digital

Telecomunicaciones servicios
- Proporcionan datos de voz video y empleados, clientes y proveedores

Servicios de administracion de datos
- Almacenan y manejan datos corp. y dan capacidades para analisis de datos

Servicios de software de apps
- Que proporcionan capcaidades para toda la empresa

Servicios de adm. de instalaciones fisicas
- Desarrollan y manejan instalaciones fisicas requeridas por los servicios de computo, telecomunicaciones y adm. de datos (por ejempo aquellos sistemas que gestionan la asistencia de los empleados)

Servicios de administracion de Ti
- Donde se gestionan los proyectos y donde se hacne el seugimiento y monitoreo de estos

Servicios de estándares de TI
- Dotan a la empresa y sus unidades de negocios políticas que determinam cuál tecnología de información utilizará, en qué momento y que manera

Servicios de entrenamiento en TI
- Proporcionan capacitación a los empleados en el uso de los sistemas y a los gerentes capacitación sobre la manera de planificar y manejar inversiones en TI

Servicios de investigación y desarrollo de TI
- Dan a la empresa investigación sobre que proyectos e inversiones de TI potenciales podrían ayudar a la empresa

Todo esto es parte de LA ARQUITECTURA pero no todas las empresas cuentan con TODOS estos servicios.

#### Dispositivos

Switching
- Es el dispositivo que provee conectividad entre equipos de la red en una LAN
- Contiene puertos que se conectan físicamente a otros dispositivos, incluído otros swtiches, routers y servidores

Dentro de servidores nos refereimos de forma fisica no los digitales de software.

Las redes mas viejas antes usaban PUENTES donde se podia ver el trafico 

Routers
- Mueve los paquetes de datos
- Permiten a los dispositivos de diferentes LAN comunicarse al determinar el siguiente "salto" que dejara el paquete al llegar a su destino
- En caso de dirección IP configurada manualmente, el valor de la puerta de enlace ingresado será la dirección del router

Cuando se hace una configuracion manual, una ves que tengamos toda esta información podemos configurarla directamente en el Switch mediante un cable y una consola

Firewalls
- Dispositivos de seguridad en el borde de la red
- Piensa en ella como un guardian
- Conjunto de reglas que definen que tipos de trafico podrán pasar por ella y cuáles serán bloqueados
- En la versión más simple, la configuración permite especificar un puerto o protocolo para el tráfico de un dispositivo a otro o hacia un grupo de estos

Firewalls podemos hablarlo dentro de SOFTWARE o HARDWARE

Por ejemplo el firewall que vienen en SO Windows es de SOFTWARE, en otras empresas se usan dispositivos fisicos que son de seguridad que se encuentran en el borde de la red

No permiten entrar que entre software o actores maliciosos

![](https://i.imgur.com/v7vjd7O.png)

![](https://i.imgur.com/VfhZIMt.png)

![](https://i.imgur.com/p2ROfBS.png)


EJERCICIO MENTAL PARA LA SIGUIENTE CLASE
![](https://i.imgur.com/ITjGGID.png)
