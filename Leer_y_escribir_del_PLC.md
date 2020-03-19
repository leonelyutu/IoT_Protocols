# LEER Y ESCRIBIR DESDE EL PLC
## OBJETIVOS
*Enviar mensajes de alarma por Telegram
*Usar protocolos MQTT

## Introducción
La gama **M221, M241, M251** no tiene conectividad con la nube, y para ello se necesita de una **Edge Box de Schneider**
La gama **M262** se conecta directamente a la nube **Machine Advisor**, no necesita Edge Box.
Para ver la funcionalidad de Edge Box, se usará y se harán pruebas mediante una Raspberry Pi, el efecto es similar. La diferencia es que con **Edge Box** la seguridad aumenta, debido a la compatibilidad con el equipo y soporte de Schneider-

### Configurando los dispositivos
Definir las siguientes IPs

* PLC **M241**: 192.168.1.58

* **Edge Box (Raspberry)** (Obtenida por DHCP al conectar este dispositivo al router mediante un patchcord, o bien por Wifi): 192.138.1.61


Esta dirección se usara posteriormente para interactuar con **node-red** mediante un explorador de internet.



