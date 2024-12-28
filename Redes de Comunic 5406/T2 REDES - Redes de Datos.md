---
keywords:
  - Ventajas y desventajas
  - Objetivos
  - Redes de datos
  - Tipos y modelos
---
# T2 REDES - Redes de Datos
#4toSemestre/REDES 

## Resumen

___

## Introducción
Modificación del viejo concepto de centro de cómputos a los sistemas basados en computadoras interconectadas

Viene de la mano de la miniaturización en electrónica, ahora los circuitos están interconectados a 5 nanómetros

Computadoras + comunicaciones = redes de computadoras, computadoras autónomas conectadas para intercambio de información


## Objetivos de las Redes de Datos
- Compartir
    - Recursos
    - Equipos
    - Información
    - Programas

- Estar alojados en ubicaciones seguras, robustas con alta disponibilidad.
- Brindar confiabilidad en la información, disponibilidad, integridad
    - Rápido
    - Seguro
    - Económico

Por ejemplo los teléfonos antiguos dependiendo del tipo de tecnología para la conectividad a las antenas. El mismo teléfono en GSM podría estar costando 500$, pero con CDMA costaba 900 $


## Ventajas de las Redes
Son más confiables y más baratas estos mainframes fueron reemplazados por PC personales y la idea de las redes que sean masificadas y agregarles de nodos fáciles

- Compartir recursos
- Aumento de la confiabilidad
- Ahorro (PCs versus Mainframes)
    - Cliente - Servidor
- Escalabilidad
- Medio de comunicación


## Tipos de Conexiones

![|400](https://i.imgur.com/Sm6AjKo.png)

Actualmente, las conexiones Mainframe han sido reemplazadas por Servidores debido a sus ventajas, por tanto, nomas existen 2 tipos de conexiones

- Peer-to-Peer Environment
    - Recursos compartidos entre todos
    - La información circula por todo el entorno, existe de que se pueda volver un caos
    - Alta redundancia

- Client/Server Environment
    - Recursos y conexión solo en servidor, no todos a todos
    - Ventaja en el tema de seguridad
    - Una desventaja es tienen un **ÚNICO PUNTO DE FALLA** en las comunicaciones siempre se debe tener redundancia para evitar esto

### Granjas de servidores
**SOLUCIÓN A LA DESVENTAJA**
![|300](https://i.imgur.com/PrS6DeR.png)

Generar un conjunto de servidores de forma distribuida o que actúen de forma Backup por ejemplo tenemos las **GRANJAS DE SERVIDORES o (DMZ)**

**TIPOS**
**Distribuida:** Si algún servidor se cae tenemos todavía los demás servicios
- Servidor de correo
- Servidor Web
- Servidor archivos FTP

**Backup**: Se puede redundar el servicio, si algún servidor primario se cae el servidor secundario sale a solventar
- Servidor de correo (Primario)
    - Servidor Web (Backup)
- Servidor Web (Primario)
    - Servidor FTP (Backup)
- Servidor archivos FTP


## Modelo Cliente - Servidor

![](https://i.imgur.com/yCaB2dW.png)

- Contiene un **proceso cliente**, encargado de enviar peticiones al servidor y de procesar las respuestas recibidas.
- Contiene un **proceso servidor**, que atiende las peticiones escuchando mediante un puerto y proporciona los datos o servicios requeridos.
- La red interconecta ambas máquinas y facilita el intercambio de mensajes entre cliente y servidor.
- **Intercambio de Mensajes**:
    - **Request (Petición)**: El cliente envía una solicitud al servidor para acceder a un recurso o servicio.
    - **Reply (Respuesta)**: El servidor procesa la solicitud y envía una respuesta con los datos o el resultado.


### Ventajas y Desventajas

| Ventajas Punto a Punto                   | Ventajas Cliente - Servidor                                                           |
| ---------------------------------------- | ------------------------------------------------------------------------------------- |
| Menos cara de implementar                | Provee mayor seguridad                                                                |
| No requiere software especiializado      | Facil de administrar cuando la red es grande porque la administración es centralizada |
| No requiere un administrador de dedicado | todos los dato pueden ser almacenados en una localización central                     |

| Desventajas Punto a Punto                                                                                | Desventajas Cliente  - Servidor                                                                            |
| -------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| No se puede escalar a redes grandes y la administracion se vuelve inmanejable                            | Requiere software caro y especiializado para la administracion y operación de la red                       |
| Cada usuario debe ser entrado para ejecutar trareas administrativas de gestión y configuración de la red | Requiere maquians servidores mas potente y caras                                                           |
| Menos seguras                                                                                            | Requierer un administrador profesional                                                                     |
| Todas las maquinas comparten recursos negativamente afectando el desempeño                               | Tiene un solo punto de falla los datos de usuario no son disponibles si el servidor esta fuera de servicio |

## Servicios mediante este modelo
- Comunicación interpersonal
- Correo electrónico (e-mail)
- Telefonía Electrónica (i-phone)
- Reuniones virtuales
- Grupos de trabajo dispersos
- Intercambio entre grupos geográficamente distanciados
- Acceso a información remota
- Acceso a computadoras remotas (telnet)
- Transferencia de archivos (FTP)
- Navegación (WWW)
- Entretenimiento interactivo


## Clasificación de las redes
### Según la tecnología de transmisión

- Redes por difusión (Brodcast Networks)
    - Único canal de comunicación
    - Las estaciones comparten un canal (RadioDifusión FM) (Ethernet)
        - FM comparten el medio el aire
    - Mensaje se difunde a todas las demás estaciones, pero solo el destinatario lo procesa; las demás lo ignoran
    - Eficiencia limitada, menos eficiente en redes grandes

- Redes punto a punto
    - Enlaces directos entre pares, (Solo entre dos dispositivos)
    - Enlaces entre equipos (Conexión por MÓDEM)
    - Datos viajan directamente, o por múltiples enlaces si hay topologías
    - Mejor para grandes redes, mucha eficiencia

### Según el tamaño
- PAN (Redes de Área Personal)
    - Bluetooth no tiene mucho alcance (10m - 9m)
    - Conexión teclado hacia computador, tecnologías propias, área personal
    - De usos específicos

- LAN (Redes de Área Local)
    - Edificios o campus (100m - 1000m)
    - Generalmente Mbps o Gbps
    - Ethernet/Wi-Fi

- MAN (Redes de Área Metropolitana)
    - Ciudades (10 - 50 km)
    - Conexión pública o privada
    - Fibra óptica
    - Comunicar múltiples LANs

- WAN (Redes de Área Amplia)
    - Países o continentes
    - Internet
    - Satélite, líneas troncales

### Distancia Interprocesadores

![](https://i.imgur.com/gr1Tba3.png)

en las redes PAN no hay un límite explícito en su distancia, sino que está relacionado con la tecnología de transmisión, tienen distancias y tecnologías propias

Las LAN redes de área local pueden ser conexiones entre múltiples dispositivos en una sala o edificio, estas pueden agruparse y desagruparse

Las redes LAN también utilizan tecnologías de MAN son casi lo mismo

Una LAN su frontera no está bien definida por ello nos basamos en su tecnología, si usa la misma tecnología (Ethernet/Wi-Fi) pero una vez se tiene un "Router" que intercambia de un lado hacia otro la tecnología para conectarse a una Extranet se trata de una WAN

Redes en LAN generalmente estan basadas en redes Broadcast
Redes en WAN basadas generalmente en Peer-to-Peer

## Dispositivos de redes
Los componentes de la red, los dispositivos de usuario final y los dispositivos de redes

## End User Devices
![](https://i.imgur.com/kLlCGzi.png)

- Computadoras personales
- Laptop
- Impresoras
- Servidores
- Celulares
- Tablets
- Televisores

Todo dispositivo inteligente que tenga conexión a internet, todos estos son dispositivos terminales de usuario

Estos deben interconectarse a traves de los dispositivos de los Network Devices

En cada uno de estos dispositivos necesitaremos unas [[T2 REDES - Redes de Datos#Network Interface Cards NICs|NICs]] que pueden ser cableadas o inalambricas

### Network Devices
![](https://i.imgur.com/zFQG3AN.png)

Repetidor lo unico que hace es regenerar la señal, una señal atenuada la regenera como nueva

Un bridge que interconecta dos entornos de red

Un hub de diferentes tipos que tiene varios puertos para interconexión creando un entorno de red

Un switch que son una optimización de los Hub tambien tienen varios puertos de red

Los router que por un lado tienen una tecnologia y por el otro otra (digital a analogico y viceversa)

Y todo esto en conjunto los dispositivos end user y los dispositivos de network conformaran una nube de red

## Network Interface Cards (NICs)

Para hacer estas conexiones necesitamos de algun modulo, son tarjetas interfaces de red.

Son propias de cada una de las tecnologías

![](https://i.imgur.com/b8lyG9d.png)

Estas NICs junto con los dispositivos de usuario final nos permite generar las topologías de red

## Topologías de Redes

![](https://i.imgur.com/CfM1See.png)

Las tres topologías mas fundamentales son
- Bus Topology
- Ring Topology
- Mesh Topology

Estas otras que se ven en el grafico basicamente son las mismas que la topologia en bus, tienen las mismas caracteristicas con ciertas diferencias

#### Topologia en Bus
En las primeras redes se tenia un cable coaxial con unos conectores donde se conectaban muchas computadoras a ese cable a traves de la NIC

Cuando se nos acaba el numero de puertos disponibles pensemos en un Hub de 8 puertos y queremos conectar 10 computadoras
- Podriamos sacar un nodo
- Conectar otro hub
- Y conectar los dispositivos necesarios

Si una topologia en bus se dice que esta a 10 Mbps y tengo un medio compartido ese ancho de banda se dividira para todo el numero de usuarios conectados
10 Mbps / 10 Users Conectados = 1Mpbs

Problema de conexiones
El problema principal de conexión en las topologías en bus por cable es la **colisión de datos**. Esto ocurre cuando dos dispositivos transmiten datos simultáneamente en el cable compartido, provocando que las señales interfieran entre sí. Esto resulta en pérdida de información y la necesidad de retransmisiones, lo que reduce la eficiencia de la red