Substituindo o comando `mycolv` pelo indicado para representar matrizes na forma matricial, o texto ajustado ficaria assim:

---

# Matriz Inversa

> **Definição**. Refere-se à matriz que, quando multiplicada por outra, resulta na identidade.

Formalmente, uma matriz genérica $A$ possui uma inversa $B$ se, e somente se,

```math
AB=I\quad \text{e}\quad BA=I
```

Ou seja, o produto entre a matriz original e inversa resulta na matriz identidade (definida na dimensão das matrizes $A,B$).

## Fórmula geral

Dada uma matriz genérica de determinante não nulo

```math
\begin{align}
A=\begin{bmatrix}a_{11} & a_{12}\\a_{21} & a_{22}\end{bmatrix}
\end{align}
```

A inversa $A$ corresponde à seguinte matriz

```math
\begin{align}
\boxed{A^{-1}=\dfrac{1}{\det(A)}\begin{bmatrix}a_{22} & -a_{12}\\-a_{21} & a_{11}\end{bmatrix}}\tag{1}
\end{align}
```

$\textbf{Demonstração.}$ Podemos testar a hipótese: Dada a matriz genérica $A$, o produto entre $A$ e sua inversa deverá resultar na identidade. Portanto, teremos

```math
AA^{-1}=I
```

Em que $A^{-1}$ é definida pela expressão $(1)$. Calculando o produto, obteremos

```math
\begin{align}
AA^{-1}&=\begin{bmatrix}a_{11} & a_{12}\\a_{21} & a_{22}\end{bmatrix}\begin{bmatrix}a_{22} & -a_{12}\\ -a_{21} & a_{11}\end{bmatrix} \dfrac{1}{\det(A)} \\ \\
&=\begin{bmatrix}a_{11}a_{22}-a_{12}a_{21} & a_{11}(-a_{12})+a_{12}a_{11}\\ a_{21}a_{22}-a_{21}a_{22} & -a_{21}a_{12}+a_{22}a_{11}\end{bmatrix} \dfrac{1}{\det(A)}
\end{align}
```

Agora nos resta substituir o determinante $\det(A)$ na expressão do produto entre as matrizes. Desse modo, calcularemos ele primeiro

```math
\begin{align}
\det(A)=a_{11}a_{22}-a_{12}a_{21}
\end{align}
```

Substituindo, obteremos

```math
\begin{align}
&=\begin{bmatrix}1 & 0\\0 & 1\end{bmatrix}\qquad \blacksquare 
\end{align}
```

Como podemos perceber, chegamos à matriz identidade tendo feita a multiplicação $AA^{-1}$. Portanto, está provada a fórmula para se obter a matriz inversa de uma transformação $\Bbb{R}^{2}$.
