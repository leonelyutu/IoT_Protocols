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
El rRPC es un patron de ejecución remota de procedimientos donde un agente, llamado "Callee", comunica al Router que proporiona un cierto procedimiento 
