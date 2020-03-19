# Protocolo MQTT
MQ Telemetry Transport, **es un protocolo de comunicación M2M (Machine to Machine) de tipo message queue.**

Esta **basado en la pila TCP/IP** como base para la comunicación. En el caso del MQTT cada conexión se mantiene abierta y se "reutiliza" en cada comunicación. Es una diferencia por ejemplo a una petición HTPP 1.0 donde cada transmisión se realiza a través de la conexión.

## Funcionamiento del MQTT
Es **Es un servicio de mensajeria push con patrón publicador/suscriptor (pub-sub)**. En esta infraestructura los clientes se conectan con un servidor dentral denominado Broker.

Para filtrar los mensajes que son nviados a cada cliente **Los mensajes se disponen en topics organizados jerárquicamente.** Un cliente puede publicar un mensaje en un determinado topic. 

Los clientes inician una conexión TCP/IP con el broker, el cual mantiene un registro de los clientes conectados. Esta conexión se mantiene abierta hasta que el cliente la finaliza. Por defecto, MQTT emplea el puerto 1883 y 8883 cuando funciona sobre TLS (Transport Layer Security).

