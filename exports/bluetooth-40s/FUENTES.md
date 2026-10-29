# Fuentes y alcance de la explicación

Consultadas el 29 de octubre de 2026 desde los archivos públicos del proyecto ESP-IDF de Espressif:

| Fuente | Contenido utilizado |
| --- | --- |
| [Bluetooth architecture — overview](https://github.com/espressif/esp-idf/blob/master/docs/en/api-guides/bt-architecture/overview.rst) | PHY en la banda ISM de 2,4 GHz; baseband, temporización, salto de frecuencia y paquetes; descubrimiento y establecimiento de conexión. |
| [Bluetooth Classic GAP API](https://github.com/espressif/esp-idf/blob/master/docs/en/api-reference/bluetooth/esp_gap_bt.rst) | Descubrimiento, emparejamiento y gestión de conexiones. |
| [A2DP API](https://github.com/espressif/esp-idf/blob/master/docs/en/api-reference/bluetooth/esp_a2dp.rst) | Audio desde una fuente como un teléfono hacia un receptor como auriculares; recepción de audio y salida I2S en los ejemplos. |
| [GAP API header — esp_bt_gap_set_afh_channels](https://github.com/espressif/esp-idf/blob/master/components/bt/host/bluedroid/api/include/api/esp_gap_bt_api.h) | Clasificación de canales AFH, incluido el marcado de canales malos. Sustenta la ilustración de exclusión de un canal, sin reproducir una secuencia real del controlador. |

Los archivos se leyeron mediante raw.githubusercontent.com; no se atribuye la consulta a una página web que no se abrió. Las rutas apuntan a una rama que puede evolucionar. Los hashes de las versiones leídas figuran en `fuentes-hashes.json`.

## Simplificaciones intencionales

- Se muestra el caso cotidiano de audio entre celular y auriculares y el primer emparejamiento. Equipos ya emparejados pueden reconectarse; no necesitan repetir ese paso cada vez.
- Bluetooth incluye diferentes modos y perfiles, incluido LE Audio. No se afirma que todo Bluetooth use A2DP ni un codec específico.
- Los datos del audio se representan por paquetes y unos bits ilustrativos, no por una captura de tráfico real.
- Cinco líneas muestran el concepto de canales. **No representan la cantidad total de canales ni sus frecuencias exactas**. Los saltos y tiempos están ralentizados; las curvas que enlazan líneas son un recurso gráfico, no barridos físicos de frecuencia.
- La reducción de interferencias no garantiza una conexión perfecta. La secuencia adaptativa dibujada no reproduce un algoritmo concreto ni valores de rendimiento.
- «Coordinan cuándo transmitir y cuándo escuchar» no significa que ambos transmitan simultáneamente. Las luces indican coordinación conceptual.
- La comunicación Bluetooth local no necesita internet. Una aplicación de streaming sí puede requerir internet para obtener la música; son enlaces distintos.
- Las ondas de radio y de sonido están diferenciadas por contexto y color. El sonido se produce en el auricular después de recibir y procesar datos, no viaja por el aire como audio acústico desde el teléfono.

Los diagramas son una explicación conceptual, no una simulación electromagnética, prueba de cobertura ni medición de velocidad. No se reutilizaron dibujos, logos ni audio de las referencias.
