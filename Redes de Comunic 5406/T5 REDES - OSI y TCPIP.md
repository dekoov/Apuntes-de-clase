---
keywords:
  - OSI
  - Definición
  - Protocolos
  - Componentes
tags:
  - estudios
  - 4toSemestre/REDES
---
## Resumen
- Que es un payload
- 


---
# T5 REDES - OSI y TCP/IP

## Introducción

El Modelo OSI (Open Systems Interconnection) es un marco conceptual que estandariza las funciones de un sistema de telecomunicaciones o computación en siete capas distintas

Desarrollado por la Organización Internacional de Normalización (ISO) en 1984 para facilitar la interoperabilidad entre diferentes sistemas de red

## Objetivos

- **Interoperabilidad**: Permitir que diferentes sistemas de red se comuniquen entre sí
- **Estandarización**: Proporcionar un marco común para el diseño y desarrollo de protocolos de red
- **Facilidad de diagnóstico**: Ayudar en la identificación y resolución de problemas de red

### Principios

Estos principios sirven para estructurar, diseñar y comprender las redes de manera modular y estandarizada. Fueron fundamentales para la creación del modelo

1. Una capa debe ser creada donde se requiera un diferente nivel de abstracción
2. Cada capa debe realizar una función bien definida
3. La función de cada capa debe ser elegida teniendo en cuenta la definición de protocolos estandarizados internacionales
4. Las fronteras entre las capas deben ser elegidas para minimizar el flujo de información en las interfaces
5. El número de capas debe ser:
    1. Grande para que funciones diferentes no caigan por necesidad dentro de la misma capa, pero. 
    2. Lo suficiente pequeño para que la arquitectura sea manejable

Teniendo en cuenta todo lo anterior se crea el modelo de 7 capas

> [!tip] 
> Aprendetelo de memoria bro

## Modelo OSI

Es esencial no solo en el tema de redes, sino también en toda el área de comunicaciones. Es crucial entenderlo y asociarlo debido a su presencia constante en estas áreas

![](https://i.imgur.com/BS87ryU.png)


*EJEMPLO*
Un dispositivo celular llega hasta la capa de aplicación, por el realiza todas las funciones desde la capa de aplicación hasta la capa física

Esto lo convierte en un dispositivo más inteligente en comparación con otros que solo alcanzan capas inferiores

La inteligencia del sistema se define por las funciones disponibles en cada etapa, siendo la 7 la más alta y compleja

### Pequeños datos

- Después de la capa 7 (aplicación) tenemos a la capa 8 (usuario)

- Antes de la capa 1 (físico) tenemos a la capa 0 (medio) que por ejemplo redes inalámbricas es el aire

**INFRAESTRUCTURA DE RED**
- Esta abarca hasta la capa 3 que es la capa de red, incluyendo las capas 1 (física) y 2 (enlace de datos).

- Todo lo de esta capa no comparte recursos solo es necesario para generar la estructura en sí

**PROCESOS Y SERVICIOS SOFTWARE**
- Desde la capa 4 (transporte) hasta la capa 7 (aplicación) se habla sobre  


## 1. Capa Física
Funciones específicas como la modulación de señales, sincronización de bits y gestión de la señalización. Esencial para el funcionamiento de la red

- Encargada de transmitir bits a través de un canal de comunicación mediante unos y ceros

- La codificación de los datos es importante para la correcta interpretación de los bits transmitidos. Diferentes esquemas pueden ser usados para optimizar la transmisión

- Hace usos de medios físicos

- Diferentes medios: cables de cobre, fibra óptica, señales inalámbricas

- La elección del medio afecta la velocidad y calidad de transmisión

- Se consideran interfaces mecánicas y eléctricas, cruciales para conexión y comunicación entre dispositivos

- Factores que influyen en la calidad de la señal son niveles de voltaje y potencia en la transmisión de datos


## 2. Capa de Enlace de Datos
Esencial para la comunicación efectiva entre dispositivos implementando agrupación de datos o "frames"

> [!warning]
> Los paquetes en esta capa se los conocen como "frames" o "tramas", después del medio físico esta trama tendrá una cabecera y una terminación

- Ya con los unos y ceros, aquí se transforma el canal crudo en un enlace libre de errores de transmisión

- Los datos se organizan en unidades llamadas "tramas" (frames). Contienen datos, información de control como direcciones de origen y destino y datos de verificación para detectar errores

- Se implementan mecanismos para detectar errores como, códigos de verificación y técnicas de retransmisión

- Puede hacer un control de flujo de datos para evitar la saturación de la red con mecanismos como "control de ventana" para regular la cantidad de datos que se pueden enviar antes de recibir una confirmación

- En redes por difusión, resuelve el acceso al medio (revisar el modelo TCP/IP para más detalle)


## 3. Capa de Red
Aquí ya se controla tienen las infraestructuras de red de diferentes tipos, y se permite el control de estas, la interconexión de redes (Router)

- **Encargada de entregar de paquetes** entre dispositivos en diferentes redes. Se asegura que los datos lleguen a su destino a través de múltiples redes interconectadas

- Ya se usan las direcciones IP para identificar de manera única a cada dispositivo en la red.

- Las direcciones IP permiten el enrutamiento de paquetes a través de diferentes redes, facilita la comunicación para dispositivos que no están en la misma red

- **Responsable del "enrutamiento"** que es determinar la mejor ruta para que los datos lleguen a su destino. Routers dispositivos clave

- **Protocolos importantes** como IP, ICMP (Internet Control Message Protocol) para gestión de errores y control de comuni. y ARP (Addres Resolution Protocol) para la resolución de direcciones IP a direcciones MAC

- Maneja la fragmentación y el reensamblado de paquetes grandes en unidades pequeñas en redes con un tamaño máximo de paquete (MTU) limitado

- Maneja la interconexión de redes de forma heterogénea, o sea que gestiona la comunicación entre diferentes tipos de redes y tecnologías


> [!info] A partir de aquí para arriba es posible identificar el tipo de servicio que se está enviado

## 4. Capa de Transporte

- Entrega datos a la capa superior en unidades menores si es necesario

- Protocolos principales en esta capa
    - **TCP (Transmission Control Protocol):** Orientado a la conexión garantizando la entrega de datos, controla el flujo de datos y asegura que los paquetes lleguen en orden correcto retransmitiendo aquellos perdidos 
    - **UDP (User Datagram Protocol):** No orientado a la conexión, permite la transmisión rápida de datos sin garantías de entrega en confiabilidad. Útil para streaming de video o juegos en línea

- **Multiplexado**: Puede gestionar múltiples flujos de datos de diferentes aplicaciones simultáneamente *usando puertos para identificar cada conexión*

- Determina el tipo de servicio que reciben las capas superiores

- Es la primera capa punta a punta en la comunicación, o sea se ocupa directamente de la conexión entre los dispositivos finales (hosts) sin importarle nodos intermedios

- Control de flujo para evitar saturación mediante el uso de ventanas deslizantes y confirmaciones

- Direccionamiento entre procesos usando puertos para identificar aplicaciones específicas en un dispositivo


## 5. Capa de Sesión
Bastante difícil de definir por ser procesos realizando de forma oculta del usuario pero necesarios para mantener la comunicación adecuada

Encargada de establecer, mantener y terminar sesiones de comunicaciones entre diferentes aplicaciones en diferentes dispositivos

- **Gestiona el control de diálogo entre las aplicaciones**, permitiendo que se realicen comunicaciones;
    - En ambas direcciones (full-duplex)
    - O en una sola dirección (half-duplex)
    - Necesario para coordinar el flujo de info. y evitar confusiones en la comuni.

- Proporciona mecanismos de sincronización para asegurar que, las apps. Estén alineadas durante la comunicación
    - Incluye gestión de puntos de control
    - Recuperación de sesiones en caso de interrupciones

- Usa Tokens para controlar el acceso a recursos compartidos durante la comuni. Importante cuando varios usuarios tratan de acceder al mismo recursos simultáneamente

- Recuperación de errores si se producen errores en la comuni. Esta puede reiniciar la comuni. Desde el último punto de control minimizando la perdida de datos

- Establece sesiones que es negociar parámetros de autenticación entre los participantes, así solo apps autorizadas se comunican entre sí

- Termina sesiones asegurándose que todos los recursos se liberen de forma normal sin conexiones abiertas innecesarias.


## 6. Capa de Presentación
Se encarga de traducir los datos entre el formato usado por la aplicación y el formato que puede ser transmitido a través de la red. En resumen se asegura que sean datos comprensibles para la app receptora

- Realiza la conversión de diferentes formatos de datos incluyendo la codificación y decodificación de datos permitiendo que diferentes sistemas y apps se comuniquen sin problemas
    - Formato de datos como texto, imágenes, audio y video

- Se encarga de resolver las "Diferencias Sintácticas" (Estructura de datos) y "Semánticas" (Significado de los datos) entre las apps que se comunican. Se interpreta bien la fino en ambos extremos de la comuni.

- Se pueden mencionar estándares o protocolos como XDR (External Data Representation) y ASN.1 (Abstract Syntax Notation One), que son utilizados para la representación de datos en esta capa.

> [!warning] Little-endian MSB primero vs Big-endian LSB primero
> Es todo un tema aparte, pero tiene que ver con este tema, cacharlo despues

## 7. Capa de Aplicación
Esta ya proporciona la interfaz entre las aplicaciones del usuario y la red. Su objetivo es facilitar la comuni. y intercambio de datos entre apps de diferentes dispositivos.

Permite que los usuarios interactúen con los servicios de la red

Protocolos de aplicación general: terminal virtual, transferencia de archivos, mensajería, etc.

1. **Protocolos de Capa de Aplicación**: Se mencionan varios protocolos importantes que operan en esta capa, como:
    
    - **HTTP (Hypertext Transfer Protocol)**: Utilizado para la transferencia de páginas web.
        
    - **FTP (File Transfer Protocol)**: Utilizado para la transferencia de archivos entre sistemas.
        
    - **SMTP (Simple Mail Transfer Protocol)**: Utilizado para el envío de correos electrónicos.
        
    - **DNS (Domain Name System)**: Utilizado para la resolución de nombres de dominio a direcciones IP.


## Paquetería total del OSI

![](https://i.imgur.com/mglO5Gh.png)

La paquetería se refiere al proceso de dividir los datos en unidades más pequeñas, conocidas como paquetes o tramas, para su transmisión a través de la red.

Cada paquete o trama tiene una estructura específica que incluye una cabecera y un cuerpo. La cabecera contiene información de control y otros datos necesarios para la entrega. El cuerpo del paquete contiene los datos reales que se están transmitiendo.

la paquetería puede generar ciertas complicaciones, como la necesidad de gestionar múltiples cabeceras y la posibilidad de que los paquetes lleguen fuera de orden

> [!error] Este modelo OSI no tiene ninguna tecnología implementada

___

## Modelo TCP/IP

Existe dos variantes de este modelo
- TCP/IP Puro donde se compone de 4 capas
- TCP/IP Hibrido compuesto por 5 capas

## TCP/IP Hibrido
En este 