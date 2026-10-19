# Estado técnico actual — Galaxy Fit3 AZA3

**Proyecto:** Project Beyond · DiegOS Studio  
**Dispositivo:** Samsung Galaxy Fit3 SM-R390  
**Firmware base:** `R390XXU0AZA3`  
**Última versión experimental documentada:** v24

## Prioridad: entrada táctil

El sistema oficial responde bien. El problema está localizado en las aplicaciones añadidas y sus overlays. No hay evidencia suficiente para modificar el driver táctil.

| Versión | Cambio | Evidencia |
|---|---|---|
| v21 | Tolerancias: launcher 24 px, teclado 22 px, galería 14 px; latch al presionar en juegos | Pruebas de host parciales |
| v22 | Corregida bandera scroll de `make_canvas` y limpiado scroll-chain `0x300` | Revisión de código/LVGL; sin reloj real |
| v23 | Cada press inicia gesto nuevo para evitar bloqueo tras release perdido | Reproducido en PC |
| v24 | La X de Super Hex se detecta al presionar desde cualquier pantalla | Arnés de PC; falta hardware |

## Pendientes críticos

- Confirmar si el reloj tiene stock AZA3 o v12.
- Probar en reloj el toque, el movimiento del overlay y la X de Super Hex.
- Si el overlay desplaza Ajustes, investigar contenedores padre con `lv_obj_get_parent`.
- Si la pantalla no devuelve coordenadas al presionar, la última posición puede reutilizarse; no hay solución segura confirmada.
- Revisar visualmente en PC la UI nueva de Cubo.
- Probar el teclado QWERTY y respuesta rápida.
- Medir FPS reales antes de cambiar el periodo del temporizador.
- Decidir si se mantiene el tile Recuperación.
- Regenerar la fuente antialias final con la tipografía elegida por Diego.

## Módulos documentados

- **Launcher:** `menu.inc.c`, filas 76 px; Galería, Super Hex, Cubo, Recuperación, Ayuda y Cerrar.
- **Galería:** `gallery.inc.c`; `/user/index.txt`, `/user/fNN.rgb565`, `/user/t_fNN.rgb565`; hasta 24 imágenes.
- **Teclado:** `kbd_qwerty.c`; horizontal, margen 22 px.
- **Super Hex:** `superhex.inc.c`; modo sin fin.
- **Cubo:** `runner.inc.c`, `runner_levels.inc`; 15 niveles originales.
- **Música:** retirada; no hay una ruta A2DP Source demostrada.

## Firmware y símbolos de referencia

Los offsets, hashes y direcciones son datos de trabajo reportados por el autor, no una garantía de compatibilidad. Imagen principal: `best1502x_b319_user.bin`; cave libre reportada en offset `0x320522`; hooks reportados en `0x2c1d0802` y `0x2c1b76a0`. Driver táctil sin modificar.

**No distribuir ni flashear binarios desde este repositorio.** Las pruebas de host no prueban el arranque ni el comportamiento en reloj.
