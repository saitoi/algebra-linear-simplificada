$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
# Vetores

> **Definição.** Entidade matemática dotada de magnitude, direção e sentido.

**Representação algébrica.**
$$
v=(v_{1},v_{2},\,\dots\,,v_{n})\quad  \text{ ou }\quad  v=\mycolv{v_{1}\\v_{2}\\\vdots\\v_{n}}
$$

**Representação gráfica.** Suponha o vetor genérico $\vec{v}$ definido por $v=\mycolv{3\\2}$.

```tikz
\begin{document}
\begin{tikzpicture}[scale=1.8]
    \draw[->, ultra thick] (0, 0) -- (3, 2);
    \node at (1.5, 1.5) {$\mathbf{\vec{v}}$};
\end{tikzpicture}
\end{document}
```

**Vetores esparsos.** Vetores ou matrizes cuja maioria de suas entradas são nulas (iguais à zero).

$$
\begin{rcases}
\mycolv{0\\0\\a\\\vdots\\b\\0}
\end{rcases}n
$$

**Vetores transpostos.** Normalmente empregado em matrizes, a transposição quando aplicada em vetores resulta em uma matriz de uma linha e $n$ colunas em que $n$ representa a dimensão do vetor.
