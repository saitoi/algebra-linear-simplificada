# Determinante

> **Definição.** Grandeza escalar associada a uma matriz quadrada que descreve o comportamento do volume ou área (depende da dimensão) em uma transformação.

## Definição Recursiva

Seja $A$ uma matriz $n\times n$, definimos o *j-ésimo cofator* de $A$ como sendo a matriz obtida ao retirarmos a primeira linha e sua *j-ésima coluna*. Essa matriz é denotada por $\widehat{A}_{j}$ e possui tamanho $(n-1)\times(n-1)$.

O caso base corresponde a $n=1$, ou seja, se trata de uma matriz $1\times 1$ cujo determinante é o único elemento da matriz. Feito isso, definimos os casos sucessores $(n\geq 2)$ como

```math
\det(A)=a_{1,1}\det(\widehat{A}_{1})-a_{1,2}\det(\widehat{A}_{2})+a_{1,3}\det(\widehat{A}_{3})-\dots+(-1)^{n-1}a_{1,n}\det(\widehat{A}_{n})\tag{1}
```

Como exemplo, suponha a matriz $A$ dada por

```math
\begin{align}
A=\begin{bmatrix}a_{1,1} & a_{1,2} \\a_{2,1} & a_{2,2}\end{bmatrix}
\end{align}
```

E seus cofatores correspondem a

```math
\widehat{A}_{1}=\begin{bmatrix}a_{2,2}\end{bmatrix}\quad \text{e}\quad \widehat{A}_{2}=\begin{bmatrix}a_{2,1}\end{bmatrix},
```

Por fim, segundo a fórmula recursiva teremos

```math
\det(A)=a_{1,1}\det(\widehat{A}_{1})-a_{1,2}\det(\widehat{A}_{2})=a_{1,1}a_{2,2}-a_{1,2}a_{2,1}.
```

## Propriedades

Aqui estão algumas das principais propriedades dos determinantes. De antemão, considere matrizes genéricas $A,B$.

#### 1. Uma matriz de transformação não possui inversa **se, e somente se,** seu determinante for zero.

**Demonstração da ida.** 
**Demonstração da volta.** Suponha a matriz de transformação $A$ com determinante nulo e sua inversa $B$. Segundo a definição de matriz inversa, temos que a matriz $A$ multiplicada por $B$ resultaria na identidade.

```math
AB=I
```

Podemos aplicar o determinante em ambos os lados da expressão e teremos

```math
\begin{align}
\det(AB)&=\det(I) \\ \\
\underbrace{\det(A)}_{0}\det(B)&=\underbrace{\det(I)}_{1} \\ \\
0\cdot \det(B)&=1\;  \therefore\;  \nexists\;  \det(B)\qquad \blacksquare 
\end{align}
```

Portanto, chegamos em uma contradição, tendo em vista que nenhum valor de $\det(B)$ satisfaria a equação. Por consequência, a matriz inversa de $A$ não existe.

#### 2. $\det(AB)=\det(A)\det(B)\quad \forall\;A,B\in\Bbb{R}^{2}$

**Demonstração.** Provaremos a proposição de forma algébrica. Desse modo, para as matrizes $A,B$ teremos

```math
\begin{align}
A&=\begin{bmatrix}a_{11} & a_{12}\\ a_{21} & a_{22}\end{bmatrix}\quad B=\begin{bmatrix}b_{11} & b_{12}\\ b_{21} & b_{22}\end{bmatrix} \\ \\
AB&=\begin{bmatrix}a_{11}b_{11}+a_{12}b_{21} & a_{11}b_{12}+a_{12}b_{22}\\a_{21}b_{11}+a_{22}b_{21} & a_{21}b_{12}+a_{22}b_{22}\end{bmatrix} \\ \\
\det(AB)&=(a_{11}b_{11}+a_{12}b_{21})(a_{21}b_{12}+a_{22}b_{22})-(a_{21}b_{11}+a_{22}b_{21})(a_{11}b_{12}+a_{12}b_{22}) \\ \\
&=a_{11}a_{22}b_{11}b_{22}+a_{12}a_{21}b_{21}b_{12}-a_{21}a_{12}b_{11}b_{22}-a_{22}a_{11}b_{12}b_{21} \\ \\
&=(a_{11}a_{22}-a_{12}a_{21})(b_{11}b_{22}-b_{12}b_{21}) \\ \\
\det(A)\det(B)&=(a_{11}a_{22}-a_{12}a_{21})(b_{11}b_{22}-b_{12}b_{21}) \\ \\
&=\det(A)\det(B) \qquad \blacksquare
\end{align}
```

#### 3. $\det(A^{T})=\det(A)\quad \forall\;A\in\Bbb{R}^{2}$

**Demonstração.** Para a matriz $A$ e sua transposta $A^T$, temos:

```math
\begin{align}
A&=\begin{bmatrix}a_{11} & a_{12}\\a_{21} & a_{22}\end{bmatrix}\qquad A^{T}=\begin{bmatrix}a_{11} & a_{21}\\a_{12} & a_{22}\end{bmatrix} \\ \\
\det(A)&=a_{11}a_{22}-a_{12}a_{21} \\ \\
\det(A^{T})&=a_{11}a_{22}-a_{21}a_{12} \\ \\
&=\det(A) \qquad \blacksquare
\end{align}
```

#### 4. $\det(\lambda A)=\lambda^{n}\det(A)$ para uma matriz $n \times n$

**Demonstração.** Para um escalar $\lambda$ e uma matriz $A$ $n \times n$:

```math
\begin{align}
\lambda A&=\lambda\begin{bmatrix}a_{11} & a_{12}\\a_{21} & a_{22}\end{bmatrix} \\ \\
\det(\lambda A)&=\lambda^n(a_{11}a_{22}-a_{12}a_{21}) \\ \\
&=\lambda^n\det(A) \qquad \blacksquare
\end{align}
```

Esta correção reflete a generalização para matrizes $n \times n$, onde o fator $\lambda^{n}$ é aplicado ao determinante original da matriz $A$.
