---
aliases:
  - det
tags:
  - ALA
date: 2023-09-17
time: 11:09
complete: false
---
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
# Determinante

> $\textit{Definição.}$ Grandeza escalar associada a uma matriz quadrada que descreve o comportamento do volume ou área (depende da dimensão) em uma transformação.

## $\texttt{Definição Recursiva.}$

Seja $A$ uma matriz $n\times n$, definimos o $\textit{j-ésimo cofator}$ de $A$ como sendo a matriz obtida ao retirarmos a primeira linha e sua $\textit{j-ésima coluna}$. Essa matriz é denotada por $\widehat{A}_{j}$ e possui tamanho $(n-1)\times(n-1)$.

O caso base corresponde a $n=1$, ou seja, se trata de uma matriz $1\times 1$ cujo determinante é o único elemento da matriz. Feito isso, definimos os casos sucessores $(n\geq 2)$ como
$$
\det(A)=a_{1,1}\det(\widehat{A}_{1})-a_{1,2}\det(\widehat{A}_{2})+a_{1,3}\det(\widehat{A}_{3})-\dots+(-1)^{n-1}a_{1,n}\det(\widehat{A}_{n})\tag{1}
$$
Como exemplo, suponha a matriz $A$ dada por
$$
\begin{align}
A=\mycolv{a_{1,1} & a_{1,2} \\a_{2,1} & a_{2,2}}
\end{align}
$$
E seus cofatores correspondem a
$$
\widehat{A}_{1}=\mycolv{a_{2,2}}\quad \text{e}\quad \widehat{A}_{2}=\mycolv{a_{2,1}},
$$
Por fim, segundo a fórmula reacursiva teremos
$$
\det(A)=a_{1,1}\det(\widehat{A}_{1})-a_{1,2}\det(\widehat{A}_{2})=a_{1,1}a_{2,2}-a_{1,2}a_{2,1}.
$$

## $\texttt{Propriedades.}$

Aqui estão algumas das principais propriedades dos determinantes. De antemão, considere matrizes genéricas $A,B$.

#### $1.$ Uma matriz de transformação não possui inversa **se, e somente se,** seu determinante for zero.

**Demonstração da ida.** 
**Demonstração da volta.** Suponha a matriz de transformação $A$ com determinante nulo e sua inversa $B$. Segundo a definição de matriz inversa, temos que a matriz $A$ multiplicada por $B$ resultaria na identidade.
$$
AB=I
$$
Podemos aplicar o determinante em ambos os lados da expressão e teremos
$$
\begin{align}
\det(AB)&=\det(I) \\ \\
\underbrace{\det(A)}_{0}\det(B)&=\underbrace{\det(I)}_{1} \\ \\
0\cdot \det(B)&=1\;  \therefore\;  \nexists\;  \det(B)\qquad \blacksquare 
\end{align}
$$
Portanto, chegamos em uma contradição, tendo em vista que nenhum valor de $\det(B)$ satisfaria a equação. Por consequência, a matriz inversa de $A$ não existe.

#### $2.\;  \det(AB)=\det(A)\det(B)\quad \forall\;A,B\in\Bbb{R}^{2}$

**Demonstração.** Provaremos a proposição de forma algébrica. Desse modo, para as matrizes $A,B$ teremos
$$
\begin{align}
A&=\mycolv{a_{11} & a_{12}\\ a_{21} & a_{22}}\quad B=\mycolv{b_{11} & b_{12}\\ b_{21} & b_{22}} \\ \\
AB&=\mycolv{a_{11} & a_{12}\\a_{21} & a_{22}}\mycolv{b_{11} & b_{12}\\b_{21} & b_{22}}=\mycolv{a_{11}b_{11}+a_{12}b_{21} & a_{11}b_{12}+a_{12}b_{22}\\a_{21}b_{11}+a_{22}b_{21} & a_{21}b_{12}+a_{22}b_{22}} \\ \\
\det(AB)&=(a_{11}b_{11}+a_{12}b_{21})(a_{21}b_{12}+a_{22}b_{22})-(a_{21}b_{11}+a_{22}b_{21})(a_{11}b_{12}+a_{12}b_{22}) \\ \\
&=\cancel{a_{11}b_{11}(a_{21}b_{12}}+a_{22}b_{22})+\cancel{a_{12}b_{21}(a_{22}b_{22}}+a_{21}b_{12})-\cancel{a_{21}b_{11}(a_{11}b_{12}}+a_{12}b_{22})-\cancel{a_{22}b_{21}(a_{12}b_{22}}+a_{11}b_{12}) \\ \\ 
&=\underbrace{a_{11}a_{22}b_{11}b_{22}+a_{12}a_{21}b_{12}b_{21}}_{\alpha}-\underbrace{(a_{11}a_{22}b_{12}b_{21}+a_{12}a_{21}b_{11}b_{22})}_{\beta} \\ \\
\det(AB)&=\alpha-\beta
\end{align}
$$
Ao calcular o determinante de $AB$ obtemos a diferença entre dois produtos. Com a finalidade de simplificar os cálculos, resumi o primeiro à $\alpha$ e o segundo à $\beta$. Agora faremos o cálculo dos determinantes separadamente.
$$
\begin{align}
\det(A)&=a_{11}a_{22}-a_{12}a_{21} \\ \\
\det(B)&=b_{11}b_{22}-b_{12}b_{21} \\ \\
\det(A)\det(B)&=(a_{11}a_{22}-a_{12}a_{21})(b_{11}b_{22}-b_{12}b_{21}) \\ \\
&=a_{11}a_{22}b_{11}b_{22}-a_{11}a_{22}b_{12}b_{21}-a_{12}a_{21}b_{11}b_{22}+a_{12}a_{21}b_{12}b_{21} \\ \\
&=\underbrace{a_{11}a_{22}b_{11}b_{22}+a_{12}a_{21}b_{12}b_{21}}_{\alpha}-\underbrace{(a_{11}a_{22}b_{12}b_{21}+a_{12}a_{21}b_{11}b_{22})}_{\beta} \\ \\
\det(A)\det(B)&= \alpha-\beta \qquad \blacksquare 
\end{align}
$$
Como podemos observar, o resultado obtido é o mesmo em ambos os casos, isto é, $\alpha-\beta$ dada algumas manipulações algébricas.

#### $3.\; \det(A^{T})=\det(A)\quad \forall\;A\in\Bbb{R}^{2}$

$\textbf{Demonstração.}$ Provaremos que o determinante da matriz transposta é equivalente ao determinante da matriz original de forma algébrica para $\Bbb{R}^{2}$. Dada uma matriz genérica $A$ e sua inversa $A^{T}$
$$
\begin{align}
A=\mycolv{a_{11} & a_{12}\\a_{21} & a_{22}}\qquad A^{T}=\mycolv{a_{11} & a_{21}\\a_{12} & a_{22}}
\end{align}
$$
O determinante de ambas matrizes correspondem aos produtos
$$
\begin{align}
\det(A)&=a_{11}a_{22}-a_{12}a_{21} \\ \\
\det(A^{T})&=a_{11}a_{22}-a_{21}a_{12}\qquad \blacksquare
\end{align}
$$
Como podemos perceber, a inversão dos fatores na diagonal secundária não influencia o resultado do determinante pois a multiplicação é comutativa. Assim sendo, ao calcular o determinante obtemos o mesmo resultado. 

#### $4.\; \det(\lambda A)=\lambda^{2}\det(A)$

$\textbf{Demonstração.}$ Provaremos que o determinante de um escalar $\lambda$ multiplicado por uma matriz genérica $A$ é equivalente ao quadrado do coeficiente escalar $\lambda^{2}$ multiplicado pelo determinante dessa matriz de forma algébrica.
$$
\begin{align}
\lambda A&=\lambda\mycolv{a_{11} & a_{12}\\a_{21} & a_{22}} \\ \\
\det(\lambda A)&=(\lambda a_{11}\cdot \lambda a_{22})-(\lambda a_{12}\cdot \lambda a_{21}) \\ \\
&=\lambda^{2}(a_{11}a_{22}-a_{12}a_{21}) \\ \\
&=\lambda^{2}\det(A)\qquad \blacksquare 
\end{align}
$$
Assim sendo, o determinante de uma matriz genérica $A$ multiplicada por um escalar $\lambda$ equivale a $\lambda^{2}$ multiplicado pelo determinante de $A$.

## $\texttt{Fórmula geral.}$



