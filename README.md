# Integral B -- ENIM 2026

Plantilla simple para trabajar en equipo en un proyecto LaTeX usando GitHub.

## Idea del proyecto

El repo tiene un archivo principal:

```text
main.tex
```

Ese archivo junta automáticamente los aportes de cada integrante:

```latex
\input{aportes/nicolas}
\input{aportes/fonseca}
\input{aportes/kenneth}
```

Cada integrante edita solamente su propio archivo:

```text
aportes/nicolas.tex
aportes/fonseca.tex
aportes/kenneth.tex
```

Así se evitan conflictos de Git y nadie pisa el trabajo de otra persona.

---

## Regla de oro

1. Antes de trabajar: hacer **Pull**.
2. Editar solo el archivo propio.
3. Revisar que el documento compile, si se tiene LaTeX instalado.
4. Hacer **Commit** con un mensaje claro.
5. Hacer **Push**.

No editar el archivo de otra persona sin avisar.
No tocar `main.tex` salvo que sea necesario.

---

## Estructura

```text
integral-b-enim/
│
├── main.tex
├── preambulo.tex
├── macros.tex
├── README.md
│
├── aportes/
│   ├── nicolas.tex
│   ├── fonseca.tex
│   └── kenneth.tex
│
├── figuras/
│   ├── nicolas/
│   ├── fonseca/
│   └── kenneth/
│
└── .github/
    └── workflows/
        └── build-latex.yml
```

---

## Cómo agregar un ejercicio

Dentro del archivo propio, escribir:

```latex
\begin{ejercicio}[Título del ejercicio]
Escriba aquí el enunciado.
\end{ejercicio}

\begin{solucion}
Escriba aquí la solución.
\end{solucion}
```

No agregar en los archivos personales:

```latex
\documentclass
\begin{document}
\end{document}
```

Eso ya está en `main.tex`.

---

## Cómo agregar una figura

Cada integrante guarda sus figuras en su propia carpeta:

```text
figuras/nicolas/
figuras/fonseca/
figuras/kenneth/
```

Ejemplo:

```latex
\begin{center}
    \includegraphics[width=0.55\textwidth]{figuras/nicolas/region.png}
\end{center}
```

---

## Cómo ver el PDF en GitHub

Cada vez que alguien hace `Push`, GitHub intenta compilar el documento.

Para descargar el PDF compilado:

1. Entrar al repo en GitHub.
2. Ir a la pestaña **Actions**.
3. Abrir la última ejecución de **Build LaTeX PDF**.
4. Descargar el artifact llamado **integral-b-enim-pdf**.

---

## Instalación mínima recomendada

Para cada integrante:

- GitHub Desktop
- VS Code

Opcional para quien quiera compilar localmente:

- MiKTeX o TeX Live
- Extensión LaTeX Workshop de VS Code

Si alguien no quiere instalar LaTeX, puede escribir igual y dejar que GitHub compile el PDF automáticamente.

---

## Mensajes de commit recomendados

Buenos ejemplos:

```text
Agrega ejercicio de cambio de orden de integración
Corrige solución de integral triple
Añade figura de región polar
Ordena enunciado de ejercicio suplementario
```

Evitar mensajes como:

```text
cambios
avance
latex
update
```
