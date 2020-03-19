# Protocolo MQTT
MQ Telemetry Transport, **es un protocolo de comunicación M2M (Machine to Machine) de tipo message queue.**

Esta **basado en la pila TCP/IP** como base para la comunicación. En el caso del MQTT cada conexión se mantiene abierta y se "reutiliza" en cada comunicación. Es una diferencia por ejemplo a una petición HTPP 1.0 donde cada transmisión se realiza a través de la conexión.

## Funcionamiento del MQTT
Es **Es un servicio de mensajeria push con patrón publicador/suscriptor (pub-sub)**. En esta infraestructura los clientes se conectan con un servidor dentral denominado Broker.

Para filtrar los mensajes que son nviados a cada cliente **Los mensajes se disponen en topics organizados jerárquicamente.** Un cliente puede publicar un mensaje en un determinado topic. 

Los clientes inician una conexión TCP/IP con el broker, el cual mantiene un registro de los clientes conectados. Esta conexión se mantiene abierta hasta que el cliente la finaliza. Por defecto, MQTT emplea el puerto 1883 y 8883 cuando funciona sobre TLS (Transport Layer Security).

Para ello el cliente envía un mensaje **CONNECT** que contiene información necesaria (nombre de usuario, contraseña, cliente-id). El broker responde con un mensaje **CONNACK**, que contiene el resultado de la conexión (aceptada, rechazada, etc).

Para **enviar** los mensajes el cliente emplea mensajes PUBLISH, que contienen el topic y el payload.
Para **suscribirse y desuscribirse** se emplean los mensajes de ***SUBSCRIBE** Y **UNSUSCRIBE** el servidor responde con **SUBACK** Y **UNSUBACK**.
Para asegurar que la conexión está activa los clientes mandan periódicamente un mensaje **PINGREQ** que es respondido por el servidor con un **PINGRESP**. Finalmente, el cliente se desconecta enviando un mensaje **DISCONNECT**.

## CALIDAD DEL SERVICIO (QOS)
MQTT dispone de un **mecanismo de calidad de servicio o QoS**, entendiendo la forma de gestionar la robustez del envío de mensajes al cliente ante fallos (por ejemplo de conectividad).
**MQTT tiene tres niveles QoS posibles
**Qos 0 unacknowledged (at most one):** El mensaje se envía una única vez. En caso de fallo por lo que puede que alguno no se entregue.
**QoS 1 acknowledged (at last one)**: El mensaje se envía hasta que se garantiza la entrega. En caso de fallo, el suscriptor puede elegir algún mensaje duplicados.

**QoS 2 (Exactly one)**: Se garantiza que cada mensaje se entrega al suscriptor y únicamente una vez.



