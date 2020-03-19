# IoT_Protocols
IoT_Protocols_Implements_With_PLC

## Protocolo:
Un protocolo de comunicación es una serie de normas que definimos para que dos o mas dispositivos puedan comunicarse y entenderse.

## M2M:
Tipo de comunicacion Machine to Machine.

## Objetivos de los Protocolos
*Escalables
*Acoplamiento débil entre dispositivos
*Interoperatibilidad
*Gran número de comunicaciones simultaneas
*Seguridad incorporada
*Fácil acceso a dispositivos

## Externalización de la comunicación a un servicio de notificaciones centralizado
La solución que se plantea en este modelo es disponer de un servidor central que se encarga de recibir todos los mensajes de todos los dispositivos emisores y distribuirlos a los receptores, se llemara de forma generica *Router o *Brocker.

## Metodologías en IoT
### PUBLISH / SUSBCRIBE (PUBSUB)
Es un patrón de mensajería donde un agente, el "Subscriber", informa al Router que quiere recibir un tipo de mensjes. Otro agente, el "Publisher" pude publicar mensajes. El router distribuye los mensajes a los Subscribers.

### ROUTER REMODER PROCEDURE CALLS (RRPC)
El rRPC es un patron de ejecución remota de procedimientos donde un agente, llamado "Callee", comunica al Router que proporiona un cierto procedimiento. Otro agente, llamado "Caller", puede llamar a este procedimiento. El Router invoca el procedimiento en el Callee, recoge los resultados del proceso. y lo comunica al caller que lo ha invocado.

## INFRAESTRUCTURAS DE SERVICIOS EN IOT
### MESSAGE QUEUE
es este servicio de mensajeria de tipo Message Queue el Router *genera una cola de mensajes única para cada uno de los clientes* que inician la subscripción. El Router discrimina los mensajes empleando el identificador del cliente, aunque existen diversos mecanismos para distribuir multiples clientes.

Estas colas de mensajes de cliente *mantienen los mensajes reibidos hasta que son entregados al cliente*. De forma que si se recibe un mensaje cuando el cliente no esta conectado, se mantienen en el Router y son entregados cuando se conecta.

un ejemplo de Message Queue es una aplicación de mensajería de tipo Whatsapp o Telegram, donde el usuario recibe los mensajes que ha recibido mientras no estaba conectado. 

### MESSAGE SERVICE
Servicio de Mensajeria puro o Message Service. El Router Distribuye inmediatamente los mensajes a los clientes conectados. Los mensajes se filtran por algun criterio, como el tema o el contenido del mensaje.

A diferencia de un Message Queuem **Los mensajes entrewgados mientras el cliente esta desconectado de pierden.** Pero esto no significa que un servicio Message Service no pueda ser implementado con persistencia de datos, por ejemplo, para analítica, historicos o calidad de servicios.

Un ejempls de Message Services e sun chat, donde no podemos recuperar mensajes emitidos cuando no estabamos en la sala.

# PROTOCOLOS PARA IOT

* **MQTT (MQ TELEMETRY TRANSPORT):** Es un protocolo PubSub de Message Service que actúa sobre TCP. Destaca pro ser ligero, sencillo de implementar. Resulta apropiado para dispositivos de baja potencia como los que se frecuentan en IoT. Esta optimizado para el Routing activo de un gran número de clientes conectados de forma simultanea.

* **AMQP (ADVANCED MESSAGE QUEUING PROTOCOL):** Es un protocolo PubSub de Message Queue. está diseñado para asegurar la confiabilidad e interoperatibilidad. Está pensado para aplicaciones corporativas, con mayor rendimiento y redes de baja latencia. No resulta tan adecuado para aplicaciones de IoT con dispositivos de bajos recursos.



