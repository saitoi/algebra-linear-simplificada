---
aliases:
  - matrix_product
  - multiplicacao_matriz
tags:
  - ALA
date: 2023-09-11
time: 08:21
complete:
---
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
# Multiplicação de Matrizes

> $\textit{Definição.}$ *Operação matemática que combina duas matrizes para produzir uma terceira, dada algumas compatibilidades.*

$\textbf{Regra da multiplicação de Matrizes.}$ Número de colunas da primeira matriz deve ser igual ao número de linhas da segunda.
$$
A_{m\times\underline{n}}\cdot A_{\underline{n}\times c}=A_{m\times c}
$$
A matriz resultante terá dimensões $m\times c$, isto é, conterá o número de linhas da primeira $\times$ número de colunas da segunda.

$\textbf{Obs.}$ A multiplicação de matrizes $\textbf{NÃO}$ é uma operação comutativa. Se considerarmos as matrizes $A,M$ $\textbf{NÃO}$ podemos afirmar que
$$
A\cdot M=M\cdot A
$$
Embora hajam casos em que a ordem de multiplicação de matrizes não altera o resultado, não se trata de uma condição obrigatória.

## $\texttt{Multiplicação.}$

O processo multiplicativo entre matrizes envolve 

