---
aliases:
  - gaussiana
  - decomposicao_LU
  - eliminacao_gaussiana
  - substituicao_reversa
tags:
  - ALA
  - P3
date: 2023-10-04
time: 18:05
complete:
---
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
# Eliminação Gaussiana e Decomposição LU

> $\textit{Definição.}$ *Algoritmo fundamental para a resolução de sistemas lineares que consiste em transformar o sistema atual em um triangular superior por meio de uma série de operações elementares.*

A operação elementar mencionada envolve multiplicar a primeira linha do sistema de equações por uma constante e somá-la à segunda expressão com o intuito de eliminar um dos termos.

## $\texttt{Eliminação em Matrizes (CLÁSSICA).}$

Ao contrário do método de solução de sistemas triangulares superiores por substituição, as variáveis desempenham um papel secundário no algoritmo de eliminação.

Usaremos o conceito de $\textit{matriz aumentada do sistema}$, por exemplo dado o seguinte sistema de equações
$$
\begin{align}
x+y+z+w=1  \\
2x+3y+z+5w=5  \\
x+7y-z+2w=3 \\
5x-y-3z+w=7
\end{align}
$$
a matriz aumentada corresponde a
$$
A = \left[\begin{array}{cccc|c}
1 & 1 & 1 & 1 & 1 \\
2 & 3 & 1 & 5 & 5 \\
1 & 7 & -1 & 2 & 3 \\
1 & 7 & -1 & 2 & 3 \\
5 & -1 & -3 & 1 & 7
\end{array}\right]
$$
Considerando as linhas de $A$ como matrizes $1\times 5$, a operação executada para se anular o primeiro coeficiente $m_{21}$ corresponde a substituir a segunda linha por ela mesma somada a $-2$ vezes a primeira linha:
$$
\begin{align}
\mycolv{2 & 3 & 1 & 5 & 5}-2\mycolv{1 & 1 & 1 & 1 & 1}=\mycolv{0 & 1 & -1 & 3 & -3}
\end{align}
$$
De um modo geral, se $L$ e $L'$ são duas linhas de uma matriz $M$ e $c$ é um número real, uma $\textit{operação elementar por linha}$ consiste em substituir $L'$ por $L'+cL$.

Posto isso, se repetimos o mesmo processo continuamente sobre a matriz $A$, obteremos a resolução do sistema.

$\textup{Propriedade.}$ *O determinante de uma matriz não muda quando uma de suas linhas é substituída por ela mesma mais um múltiplo de outra linha.*

## $\texttt{Eliminação (MODERNA).}$

Desse modo, retornando ao conceito de [[Tipos de Matrizes#^3f7ad4|matriz elementar]] podemos constatar que a matriz obtida após uma operação elementar de linha corresponde a multiplicar a matriz original por uma elementar.

Suponha a matriz abaixo
$$
A = \begin{bmatrix}
1 & 1 & 1 & 1 & 1 \\
2 & 3 & 1 & 5 & 5 \\
1 & 7 & -1 & 2 & 3 \\
5 & -1 & -3 & 1 & 7 \\
\end{bmatrix}
$$
Para solucioná-la, basta aplicarmos a sequência de operações abaixo:

| Operação por linha | matriz elementar |
|---|---|
| segunda linha menos o dobro da primeira | $L_{21}(-2)$ |
| terceira linha menos a primeira | $L_{31}(-1)$ |
| quarta linha menos o quíntuplo da primeira | $L_{41}(-5)$ |
| terceira linha menos o sêxtuplo da segunda | $L_{32}(-6)$ |
| quarta linha mais o sêxtuplo da segunda | $L_{42}(6)$ |
| quarta linha mais sete meios da terceira | $L_{43}(\frac{7}{2})$ |

De um modo geral, uma matriz elementar do tipo $L_{ij}(\alpha)$ realiza a multiplicação a linha $j$ pelo fator $\alpha$ e a soma desse resultado à linha $i$ para depois substituirmos a linha $i$ por esse resultado.

Por exemplo, ao aplicar $L_{21}(-2)$ à matriz $A$ teremos
$$
\begin{align}
A\cdot L_{21}(-2)=
\mycolv{1 & 1 & 1 & 1 & 1 \\
0 & 1 & -1 & 3 & 3 \\
1 & 7 & -1 & 2 & 3 \\
5 & -1 & -3 & 1 & 7}
\end{align}
$$
$\textup{Lema.}$ *Sejam $i$ e $j$ inteiros positivos distintos menores ou iguais a $n$ e $a$ um número real. A matriz elementar $L_{ij}(a)=I+aE_{ij}$ tem determinante igual a 1 e sua inversa é igual a $L_{ij}(-a).$*

No início vimos que as matrizes elementares nos permitem interpretar o resultado da eliminação gaussiana como uma decomposição de matrizes. Podemos generalizar esse resultado da seguinte forma:

Suponha uma matriz genérica $A$ que após sucessivas multiplicações por matrizes elementares do formato $L_{ij}(\alpha)$ se torna na matriz triangular superior $U$. Formalmente,
$$
L_{21}(\alpha_{1})\cdot L_{31}(\alpha_{2})\dots L_{ij}(\alpha_{i})\cdot A=U
$$
Segundo o lema acima, posso por exemplo multiplicar cada lado da equação por $L_{21}(\alpha_{1})^{-1}$ teremos
$$
\underbrace{(L_{21}(\alpha_{1})\cdot L_{21}(-\alpha_{1}))}_{I}\cdot L_{31}(\alpha_{1})\dots L_{ij}(\alpha_{i})\cdot A=U\cdot L_{21}(\alpha_{1})^{-1}
$$
Repetindo o processo a todas as matrizes elementares obteremos
$$
\begin{align}
A&=U\cdot L_{21}(-\alpha_{1})\cdot L_{31}(-\alpha_{2})\dots L_{ij}(-\alpha_{i}) \\ \\
A&=LU
\end{align}
$$
em que $L$ corresponde ao produto de matrizes elementares. Denominados isso de decomposição $LU$ como a expressão sugere.

## $\texttt{Eliminação Gaussiana.}$

Descrito anteriormente, resume-se à transformação da matriz original em uma triangular superior como método de resolução do sistema linear formado.

## $\texttt{Código.}$

```python
def eliminacaoGaussiana(A, b):
    n = len(b)
    U = A.astype(np.float64).copy()
    y = b.astype(np.float64).copy()

    for k in range(n - 1):
        pivot_row = np.argmax(np.abs(U[k:, k])) + k
        U[[k, pivot_row]] = U[[pivot_row, k]]
        y[k], y[pivot_row] = y[pivot_row], y[k]

        pivot_element = U[k, k]
        U[k, :] /= pivot_element
        y[k] /= pivot_element

        for i in range(k + 1, n):
            factor = U[i, k]
            U[i, k:] -= factor * U[k, k:]
            y[i] -= factor * y[k]
    return U, y
```

## $\texttt{Substituição Reversa.}$

O processo de substituição reversa corresponde à resolução da matriz triangular superior obtida por meio da eliminação gaussiana.

### $\texttt{Pseudocódigo.}$

```c
substituicaoReversa(matriz, y)
	comprimento = len(y)
	solucoes = np.zero(comprimento)
	
	para i de n-1 até -1
		soma = 0
		para j de i+1 até n
			soma += matriz[i][j]
		solucoes[i] = (y[i]-soma) / matriz[i][i]
	retorne solucoes	
```

Em primeiro lugar, irei explicar o que está acontecendo no problema acima. Temos uma matriz aleatória $A$ de tamanho $3\times 3$ generada por `np.random.rand(3,3)` e sabemos que a multiplicação dela por um vetor $x_{i}$ para $i=\{1,2,3\}$ nos fornece os vetores da base de $\Bbb{R}^{3}$, ou seja, $e_{1},e_{2},e_{3}$. Posto isso, devemos provar que os vetores $x_{i}$ correspondem às colunas da inversa de $A$.

$\textbf{Explicação.}$ Podemos demonstrar essa relação de forma algébrica. Com efeito, suponha uma matriz genérica $A$ e sua inversa $A^{-1}$ dadas por
$$
\begin{align}
A=\mycolv{a_{1} & a_{2} & a_{3} \\b_{1} & b_{2} & b_{3} \\c_{1} & c_{2} & c_{3}}\quad \text{e}\quad A^{-1}=\mycolv{i_{1} & j_{1} & k_{1} \\i_{2} & j_{2} & k_{2} \\i_{3} & j_{3} & k_{3}}  
\end{align}
$$
Posto isso, iremos analisar o resultado obtido a partir do produto $A\cdot x_{i}$ para $i=\{1,2,3\}$, para isso veremos o primeiro caso $A\cdot x_{1}$
$$
\begin{align}
A\cdot x_{1}=\mycolv{a_{1} & a_{2} & a_{3} \\b_{1} & b_{2} & b_{3} \\c_{1} & c_{2} & c_{3}}\mycolv{\alpha_{1} \\\alpha_{2} \\\alpha_{3}}=\mycolv{1 \\0 \\0}\implies 
\begin{cases}
a_{1}\alpha_{1}+a_{2}\alpha_{2}+a_{3}\alpha_{3}=1 \\ \\
b_{1}\alpha+b_{2}\alpha_{2}+b_{3}\alpha_{3}=0 \\ \\
c_{1}\alpha_{1}+c_{2}\alpha_{2}+c_{3}\alpha_{3}=0
\end{cases}
\end{align}
$$
Isto é, considerando $x_{1}=[\alpha_{1}\quad \alpha_{2}\quad \alpha_{3}]^{t}$. Se repetirmos o processo para $x_{2}\text{ e }x_{3}$ veremos alguma correlação com o produto $A\cdot A^{-1}$, aqui está um exemplo
$$
\begin{align}
A\cdot A^{-1}=\mycolv{a_{1} & a_{2} & a_{3} \\b_{1} & b_{2} & b_{3} \\c_{1} & c_{2} & c_{3}}\mycolv{i_{1} & j_{1} & k_{1} \\i_{2} & j_{2} & k_{2} \\i_{3} & j_{3} & k_{3}}=\mycolv{1 & 0 & 0 \\0 & \ddots & \vdots \\0 & \dots & 1}
\end{align}
$$
Se você notar, a multiplicação da primeira coluna da matriz $A$ com a primeira linha de $A^{-1}$ equivale a $1$, isto é, o mesmo resultado obtido para o primeiro produto de $A\cdot x_{1}$. Podemos colocar da seguinte forma
$$
\begin{align}
1^{\underline{\text{a}}}\text{ linha de $A$ com a 1}&^\underline{\text{a}}\text{ coluna de $A^{-1}$}=1 \\
1^\underline{\text{a}}\text{ linha de $A$ com a 2}&^\underline{\text{a}}\text{ coluna de $A^{-1}$}=0 \\
&\vdots \\
2^\underline{\text{a}} \text{ linha de $A$ com a 1}&^\underline{\text{a}} \text{ coluna de $A^{-1}$}=0 \\
2^\underline{\text{a}} \text{ linha de $A$ com a 2}&^\underline{\text{a}} \text{ coluna de $A^{-1}$}=1 \\
&\vdots \\
3^\underline{\text{a}} \text{ linha de $A$ com a 2}&^\underline{\text{a}} \text{ coluna de $A^{-1}$}=0 \\
3^\underline{\text{a}} \text{linha de $A$ com a 3}&^\underline{\text{a}} \text{ coluna de $A^{-1}$}=1
\end{align}
$$
Assim sendo, observamos que o produto $A\cdot x_{1}$ tem o mesmo efeito que parte da multiplicação $A\cdot A^{-1}$ e o mesmo vale para $x_{2}$ e $x_{3}$. Por fim, concluímos que 
