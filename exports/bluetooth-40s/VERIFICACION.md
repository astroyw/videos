# Verificación del Reel de Bluetooth

29 de octubre de 2026. Linux, Node.js 24.19.0, npm 11.9.0, Chromium y FFmpeg/FFprobe 7.1.5.

## Archivo final

- `como-funciona-el-bluetooth.mp4`: 3,502,985 bytes.
- 40.000 segundos, 1200 cuadros, 1080×1920, 30 FPS nominales y promedio.
- H.264, yuv420p, BT.709, rango limitado y faststart.
- Ninguna pista de audio.
- SHA-256: `a692fb92f667d8820cd58aea09a9c458bfaa83ae2c4960abc6978ec3d5ac44c1`.

## Pruebas

- Instalación desde lockfiles de Remotion y HyperFrames; TypeScript y guion sin errores.
- Los 14 subtítulos coinciden con el guion. SRT y subtítulos incrustados usan la misma fuente de textos e intervalos.
- HyperFrames: check de lint/runtime/layout; 300 muestras de movimiento y 15 comprobaciones de contraste aprobadas. Mundo SVG de 40 s renderizado a 1080×820, integrado a tamaño nativo en el lienzo final.
- Render completo de Remotion. FFprobe y decodificación completa con FFmpeg aprobados.
- Inspección de muestras del MP4, título completo, márgenes, CTA y ausencia de numeración.
- Revisión de secuencias cada 0,1 s alrededor de 12, 14, 18, 21, 25, 30, 33 y 37 s. Se corrigió la superposición temporal de etiquetas del gráfico, decodificación y enlace local, y se volvió a renderizar.
- Medición de los 1200 cuadros del área de animación, excluyendo título y subtítulos: pico de diferencia absoluta media entre cuadros consecutivos de 1.418/255, sobre imágenes reducidas a 108×70. Datos en `continuidad.json`.

## Continuidad y límites

El montaje contiene un solo clip de 40 s, con los mismos objetos persistentes, y una pista de subtítulos independiente. Hay cero cortes de montaje entre escenas; los cambios de frase no desmontan el mundo. Se revisaron secuencias de cuadros, no una reproducción humana completa. La medición de píxeles no certifica por sí sola fluidez ni exactitud técnica.

El esquema simplifica canales, tiempos y transmisión. Las fuentes consultadas y matices se registran en FUENTES.md. La comunicación Bluetooth local no necesita internet; una aplicación de streaming puede requerirlo.

Código ejecutado en Linux; Windows/macOS no se probaron. No se generaron voces, música ni efectos sonoros.
