<div align="center">

# PROJECT BEYOND
### Galaxy Fit3 · SM-R390 · R390XXU0AZA3

**Beyond the limits of your device.**  
An independent project by **DiegOS Studio**.

[Web interactiva](./index.html) · [Estado real](./docs/ESTADO-ACTUAL.md) · [Instalación](./docs/INSTALACION.md) · [Versiones](./releases/README.md)

</div>

> [!WARNING]
> **Estado experimental.** La galería, Cubo y el teclado funcionan según las pruebas de Diego. La entrada táctil sigue fallando ocasionalmente; el launcher se comporta mal a veces al deslizar, y Super Hex es inestable y actualmente injugable por el fallo táctil. No describir v24 como estable ni recomendarla como una release probada en hardware.

## ¿Qué es Project Beyond?

Project Beyond amplía de forma experimental el firmware de la Samsung Galaxy Fit3 con una interfaz de aplicaciones y experiencias propias en C/LVGL. No es un sistema operativo nuevo ni un producto oficial de Samsung.

## Estado confirmado por el desarrollador

| Función | Estado actual |
|---|---|
| Galería | Funciona |
| Cubo | Funciona; juego inspirado en *Geometry Dash* |
| Teclado QWERTY | Funciona |
| Táctil de las apps añadidas | Mejoró, pero todavía falla ocasionalmente |
| Launcher Apps extras | No está suficientemente optimizado; algunos toques fallan, especialmente al deslizar |
| Super Hex | Inestable e injugable actualmente por los problemas táctiles |

**Inspiraciones:** Cubo toma inspiración de *Geometry Dash* y Super Hex de *Super Hexagon*. Son proyectos independientes; no se afirma afiliación ni se incluyen recursos oficiales de esos juegos.

## Base y créditos

Project Beyond se desarrolla sobre la base del proyecto **FreeMyFit3**. Agradecimientos a Musicalista por la base y a yuriyurin por el instalador web original.

- [FreeMyFit3 — código y documentación de la base](https://github.com/Musicalista/freemyfit3)
- [fit3-flasher — instalador web de yuriyurin](https://github.com/yuriyurin/fit3-flasher)

El fit3-flasher no es una herramienta creada por DiegOS Studio. Consulta siempre las advertencias de sus autores y las de FreeMyFit3 antes de instalar firmware.

## Instalación y versiones

Lee primero [Instalación y recuperación](docs/INSTALACION.md). El ZIP de una release será añadido por el autor e incluirá el firmware `.bin` y el HTML para transferir fotos desde el PC al reloj. **El ZIP todavía no está adjunto.**

La última versión experimental documentada es v24. Sus correcciones táctiles fueron verificadas con arneses en PC, pero el comportamiento físico no se ha confirmado. No la trates como estable hasta que el autor publique los resultados de prueba en el reloj.

## Seguridad

- La base está dirigida a Galaxy Fit3 **SM-R390** y firmware base **R390XXU0AZA3**; no asumas compatibilidad con otras versiones, variantes o dispositivos.
- Conserva una copia de la firmware original y confirma cómo recuperar el reloj antes de modificarlo.
- Batería ≥50 % y cierra Galaxy Wearable/otras conexiones que usen el Bluetooth antes de conectar el flasher.
- No restablezcas ni flashees a ciegas: un restablecimiento de fábrica no cambia la versión del firmware.
- No publicar firmware original, dumps completos, claves ni direcciones MAC.
- No usar comandos `FORMAT`, `SHIPMODE` ni `DELLBTADDR`.

## Código fuente y licencia

El código fuente completo de trabajo aún no está incorporado. La licencia del código derivado está pendiente de revisión; no se declara permiso general de redistribución. Consulta [licencias y atribuciones](docs/LICENCIAS-Y-ATRIBUCIONES.md).

Project Beyond es independiente y no está afiliado, patrocinado ni certificado por Samsung.
