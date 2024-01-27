---
aliases:
  - ed_2
tags:
  - ALA/trabalho
date: 2023-10-22
time: 11:06
complete:
---
### Nome: Pedro Henrique Honorio Saito
### DRE: 122149392
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
# $\texttt{Resolução Sistema Linear.}$

![[Estudo Dirigido 2.pdf]]

# $\texttt{Resolução.}$

1. Dada a seguinte matriz: $A=\mycolv{1 & 3 & 3 & 2 \\2 & 6 & 9 & 7 \\ -1 & -3 & 3 & 4}$

1. $(a).$ Essa matriz representa uma transformação de $\Bbb{R}^{N}$ a $\Bbb{R}^{M}$ , explique $N$ e $M$.

A matriz de transformação $A$ converte vetores do subespaço de origem $\Bbb{R}^{4}$ para o $\Bbb{R}^{3}$ e, portanto, os índices $N$ e $M$ valem, respectivamente, 4 e 3. Isso pode ser evidenciado por meio da **regra de multiplicação de matrizes** segundo a qual duas matrizes podem ser multiplicadas se, e somente se, o número de colunas da primeira for igual ao número de colunas da segunda. Nesse sentido, se desejarmos aplicar a transformação $A$ a um vetor $v$ qualquer, este terá 4 linhas e, por consequência, pertencerá ao subespaço $\Bbb{R}^{4}$. Por fim, como associamos cada linha de $A$ a uma coluna em $v$, o vetor transformado conterá 3 linhas e uma coluna, pertencendo, assim, ao subespaço $\Bbb{R}^{3}$.

***

1. $(b).$ Encontre a decomposição $LU$. Apresente passo a passo de forma algorítmica.

A decomposição $LU$ da matriz $A$ será feita por meio do algoritmo de eliminação gaussiana aplicada à $A$ e para cada elemento eliminado, teremos uma matriz elementar correspondente. Em síntese, as matrizes $L$ e $U$ serão preenchidas simultaneamente.

Em um primeiro momento, escolheremos $a_{11}$ como pivô e eliminaremos os elementos abaixo. Começando pela linha 2,
$$
\begin{flalign}
&1.\;  L_{2}=-2(L_{1})+L_{2}&& \\ \\
&L_{21}(-2)\cdot A=\mycolv{1 & 3 & 3 & 2 \\2 & 6 & 9 & 7 \\ -1 & -3 & 3 & 4}\to \mycolv{1 & 3 & 3 & 2 \\0 & 0 & 3 & 3 \\ -1 & -3 & 3 & 4} \\ \\
&L_{21}^{-1}(-2)=L_{21}(2)=\mycolv{1 & 0 & 0 \\2 & 1 & 0 \\0 & 0 & 1} \\ \\
\end{flalign}
$$
Feito isso, usaremos $a_{11}$ como pivô novamente a fim de eliminar o termo $a_{31}$.
$$
\begin{flalign}
&2.\; L_{3}=1(L_{1})+L_{3}&& \\ \\
&L_{31}(1)\cdot \mycolv{1 & 3 & 3 & 2 \\0 & 0 & 3 & 3 \\ -1 & -3 & 3 & 4}\to \mycolv{1 & 3 & 3 & 2 \\0 & 0 & 3 & 3 \\0 & 0 & 6 & 6} \\ \\
&L_{31}^{-1}(-1) \cdot L_{21}(2) = L_{31}(1) \cdot L_{21}(2)=\mycolv{1 & 0 & 0 \\2 & 1 & 0 \\ -1 & 0 & 1} \\ \\
\end{flalign}
$$
O último passo será eliminar a terceira linha por completo selecionando o elemento $a_{22}$ como pivô.
$$
\begin{flalign}
&3.\; L_{3}=-2(L_{2})+L_{3}&&  \\ \\
&L_{32}(-2)\cdot \mycolv{1 & 3 & 3 & 2 \\0 & 0 & 3 & 3 \\0 & 0 & 6 & 6}\to \boxed{\mycolv{1 & 3 & 3 & 2 \\0 & 0 & 3 & 3 \\0 & 0 & 0 & 0}=U} \\ \\
&L_{32}^{-1}(-2) \cdot L_{31}(-1) \cdot L_{21}(2) = L_{32}(2) \cdot L_{31}(-1) \cdot L_{21}(2)=\boxed{\mycolv{1 & 0 & 0 \\2 & 1 & 0 \\ -1 & 2 & 1}=L} \\ \\
\end{flalign}
$$
Por fim, obtemos a matriz escalonada $U$ e o produto de todas as elementares $L$ explicitadas acima.
