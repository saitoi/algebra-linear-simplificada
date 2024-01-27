---
aliases: 
tags:
  - ALA
date: 2023-11-25
time: 12:37
complete:
---
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
# Geradores

> $\textit{Definição.}$ *Refere-se a um conjunto mínimo de vetores que, por meio de combinações lineares, podemos gerar todo o espaço vetorial. É um conceito fundamental para generalizar retas e planos do $\Bbb{R}^{n}$.*

Em geral, se $v,w_{1},\dots,w_{nm}\in\Bbb{R}^{n}$, diremos que $v$ é uma *combinação linear* de $w_{1},\dots,w_{m}$ se existem números reais $a_{1},\dots,a_{n}$ tais que
$$
v=a_{1}w_{1}+\dots+a_{m}w_{m}.
$$
Nesse sentido, denotaremos o conjunto de vetores que são combinações lineares de $w_{1},\dots,w_{m}$ por
$$
\langle w_{1},\dots,w_{m} \rangle,
$$
e diremos que este conjunto é *gerado* por $w_{1},\dots,w_{m}$. Portanto, os conjunto de vetores $\langle w_{1},\dots,w_{m} \rangle$ é denominado de *geradores*.