# Resolução Sistema Linear

[Estudo Dirigido 2](/Materiais/Estudo%20Dirigido%202.pdf)

# Resolução

1. Dada a seguinte matriz: $A=\begin{bmatrix}1 & 3 & 3 & 2 \\2 & 6 & 9 & 7 \\ -1 & -3 & 3 & 4\end{bmatrix}$

1. $(a).$ Essa matriz representa uma transformação de $\Bbb{R}^{N}$ a $\Bbb{R}^{M}$, explique $N$ e $M$.

A matriz de transformação $A$ converte vetores do subespaço de origem $\Bbb{R}^{4}$ para o $\Bbb{R}^{3}$ e, portanto, os índices $N$ e $M$ valem, respectivamente, 4 e 3. Isso pode ser evidenciado por meio da **regra de multiplicação de matrizes** segundo a qual duas matrizes podem ser multiplicadas se, e somente se, o número de colunas da primeira for igual ao número de colunas da segunda. Nesse sentido, se desejarmos aplicar a transformação $A$ a um vetor $v$ qualquer, este terá 4 linhas e, por consequência, pertencerá ao subespaço $\Bbb{R}^{4}$. Por fim, como associamos cada linha de $A$ a uma coluna em $v$, o vetor transformado conterá 3 linhas e uma coluna, pertencendo, assim, ao subespaço $\Bbb{R}^{3}$.

***

1. $(b).$ Encontre a decomposição $LU$. Apresente passo a passo de forma algorítmica.

A decomposição $LU$ da matriz $A$ será feita por meio do algoritmo de eliminação gaussiana aplicada à $A$ e para cada elemento eliminado, teremos uma matriz elementar correspondente. Em síntese, as matrizes $L$ e $U$ serão preenchidas simultaneamente.

Em um primeiro momento, escolheremos $a_{11}$ como pivô e eliminaremos os elementos abaixo. Começando pela linha 2,

```math
\begin{flalign}
&1.\;  L_{2}=-2(L_{1})+L_{2}&& \\ \\
&L_{21}(-2)\cdot A=\begin{bmatrix}1 & 3 & 3 & 2 \\2 & 6 & 9 & 7 \\ -1 & -3 & 3 & 4\end{bmatrix}\to \begin{bmatrix}1 & 3 & 3 & 2 \\0 & 0 & 3 & 3 \\ -1 & -3 & 3 & 4\end{bmatrix} \\ \\
&L_{21}^{-1}(-2)=L_{21}(2)=\begin{bmatrix}1 & 0 & 0 \\2 & 1 & 0 \\0 & 0 & 1\end{bmatrix} \\ \\
\end{flalign}
```

Feito isso, usaremos $a_{11}$ como pivô novamente a fim de eliminar o termo $a_{31}$.

```math
\begin{flalign}
&2.\; L_{3}=1(L_{1})+L_{3}&& \\ \\
&L_{31}(1)\cdot \begin{bmatrix}1 & 3 & 3 & 2 \\0 & 0 & 3 & 3 \\ -1 & -3 & 3 & 4\end{bmatrix}\to \begin{bmatrix}1 & 3 & 3 & 2 \\0 & 0 & 3 & 3 \\0 & 0 & 6 & 6\end{bmatrix} \\ \\
&L_{31}^{-1}(-1) \cdot L_{21}(2) = L_{31}(1) \cdot L_{21}(2)=\begin{bmatrix}1 & 0 & 0 \\2 & 1 & 0 \\ -1 & 0 & 1\end{bmatrix} \\ \\
\end{flalign}
```

O último passo será eliminar a terceira linha por completo selecionando o elemento $a_{22}$ como pivô.

```math
\begin{flalign}
&3.\; L_{3}=-2(L_{2})+L_{3}&&  \\ \\
&L_{32}(-2)\cdot \begin{bmatrix}1 & 3 & 3 & 2 \\0 & 0 & 3 & 3 \\0 & 0 & 6 & 6\end{bmatrix}\to \boxed{\begin{bmatrix}1 & 3 & 3 & 2 \\0 & 0 & 3 & 3 \\0 & 0 & 0 & 0\end{bmatrix}=U} \\ \\
&L_{32}^{-1}(-2) \cdot L_{31}(1) \cdot L_{21}(2) = L_{32}(2) \cdot L_{31}(1) \cdot L_{21}(2)=\boxed{\begin{bmatrix}1 & 0 & 0 \\2 & 1 & 0 \\ -1 & 2 & 1\end{bmatrix}=L} \\ \\
\end{flalign}
```

Por fim, obtemos a matriz escalonada $U$ e o produto de todas as elementares $L$ explicitadas acima.
