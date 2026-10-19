# Seguridad y recuperación

Estas reglas son obligatorias para cualquier prueba física de Project Beyond.

## Antes de flashear

1. Volver primero al firmware stock conocido: `R390XXU0AZA3`, usando el flasher oficial y un procedimiento de recuperación que el usuario haya comprobado.
2. Confirmar que el reloj arranca correctamente en stock.
3. Batería de al menos 50 %.
4. Desconectar otras conexiones Bluetooth.
5. No cerrar la página del flasher mientras la operación esté en curso.
6. No continuar si el paquete, la ruta o la recuperación no están claros.

**No está probado flashear v24 directamente sobre v12.** El restablecimiento de fábrica no cambia la versión del firmware.

## Prohibiciones

- No enviar comandos `FORMAT`, `SHIPMODE` ni `DELLBTADDR`.
- No reutilizar la ruta fija `REMOTE_PATH` del flasher con archivos arbitrarios.
- No modificar el driver táctil sin mediciones y evidencia.
- No considerar un validador de imagen como prueba de recuperación o arranque.
- No publicar dumps completos, binarios de firmware, claves, direcciones MAC ni datos personales.

Si no existe una ruta de recuperación verificada, detenerse. No experimentar con un dispositivo que el usuario no pueda recuperar.
