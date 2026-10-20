<div align="center">

# PROJECT BEYOND
### Galaxy Fit3 · SM-R390 · R390XXU0AZA3

**Beyond the limits of your device.**  
Un proyecto independiente de **DiegOS Studio**.

[Web interactiva](./index.html) · [LEEME antes de instalar](./LEEME-ANTES-DE-INSTALAR.md) · [Estado actual](./docs/ESTADO-ACTUAL.md) · [Instalación](./docs/INSTALACION.md) · [Release](./releases/README.md)

</div>

> [!WARNING]
> **Versión inicial experimental.** Project Beyond ha sido probado en un reloj real, pero mantiene fallos conocidos: el teclado pierde algunos toques, el launcher puede requerir varios intentos, Cubo presenta pausas ocasionales, Super Hex es inestable y la galería puede reemplazar fotos anteriores al volver a transferir imágenes.

## ¿Qué es Project Beyond?

Project Beyond amplía de forma experimental componentes adicionales del software de la Samsung Galaxy Fit3 mediante una interfaz de aplicaciones y experiencias propias. Incluye una galería, un teclado QWERTY y juegos. No es un sistema operativo nuevo ni un producto oficial de Samsung.

## Estado actual reportado por el desarrollador

| Función | Estado |
|---|---|
| Galería | Funciona; al volver a transferir fotos desde el instalador HTML del PC, las nuevas pueden reemplazar las anteriores. |
| Cubo | Jugable; ocasionalmente se congela alrededor de medio segundo y continúa. Inspirado en Geometry Dash. |
| Teclado QWERTY | Experimental e inconsistente; no recomendado para el uso diario. |
| Launcher Apps extras | Mejoró, pero algunos toques o deslizamientos pueden fallar. |
| Pantalla táctil | Mejoró respecto a versiones previas; quedan fallos ocasionales y raros toques fantasma. |
| Super Hex | Inestable; no se recomienda jugarlo actualmente. Inspirado en Super Hexagon. |

Si una sección no abre tras tocarla, el desarrollador ha observado que apagar y volver a encender la pantalla puede hacer que aparezca la sección previamente tocada. Es una solución temporal, no una reparación definitiva. La respuesta táctil también puede parecer mejorar tras un tiempo de uso, pero no es un comportamiento confirmado.

Consulta el [estado actual detallado](./docs/ESTADO-ACTUAL.md) y el [LEEME antes de instalar](./LEEME-ANTES-DE-INSTALAR.md) antes de modificar el reloj.

## Compatibilidad

Objetivo de esta publicación: **Samsung Galaxy Fit3 SM-R390**, firmware base **R390XXU0AZA3**. No instales el paquete en otros modelos o firmwares sin verificar su compatibilidad.

El archivo previsto para la publicación es `Proyect Beyond.bin`. La disponibilidad del binario debe comprobarse en la sección de releases; no se debe asumir que el archivo está adjunto si no aparece allí.

## Créditos

- [FreeMyFit3 — Musicalista](https://github.com/Musicalista/freemyfit3), proyecto base.
- [fit3-flasher — yuriyurin](https://github.com/yuriyurin/fit3-flasher), herramienta externa de instalación.
- [LVGL](https://lvgl.io/), biblioteca gráfica.
- Cubo toma inspiración de Geometry Dash; Super Hex, de Super Hexagon.

Project Beyond no está afiliado, patrocinado ni certificado por Samsung ni por los autores de los juegos citados. El flasher no es una herramienta creada por DiegOS Studio.

## Seguridad y responsabilidad

Lee la guía de [instalación y recuperación](./docs/INSTALACION.md). Mantén al menos un 50 % de batería, conserva el firmware original y verifica que existe un procedimiento de recuperación compatible antes de instalar. No uses comandos `FORMAT`, `SHIPMODE` ni `DELLBTADDR`.

El proyecto es experimental, se proporciona tal como está y sin garantía de funcionamiento. Modificar el software puede provocar pérdida de datos, fallos o dejar el dispositivo inutilizable. La compatibilidad y la recuperación no están garantizadas. No se debe redistribuir firmware propietario de Samsung sin autorización.

**Project Beyond: más posibilidades para la Galaxy Fit3, con transparencia sobre sus límites.**
