---
aliases: 
tags:
  - ALA
date: 2023-11-25
time: 16:35
complete:
---
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
# Base Ortonormal

> $\textit{Definição.}$ *Conjunto de vetores linearmente independentes (definição de [[Bases e Dimensão|base]]) que são ortogonais entre si e possuem comprimento unitário.*

Diremos que o conjunto
$$
\beta=\{u_{1},\dots,u_{m}\}
$$
é uma *base ortonormal* de um subespaço $U$ do $\Bbb{R}^{n}$ se estes vetores geram $U$ e satisfazem
$$
\langle u_{i}|u_{j} \rangle =
\begin{cases}
1&\text{se}\;  i=j,\\
2&\text{se}\;  i\neq j.   
\end{cases}
$$

## Vetor Ortogonal a um Subespaço

Suponha um subespaço $S$ do $\Bbb{R}^{n}$ do qual conhecemos uma base ortonormal
$$
\beta=\{u_{1},\dots,u_{m}\}
$$
e que $v\neq 0$ seja um vetor do $\Bbb{R}^{n}$ que *não* pertence a $S$. Desejamos descobrir um vetor $w$ que seja ortogonal a $S$ e, portanto, é ortogonal a todos os vetores da base $\beta$. Com efeito, subtrairemos de $v$ um vetor de $S$ e encontraremos os fatores $a_{1},\dots,a_{m}$ tal que
$$
w=v-(a_{1}v_{1}+\dots+a_{m}u_{m}).
$$
Calculando o produto interno entre $w$ os vetores da base $\beta$ temos que obter 0, tendo em vista que são ortogonais entre si. Por esse motivo, faremos
$$
\langle u_{i}|w \rangle =\langle u_{i}|v \rangle-a_{1}\langle u_{i}|u_{1} \rangle -\dots-a_{m}\langle u_{i}|u_{m} \rangle.
$$
Considerando que $\beta$ é uma base ortonormal, a equação anterior corresponde a
$$
\langle u_{i}|w \rangle =\langle u_{i}|u_{1} \rangle -a_{i}.
$$
Portanto, podemos extrair disso a seguinte proposição:

$\textup{Proposição}$. *Se $\beta=\{u_{1},\dots,u_{m}\}$ é uma base ortonormal de um subespaço $S$ do $\Bbb{R}^{n}$ e $v\not\in S$, então*
$$
v-\langle u_{1}|v \rangle u_{1}-\dots-\langle u_{m}|v \rangle u_{m}
$$
*é um vetor ortogonal a $S$*.