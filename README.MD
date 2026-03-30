Analisis de red local con Nmap y Wireshark

Objetivo:
Analizar una red local para identifica puertos abiertos, servicios activos y trafico de red.

Herramientas utilizadas:
-Kali Linux
-Nmap
-Wireshark

Escaneo con Nmap

Se realizo un escaneo rapido al router:

Comando: 
-Nmap -sS 192.168.0.1

Resultados:
-53/tcp -> open -> DNS
-80/tcp -> open -> HTTP
-443/tcp-> open -> HTTPS
-22/tcp -> filtered -> SSH
-23/tcp -> filtered -> Telnet

'/home/kali/Desktop/network-analysis-lab/screenshots/Evidencia Nmap.png' 

Analisis de Wireshark

DNS:
Se observo una consulta DNS a: 
api.github.com

Respuesta:
api.github.com -> 34.160.144.191

Trafico HTTPS

se detecto trafico TCP hacia:
34.160.144.191:443

incluyendo;

SYN
ACK
FIN / RST

'/home/kali/Desktop/network-analysis-lab/screenshots/Evidencia DNS.png' 

Concluciones:

-Se identificaron servicios activos en el router
-Se analizo el proceso completo de resoluciones DNS
-Se observo trafico cifrado mediante HTTPS
-Se comprendio el flujo de comunicacion en una red real

Aprendizajes:

-Se uso Nmap para escaneo de puertos
-Interpretacion de estados
-Analisis de trafico con Wireshark
-Funcionamiento del protocolo DNS

Autor:
Brown Tomas
