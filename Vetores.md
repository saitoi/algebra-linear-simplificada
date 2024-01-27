---
aliases:
  - vectors
  - esparsos
tags:
  - ALA/vetor
date: 2023-08-15
time: 13:40
complete: true
---
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$

# Vetores

> $\textit{Definição.}$ Entidade matemática que representa uma quantidade com magnitude, direção e sentido. Vetores podem ser visualizados como uma seta em um espaço multidimensional, de modo que o tamanho da seta indica a magnitude do vetor e a direção reflete sua orientação no plano.

**Representação algébrica.** Para indicar grandezas vetoriais, utilizamos as notações abaixo:
$$
v=(v_{1},v_{2},\,\dots\,,v_{n})\quad  \text{ ou }\quad  v=\mycolv{v_{1}\\v_{2}\\\vdots\\v_{n}}
$$
**Representação gráfica.** Suponha o vetor genérico $\vec{v}$ definido por $v=\mycolv{3\\2}$. Teremos a seguinte visualização:

```tikz
\begin{document}
\begin{tikzpicture}[scale=1.8]
    \draw[->, ultra thick] (0, 0) -- (3, 2);
    \node at (1.5, 1.5) {$\mathbf{\vec{v}}$};
\end{tikzpicture}
\end{document}
```

**Vetores esparsos.** Representação de vetores ou matrizes cujas entradas, em sua maioria, são nulas (zero). Considere um vetor esparso $v$ com $n$ posições, de modo que $a,b$ representam algumas de suas entradas. Teremos a representação abaixo:
$$
\begin{rcases}
\mycolv{0\\0\\a\\\vdots\\b\\0}
\end{rcases}n
$$
**Vetores transpostos.** Normalmente empregado em matrizes, a transposição quando aplicada em vetores resulta em uma matriz de uma linha e $n$ colunas em que $n$ representa a dimensão do vetor.