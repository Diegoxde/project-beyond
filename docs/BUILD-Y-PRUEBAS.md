# Construcción y pruebas

## Estado de la fuente

El archivo `fit3-trabajo-fuente.tar.gz` fue mencionado en el traspaso, pero no se ha añadido a este repositorio. La carpeta `src/` es un marcador documental; por tanto, **la compilación aún no se puede ejecutar desde este repo**.

## Comando conocido

En el entorno de desarrollo original:

```bash
python3 build_linux.py apps
```

Configuración documentada: `-DNO_DOOM -DWITH_GALLERY -DNO_GAMES -DWITH_SUPERHEX -DWITH_RUNNER`.

Dependencias reportadas: `arm-none-eabi-gcc`, Capstone, Pillow, SciPy, NumPy, Playwright/Chromium y Node para el validador. Verificar versiones en el entorno real antes de reproducir.

## Pruebas host

Arneses citados en el traspaso: `host_tap_test.c`, `host_lost_release_test.c`, `host_x_test.c`, `host_run_test.c`, `host_sh_test.c`. Cada uno puede tener un stub de toque diferente (`tp_*` o `h_*`); comprobar cuál usa antes de atribuir un resultado.

## Principios

1. Reproducir el fallo con el código anterior.
2. Ejecutar la misma prueba con el cambio.
3. Guardar logs y resultados.
4. No afirmar mejoras porcentuales sin mediciones.
5. Probar el render en host antes de compilar otra versión.
6. La validación binaria no equivale a prueba en reloj.
