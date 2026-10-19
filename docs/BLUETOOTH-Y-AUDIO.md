# Bluetooth y audio — notas de investigación

## Transferencia SPP

UUID SPP documentado: `db764ac8-4b08-7f25-aafe-59d03c27bae3`.

Se describieron dos páginas HTML de PC:
- `fit3-fotos.html`: transferencia de fotografías por SPP.
- `music_transfer_unificado.html`: fotos/MP3 y prueba de respuesta AT.

Los flujos se probaron con un reloj simulado en Chromium, no con hardware real. No afirmar que todas las transferencias estén verificadas físicamente. No guardar direcciones MAC personales en el repositorio.

## Audio

No se encontró codificador SBC ni endpoint A2DP Source. La música integrada se retiró de la compilación. No existe una ruta verificada para reproducir audio directamente desde la pulsera.

Una vía de investigación futura es probar si el reloj puede actuar como controlador AVRCP del teléfono (play/pausa/volumen), primero con controles oficiales y sin modificar firmware. Sigue siendo una hipótesis, no una función implementada.
