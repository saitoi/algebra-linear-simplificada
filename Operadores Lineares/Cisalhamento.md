---
aliases:
  - cisalhamento
tags:
  - ALA/Operadores
date: 2023-09-11
time: 20:27
complete:
---
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
# Cisalhamento

> $\textit{Definição.}$ Transformação linear que deforma as uma figura geométrica mantendo sua área, mas alterando a forma e orientação dos objetos.

Dado um número real $\alpha$, definimos o operador do cisalhamento como
$$
\begin{align}
c_{\alpha}(x,y)=(x+\alpha y,y)\;\;&\equiv\textquotedblleft \text{Cisalhamento Horizontal}\textquotedblright \\
&\text{ou} \\ 
c_{\alpha}(x,y)=(x,\alpha x+y)\;\;&\equiv \textquotedblleft \text{Cisalhamento Vertical}\textquotedblright  
\end{align}
$$
Ou seja, a matriz de cisalhamento possui duas formas distintas a depender do tipo de cisalhamento. Normalmente, trabalhamos com o cisalhamento horizontal como visto abaixo.
$$
\begin{align}
c_{\alpha}=\mycolv{1 & \alpha  \\0 & 1}
\end{align}
$$