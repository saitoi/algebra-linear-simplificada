---
dg-home: true
dg-publish: true
---
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
# Autovalores e Autovetores

> $\textit{Definição.}$ Autovetores (ou $\textit{eigenvectors}$) se referem ao conjunto de vetores cuja direção não varia após uma transformação linear. Por outro lado, os autovalores (ou $\textit{eigenvalues}$) correspondem às grandezas escalares que descrevem o escalonamento dos autovetores após uma transformação.

Seja $T$ um operador linear do plano. Um $\textit{autovetor}$ de $T$, associado ao $\textit{autovalor}\; \lambda \in\Bbb{R}$ é um vetor **não nulo** $v$ do plano que satisfaz a expressão.
$$
T(u)=\lambda v\tag{1}
$$
Se $\mu$ é um número real qualquer, então
$$
T(\mu v)=\mu T(v)=\mu(\lambda v)=\lambda(\mu v) 
$$
nos mostrando que qualquer múltiplo de $v$ também é um autovetor de $T$ associado a $\lambda$.

## $\texttt{Operadores Lineares.}$

Podemos determinar os autovetores e autovalores associados a cada um dos principais operadores lineares.

1. **Rotação.** Os autovetores de uma rotação são todos aqueles cujo ângulo de rotação equivale a um múltiplo de $\pi$. Mais precisamente, os autovetores cujo ângulo de rotação é um múltiplo de $2\pi$ são todos os vetores não nulos associados ao autovetor $\lambda=1$. Por outro lado, se o fator multiplicador de $\pi$ for ímpar, então todos os vetores são autovetores, porém invertidos e associados ao autovalor $\lambda=-1$.
2. **Projeção.** Se considerarmos uma projeção sobre a reta $l$, sabemos que todos os vetores pertencentes a $l$ são autovetores associados ao autovalor um. No entanto, se levarmos em conta a reta ortogonal a $l$, teremos autovetores associados ao autovalor zero. 
3. **Reflexão.** Possui um resultado semelhante, isto é, os vetores pertencentes ao espelho são autovetores associados a um, enquanto os vetores ortogonais ao espelho são autovetores associados a $-1$.
4. **Cisalhamento.** Suponha o cisalhamento $S$ que deixa fixo os vetores múltiplos de $e_{1}$ e move $e_{2}$ para $e_{2}+e_{1}c$, para algum real não nulo $c$. Nesse sentido, os vetores múltiplos a $e_{1}$ são autovetores associados a um, não havendo outros autovetores possíveis em função da inclinação de $e_{2}$. A prova dessa proposição se encontra na [[Apostila Atualizada Álgebra Linear - Collier.pdf|apostila do Collier]].

## $\texttt{Calculando Autovetores e Autovalores.}$

Seja $T$ um operador linear e sua matriz na base canônica representada por:
$$
A=\mycolv{a_{11} & a_{12} \\ a_{21} & a_{22}}
$$
Assim sendo, a equação $T(v)=\lambda v$ empregada para definir $v\neq 0$ como autovetor associado ao autovalor $\lambda$ pode ser descrita na forma
$$
\begin{align}
\mycolv{a_{11} & a_{12} \\ a_{21} & a_{22}}\mycolv{x\\y}=\lambda\cdot \mycolv{x\\y}\tag{1} \\ \\
a_{11}x+a_{12}y=\lambda x \\ \\
a_{21}x+a_{22}y=\lambda y \\
\end{align}
$$
Como os termos constantes são nulos em ambas as equações, temos como solução possível $x,y=0$ (o que não pode ser autovetor de $T$). Portanto, para encontrar os autovetores de $T$, basta que o sistema possua mais de uma solução, ou seja, se as equações são múltiplas uma da outra. Desse modo, suponha a seguinte expressão
$$
\begin{align}
&(a_{11}-\lambda)x+a_{12}y=\mu(a_{21}x+(a_{22}-\lambda)y) \\ \\
&\begin{rcases}
a_{11}-\lambda=\mu a_{21} \\ \\
a_{12}=\mu(a_{22}-\lambda)
\end{rcases}\quad  \mu=\dfrac{a_{11}-\lambda}{a_{21}}=\dfrac{a_{12}}{a_{22}-\lambda}
\end{align}
$$
Por fim, obtemos
$$
(a_{11}-\lambda)(a_{22}-\lambda)=a_{21}a_{12}
$$
O que equivale a
$$
\lambda^{2}-(a_{11}+a_{22})\lambda+(a_{11}a_{22}-a_{21}a_{12})=0
$$
De modo que qualquer autovalor de $\lambda$ de $T$ é raiz da equação quadrática $p_{A}(t)=0$, em que
$$
p_{A}(t)=t^{2}-(a_{11}+a_{22})\lambda+(a_{11}a_{22}-a_{21}a_{12})
$$
em que $p_{A}(t)$ é o $\textit{polinômio característico}$ de $A$ (e de $T$). Podemos usar determinantes para escrever o polinômio característico de forma compacta, tal como abaixo
$$
\begin{align}
p_{A}(t)=\det(A-tI)=\det \mycolv{a_{11}-t & a_{12} \\ a_{21} & a_{22}-t}
\end{align}
$$
em que $I$ denota a matriz de identidade de $\Bbb{R}^{2}$. Por fim, para determinarmos o autovalor de uma matriz $A$ qualquer, basta substituir os valores na matriz e resolver a equação do segundo grau para $t$. Tendo encontrado o autovalor $t$ da matriz, podemos substituir em $(1)$ todos os valores correspondentes, resolvendo um sistema para as componentes $x,y$.

Por fim, tendo descoberto os autovalores podemos determinar o conjunto de autovetores associados a cada um deles. Desse modo, retornaremos à expressão $(1)$ no topo.
$$
\begin{align}
T(u)&=\lambda u \\ \\
T(u)-\lambda u&=0 \\ \\
\underbrace{(T-\lambda I)}_{\det=0}u&=0 \\ \\
\end{align}
$$
Como descobrimos o autovalor $\lambda$, podemos determinar o conjunto de autovetores $u$ por meio disso. Assim sendo teremos a seguinte expressão
$$
\begin{align}
\mycolv{a_{11}-\lambda & a_{12}\\a_{21} & a_{22}-\lambda}\mycolv{x\\y}&=\mycolv{0\\0}\tag{2} \\ \\
(a_{11}-\lambda)x+a_{12}y&=0 \\ \\
a_{21}x+(a_{22}-\lambda)y&=0
\end{align}
$$
Como já determinarmos $\lambda$, nos resta identificar $x,y$ que, usualmente, corresponde a um conjunto de vetores que satisfazem a expressão dada.

- [i] Poderíamos também calcular os autovetores da seguinte forma
$$
\begin{align}
\mycolv{a_{11} & a_{12} \\a_{21} & a_{22}}\mycolv{x \\y}=\mycolv{x \\y}\lambda_{1}\quad \text{e}\quad  \mycolv{a_{11} & a_{12} \\a_{21} & a_{22}}\mycolv{x \\y}=\mycolv{x \\y}\lambda_{2} 
\end{align}
$$
Ao resolver esse sistema linear, encontraremos os mesmos autovetores em relação aos obtidos na expressão $(2)$.


