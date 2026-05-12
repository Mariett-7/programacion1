# Descripción

Este programa fue desarrollado como tarea de la asignatura Programación I 
## Estructura del proyecto

    proyecto_matrices/
    │
    ├── main.py                    # Programa principal: importa módulos y controla el flujo
    ├── menu.py                    # Muestra el menú y captura la opción del usuario
    ├── entrada.py                 # Maneja el ingreso y la visualización de matrices
    └── operaciones_matrices.py    # Implementa las cuatro operaciones matemáticas

# Instalación

1. Clona este repositorio en tu máquina local

2. Entra a la carpeta del proyecto:

        cd matrices

No es necesario instalar dependencias adicionales.

# Cómo ejecutar

**En consola local:**

Dentro de la carpeta del proyecto, ejecuta:

    python main.py

**En Google Colab:**

1. Ejecuta cada celda con `%%writefile` en orden para crear los archivos en el entorno.

2. Finalmente, en la última celda llama al programa:

       exec(open("main.py").read())

# Cómo ingresar una matriz

El programa solicita primero las dimensiones y luego pide cada elemento individualmente, indicando su posición por fila y columna:

    Ingrese el número de filas: 2
    Ingrese el número de columnas: 2
      Elemento [1][1]: 1
      Elemento [1][2]: 2
      Elemento [2][1]: 3
      Elemento [2][2]: 4

Si se ingresa un carácter no numérico en cualquier punto, el programa muestra un mensaje de error y vuelve a pedir el mismo dato sin perder el progreso anterior.

# Operaciones disponibles

1. **Suma de matrices** — ambas matrices deben tener exactamente las mismas dimensiones (mismo número de filas y columnas).
2. **Multiplicación de matrices** — el número de columnas de A debe ser igual al número de filas de B.
3. **Producto de Hadamard** — multiplicación elemento a elemento; ambas matrices deben tener las mismas dimensiones.
4. **Producto de Kronecker** — no tiene restricción de dimensiones. Si A es de tamaño m×n y B es de tamaño p×q, el resultado será de tamaño (m·p)×(n·q).

El programa muestra las dos matrices ingresadas y el resultado antes de volver al menú.

# Manejo de errores

El programa valida todos los datos ingresados por el usuario:

- Si se ingresa una letra o símbolo donde se espera un número, se muestra un mensaje de error y se vuelve a pedir el dato.
- Si se ingresa una dimensión menor o igual a cero, se informa el error y se solicita nuevamente.
- Si las dimensiones de las matrices no son compatibles con la operación elegida, se muestra un mensaje explicando el problema y se regresa al menú principal.
- El programa continúa ejecutándose hasta que el usuario elige explícitamente la opción Salir.


## Ramas del repositorio

Cada rama del repositorio corresponde a uno de los archivos del proyecto:

- `main` → main.py
- `menu` → menu.py
- `entrada` → entrada.py
- `operaciones` → operaciones_matrices.py
