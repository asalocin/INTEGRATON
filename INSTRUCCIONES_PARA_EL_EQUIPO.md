# Instrucciones rápidas para trabajar

Cabros, el proyecto funciona así:

- `main.tex` es el archivo principal y junta todo.
- Cada uno tiene su propio archivo en `aportes/`.
- Nicolás edita `aportes/nicolas.tex`.
- Fonseca edita `aportes/fonseca.tex`.
- Kenneth edita `aportes/kenneth.tex`.

El `main.tex` ya tiene esto:

```latex
\input{aportes/nicolas}
\input{aportes/fonseca}
\input{aportes/kenneth}
```

Eso significa que todo lo que escribamos en nuestros archivos aparece automáticamente en el PDF final.

## Flujo de trabajo

Antes de escribir:

```text
Pull
```

Después:

```text
Commit
Push
```

La regla más importante:

```text
No editar el archivo de otra persona sin avisar.
No tocar main.tex salvo que sea necesario.
```

## Cómo escribir un ejercicio

```latex
\begin{ejercicio}[Nombre del ejercicio]
Aquí va el enunciado.
\end{ejercicio}

\begin{solucion}
Aquí va la solución.
\end{solucion}
```

Nada de `\documentclass`, `\begin{document}` ni `\end{document}` en los archivos personales.
