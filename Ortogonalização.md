---
aliases:
  - ortogonalizacao
tags:
  - ALA
date: 2023-11-02
time: 19:50
complete:
---
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
# Ortogonalização

> $\textit{Definição.}$ Refere-se à transformação de um conjunto de vetores linearmente independentes (LI) em um conjunto/base de vetores ortogonais cujas colunas são ortonormais.

Existem diversas técnicas para a ortogonalização, sendo o mais comum o **processo de Gram-Schmidt** cuja demonstração será realizada abaixo.

Suponha que temos uma base $\beta=\{V_{1},V_{2},\dots,V_{n}\}$ cujos vetores são linearmente independentes (LI), porém não são ortogonais entre si. Para transformá-la em uma base ortogonal faremos o seguinte:

1. Escolheremos um dos vetores da base, tal como $V_{1}$ por exemplo.
2. Normalize o vetor escolhido, ou seja, $\lvert V_{1} \rvert=u_{1}$.
3. Nos resta encontrar a componente de $V_{2}$ ortogonal à $u_{1}$ que chamaremos de $V_{2x}$ por convenção.
4. Calcularemos $V_{2x}$ da seguinte forma: $V_{2x}=V_{2}-\textup{Proj}_{u_{1}}V_{2}$.
5. Normalizaremos $V_{2x}$, ou seja, $\lvert V_{2} \rvert=u_{2}$.
6. Tendo os vetores $u_{1}$ e $u_{2}$ normalizados corretamente, aplicaremos o algoritmo às próximas posições $V_{3},V_{4},\dots,V_{n}$.
7. Teremos a base $\beta=\{u_{1},u_{2}\}$.

**Explicação.** Para determinar a componente $V_{2x}$ de $V$, basta 
