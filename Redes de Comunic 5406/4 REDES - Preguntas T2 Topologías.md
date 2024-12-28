---
fecha: 2024-11-20
tags:
  - 4toSemestre
  - 4toSemestre/REDES
---
## Resumen:

___
# 4 REDES - Preguntas T2 Topologías

## Introducción

- Sesiones prácticas para emponchado y empalmado de cables
- En los videos hay mucha información, por tanto, se irán subiendo diapositivas

## Instalación

- 2 o 3 dólares se necesitará para el material para el empalme y emponchado, para la fibra óptica si es demoroso y la precisión necesaria para esto es mayor

- Los programas que iremos utilizando serán GNS3 para la simulación de redes
    - https://cyberlab.pacific.edu/courses/comp177/labs/lab-1-gns3 **INSTALACIÓN**

- Cisco Packet Tracer será otra herramienta a utilizar, no son temática de la clase nos eran evaluadas o juzgadas 
    - https://www.netacad.com/resources/lab-downloads?courseLang=es-XL

- **Tomar el curso de Cisco Packet Tracer para ir avanzando en la clase el que necesitaremos es "Introducción a Packet Tracer"**

## Tareas

- Las simulaciones que hagamos van a correr con la versión 8.2.2 
    - Versiones anteriores no habrá compatibilidad con los archivos enviados

- el GSN3 es un emulador, además de instalar un cliente se necesita un servidor para hacer la virtualización
    - no es necesario VMware, pero si se desea se puede instalar

- Después instalar la máquina virtual del GSN3 en ella guardaremos las simulaciones y los sistemas operativos de los diferentes routers que podamos utilizar
    - Por ejemplo nos pide instalar un MKRotkit de un router microtick descargar el firmware

- *Simulador Packet Tracer*
- *Emulador GSN3*

![](https://i.imgur.com/11UrRLk.png)

___

# Tema 2

- Las redes necesitan para poder transmitir a través de dos nodos, necesitan un medio de comunicación
    - Medio Compartido
    - Enlace punto a punto

- Para eso se pueden obtener diferentes formas para los dispositivos esas topologías así podemos ir dibujando estas topologías de manera interactiva en los simuladores

![](https://i.imgur.com/PhDAJqu.png)

- Estas topologías tendrán característica especial, dentro de ellas en la red de datos podríamos mencionar
    - Sea escalable o sea añadir nodos de forma fácil
    - Sea redundante

## *EJEMPLO*
- Imaginate ir a una universidad lugar público, conectarnos a la red inalámbrica viendo el ESSID y ya tenemos internet, pero para dar esa conectividad se necesitan ==procesos adicionales y se necesitan de este paradigma cliente-servidor==

En el tema 2 se menciona ese paradigma y todas las comunicaciones usan esta estructura "cliente-servidor" de una administración centralizada y datos

El acceso y escalabilidad también es transparente para el usuario la topología se va agrandando fácilmente

- La topología dominante es en bus y similar a estrella y estrella extendida para un medio compartido

## *PROBLEMÁTICA*

Una de ellas es el tener un único punto de falla, **si es que el bus de comunicaciones se daña, esa línea se daña ya no hay forma de redundancia**

Esa es otra CARACTERÍSTICA **debemos tener alta redundancia para tener ALTA DISPONIBILIDAD**
- Sea disponible mediante alta redundancia

La disponibilidad se mide en PORCENTAJE, si la red tiene disponibilidad del 95% eso para ir aumentando esos porcentajes la RED TIENE QUE SER MÁS ROBUSTA ante caídas y eso significan costos

La topología en anillo tiene UNA REDUNDANCIA De 2 A 1, un punto en un círculo tiene dos rutas, si se cae un segmento existe el otro

==En una primera instancia podemos entender esa gráfica COMO LAS TOPOLOGÍAS TAMBIÉN PUEDEN SER COMPLEJAS dependiendo la naturaleza y los requerimientos de la organización== 

*DUDAS*

**¿Si no podemos ir a la parte práctica para armar el cable de red, conocemos podemos grabar y nos acepten eso para tarea?**
Los que pueden ir puede ser enriquecedor para ellos, pero los que no pueden si pueden simular o replicar sería genial, pero eso no significa BAJA DE NOTAS o algo así

- Como herramientas necesitamos una ponchadora y una cortadora, esas nos son fáciles de conseguir
- El analizado de redes si es difícil, ese se puede usar en la ESPE y eso no está al alcance de otras personas
- La parte de ==fibra óptica una empalmadora de fusión== no es asequible puede estar costando 5000 $ y el ver como funciona es interesante

**¿Los sistemas operativos van a ocupar muchos recursos no?**
- Si una computadora de 500 GB no se espera problema
    - La máquina virtual de GSN3 del servidor pesa 1.5 GB
    - Los sistemas operativos el microtick el firmware son 34 MB en cuestión de disco NO HAY MUCHO LÍO

- Lo que si es jodido es el tema del procesador y la RAM si vamos metiendo más dispositivos, router cisco consumiendo 500 MB en RAM con 16 GB de RAM si podríamos irnos cómodos

Hay un entregable en el tema 2 nomas son como un aviso? no hay que hacer ninguna entrega solo son un aviso de como es el avance de la materia

El tema 2 no es mucha cosa, conocimiento cotidiano, ya nosotros ya estamos muy metidos con las redes usuario de redes ya tenemos medio conocimiento de ello. 

YA EN EL TEMA 5 SE ANALIZARA el modelo OSINT un modelo para analisis de red (arquitectura de red) **se espera que existan mas dudas para ir solventando** para este tema planteado TEMA 2 

todos estos problemas son CAPA FISICA todos estos son de ciertas limitaciones en cualqueir sistemas de comunicaciones
- Potencia limitante
- Ancho de banda limitante
Lo q se transmite son ondas electromagneticas

Para esto tenemos diferentes tecnologias, si abrimos las redes inalambricas estas redes dependiendo del SO (este caso MAC) en windows se puede ir ver tambien otras opciones, se tiene otras opciones para ver en detalle

El mecanismo por el cual se esta conectado es WPA2 PERSONAL
![](https://i.imgur.com/qlxAsNh.png)

Ancho de banda es de 5 GHz
El estandar trabajhado es 802.11ax

MIMO usa esa tecnica para varios portadores de informacion para transmitir por tanto es mas rapida

El tema de las redes inalambricas es q dependiendo de las interferencias se van reduciendo las velocidades 

EL TEMA es que si nuestra velocidad es bien lenta podemos optar por conectarnos via cable mandando un cablesito mas cerca y ahi dependiendo , tambien hay repetidores Wireless y repetidores Ethernet. es mas ahi repetidores usando la RED ELETRICA A TRAVES DE ELLA SE VA LA SEÑAL si se esta en el mismo transformador mismo fase mismo braker se tiene conectividad pero las velocidades no son muy grandes

EL TEMA DE LA VELOCIDAD
Es algo asi como un sistema de tuberias, si se tiene una tubieria grande fluYE ;MAS ANCHO DE BANDA MAS PAQUETES MAS INFO y si la lalve de paso esta abierta un poquito tiene un cuello de botella esa restriccion el ancho de banda y la velocidad de enlaces es lo mismo

ANCHO DE BANDA ROUTER ETC TEMA
Es posible por esta isntancia que se dañe el cableado optico debido que las velocidades son menores 
Problema: El equipo router no es actualizado no soporta temas de ancho de banda y por eso se daño un cableado optico??

Cuando uno contrata un proveedor de servicios se ponen ciertas condiciones,
- Contrate internet y me dieron 100MB por 30$ y dieron un equipo que soporta 100MB
- Como el internet se va ofertando los costos tienden a bajar, si por eso mismos 30$ se revisa otros proveedores hay otros de 300MB por el mismo costo
- Se reclama subir el ancho de banda o bajar presio, pero el equipo sigue soportando 100MB entonces no se nota
- Por eso tal vez tambien pudo haber algnuna problematica con el acceso a internet, aveces los dispositivos no soportan la capacidad contratada y por eso se actualiza el dispositivo (no tiene en stock)
- DE AHI QUE SE DAÑE EL CABLEADO eso no puede pasar, se manda señales de luz, no es que se mande con mas potencia eso no daña NI EL EQUIPO ni EL CABLE

bhay que presionar el insumo ellos juegan con el ancho de banda, si no se usa mucho ancho de banda y tienen contratado bastante, EL PROVEEDOR QUITA ya que se puede usar en otro lado, pero como lo tienen sin utilizar el ISP monitorea eso quita y da a otro

El Speedtest lo que hace es deescargar un archivo desde un servidor (MIAMI) hasta nuestro proveedor, y esa descarga se va midiendo cuanto tiempo toma y cual es la velocidad 
ESTA MEDIDA No es muy certera ya que se usa internet en otras cosas 