# Networking

## OSI Model
El modelo OSI (Open Systems Interconnection) es un modelo conceptual que describe cómo se realiza la comunicación entre sistemas de computadoras en una red. Fue desarrollado por la Organización Internacional de Normalización (ISO) en la década de 1980.

El modelo OSI se organiza en siete capas, cada una de las cuales representa una función específica relacionada con la comunicación de datos. Estas capas son:

Capa física: Esta capa se encarga de la transmisión física de los bits a través de medios de comunicación como cables, fibra óptica o señales inalámbricas.

Capa de enlace de datos: Aquí se establece una conexión confiable y libre de errores entre nodos adyacentes. Se encarga de la detección y corrección de errores, así como del control de flujo y acceso al medio.

Capa de red: Esta capa se ocupa del enrutamiento de los datos a través de la red, seleccionando la mejor ruta para enviar los paquetes de datos entre diferentes redes. También se encarga de la segmentación y reensamblaje de paquetes.

Capa de transporte: En esta capa se proporciona un transporte confiable y sin errores de los datos. Se segmentan los datos en unidades más pequeñas y se reensamblan en el destino. También se encarga de la detección y corrección de errores a nivel de transporte.

Capa de sesión: Aquí se establecen, administran y finalizan las conexiones entre las aplicaciones en sistemas de origen y destino. Permite la sincronización y el control del diálogo entre las aplicaciones.

Capa de presentación: Esta capa se encarga de la representación de los datos, definiendo el formato en el que se transmiten los datos entre las aplicaciones. También se ocupa de la compresión y encriptación de los datos.

Capa de aplicación: Es la capa más cercana al usuario final y proporciona servicios de red a las aplicaciones. Aquí es donde se encuentran las aplicaciones de usuario final, como navegadores web, clientes de correo electrónico, servicios de transferencia de archivos, etc.

![Imgur](https://imgur.com/fCfXdSY)

## LAN, WAN, Internet
__LAN__ (Red de Área Local): Una LAN es una red de computadoras que se limita a un área geográfica pequeña, como una casa, una oficina o un campus. Se utiliza para la comunicación y el intercambio de recursos entre dispositivos cercanos.

*Uso típico*: Las LAN se utilizan en entornos locales, como hogares u oficinas, para compartir archivos, impresoras, conexión a Internet, juegos en red, etc.

*Tamaño geográfico típico*: El tamaño de una LAN generalmente abarca desde unos pocos metros hasta unos pocos kilómetros.

__WAN__ (Red de Área Amplia): Una WAN es una red que abarca una gran área geográfica, como un país, continente o incluso a nivel global. Se utiliza para conectar redes locales entre sí.

*Uso típico*: Las WAN se utilizan para establecer comunicación entre ubicaciones distantes, como sucursales de una empresa, permitiendo compartir datos, voz y video a través de una infraestructura de red amplia.

*Tamaño geográfico típico*: Las WAN pueden abarcar distancias largas, desde unos pocos kilómetros hasta miles de kilómetros o más.

__Internet__: Es una red global de redes interconectadas que permite la comunicación y el intercambio de información a nivel mundial. Es una red pública masiva basada en el protocolo TCP/IP y ofrece una amplia gama de servicios como correo electrónico, navegación web, transferencia de archivos, entre otros.

*Dirección IP de la red*: La dirección IP de la red, también conocida como dirección IP pública, es la dirección que identifica a toda una red en Internet. Cada red conectada a Internet tiene una dirección IP única que se utiliza para enrutar el tráfico de datos entre diferentes redes. Esta dirección se asigna al enrutador o al dispositivo que conecta la red local a Internet.

*Dirección IP del dispositivo (IP de host)*: La dirección IP del dispositivo, también conocida como dirección IP de host, es una dirección única asignada a cada dispositivo dentro de una red. Cada dispositivo conectado a una red, ya sea una computadora, un teléfono inteligente u otro dispositivo, tiene su propia dirección IP de host. Esta dirección se utiliza para identificar y comunicarse con un dispositivo específico en la red.

*Localhost*: Localhost es un nombre de dominio reservado que se utiliza para hacer referencia a la dirección IP de loopback de la máquina local. En otras palabras, localhost se refiere a la dirección IP de tu propia máquina. Cuando accedes a localhost, estás accediendo a los servicios y recursos alojados en tu propia máquina local.

*Dos tipos de direcciones IP: IPv4 e IPv6*
IPv6 se creó para abordar el agotamiento de las direcciones IPv4 y proporcionar un espacio de direcciones más amplio debido al crecimiento exponencial de dispositivos conectados a Internet. IPv6 utiliza direcciones más largas (128 bits) en comparación con IPv4 (32 bits) para permitir un mayor número de direcciones disponibles para futuras expansiones de Internet.

*Una subnet (subred)*: es una división lógica de una red IP más grande en subredes más pequeñas. En otras palabras, es una forma de particionar una red en segmentos más pequeños para mejorar la administración y la eficiencia en el enrutamiento de paquetes.

![Imgur](https://imgur.com/YoPow3h)

## MAC and IP address

### Similitudes:

Ambas son identificadores únicos utilizados en las redes de computadoras.
Ambas se utilizan para facilitar la comunicación entre dispositivos en una red.

### Diferencias:

*Dirección MAC*: Es un identificador único a nivel de enlace de datos asignado a una tarjeta de interfaz de red (NIC) de un dispositivo. Es una dirección física y está asociada a nivel de hardware. La dirección MAC es asignada por el fabricante y es estática, es decir, no cambia.

*Dirección IP*: Es un identificador único asignado a un dispositivo de red en la capa de red. Es una dirección lógica y está asociada a nivel de software. La dirección IP puede ser asignada de manera estática o dinámica, y puede cambiar en función de la configuración de red.

La dirección MAC se utiliza para la comunicación dentro de una red local y es utilizada en la capa de enlace de datos, mientras que la dirección IP se utiliza para la comunicación entre redes y es utilizada en la capa de red.

La dirección MAC se utiliza para el direccionamiento a nivel de enlace, es decir, para identificar dispositivos específicos dentro de la misma red local, mientras que la dirección IP se utiliza para el direccionamiento a nivel de red, es decir, para identificar redes y dispositivos dentro de esas redes.

## UDP and TCP
UDP (User Datagram Protocol) y TCP (Transmission Control Protocol) son dos protocolos de comunicación utilizados en redes de computadoras para transmitir datos de manera confiable y eficiente. Ambos protocolos operan en la capa de transporte del modelo TCP/IP.

*UDP* es un protocolo de transporte sin conexión. Esto significa que no se establece una conexión antes de enviar datos y no hay garantía de entrega o reordenamiento de los paquetes.
UDP es rápido y eficiente, ya que no tiene la sobrecarga de establecer y mantener una conexión.
Se utiliza para aplicaciones donde la velocidad es más importante que la confiabilidad, como en transmisiones en tiempo real, videojuegos en línea o servicios de transmisión multimedia.
UDP no tiene mecanismos incorporados para controlar la congestión y los errores, lo que puede resultar en la pérdida de paquetes o paquetes duplicados.

*TCP* es un protocolo de transporte orientado a la conexión. Antes de enviar datos, se establece una conexión entre el emisor y el receptor, y se garantiza la entrega ordenada y confiable de los paquetes.
TCP es más lento que UDP debido a la sobrecarga adicional de establecer y mantener la conexión, y realizar el control de flujo y la corrección de errores.
Se utiliza para aplicaciones que requieren una entrega confiable de los datos, como transferencia de archivos, navegación web, correo electrónico y cualquier aplicación donde se necesite garantizar la integridad de los datos.
TCP incluye mecanismos de control de congestión y retransmisión de paquetes para asegurar una entrega confiable y eficiente.


## The Internet Control Message Protocol (ICMP)
El Protocolo de Mensajes de Control de Internet es un protocolo de la capa de red del modelo TCP/IP que se utiliza para enviar mensajes de control y errores entre dispositivos de una red. ICMP es parte integral del funcionamiento y la gestión de las redes IP.

El objetivo principal de ICMP es proporcionar información sobre la conectividad y el estado de los dispositivos en una red IP.
