# Prácticas de Complejidad Computacional — 2026-2
**Facultad de Ciencias, UNAM**

Este repositorio contiene las prácticas de programación del curso.
Cada práctica es un Jupyter Notebook donde implementarás algoritmos
relacionados con las clases de complejidad que hemos estudiado.

---

## Índice de prácticas

| # | Tema | Clase | Algoritmos |
|---|------|-------|------------|
| [01](01_programacion_lineal.ipynb) | Programación Lineal | **P** | Simplex (tableau) |
| [02](02_subset_sum.ipynb) | Subset Sum | **NP-completo** | Fuerza bruta · DP |
| [03](03_tsp.ipynb) | Agente Viajero (TSP) | **NP-completo** | Fuerza bruta · Held-Karp |
| [04](04_isomorfismo_graficas.ipynb) | Isomorfismo de Gráficas | **GI** | Fuerza bruta · Weisfeiler-Leman |
| [05](05_factorizacion.ipynb) | Factorización de Enteros | **NP ∩ co-NP** | División de prueba · Pollard rho |

---

## Instrucciones de entrega

- Las prácticas son **puntos extra** sobre el promedio global del curso.
- Cada práctica vale hasta **1 punto extra** sobre el promedio (máximo **5 puntos extra** en total).
- La calificación de cada práctica se distribuye así:

  | Criterio | Puntos |
  |----------|--------|
  | Código correcto (todos los `# TODO` completos y con resultados coherentes) | 6 |
  | Experimentos completos (mediciones de tiempo y gráficas generadas) | 2 |
  | Preguntas de análisis respondidas (sección 7 de cada notebook) | 2 |

  El punto extra se calcula proporcionalmente: `(calificación / 10) × 1.0`.

- **Fecha límite:** se publicará en la asignación de Google Classroom.
- **Entrega:** comparte el enlace a tu fork en la asignación de Google Classroom correspondiente.

---

## Configuración del entorno (hazlo una sola vez)

### Requisitos previos

- Tener una cuenta en [GitHub](https://github.com).
- Tener instalado [Git](https://git-scm.com/downloads).
- Tener instalado [Python 3.9+](https://www.python.org/downloads/) y `pip`.
- Tener instalado [VS Code](https://code.visualstudio.com/) con la extensión
  **Jupyter** (o usar [JupyterLab](https://jupyter.org/install)).

> Si usas Windows, todos los comandos de terminal a continuación funcionan
> en **Git Bash** o en el **Símbolo del sistema** (cmd). Se recomienda Git Bash.

---

### Paso 1 — Hacer un fork del repositorio

1. Entra a la página del repositorio del curso en GitHub.
2. Haz clic en el botón **Fork** (esquina superior derecha).
3. Deja las opciones predeterminadas y haz clic en **Create fork**.

Esto crea una copia del repositorio en **tu propia cuenta de GitHub**
(`https://github.com/TU_USUARIO/complejidad-practicas`).

---

### Paso 2 — Clonar tu fork en tu computadora

Abre una terminal y ejecuta (sustituye `TU_USUARIO` con tu nombre de usuario de GitHub):

```bash
git clone https://github.com/TU_USUARIO/complejidad-practicas.git
cd complejidad-practicas
```

---

### Paso 3 — Crear un entorno virtual de Python

Un entorno virtual aísla las bibliotecas de este curso para que no interfieran
con otros proyectos.

```bash
# Crear el entorno virtual (solo una vez)
python -m venv .venv

# Activar el entorno virtual
# En Linux / macOS:
source .venv/bin/activate

# En Windows (Git Bash):
source .venv/Scripts/activate

# En Windows (cmd):
.venv\Scripts\activate.bat
```

Sabrás que el entorno está activo porque aparece `(.venv)` al inicio de tu terminal.

---

### Paso 4 — Instalar las dependencias

Con el entorno virtual activo:

```bash
pip install numpy scipy matplotlib jupyter
```

Verifica que todo quedó instalado correctamente:

```bash
python -c "import numpy, scipy, matplotlib; print('OK')"
```

---

### Paso 5 — Abrir un notebook

**Opción A — VS Code** (recomendada):

```bash
code .
```

Abre el archivo `.ipynb` que quieras. VS Code detectará automáticamente el
entorno virtual (`.venv`) como kernel. Si te pregunta qué kernel usar, elige
**Python (.venv)**.

**Opción B — Jupyter en el navegador:**

```bash
jupyter notebook
```

Se abrirá una página en tu navegador. Navega al archivo `.ipynb` y ábrelo.

---

## Cómo trabajar en cada práctica

Cada notebook está estructurado en 7 secciones:

1. **Contexto teórico** — Repaso del problema y su clase de complejidad.
2. **Objetivo** — Qué vas a implementar y medir.
3. **Mini-tutorial de Python** — Los conceptos de Python que necesitas para esta práctica.
4. **Algoritmo** — Explicación del algoritmo con pseudocódigo o fórmulas.
5. **Implementación** — Celdas con bloques `# TODO` que debes completar.
6. **Medición de tiempos** — Celdas que generan instancias aleatorias y miden tiempos.
7. **Preguntas de análisis** — 5 preguntas que debes responder en celdas Markdown.

### Flujo de trabajo recomendado

1. Lee la sección de contexto teórico completa antes de programar.
2. Lee el mini-tutorial de Python de esa práctica.
3. Completa los bloques `# TODO` uno por uno, ejecutando cada celda para verificar.
4. Ejecuta las celdas de medición (pueden tardar unos minutos).
5. Responde las preguntas de análisis en las celdas Markdown al final.
   Haz doble clic en la celda para editarla y escribe tu respuesta debajo de cada pregunta.

> **Consejo:** Ejecuta todas las celdas desde el principio en orden
> (*Kernel → Restart & Run All*) antes de entregar, para asegurarte de que
> el notebook corre completo sin errores.

---

## Guardar y subir tu trabajo

Después de completar una práctica (o al terminar una sesión de trabajo),
guarda tus cambios en GitHub con estos tres comandos:

```bash
# 1. Ver qué archivos cambiaron
git status

# 2. Registrar los cambios (sustituye el número de práctica)
git add 01_programacion_lineal.ipynb

# 3. Crear un commit con un mensaje descriptivo
git commit -m "Practica 01: implementacion del Simplex y analisis"

# 4. Subir los cambios a tu fork en GitHub
git push
```

Puedes hacer `git add` y `git commit` tantas veces como quieras mientras
trabajas — es buena práctica hacerlo frecuentemente.

---

## Entregar la práctica

1. Asegúrate de haber hecho `git push` con tu versión final.
2. Ve a tu fork en GitHub (`https://github.com/TU_USUARIO/complejidad-practicas`).
3. Copia la URL de tu repositorio.
4. Entra a Google Classroom, abre la asignación correspondiente y pega la URL.

---

## Preguntas frecuentes

**¿Puedo usar bibliotecas adicionales?**
Sí, siempre que las justifiques brevemente en una celda de comentario.
No uses bibliotecas que resuelvan directamente el problema del notebook
(por ejemplo, no uses `networkx.is_isomorphic` en la Práctica 4 como solución
principal — está bien usarlo para *verificar* tu implementación).

**¿Puedo trabajar con un compañero?**
Las prácticas son individuales. Puedes discutir ideas con tus compañeros,
pero el código y las respuestas deben ser propios.

**¿Qué pasa si una celda de medición tarda demasiado?**
Reduce el rango de tamaños en la variable `tamanos` (o equivalente en cada
práctica). Anota en una celda Markdown que redujiste el rango y por qué.

**¿Tengo que entregar todas las prácticas?**
No. Cada práctica es independiente y suma puntos extra de manera proporcional.
Entrega las que puedas completar bien.

**El notebook me da un error de importación (`ModuleNotFoundError`).**
Asegúrate de que el entorno virtual está activo y de que ejecutaste
`pip install numpy scipy matplotlib jupyter`. Si usas VS Code, verifica
que el kernel seleccionado es **Python (.venv)**.

---

## Estructura del repositorio

```
Complejidad_computacional_FC_2026-2/practicas/
├── README.md                       ← este archivo
├── 01_programacion_lineal.ipynb
├── 02_subset_sum.ipynb
├── 03_tsp.ipynb
├── 04_isomorfismo_graficas.ipynb
└── 05_factorizacion.ipynb
```

Las imágenes generadas por los notebooks (`01_lp_tiempos.png`, etc.) se
guardarán en la misma carpeta cuando ejecutes las celdas de graficación.
Inclúyelas en tu `git push` final — son parte de la entrega.

---

*Facultad de Ciencias, UNAM · Complejidad Computacional 2026-2*
