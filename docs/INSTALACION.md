# Instalación y recuperación

Lee todo antes de continuar. Modificar firmware puede dejar el reloj inutilizable. Project Beyond y FreeMyFit3 son proyectos no oficiales y se usan bajo tu propio riesgo.

## Antes de empezar

- Dispositivo objetivo: **Samsung Galaxy Fit3 SM-R390** con firmware base **R390XXU0AZA3**.
- Usa únicamente un paquete creado para esa base exacta. No lo instales en otras variantes, firmware o dispositivos.
- Ten disponible el firmware original y un método de recuperación que sepas utilizar.
- Carga la pulsera al menos al 50 %.
- Usa un PC con un navegador compatible con el flasher web.
- Cierra Galaxy Wearable y desconecta otras aplicaciones/dispositivos que estén usando la conexión Bluetooth de la pulsera.

**Importante sobre el restablecimiento:** restablecer de fábrica borra datos/emparejamientos, pero no cambia el firmware instalado. No es un método para volver a AZA3 ni sustituye la recuperación del firmware. La recomendación de hacerlo antes de la primera instalación es una preparación opcional, no una condición técnica verificada por este proyecto.

## Primera instalación desde firmware original

1. Comprueba en Ajustes del reloj la versión del firmware. La base objetivo debe coincidir exactamente con la indicada para el paquete, actualmente `R390XXU0AZA3`. Si no coincide, detente.
2. Si decides dejar el reloj limpio, puedes restablecerlo de fábrica y dejarlo en la pantalla inicial. Esto no cambia el firmware.
3. No lo emparejes todavía con el teléfono. Cierra Galaxy Wearable y cualquier herramienta que pueda ocupar el Bluetooth.
4. Abre el instalador web **fit3-flasher**, creado por yuriyurin: [github.com/yuriyurin/fit3-flasher](https://github.com/yuriyurin/fit3-flasher). Sigue la documentación original del proyecto y confirma que estás en la página auténtica.
5. Conecta el reloj desde el PC mediante el servicio Bluetooth serie/SPP que utiliza el flasher. Si no logra conectar o la versión no coincide, no continúes.
6. Selecciona el archivo `.bin` incluido en el ZIP de la release de Project Beyond y revisa las confirmaciones y el nombre del paquete.
7. Inicia la instalación solo si entiendes el riesgo y tienes un camino de recuperación. Mantén el reloj cerca del PC, no cierres la página y no apagues ni desconectes el reloj durante la transferencia.
8. Espera a que el instalador indique que terminó. Después comprueba que el reloj arranca y prueba las funciones. No lo emparejes con el teléfono hasta confirmar que el firmware y las funciones básicas se comportan como esperas.

## Actualizar desde una versión anterior de Project Beyond

1. Confirma el modelo y que la versión instalada pertenece a una base compatible con el paquete nuevo.
2. Descarga el ZIP de la nueva release y verifica que contiene el `.bin` correcto.
3. Repite el procedimiento con el PC, fit3-flasher y la conexión Bluetooth serie/SPP; cierra Galaxy Wearable y otras conexiones.
4. Selecciona el nuevo `.bin`, confirma el destino y espera a que finalice sin desconectar el reloj.
5. Comprueba el arranque y vuelve a probar Galería, Cubo, teclado, launcher y Super Hex.

No se necesita restablecimiento de fábrica para cada actualización según el flujo previsto por el proyecto, pero **la actualización directa solo debe hacerse entre versiones cuya compatibilidad esté confirmada**. En particular, instalar v24 directamente sobre v12 no está probado: no lo hagas basándote únicamente en estas instrucciones.

## Si algo no coincide o falla

- Si el firmware no es exactamente la base admitida por el paquete, detente.
- Si el flasher no conecta, no pruebes comandos de servicio al azar.
- Si la transferencia falla, no repitas la instalación a ciegas; guarda el mensaje/log y consulta la documentación original.
- No uses los comandos `FORMAT`, `SHIPMODE` ni `DELLBTADDR`.
- No asumas que un restablecimiento de fábrica arregla un firmware modificado.

## Créditos y herramientas

- **FreeMyFit3**, proyecto base: [github.com/Musicalista/freemyfit3](https://github.com/Musicalista/freemyfit3)
- **fit3-flasher**, instalador web de yuriyurin: [github.com/yuriyurin/fit3-flasher](https://github.com/yuriyurin/fit3-flasher)

El flasher no es obra de DiegOS Studio. Consulta las instrucciones y advertencias originales en ambos repositorios; pueden cambiar con el tiempo.
