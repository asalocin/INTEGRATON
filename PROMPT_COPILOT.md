# Prompt para GitHub Copilot / Copilot Chat

Crea o modifica este repositorio para que sea una plantilla simple de colaboración LaTeX para tres personas trabajando en un proyecto llamado "Integral B -- ENIM 2026".

Quiero una estructura simple, no engorrosa, con estos archivos y carpetas:

```text
main.tex
preambulo.tex
macros.tex
README.md
aportes/nicolas.tex
aportes/fonseca.tex
aportes/kenneth.tex
figuras/nicolas/
figuras/fonseca/
figuras/kenneth/
.github/workflows/build-latex.yml
.gitignore
```

Requisitos:

1. `main.tex` debe ser el archivo principal del documento y debe incluir `preambulo.tex` y `macros.tex`.
2. `main.tex` debe juntar automáticamente los aportes con:

```latex
\input{aportes/nicolas}
\input{aportes/fonseca}
\input{aportes/kenneth}
```

3. Los archivos personales no deben contener `\documentclass`, `\begin{document}` ni `\end{document}`.
4. `macros.tex` debe definir un ambiente `ejercicio` y un ambiente `solucion`, para que todos escriban con el mismo formato.
5. `preambulo.tex` debe cargar paquetes básicos de LaTeX en español: `babel`, `inputenc`, `fontenc`, `amsmath`, `amssymb`, `amsthm`, `mathtools`, `geometry`, `graphicx`, `hyperref`, `tcolorbox` y paquetes útiles similares.
6. Agrega un ejemplo mínimo de ejercicio y solución en `aportes/nicolas.tex`.
7. En `aportes/fonseca.tex` y `aportes/kenneth.tex`, deja bloques de ejemplo editables.
8. Agrega un workflow de GitHub Actions en `.github/workflows/build-latex.yml` que compile `main.tex` y suba `main.pdf` como artifact.
9. Agrega un `.gitignore` adecuado para LaTeX, ignorando archivos auxiliares como `.aux`, `.log`, `.out`, `.toc`, `.fdb_latexmk`, `.fls`, etc.
10. Agrega un `README.md` en español explicando el flujo de trabajo:
    - antes de editar, hacer Pull;
    - editar solo el archivo propio;
    - hacer Commit con mensaje claro;
    - hacer Push;
    - no editar el archivo de otra persona sin avisar;
    - no tocar `main.tex` salvo que sea necesario.

El objetivo es que tres personas puedan trabajar de forma simple en un proyecto LaTeX común sin pisarse entre ellas.
