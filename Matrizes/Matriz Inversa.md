---
aliases:
  - inverse
tags:
  - ALA
date: 2023-09-20
time: 19:52
complete: true
---
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
# Matriz Inversa

> $\textit{Definição.}$ Refere-se à matriz que quando multiplicada por outra resulta na identidade.

Formalmente, uma matriz genérica $A$ possui uma inversa $B$ se, e somente se,
$$
AB=I\quad \text{e}\quad BA=I
$$
Ou seja, o produto entre a matriz original e inversa resulta na matriz identidade (definida na dimensão das matrizes $A,B$).

## $\texttt{Fórmula geral.}$

Dada uma matriz genérica de determinante não nulo

$$
\begin{align}
A=\mycolv{a_{11} & a_{12}\\a_{21} & a_{22}}
\end{align}
$$

A inversa $A$ corresponde à seguinte matriz
$$
\begin{align}
\boxed{A^{-1}=\dfrac{1}{\det(A)}\mycolv{a_{22} & -a_{12}\\-a_{21} & a_{11}}}\tag{1}
\end{align}
$$
$\textbf{Demonstração.}$ Podemos testar a hipótese: Dada a matriz genérica $A$, o produto entre $A$ e sua inversa deverá resultar na identidade. Portanto, teremos
$$
AA^{-1}=I
$$
Em que $A^{-1}$ é definida pela expressão $(1)$. Calculando o produto, obteremos
$$
\begin{align}
AA^{-1}&=\mycolv{a_{11} & a_{12}\\a_{21} & a_{22}}\mycolv{a_{22} & -a_{12}\\ -a_{21} & a_{11}} \dfrac{1}{\det(A)} \\ \\
&=\mycolv{a_{11}a_{22}-a_{12}a_{21} & a_{11}a_{12}-a_{11}a_{12}\\ a_{21}a_{22}-a_{21}a_{22} & a_{11}a_{22}-a_{12}a_{21}} \dfrac{1}{\det(A)}
\end{align}
$$
Agora nos resta substituir o determinante $\det(A)$ na expressão do produto entre as matrizes. Desse modo, calcularemos ele primeiro
$$
\begin{align}
\det(A)=a_{11}a_{22}-a_{12}a_{21}
\end{align}
$$
Substituindo, obteremos
$$
\begin{align}
&=\mycolv{a_{11}a_{22}-a_{12}a_{21} & a_{11}a_{12}-a_{11}a_{12}\\ a_{21}a_{22}-a_{21}a_{22} & a_{11}a_{22}-a_{12}a_{21}} \dfrac{1}{a_{11}a_{22}-a_{12}a_{21}} \\ \\
&=\mycolv{1 & 0\\0  & 1}\qquad \blacksquare 
\end{align}
$$
Como podemos perceber, chegamos à matriz identidade tendo feita a multiplicação $AA^{-1}$. Portanto, está provada a fórmula para se obter a matriz inversa de uma transformação $\Bbb{R}^{2}$.
