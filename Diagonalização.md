---
aliases:
  - diagonalizacao
tags:
  - ALA
  - P3
date: 2023-10-16
time: 18:43
complete:
---
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
# Diagonalização
### $\texttt{}$
> $\textit{Definição.}$ Refere-se à transformação de uma matriz em sua forma diagonal.

- [i] De antemão, precisamos relembrar do conceito de <ins>matriz diagonal</ins>, isto é, uma matriz quadrada em que todos os elementos fora da diagonal principal são nulos. Por exemplo, considere a matriz diagonal $A$ descrita abaixo.
$$
\begin{align}
A=\mycolv{-1 & 0 \\0 & 1}
\end{align}
$$
Quando uma matriz puder ser transformada em sua forma diagonal, diremos que ela é uma <ins>matriz diagonalizável</ins>. Por definição, uma matriz quadrada $A$ é **diagonalizável** se existe uma matriz $P$ invertível tal que
$$
P^{-1}AP=D\tag{1}
$$
Em que $D$ se refere à matriz diagonal.

Reorganizando a expressão anterior, encontramos a igualdade
$$
A=PDP^{-1}
$$
Essa equação é denominada de **decomposição espectral** de uma matriz.

## $\texttt{Sabendo se uma matriz é diagonalizável.}$

Para determinarmos se uma matriz $(T)_{\varepsilon}$ é diagonalizável ou não, seguiremos os seguintes passos:

1. Encontraremos os autovalores de $T$. Caso $\lambda_{1}=\lambda_{2}$, então a matriz $(T)_{\varepsilon}$ não é **diagonalizável** por definição.
2. Encontramos os autovetores $v_{1},v_{2}$ de $T$. Caso a matriz $P=[v_{1}\quad v_{2}]$ for linearmente dependente, então $T$ também não é **diagonalizável** por definição.
3. Montamos a matriz $D=(T)_{\beta}$ com os autovalores obtidos e inserindo-os na diagonal principal.