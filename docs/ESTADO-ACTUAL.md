# Estado actual — Project Beyond

**Publicación prevista:** versión 1  
**Dispositivo:** Samsung Galaxy Fit3 SM-R390  
**Firmware base:** R390XXU0AZA3  
**Estado:** experimental; probado en un reloj real, con limitaciones conocidas.

## Resultados reportados por Diego

| Módulo | Estado observado en el reloj |
|---|---|
| Galería | Funciona, pero existe un error al transferir fotos por segunda vez desde el instalador HTML del PC: las nuevas reemplazan a las anteriores. |
| Cubo | Jugable. En ocasiones se congela aproximadamente medio segundo y continúa. Inspirado en Geometry Dash. |
| Teclado QWERTY | Experimental; todavía pierde algunos toques y es inconsistente para el uso diario. |
| Launcher Apps extras | Mejoró, pero a veces no registra el toque o se comporta mal al deslizar. |
| Táctil | Mejoró considerablemente; quedan retrasos ocasionales y muy pocos toques fantasma. |
| Super Hex | Sigue inestable y no se recomienda jugarlo actualmente. Inspirado en Super Hexagon. |

Estos son resultados reportados tras probar el paquete en un reloj físico. Las pruebas de compilación, validación y host en PC son complementarias y no sustituyen las pruebas reales.

## Navegación táctil: solución temporal observada

A veces, abrir una aplicación o tocar una tecla puede requerir entre 6 y 20 toques rápidos. Si el toque no produce respuesta, el desarrollador ha observado que apagar y volver a encender la pantalla puede hacer que aparezca la sección que se había tocado. También ha funcionado con el teclado.

Es una solución temporal, no una corrección definitiva. El desarrollador también observa que la respuesta podría parecer mejorar después de un tiempo de uso, pero no está confirmado que el sistema se adapte al toque.

## Problemas pendientes

1. Mejorar el registro de toques en el launcher y distinguir correctamente toques y deslizamientos.
2. Corregir la entrada táctil del teclado QWERTY.
3. Investigar por qué la segunda transferencia de fotos reemplaza las imágenes anteriores en vez de añadirlas.
4. Mejorar la estabilidad de Cubo y resolver los problemas que hacen que Super Hex no sea recomendable.
5. Volver a probar todas las funciones en el reloj tras cada cambio.

## Componentes principales

- **Launcher:** `menu.inc.c`.
- **Galería:** `gallery.inc.c`; imágenes RGB565 bajo `/user/`.
- **Teclado:** `kbd_qwerty.c`.
- **Super Hex:** `superhex.inc.c`.
- **Cubo:** `runner.inc.c` y `runner_levels.inc`.

La función de música se retiró de la compilación al no estar demostrada una ruta A2DP Source funcional.

## Compatibilidad y seguridad

El objetivo de esta publicación es SM-R390 con firmware base R390XXU0AZA3. No se debe asumir compatibilidad con otras variantes o firmware. No instales si no puedes comprobar el paquete y disponer de un procedimiento de recuperación adecuado.

No uses comandos `FORMAT`, `SHIPMODE` ni `DELLBTADDR`. Consulta [Instalación y recuperación](./INSTALACION.md).
