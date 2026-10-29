# Verificación de la entrega

29 de octubre de 2026. Linux, Node.js 24.19.0, npm 11.9.0, Chromium y FFmpeg/FFprobe 7.1.5.

## Resultado medido

- Archivo: `como-se-hace-una-ventana.mp4`.
- Tamaño: 2.530.467 bytes.
- Duración: **40.000 segundos**.
- Resolución: **1080 × 1920**; relación 9:16.
- FPS: **30/1**, tanto nominal como promedio; **1200 cuadros decodificados**.
- Codec: H.264; formato de píxel yuv420p; color BT.709, rango limitado; faststart.
- Audio: **ninguna pista**.
- SHA-256: `74be00e38f1c9e196f34e8d27419fa60333049bd03681982d680327d3cc85b74`.

## Pruebas realizadas

- Instalación del proyecto desde su lockfile con `npm ci`.
- TypeScript y comprobación de las 14 partes, duración total y CTA de 90 cuadros.
- Coincidencia de los 14 subtítulos entre el storyboard y `GUION.md`; SRT generado desde la misma fuente de tiempos y textos.
- Render completo de Remotion y conversión final a MP4. FFprobe y decodificación completa con FFmpeg sin errores.
- Inspección visual de un cuadro de cada parte del MP4 final: legibilidad, composición, diagramas y ausencia de números de slide.
- Revisión adicional en 0, 16,96, 17,00, 19,90, 36,96, 37,00 y 39,96 s: primer cuadro útil, transición interna de HyperFrames, diagonales terminando en A = B, cierre de la manija y CTA hasta el final.
- Dos muestras del área central del diagrama por escena: cambios detectados en **14 de 14**. Se excluyeron encabezados y subtítulos de esa medición.
- Segmento HyperFrames nuevo de 6 segundos: check, revisión de capturas, render, 180 cuadros, ausencia de audio y decodificación completa. Auditoría de movimiento con 121 muestras y contraste con 7 muestras aprobadas.

La comparación de muestras confirma cambios, pero no certifica automáticamente fluidez ni exactitud de fabricación. La revisión visual fue por cuadros, no una reproducción humana completa. No hay audio para evaluar por escucha.

## Alcance

Ventana de aluminio abatible, representada mediante esquemas. El procedimiento exacto varía según el sistema. El acceso a documentación externa del fabricante estuvo bloqueado; `FUENTES.md` registra esa limitación. No se muestra ni se afirma una certificación de laboratorio.

La composición y los scripts se ejecutaron en Linux. El proyecto usa rutas relativas y permite configurar el navegador; no se probaron Windows ni macOS en esta sesión.
