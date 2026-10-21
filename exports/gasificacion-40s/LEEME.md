# Gasificación: 40 segundos, 14 partes, sin voz

Entrega: `gasificacion-40s-sin-voz.mp4`.

- 1080 × 1920, vertical 9:16, 30 FPS, 1200 cuadros, 40.000 segundos.
- MP4 H.264, yuv420p, BT.709, faststart.
- Sin numeración de slides ni contador de partes en pantalla.
- Sin pista de audio: no hay narración, música ni efectos sonoros, para facilitar la incorporación de voz en edición.
- Subtítulos incrustados; `subtitulos.srt` contiene los mismos textos con sus tiempos.
- `guion-y-tiempos.json` organiza los 14 intervalos para grabar una narración propia. Esos tiempos corresponden al montaje silencioso, no a una locución ya grabada.

## Producción

Remotion compone y renderiza las 14 escenas animadas. El acercamiento molecular utiliza un clip generado y validado con HyperFrames. Tipografía Manrope (SIL OFL), diagramas originales. No se utilizan los audios de la versión anterior.

La bebida fría y la alta presión parcial de CO₂ favorecen la disolución. El llenado a contrapresión y el cierre reducen las pérdidas de gas. La apertura reduce la presión, dejando un líquido sobresaturado; la nucleación facilita la aparición de burbujas, que crecen por difusión del gas y suben por flotación. Las moléculas y burbujas se representan esquemáticamente, sin escala real.

## Fuentes

`examples/remotion/src/Carbonation40.tsx` y `gasificacion40.json`. `npm run deliver:gasificacion40` reproduce el máster y la entrega. La versión anterior de 30 segundos se conserva sin reemplazar.
