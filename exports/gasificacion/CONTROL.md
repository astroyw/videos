# Control de entrega

- MP4 H.264, 1080×1920, 30 fps, 900 cuadros decodificados, duración 30.000 s.
- Pixel format yuv420p, rango limitado BT.709, faststart.
- Audio AAC estéreo a 48 kHz: narración sintética argentina y efectos de HyperFrames.
- Subtítulos incrustados y SRT por frase, sincronizados con las duraciones de audio medidas.
- Decodificación de video y audio completa sin errores de FFmpeg.
- Diferencias de imagen comprobadas dentro del área central de cada una de las seis escenas: no son diapositivas estáticas.
- Capturas de las seis escenas revisadas visualmente. Tipografía, subtítulos y diagramas dentro de márgenes conservadores para interfaces de redes.
- HyperFrames: lint/runtime/layout/motion/craft sin errores ni advertencias (canvas sin texto, por eso no hay evaluación de contraste allí). TypeScript de Remotion sin errores.
- Audio final medido aproximadamente a −16.6 LUFS, sin saturación. No se realizó una escucha humana del audio; la voz proviene de TTS y los intervalos se midieron sobre los archivos generados.

Acompañar la redistribución con los créditos de voz y efectos adjuntos.
