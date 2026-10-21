# PROJECT BEYOND — LÉEME ANTES DE INSTALAR

**Publicación:** Project Beyond v2  
**Desarrollador:** DiegOS Studio  
**Dispositivo objetivo:** Samsung Galaxy Fit3 (SM-R390)  
**Firmware base:** R390XXU0AZA3  
**Estado:** experimental; probado por el desarrollador en un reloj real.

---

## 1. ¿Qué es Project Beyond?

**Project Beyond** es un proyecto independiente que modifica componentes adicionales de la interfaz de Samsung Galaxy Fit3 para experimentar con aplicaciones, juegos y nuevas formas de interacción.

Parte del trabajo de FreeMyFit3 e incorpora una interfaz adicional con galería de imágenes, teclado QWERTY y juegos.

El objetivo es ampliar las posibilidades del reloj sin reemplazar intencionalmente el bootloader ni las particiones originales. Esto no significa que la modificación esté libre de riesgos.

**Project Beyond no es un producto oficial de Samsung, no está afiliado a Samsung ni está respaldado por la empresa.**

## 2. Compatibilidad

Esta versión está destinada exclusivamente a:

- **Modelo:** Samsung Galaxy Fit3 SM-R390.
- **Firmware base:** R390XXU0AZA3.
- **Archivo de v2 esperado:** `fit3-apps-ui-v28.bin`.

No instales el paquete en otros modelos, variantes o versiones de firmware sin verificar previamente su compatibilidad.

Una vez instalada una versión modificada, no necesariamente hace falta volver al firmware original ni restablecer de fábrica para instalar una actualización compatible. Sin embargo, no se garantiza que cualquier salto entre versiones funcione: revisa las notas de cada publicación y no instales actualizaciones no validadas.

## 3. ¿Qué funciona y qué no?

Los siguientes resultados corresponden a pruebas del desarrollador en un reloj real. No garantizan el mismo comportamiento en todos los dispositivos.

| Función | Estado en v2 |
|---|---|
| Pantalla táctil | La respuesta mejoró notablemente. Los fallos son ahora poco frecuentes, según las pruebas del desarrollador. |
| Launcher Apps extras | Responde mucho mejor que antes; todavía pueden ocurrir fallos ocasionales. |
| Galería | Funciona. Sigue pendiente un error al transferir fotografías nuevas desde el instalador HTML del PC. |
| Teclado QWERTY | Funciona, pero a veces presenta pequeños retrasos y puede registrar dos o tres teclas adicionales. Es un fallo poco frecuente. |
| Juego Cubo | Jugable; puede congelarse brevemente en ocasiones. Inspirado en Geometry Dash. |
| Super Hex | Sigue inestable y presenta problemas de rendimiento. No se recomienda para jugar con regularidad por ahora. Inspirado en Super Hexagon. |

### Mejoras táctiles de v2

v2 se centra en mejorar la respuesta táctil del launcher, la Galería y el teclado. La nueva estrategia consulta periódicamente el panel táctil y determina la liberación del dedo mediante muestras consecutivas sin contacto. También protege las pantallas nuevas para que no reaccionen a un dedo que sigue apoyado desde la pantalla anterior.

En las pruebas realizadas, los problemas que antes podían exigir muchos intentos son ahora poco frecuentes. **La mejora es importante, pero no significa que todos los errores táctiles estén eliminados.**

El teclado conserva un problema ocasional: puede retrasarse un poco o registrar dos o tres teclas adicionales. Este comportamiento sigue pendiente de optimización.

No se ha confirmado que la respuesta táctil mejore simplemente por usar el reloj durante más tiempo.

### Error conocido de la Galería: transferencia de fotos

Al enviar fotografías desde el instalador HTML del PC por segunda vez, las nuevas imágenes pueden reemplazar a las anteriores en lugar de añadirse a ellas. Es un error pendiente de investigación, no una limitación intencional confirmada.

**Conserva las fotos originales en el PC.** No des por hecho que las imágenes anteriores permanecerán en el reloj al repetir la transferencia.

### Juegos

Cubo se puede jugar, aunque puede presentar pausas ocasionales. Super Hex continúa inestable y su rendimiento sigue pendiente de optimización. La mejora táctil de v2 no significa que Super Hex se haya corregido.

## 4. Antes de instalar

- Comprueba que el modelo y el firmware coincidan con los indicados en la sección de compatibilidad.
- Asegúrate de tener al menos un **50 % de batería**.
- Conserva una copia del firmware original correspondiente a tu dispositivo.
- Comprueba que dispones de un procedimiento de recuperación compatible antes de comenzar.
- Descarga el paquete desde una fuente confiable y verifica que el archivo sea el esperado.
- Cierra Galaxy Wearable y otros programas que puedan interferir con la conexión Bluetooth, siguiendo las instrucciones del flasher.

**Restablecer el reloj a los valores de fábrica no devuelve por sí solo el firmware original.** Tampoco debe asumirse que es necesario restablecer de fábrica para cada actualización compatible.

Si no puedes confirmar cómo recuperar el reloj en caso de fallo, no continúes.

## 5. Instalación

Estos pasos son orientativos y no sustituyen las instrucciones específicas del paquete y de la herramienta de flasheo.

1. Confirma que tienes una Galaxy Fit3 SM-R390 con firmware base R390XXU0AZA3.
2. Prepara la batería, conserva el firmware original y comprueba el procedimiento de recuperación.
3. Cierra Galaxy Wearable y otras aplicaciones que puedan interferir con Bluetooth.
4. Abre la herramienta externa [fit3-flasher de yuriyurin](https://github.com/yuriyurin/fit3-flasher) y sigue su documentación original.
5. Conecta el reloj desde el PC mediante Bluetooth serial/SPP, si así lo requieren las instrucciones de la herramienta. Si la conexión falla o el firmware no coincide, detente.
6. Selecciona el archivo de v2 **`fit3-apps-ui-v28.bin`** solo si ese nombre corresponde al paquete adjunto en la publicación que descargaste. No cambies el nombre de otro binario para hacerlo coincidir.
7. Verifica nuevamente el modelo y la compatibilidad antes de iniciar.
8. No desconectes el reloj ni interrumpas el proceso durante la instalación.
9. Cuando termine, comprueba por separado el launcher, la Galería, el teclado y los juegos.

Para actualizar desde una versión anterior, no es necesario volver al firmware original ni restablecer de fábrica si la actualización es compatible. **No instales saltos entre versiones que no hayan sido validados.**

No utilices comandos destructivos como `FORMAT`, `SHIPMODE` o `DELLBTADDR`.

## 6. Recuperación y solución de problemas

- **Toques que no responden:** v2 mejora considerablemente la respuesta táctil, pero pueden persistir fallos ocasionales. No se garantiza que todas las interacciones puedan recuperarse.
- **Teclado con retraso o teclas adicionales:** es un problema conocido y poco frecuente. Evita asumir que el teclado es adecuado para uso diario hasta que se optimice.
- **Fotos reemplazadas:** conserva copias en el PC y evita transferencias repetidas hasta proteger los datos importantes.
- **Juego congelado:** sal del juego si puedes. Super Hex no se recomienda en el estado actual.
- **Reloj bloqueado o instalación interrumpida:** utiliza únicamente un procedimiento de recuperación verificado para tu modelo y firmware. No se garantiza que todos los fallos sean recuperables.

Que el paquete compile, pase pruebas en PC o sea aceptado por un validador no demuestra por sí solo que esté libre de errores en el reloj físico.

## 7. Créditos y agradecimientos

**Desarrollado por DiegOS Studio.**

- **Musicalista — FreeMyFit3:** proyecto de referencia y base de trabajo.  
  https://github.com/Musicalista/freemyfit3
- **yuriyurin — fit3-flasher:** herramienta externa relacionada con el flasheo y la comunicación con la Galaxy Fit3.  
  https://github.com/yuriyurin/fit3-flasher
- **LVGL:** biblioteca gráfica utilizada por la interfaz.
- **Cubo:** inspirado en la jugabilidad de Geometry Dash.
- **Super Hex:** inspirado en Super Hexagon.

Estos créditos e inspiraciones no implican afiliación ni autorización oficial de sus titulares. Los nombres y derechos de sus respectivos propietarios siguen perteneciendo a ellos.

## 8. Responsabilidad y advertencias

Project Beyond se proporciona con fines experimentales y educativos, **tal como está y sin garantía de funcionamiento**.

Modificar el software de un dispositivo puede ocasionar fallos, pérdida de datos, bloqueos, problemas de conectividad o la necesidad de recuperar el firmware. En determinadas circunstancias, el dispositivo podría quedar inutilizable.

El desarrollador no garantiza:

- Compatibilidad con dispositivos o firmwares distintos de los indicados.
- Ausencia de errores o pérdida de datos.
- Funcionamiento perfecto de la pantalla táctil, las aplicaciones o los juegos.
- Que todos los fallos puedan solucionarse mediante un restablecimiento o una reinstalación.
- Que exista un método de recuperación funcional en todas las situaciones.

Instala la modificación únicamente si comprendes los riesgos. Eres responsable de comprobar la compatibilidad, proteger tus datos y decidir si deseas continuar.

Estas advertencias no pretenden excluir responsabilidades que legalmente no puedan excluirse.

## 9. Distribución y estado del proyecto

Project Beyond es un proyecto independiente de DiegOS Studio. Samsung, Geometry Dash y Super Hexagon no patrocinan ni respaldan esta modificación.

Distribuye únicamente archivos para los que tengas permiso. No incluyas ni redistribuyas firmware original de Samsung sin autorización. La licencia del código derivado debe revisarse antes de establecer condiciones de redistribución.

**Project Beyond v2 se centra en la mejora de la respuesta táctil.** La mejora se ha observado en el reloj físico del desarrollador. El teclado todavía puede presentar retrasos y pulsaciones adicionales ocasionales; el error de transferencia de fotos sigue pendiente, y Super Hex continúa inestable.

**Project Beyond: más posibilidades para la Galaxy Fit3, con transparencia sobre sus límites.**
