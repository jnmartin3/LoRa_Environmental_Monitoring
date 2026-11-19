# LoRa_Environmental_Monitoring
Proyecto de transmisión de datos ambientales con módulos ESP32 y LoRa

_**Resultados del proyecto de fin del Taller**_ de hardware científico abierto para investigación y enseñanza de las ciencias dictado por la Facultad de Ciencias Exactas y Naturales de UNCuyo.

Programa y especificaciones del curso: https://fcen.uncuyo.edu.ar/upload/53dca227cc5fa8029f1ee1e3afade1f2.pdf

Docentes: Pablo Cremades, Fernando Castro, Fabricio Cano.

_Problemática abordada_

El monitoreo ambiental en zonas remotas donde la disponibilidad de redes WiFi o telefonía celular es limitada, se hace necesario instalar redes de comunicación propias, de relativo bajo costo y confiables.

La opción del almacenamiento in situ en memorias SD, con recuperación periódica, es posible pero no permite monitorear el tiempo real una cantidad de puntos de monitoreo.

_Oportunidad_

Los datos a ser transmitidos se limitan a cadenas de caracteres alfanuméricos que representan valores de variables ambientales (temperaturas, humedad, material particulado PM, velocidad y dirección de viento, entre otras). 

Por esta razón la tecnología de radios LoRa es una opción interesante en ámbitos rurales o rur-urbanos, con alcances probados de varias decenas de kilómetros en condiciones favorables.

_Desarrollo propuesto_

A través del uso de radios LoRa se implementa el núcleo de la comunicación desde los sitios de monitoreo (Emisores) hasta el sitio de registro final con comunicación a WiFi (Receptor). Se implementa una estación intermedia como Repetidora. 

El hardware de comunicación utilizado son módulos [XIAO ESP32S3 con radios LoRa SX1262 de SeedStudio](https://wiki.seeedstudio.com/wio_sx1262_with_xiao_esp32s3_kit_class/) y módulos [HELTEC V4](https://heltec.org/project/wifi-lora-32-v4/).

Las variables ambientales a monitorear son inicialmente, y a modo de primeras pruebas, temperatura del aire y presión barometrica (BMP 180), temperatura de agua (DS18B20) y velocidad de viento (Lambrecht serie 00.14574). Se implementa la electrónica para este proyecto en placas protoboard y alimentación con baterias externas o power banks. Se utilizan antenas estándar de las radios LoRa.
