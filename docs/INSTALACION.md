# Instalación y recuperación — Project Beyond

Lee todo antes de continuar. Project Beyond es una modificación experimental e independiente. Modificar firmware puede provocar fallos, pérdida de datos o dejar el reloj inutilizable.

## Antes de empezar

- Dispositivo objetivo: **Samsung Galaxy Fit3 SM-R390** con firmware base **R390XXU0AZA3**.
- Paquete previsto: `Proyect Beyond.bin`. Confirma el nombre y la integridad del archivo que descargaste.
- Ten disponible una copia del firmware original y un procedimiento de recuperación que sepas utilizar.
- Carga el reloj al menos al **50 %**.
- Usa un PC y una versión confiable del flasher compatible con el paquete.
- Cierra Galaxy Wearable y otros programas que puedan ocupar la conexión Bluetooth.

**Restablecer de fábrica no devuelve el firmware original.** Solo limpia datos y emparejamientos. No se considera necesario restablecer de fábrica ni volver al firmware stock cada vez que se instala una versión nueva compatible.

## Primera instalación desde firmware original

1. Comprueba que el reloj es SM-R390 y que el firmware coincide exactamente con la base admitida por el paquete.
2. Conserva el firmware original y verifica previamente la posibilidad de recuperación. Si no tienes un método de recuperación que entiendas, detente.
3. Cierra Galaxy Wearable y otras herramientas que puedan usar Bluetooth.
4. Abre el instalador externo [fit3-flasher de yuriyurin](https://github.com/yuriyurin/fit3-flasher) y sigue su documentación original.
5. Conecta el reloj desde el PC mediante el servicio Bluetooth serial/SPP que utilice la herramienta. Si no conecta o la versión del firmware no coincide, no continúes.
6. Selecciona `Proyect Beyond.bin` y verifica que sea el paquete correcto para tu dispositivo.
7. Inicia la instalación solo si comprendes los riesgos. No cierres el instalador ni interrumpas la conexión durante el proceso.
8. Espera a que el flasher indique que terminó. Comprueba el arranque y prueba por separado el launcher, teclado, galería y juegos.

## Actualizaciones de Project Beyond

No debería ser necesario volver al firmware stock ni restablecer de fábrica para instalar una versión nueva **si es compatible con la instalación existente**. Antes de actualizar:

1. Lee las notas de la nueva publicación.
2. Confirma que el paquete corresponde al mismo modelo y a una ruta de actualización compatible.
3. Conserva una copia de los archivos y fotos importantes.
4. Usa el procedimiento de instalación indicado por la publicación y no desconectes el reloj durante la transferencia.
5. Tras actualizar, verifica todas las funciones.

No des por hecho que cualquier salto entre versiones es compatible: instala únicamente cuando esa ruta esté validada o documentada por el proyecto.

## Problemas y recuperación

- **El toque no responde:** apagar y volver a encender la pantalla ha servido como solución temporal en las pruebas, pero no garantiza recuperar todos los eventos.
- **La galería reemplaza fotos anteriores:** conserva los originales en el PC y evita transferencias repetidas hasta respaldar las imágenes.
- **El flasher no conecta o la instalación falla:** no improvises comandos ni repitas el proceso a ciegas. Guarda el mensaje de error y consulta la documentación original.
- **El reloj queda bloqueado:** usa únicamente un método de recuperación comprobado para el modelo y firmware. No se garantiza que todos los fallos sean recuperables.

No uses los comandos `FORMAT`, `SHIPMODE` ni `DELLBTADDR`.

## Créditos

- [FreeMyFit3 — Musicalista](https://github.com/Musicalista/freemyfit3), proyecto base.
- [fit3-flasher — yuriyurin](https://github.com/yuriyurin/fit3-flasher), herramienta externa de instalación.

El flasher no es obra de DiegOS Studio. Consulta las instrucciones y advertencias originales de sus autores.
