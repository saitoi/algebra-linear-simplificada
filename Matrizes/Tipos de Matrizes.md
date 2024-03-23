# Tipos de Matrizes

Nas seções abaixo, iremos analisar as matrizes especiais e ortogonais ou base ortonormais.

## Matrizes Especiais

> **Matriz de Identidade**. Matriz quadrada em que todos os elementos da diagonal principal são $1$ e todos os outros são nulos.

Denotada por $I$ ou $I_{n}$ quando se trata de uma matriz $n\times n$. Aqui está um exemplo da matriz $I_{4}$

```math
\begin{align}
I_{4}=\begin{bmatrix}1 & 0 & 0 & 0 \\0 & 1 & 0 & 0 \\0 & 0 & 1 & 0 \\0 & 0 & 0 & 1\end{bmatrix}
\end{align}
```

> **Matriz Nula**. Matriz em que todas suas entradas são iguais a zero.

> **Matriz Elementar**. Matriz identidade que contém uma outra posição $(i,j)$ não nula e fora da diagonal.

Denotamos uma matriz elementar cuja entrada não nula fora da diagonal está na $i$-ésima linha e $j$-ésima coluna é ocupada pelo número real $\alpha$ será denotada $L_{r,s}(\alpha)$. Por exemplo,

```math
\begin{align}
L_{1,3}(-5)=\begin{bmatrix}1 & 0 & -5 \\0 & 1 & 0 \\0 & 0 & 1\end{bmatrix}\quad \text{e}\quad L_{3,2}(9)=\begin{bmatrix}1 & 0 & 0 \\0 & 1 & 0 \\0 & 9 & 1\end{bmatrix}  
\end{align}
```

> **Matriz Triangular**. Matriz quadrada em que todos os elementos acima ou abaixo da diagonal principal são nulos, sendo divididas entre matriz triangular superior e matriz triangular inferior.

Dizemos que uma matriz $U$ é *triangular superior* se todas as entradas abaixo da diagonal principal são nulas, isto é, se $U_{i,j}=0$ sempre que $i<j$. Analogamente, $L$ é dita uma matriz *triangular inferior* acima da diagonal principal são nulas, o que equivale dizer que $L_{i,j}=0$ quando $i>j$. Aqui estão os exemplos citados

```math
\begin{align}
U=\begin{bmatrix}a_{11} & a_{12} & a_{13} \\0 & a_{22} & a_{23} \\0 & 0 & a_{33}\end{bmatrix}\quad \text{e}\quad L=\begin{bmatrix}b_{11} & 0 & 0 \\b_{21} & b_{22} & 0 \\b_{31} & b_{32} & b_{33}\end{bmatrix}  
\end{align}
```

> **Matriz Simétrica**. Matriz quadrada de tamanho $n\times n$ em que suas entradas satisfazem $a_{i,j}=a_{j,i}$ para todo $1\leq i\leq j\leq n$. Por outro lado, uma matriz é dita antissimétrica quando $a_{i,j}=-a_{j,i}$ para todo $1\leq i\leq j\leq n$.

Aqui está um exemplo de uma matriz simétrica e outra antissimétrica

```math
\begin{align}
\begin{bmatrix}1 & 2 & 3 \\2 & 4 & 5 \\3 & 5 & 6\end{bmatrix}\quad \text{e}\quad \begin{bmatrix}0 & 2 & 3 \\-2 & 0 & -5 \\-3 & 5 & 0\end{bmatrix}  
\end{align}
```

## Matriz Ortogonal e Ortonormal

> **Matriz Ortogonal**.  Matriz quadrada em que os vetores colunas são vetores ortogonais entre si e formam uma base ortonormal do plano.

Aqui está um exemplo da matriz $H$ ortogonal e de reflexão.

```math
\begin{align}
H=\begin{bmatrix}\dfrac{1}{\sqrt{2}} & \dfrac{1}{\sqrt{2}} \\ \dfrac{1}{\sqrt{2}} & -\dfrac{1}{\sqrt{2}}\end{bmatrix}
\end{align}
```

## Matriz de Permutação

> **Definição**. Matriz quadrada empregada para permutar as linhas da matriz original $A$.

Para formar a matriz de permutação, basta pegarmos a identidade e modificá-la de acordo com a permutação desejada. Por exemplo, uma matriz que troca as primeiras duas linhas de uma matriz 3x3 seria:

```math
\begin{align}
P=\begin{bmatrix}0 & 1 & 0 \\1 & 0 & 0 \\0 & 0 & 1\end{bmatrix}
\end{align}
```

Esta matriz $P$, quando multiplicada por uma matriz $A$ qualquer, resultará na troca das primeiras duas linhas de $A$.
