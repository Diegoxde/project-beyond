# Estado actual — Project Beyond para Galaxy Fit3

**Dispositivo:** Samsung Galaxy Fit3 SM-R390  
**Firmware base de trabajo:** R390XXU0AZA3  
**Último paquete experimental documentado:** v24  
**Estado:** experimental; no declarar estable.

## Estado reportado por Diego

| Módulo | Estado en reloj |
|---|---|
| Galería | **Funciona** |
| Cubo | **Funciona** |
| Teclado QWERTY | **Funciona** |
| Táctil de las apps añadidas | **Mejoró, pero todavía falla ocasionalmente** |
| Launcher Apps extras | **Necesita optimización**; a veces los toques no se registran correctamente, sobre todo al deslizar, donde puede bloquearse o confundirse el gesto |
| Super Hex | **Inestable e injugable actualmente** por los fallos táctiles |

Estos estados son observaciones del desarrollador en el dispositivo, y tienen prioridad sobre las pruebas parciales de host descritas más abajo.

## Prioridades de desarrollo

1. Corregir los gestos del launcher: distinguir un toque de un deslizamiento, evitar que el overlay desplace Ajustes y recuperar correctamente el estado tras un evento de soltar perdido.
2. Resolver la entrada táctil de Super Hex para que el juego sea jugable antes de considerarlo parte de una release estable.
3. Verificar que el teclado y la galería siguen funcionando tras cada cambio táctil.
4. Revisar el render de la nueva UI de Cubo en host; su compilación no garantiza que se vea correctamente.
5. No cambiar el driver táctil oficial sin evidencia: el sistema original responde bien y los fallos se concentran en las apps añadidas.

## Cambios técnicos previos documentados

| Versión | Cambio | Evidencia/limitación |
|---|---|---|
| v21 | Tolerancias: launcher 24 px, teclado 22 px, galería 14 px; latch al presionar en juegos | Pruebas de host parciales |
| v22 | Ajuste de flags de scroll en `make_canvas` y limpieza de scroll-chain `0x300` | Revisión de código/LVGL; no prueba física |
| v23 | Cada evento de presionar inicia un gesto nuevo para evitar bloqueo tras un release perdido | Reproducido en PC |
| v24 | La X de Super Hex se detecta al presionar desde cualquier pantalla | Arnés de PC; falta validación específica en reloj |

Aunque algunos cambios de código pasaron pruebas de PC, Diego confirma que la experiencia táctil sigue siendo imperfecta en el reloj real.

## Módulos

- **Launcher:** `menu.inc.c`; Galería, Super Hex, Cubo, Recuperación, Ayuda y Cerrar.
- **Galería:** `gallery.inc.c`; imágenes RGB565 bajo `/user/`, hasta 24 imágenes.
- **Teclado:** `kbd_qwerty.c`; teclado QWERTY horizontal.
- **Super Hex:** `superhex.inc.c`; juego original inspirado en *Super Hexagon*.
- **Cubo:** `runner.inc.c`, `runner_levels.inc`; 15 niveles originales, inspirado en *Geometry Dash*.
- **Música:** retirada de la compilación; no hay ruta A2DP Source demostrada.

Las inspiraciones son referencias de diseño; Project Beyond no está afiliado a los autores de esos juegos y no debe incluir recursos protegidos sin permiso.

## Seguridad

- No se ha demostrado que v24 funcione de forma estable en el reloj.
- No flashear directamente sobre v12: ese salto no está probado en este proyecto.
- Antes de una instalación, verificar modelo, versión base, integridad del archivo y recuperación posible.
- Las instrucciones completas están en [INSTALACION.md](INSTALACION.md).
