# PROJECT BEYOND — LEEME ANTES DE INSTALAR

**Publicación:** versión 1  
**Desarrollador:** DiegOS Studio  
**Dispositivo objetivo:** Samsung Galaxy Fit3 (SM-R390)  
**Firmware base:** R390XXU0AZA3  
**Estado:** experimental; probado en un reloj real, con limitaciones conocidas.

---

## 1. ¿Qué es Project Beyond?

Project Beyond es un proyecto independiente que modifica componentes adicionales de la interfaz de la Samsung Galaxy Fit3 para experimentar con aplicaciones, juegos y nuevas formas de interacción.

Incluye una galería de imágenes, un teclado QWERTY y juegos propios. No es un sistema operativo nuevo ni un producto oficial de Samsung.

El objetivo es ampliar las posibilidades del reloj sin reemplazar intencionalmente el bootloader ni las particiones originales. Esto no significa que la modificación esté libre de riesgos.

**Project Beyond no está afiliado, patrocinado ni respaldado por Samsung.**

## 2. Compatibilidad

Esta publicación está destinada exclusivamente a:

- **Modelo:** Samsung Galaxy Fit3 SM-R390.
- **Firmware base:** R390XXU0AZA3.
- **Archivo previsto:** `Proyect Beyond.bin`.

No instales el paquete en otros modelos, variantes o versiones de firmware sin verificar su compatibilidad.

Una vez instalada una versión modificada, no debería ser necesario volver al firmware stock ni restablecer de fábrica para instalar una actualización compatible. Aun así, no asumas que cualquier salto entre versiones funcionará: revisa las notas de cada actualización.

## 3. ¿Qué funciona y qué no?

Los siguientes resultados fueron reportados por el desarrollador tras probar el proyecto en un reloj real. No son una garantía de funcionamiento en todos los dispositivos.

| Función | Estado actual |
|---|---|
| Galería | Funciona, pero tiene un error al volver a transferir fotos desde el instalador HTML del PC. |
| Cubo | Jugable; ocasionalmente se congela alrededor de medio segundo y continúa. Inspirado en Geometry Dash. |
| Super Hex | Inestable; no se recomienda jugarlo por ahora. Inspirado en Super Hexagon. |
| Launcher Apps extras | Mejoró, pero algunos toques y deslizamientos pueden fallar. |
| Teclado QWERTY | Experimental; todavía pierde toques y es demasiado inconsistente para el uso diario. |
| Pantalla táctil | Mejoró notablemente; aún pueden ocurrir retrasos y, rara vez, toques fantasma. |

### Nota sobre la respuesta táctil

En ocasiones, una aplicación o una tecla puede necesitar entre 6 y 20 toques rápidos para responder. Es posible que la respuesta parezca mejorar después de un tiempo de uso, pero no está confirmado que el sistema se adapte al toque.

Si tocas una sección y no abre, el desarrollador ha observado que apagar y volver a encender la pantalla puede hacer que aparezca la sección previamente tocada. También puede ayudar en el teclado. Es una solución temporal, no una reparación definitiva.

### Error conocido de la galería

Al enviar fotografías desde el instalador HTML del PC por segunda vez, las nuevas imágenes pueden reemplazar a las anteriores en lugar de añadirse a ellas. Se considera un error pendiente de investigación, no una limitación intencional confirmada.

**Conserva las fotos originales en el PC.** No des por hecho que las imágenes anteriores permanecerán en el reloj al repetir la transferencia.

## 4. Antes de instalar

- Comprueba el modelo y la versión del firmware.
- Asegúrate de tener al menos un **50 % de batería**.
- Conserva una copia del firmware original correspondiente a tu dispositivo.
- Verifica que dispones de un procedimiento de recuperación compatible antes de comenzar.
- Descarga el paquete desde una fuente confiable y comprueba que sea el archivo esperado.
- Cierra Galaxy Wearable y otros programas que puedan ocupar la conexión Bluetooth, siguiendo las instrucciones del flasher.

**Restablecer de fábrica no devuelve por sí solo el firmware original.** Solo limpia datos y emparejamientos. No es necesario restablecer de fábrica para cada actualización compatible.

Si no puedes confirmar cómo recuperar el reloj en caso de fallo, no continúes.

## 5. Instalación

Estos pasos son orientativos y no sustituyen las instrucciones de la herramienta de flasheo.

1. Confirma que tienes una Galaxy Fit3 SM-R390 con firmware base R390XXU0AZA3.
2. Prepara la batería, conserva el firmware original y verifica un procedimiento de recuperación.
3. Cierra Galaxy Wearable y otras aplicaciones que puedan interferir con Bluetooth.
4. Abre el instalador externo [fit3-flasher de yuriyurin](https://github.com/yuriyurin/fit3-flasher) y sigue su documentación original.
5. Conecta el reloj desde el PC mediante Bluetooth serial/SPP, según las instrucciones del flasher. Si no conecta o la versión no coincide, detente.
6. Selecciona `Proyect Beyond.bin` y verifica que es el paquete correcto.
7. Inicia la instalación solo si entiendes los riesgos. No cierres el instalador ni interrumpas la conexión durante la transferencia.
8. Espera a que termine y comprueba por separado el launcher, el teclado, la galería y los juegos.

Para actualizar, no es necesario volver al firmware stock ni restablecer de fábrica si la actualización es compatible con la versión instalada. **No instales saltos entre versiones no validados.**

No utilices comandos destructivos como `FORMAT`, `SHIPMODE` o `DELLBTADDR`.

## 6. Recuperación y solución de problemas

- **Toques que no responden:** apagar y volver a encender la pantalla ha servido como solución temporal en las pruebas; no garantiza recuperar todos los eventos.
- **Fotos reemplazadas:** conserva copias en el PC y evita transferencias repetidas hasta respaldar los datos.
- **Juego congelado:** sal del juego si puedes. Super Hex no se recomienda en el estado actual.
- **Reloj bloqueado o instalación interrumpida:** utiliza únicamente un procedimiento de recuperación comprobado para tu modelo y firmware. No se garantiza que todos los fallos sean recuperables.

Que el paquete compile o pase pruebas en PC no demuestra que esté libre de errores en el reloj físico.

## 7. Créditos y agradecimientos

**Desarrollado por DiegOS Studio.**

- **Musicalista — FreeMyFit3:** proyecto base y referencia de trabajo.  
  https://github.com/Musicalista/freemyfit3
- **yuriyurin — fit3-flasher:** herramienta externa para la comunicación e instalación.  
  https://github.com/yuriyurin/fit3-flasher
- **LVGL:** biblioteca gráfica utilizada por la interfaz.
- **Cubo:** inspirado en la jugabilidad de Geometry Dash.
- **Super Hex:** inspirado en Super Hexagon.

Las referencias no implican afiliación ni autorización oficial de los titulares. El flasher no fue creado por DiegOS Studio.

## 8. Responsabilidad y advertencias

Project Beyond se proporciona con fines experimentales y educativos, **tal como está y sin garantía de funcionamiento**.

Modificar el software puede ocasionar fallos, pérdida de datos, bloqueos, problemas de conectividad o la necesidad de recuperar el firmware. En determinadas circunstancias, el dispositivo podría quedar inutilizable.

El desarrollador no garantiza compatibilidad con otros modelos o firmwares, ausencia de errores, funcionamiento perfecto de las aplicaciones ni que exista un método de recuperación funcional en todas las situaciones.

Instala la modificación solo si comprendes los riesgos. Eres responsable de comprobar la compatibilidad, proteger tus datos y decidir si deseas continuar. Estas advertencias no excluyen responsabilidades que legalmente no puedan excluirse.

No redistribuyas firmware propietario de Samsung sin autorización. La licencia del código derivado debe revisarse antes de establecer condiciones de redistribución.

## 9. Estado de la publicación

La primera publicación se identifica como **Project Beyond — versión 1**. Los números de versiones internas de desarrollo no se utilizan como nombre de la release pública.

La existencia de este documento no significa que el archivo binario esté adjunto. Descarga el paquete solo cuando aparezca publicado explícitamente en la sección de releases.

**Project Beyond: más posibilidades para la Galaxy Fit3, con transparencia sobre sus límites.**
