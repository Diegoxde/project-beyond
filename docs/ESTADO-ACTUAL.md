# Estado actual — Project Beyond v2

**Publicación:** v2  
**Dispositivo:** Samsung Galaxy Fit3 SM-R390  
**Firmware base:** R390XXU0AZA3  
**Estado:** experimental; probado por el desarrollador en un reloj real.

## Resultados reportados por Diego

| Módulo | Estado observado en el reloj |
|---|---|
| Galería y transferencia de fotos | Estables en las pruebas actuales. El desarrollador corrigió el problema que afectaba a las transferencias repetidas. |
| Cubo | Jugable. En ocasiones puede congelarse brevemente y continuar. Inspirado en Geometry Dash. |
| Teclado QWERTY | Funciona; ocasionalmente presenta un pequeño retraso o registra dos o tres teclas adicionales. |
| Launcher Apps extras | Responde mucho mejor que antes; pueden persistir fallos ocasionales al tocar o deslizar. |
| Táctil | Mejoró notablemente; los fallos son ahora poco frecuentes según las pruebas actuales. |
| Super Hex | Sigue inestable y no se recomienda jugarlo regularmente por ahora. Inspirado en Super Hexagon. |

Estos resultados reflejan pruebas reportadas en un reloj físico. Las pruebas de compilación, validación y host en PC son complementarias y no sustituyen las pruebas reales.

## Mejoras táctiles de v2

v2 se centra en mejorar la respuesta táctil del launcher, la Galería y el teclado. En las pruebas del desarrollador, los problemas táctiles que antes requerían muchos intentos son ahora poco frecuentes. La mejora no significa que todos los errores estén eliminados.

El teclado aún puede retrasarse un poco o registrar dos o tres teclas adicionales. Este comportamiento sigue pendiente de optimización.

## Galería y transferencia de fotos

El desarrollador informa que corrigió el problema que podía hacer que una segunda transferencia desde el HTML del PC reemplazara las fotos anteriores. La Galería y la transferencia de fotos se consideran estables según las pruebas actuales. Para fotos importantes, conserva también una copia en el PC.

## Problemas pendientes

1. Reducir los fallos táctiles ocasionales del launcher y mejorar la detección de deslizamientos.
2. Optimizar el teclado QWERTY para evitar retrasos y entradas duplicadas ocasionales.
3. Investigar las pausas breves que pueden ocurrir en Cubo.
4. Mejorar el rendimiento y la estabilidad de Super Hex.
5. Volver a probar las funciones en el reloj físico después de cada cambio.

## Componentes principales

- **Launcher:** `menu.inc.c`.
- **Galería:** `gallery.inc.c`; imágenes RGB565 bajo `/user/`.
- **Teclado:** `kbd_qwerty.c`.
- **Super Hex:** `superhex.inc.c`.
- **Cubo:** `runner.inc.c` y `runner_levels.inc`.

La función de música se retiró de la compilación al no estar demostrada una ruta A2DP Source funcional.

## Compatibilidad y seguridad

El objetivo es SM-R390 con firmware base R390XXU0AZA3. No se debe asumir compatibilidad con otras variantes o firmware. No instales si no puedes comprobar el paquete y disponer de un procedimiento de recuperación adecuado.

No uses comandos `FORMAT`, `SHIPMODE` ni `DELLBTADDR`. Consulta [Instalación y recuperación](./INSTALACION.md).
