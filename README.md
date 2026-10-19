<div align="center">

# PROJECT BEYOND
### Galaxy Fit3 · SM-R390 · R390XXU0AZA3

**Beyond the limits of your device.**  
An independent project by **DiegOS Studio**.

[Website](./index.html) · [Estado técnico](./docs/ESTADO-ACTUAL.md) · [Seguridad](./docs/SEGURIDAD-Y-RECUPERACION.md)

</div>

> [!WARNING]
> **No se recomienda flashear v24 en el estado actual.** Las correcciones táctiles v21–v24 se verificaron con arneses de prueba en PC, pero aún no se han validado físicamente en el reloj. Lee las reglas de recuperación antes de cualquier prueba.

## ¿Qué es?

Project Beyond es un proyecto independiente para añadir experiencias ligeras al Samsung Galaxy Fit3 (SM-R390), manteniendo el firmware base y extendiendo su interfaz mediante código C y LVGL.

La edición documentada aquí se centra en firmware base **`R390XXU0AZA3`**, pantalla **256 × 402**, FreeRTOS y LVGL 8.

## Funciones

- **Apps extras:** launcher integrado en Ajustes.
- **Galería:** lectura de imágenes RGB565 guardadas en `/user/`.
- **Teclado QWERTY horizontal:** entrada para campos compatibles y respuestas rápidas.
- **Super Hex:** juego original sin fin y dificultad progresiva.
- **Cubo:** juego original de plataformas, 15 niveles.
- **Herramientas HTML:** transferencia de fotografías o archivos mediante Bluetooth SPP; algunas rutas siguen sin probarse en hardware real.

La música integrada se retiró del firmware porque no se encontró una ruta A2DP Source funcional ni fuente verificable de la app anterior.

## Estado resumido

| Área | Estado |
|---|---|
| Último paquete experimental documentado | `fit3-apps-toque-v24.bin` |
| v21–v24 | Código revisado y pruebas host; falta validación en reloj |
| Overlay en Ajustes | Causa identificada en v22; posible scroll en contenedor padre pendiente |
| Cierre X de Super Hex | Corregido y reproducido en arnés de PC; falta prueba física |
| UI nueva de Cubo | Compila; falta revisar su render de host |
| Firmware instalado en el reloj | Pendiente: stock AZA3 o v12 |

Más detalle: [estado técnico actual](docs/ESTADO-ACTUAL.md), [plan de pruebas](docs/PLAN-DE-PRUEBAS.md) y [construcción](docs/BUILD-Y-PRUEBAS.md).

## Seguridad

- No subir `stock-aza3.bin`, firmware empaquetado, dumps completos, archivos `.f3a`, claves ni direcciones MAC.
- No usar comandos `FORMAT`, `SHIPMODE` ni `DELLBTADDR`.
- No reutilizar la ruta fija `REMOTE_PATH` del flasher para archivos arbitrarios.
- No considerar un validador de imagen equivalente a una prueba de arranque en el reloj.
- Sigue siempre [seguridad y recuperación](docs/SEGURIDAD-Y-RECUPERACION.md).

## Licencia y marcas

La licencia del código derivado está pendiente de revisión. No se declara permiso general de redistribución. Consulta [licencias y atribuciones](docs/LICENCIAS-Y-ATRIBUCIONES.md).

Project Beyond es independiente y no está afiliado, patrocinado ni certificado por Samsung.