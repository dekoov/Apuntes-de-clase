---
fecha: 2024-11-27
tags:
  - 4toSemestre
  - 4toSemestre/REDES
---
# 5 REDES - 

Se puso en el chat de whastapp los horarios para acordar la practica de forma presencial, no es obligatorio

Se subio el aviso para revisar los videos de los temas 5 y 6 incluido el video "Demo UTP"

![](https://i.imgur.com/4e9LdED.png)

En este ejemplo vemos como se agregan datos adicinoales en las cabezeras cada ves q se tiene un nuevo nivel

En este caos se visualiza que la cantidad de capas no sea tan grande

Basicamente se tienen dos estructuras para el envio de info

1: Utiliza transmision analogica, es decir los datos son analogicos, en ese caso no tenemos la posibilidad de usar o reusar el canal, esa infraestructura es orientada a la coenxion, se debe establecer la comun. cuando se cerro el circuito cuando esos dos participantes pueden estar mandando informacion

En el ejemplo de la informacion de ROSS y es continua en el tiempo. si no hay nadie de los dos interlocutares no manda informacion, igual el canal esta ocupado y nadie mas puede usar el mismo. Esto complica cuando se piensa en la infinida de servicios que usamos en la misma computadora. Eso seria inviable en comutacion de circuots

Nos tocaria establecer una liena de com directa etnre un cliente o un servidor. Si tenemos varias ventanas en un explo y cada ventana tiene acceso a un server diferente cada una de ellas representa una conexion

La comutacion de paquetes es de ayuda. Es una idea que va alrededor de 1960 pero no se pudo implementar por que no habia los dispositivos inteligentes en los extremos. La intencion es que ahora estos dispo. hagan todo el rpoceso, la red, comunm, infraestructura tiene tareas rapidas y faciles para que los usuarios vayan usando este entorno

La comuntaciond e paquetes viene a ser una infraestructura no orientada a la conexion, osea que no necesita establecer comun entre un nodo y el nodo extremo, se debe verificar que este le siguiente salto dispnible

![](https://i.imgur.com/9iDKTvA.png)

Por ejemplo para esta lan sise desea llegar al otro extremo el primer salto es el router izquierda arriba ese toma decisiones, ya toda la infraestructura de red anterior esta desalojada y 

Genera fragmetnso de informacion cada uno de los usuariosp ueden mandar, no mandan al mismo tiempo para no colapsar, pero si un pequeño instante en el tiempo microsegundos el siguiente otro usuario manda paquetes y asi se envian tan rapido q para los usuariso finales es como estar conectados todo el tiempo. La informacion los paquetes se estan multiplexando unos ao tros se envian a traves de una pila de stack 

Sin comutacion de paquetes no habria la posibilidad de tener las comunicaciones que existen ahora 


Los paquetes se pueden desviar, esa informacion se pierde?
Ese es un problema de las infraestructura no orietnadas a conexion. No garantizan que los paquetes, sep ierden, se duplican, se desorganizan

De alguna manera se solventa eso, entonces eso es a nivel de infraestructura los fierros las capas superiorss trataran de solvetar esas problematicas, si un paquete se perdio se trata de identificar porque. Pero si uno que otro paquete en el intento habra un tiempo un timeout un tiempo maximo, no llego una confirmacion del paquete receptivo, se retransmite la informacion se manda uno nuevo. 

Cuando uno llega con errores la estrategia no es corregir, es detectarlo, se informa y solicita retransmision. La retransmision es mucho mas rapida que tratar de corregir el error en el destino


Cuando se envian paquetes existen prioridades cual es el criterio para enviar datos en esa prioridades, se pueden enviar otras que tenga prioridades

Imagina que se manda un paquete se envia al primer salto (un router) este tiene la ventaja que visualiza los sentido de los paquetes orwall o reenvio de informacion. Ese punto de reenvio visualiza los paquetes y la cabecera de la infor este paquete contiene un servicio de streaming de netflix y el otro contiene info de un correo electronico otro mas talvez llegara con una pagina web info. Cual es mas prioritario?

Que llegue mas rapido el paquete de correo electronico, la pagina web o el streaming de netflix?
Obvio el streamingi tiene mayor prioridad, visualiza la partesita de la cabecera y se identifica las calidades de servicio y ahi se organiza la prioridad, por ello los paquetes pueden llegar en desorden, un pauqete puede ir por cualquier lado y  el host puede organizar esta informacion

Los archivos multimedia tienen mayor prioridad porque se itneresa que lleguen rapido para no tener retardos, o ahi nos importa que no existan retardos entonces los paquetes van en orden, a la larga hay problemas que se deben saber manejar

Hay mucha gente que quiere ver netflix youtube, entonces esos paquetes trataran de llegar mas rapido y alguien que se queire bajar un email se demora un monton
El administrador de la red debe identificar estas necesidades si es en un trabajo se puden bloquear esos paquetes de streamingn o se puden dar prioridad bajita para que los demas viajen rapido

Si la red no tiene control los archivos multimedia o streaming siempre van a tener mayor prioridad, *serviciso orientados a laconexion servicios orientados a la no conexion  que es esa madre?*

___
## GSN3
Con el packet tracer no es mucho que hacer se baja el instalador

EL GSN3 tiene un detalle es que para el se debe necesitar alguans cosas

Para la computadora del inge tiene un procesador de apple ARM, esos tienen un problema respecto a como se puede hacer la virtualizacion y cuando se instala el GSN3 si bien existe version para MAC, primerito el cliente para el GSN3 (su version de maquina SO)


Se puede trabajar en modo standalone pero ese no nos puede servir en algunas cosas es MUY LIMITADO 

Abrismos preferencias y ahi tenemos el servidor y por defecto se tiene 
ENABLE LoCAL SERVER
Entonces con ese servidor local habilitara un servicio basico que no tiene mucho que se puede hacer, opciones muy basicas

En este menu no hay posibilidad de poner en entornos de emulacion de router cisco tanto con los dynamics o lso que trabajan con emulacion basada en unix o otros que etrabajan con QEMU tambien se puede virtuabox VMWare pero TODAS ESAS OPCIOENS Con el SERVIDOR LOCAL NO SERVIRA


Esta funcion limitada del GSN3 con un LOCAL SERVER esta no nos servira de mucho

En windows se puede tener la posibilidad de ver una maquina o algun dispositivo basico con los menus de la izquierda, como no levanta ni siquiera el servidor local si apareceran algunos pocos servicios

Hay otra opcion para usarlo con maquina virtual ENABLE THE GSN3 VM
En este caso del inge de MAC no tiene entorno de virtualizacion no tiene ni uno es un poco mas complejo, el debe seleccionar un entorno remoto

# Como instalar servidor
Necesitamos
Broadcpm vmware free en google en primer link antes vmware era un programa propietario vmware ya no esta como tal en pagians oficiales de vmware SOLO ESTA GRATIS EN LA PAGINA DE BROADCOM

Desde el 11 de noviembre de 2024 los hipervisores para PCs de escritorio VMWARE FUSION y VMWARE WORKSTATION esta con acceso gratuito 

https://knowledge.broadcom.com/external/article/368667/download-and-license-vmware-desktop-hype.html

Una ves instalado el vmware WORKSTATION esta el entorno de virtualizacion el sigueiten paso es descargar LA MAQUINA VIRTUAL y simplemente importarla al software de virtualizacion

Necesitamos un numerito de una cosa de la maquina de virtualizacion Ponerle el nombre de la maquina virtual o el servio
![](https://i.imgur.com/owPUoma.png)

Poner el IP en HOST y el puerto correspondiente

Y ya deberia levantarnos el servidor, se va al cliente El servidorl ocal ya esta levantando pero toca levantar el servidor de virtualizacion 

Una evz levantado ya sep uede ir agregando los diferentes dispositivos, como agregar algun router microtick para alguna prueba

VIDEO RECOMENDADO POR EL INGE:
![](https://www.youtube.com/watch?v=bVCO01iIs7w)

Con que sistemas operativos para los rtouers vamos a trabajar pero todos la mayoria son de pago entonces no saber cual exactamente descargar

Si es para CISCO la forma mas facil es utiizar el emulador DYNAMICS
![](https://i.imgur.com/NmVnpxA.png)

En la configuracion del GSN3 podemos dar la ubicacion de las imagenes de los diferentes dispositivos

IMAGENES CISCO GRATIS
https://networkrare.com/free-download-cisco-ios-images-for-gns3-and-eve-ng/
Funciona para el GSN3 y para el EVE

3 de diciembre a las 3 de la tarde 1 hora y media se demoraran 

Reunirse en el laboratori ode electronica redes y comunicacion de datos
