# Verificación — semáforos

- Render final: 1080×1920, 60/1 FPS, 3600 cuadros; duración 60.110000 s.
- H.264, yuv420p, BT.709, AAC 48 kHz; MP4 con faststart.
- Decodificación completa con FFmpeg `-xerror`: pasó.
- Audio medido sobre el MP4 final: -14.27 LUFS; pico de muestras -1.11 dBFS; pico verdadero -1.09 dBTP. Objetivo −14 LUFS ±0,5, pico máximo −1 dBFS: pasó. La primera exportación dio −14,52 LUFS y se corrigió sin recodificar la imagen.
- TypeScript: `npm run check`, pasó.
- HyperFrames: lint y runtime sin errores; layout sin errores. Craft informa tramos aparentemente inmóviles y ausencia de voz en el clip aislado. La animación está en Canvas y la voz se añade durante la composición. No se presenta craft como aprobación artística. Su prueba de contraste no evaluó texto (0 elementos).
- Revisión visual de 20 fotogramas del MP4, uno por pulso narrativo: subtítulos centrados arriba, etiquetas sin superposición, sin título fijo ni números de escena. La hoja de contacto corresponde a la misma pista de imagen, anterior al ajuste final exclusivo de audio.
- Movimiento: 120 muestras del clip animado; 119/119 pares sucesivos con cambio RGB medio mayor que 0,1. Esto verifica animación real muestreada, no calidad de cada transición.
- Alineación: 44 bloques, 136 palabras; tiempos fonémicos del mismo pase de síntesis. Voz sintética Piper Daniela es_AR. No se realizó escucha humana; naturalidad y pronunciación quedan sujetas a revisión del usuario.

Alcance científico: cruce simplificado; el intervalo de todos en rojo, los sensores y la coordinación se describen como posibilidades. Los tiempos visuales no son parámetros reales de ingeniería. Fuentes y licencias en el proyecto editable.
