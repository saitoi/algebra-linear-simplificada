---
aliases:
  - homogeneo
tags:
  - ALA
  - P3
date: 2023-11-24
time: 20:20
complete:
---
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
# Sistema Linear Homogêneo

> $\textit{Definição.}$ Refere-se a um conjunto de equações lineares onde todos os termos constantes são iguais a zero. Esses sistemas podem ser representados da forma $Ax=0$.

Nesse sentido, existem algumas propriedades importantes relacionadas a sistemas homogêneo que irei pontuar abaixo:

1. Todos os sistemas homogêneos possuem pelo menos uma solução trivial, isto é, quando todas as variáveis desconhecidas $x_{1},x_{2},\dots,x_{n}$ são nulas.
2. É fechado para operações de adição vetorial e multiplicação por escalar.
3. $\textup{Teorema Fundamental da Teoria dos Sistemas Lineares.}$ *Todas as soluções de um sistema linear podem ser obtidas somando-se a qualquer uma delas as soluções do sistema homogêneo associado.*

A primeira proposição pode ser concluída diretamente e não requer nenhuma forma de dedução adicional. Por outro lado, a segunda e a terceira são mais interessantes. Desse modo, suponha uma matriz $A$ qualquer e sejam $v_{1}$ e $v_{2}$ duas soluções do sistema homogêneo $AX=0$. Por esse motivo, estamos supondo que
$$
Av_{1}=0\quad \text{e}\quad Av_{2}=0
$$
Com base nisso, podemos deduzir que
$$
A(v_{1}+v_{2})=Av_{1}+Av_{2}=0+0=0.
$$
Portanto, a soma $v_{1}+v_{2}$ também é solução do sistema homogêneo mencionado. O mesmo vale se multiplicarmos qualquer uma das soluções por um escalar $\lambda \in\Bbb{R}^{}$ que obteremos
$$
A(\lambda v_{1})=\lambda Av_{1}=\lambda\cdot 0=0,
$$
Com efeito, deduzimos duas propriedades importantes de sistemas homogêneos:

1. A adição de duas soluções gera uma nova solução do sistema.
2. A multiplicação de uma solução por um escalar gera outra solução do sistema.

Por fim, a última proposição, e não menos importante, nos informa que dado um sistema linear particular tal como
$$
Ax_{p}=b,\; (b\neq 0),
$$
suas soluções podem ser obtidas se pegarmos uma das soluções desse sistema e somarmos com as **soluções do sistema homogêneo associado**. Portanto, denotando por $x_{h}$ a **família de soluções** de um sistema linear homogêneo $Ax_{h}=0$, temos que:
$$
A\mathbf{x}=b,\;(\mathbf{x}=x_{p}+x_{h}).
$$
