---
aliases:
  - simulado_1
tags:
  - ALA
date: 2023-09-19
time: 08:53
complete: true
---
### Nome: Pedro Henrique Honorio Saito
### DRE: 122149392
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
# $\texttt{Simulado.}$

![[SimuladoP1.pdf]]

# $\texttt{Resolução.}$

1. Suponha as matrizes de rotação $A,B$ definidas pelos ângulos $\theta,\omega$ respectivamente.
$$
\begin{align}
A=\mycolv{\cos(\theta) & -\sin(\theta)\\ \sin(\theta) & \cos(\theta)}\quad \quad  B=\mycolv{\cos(\omega) & -\sin(\omega) \\ \sin(\omega) & \cos(\omega)} 
\end{align}
$$
Posto isso, aplicaremos a multiplicação entre matrizes para obter a matriz resultante $AB$.
$$
\begin{align}
A\cdot B&=\mycolv{\cos(\theta) & -\sin(\theta)\\ \sin(\theta) & \cos(\theta)}\mycolv{\cos(\omega) & -\sin(\omega) \\ \sin(\omega) & \cos(\omega)} \\ \\
&=\mycolv{\cos(\theta)\cdot\cos(\omega)-\sin(\theta)\cdot\sin(\omega) & (-1)[\sin(\omega)\cdot\cos(\theta)+\sin(\theta)\cdot \cos(\omega)] \\ \sin(\theta)\cdot \cos(\omega)+\sin(\omega)\cdot \cos(\theta) & \cos(\omega)\cdot \cos (\theta)-\sin(\theta)\cdot \sin(\omega)}
\end{align}
$$
Pela identidade trigonométrica da soma e da subtração de senos e cossenos, podemos afirmar que
$$
\begin{align}
&=\mycolv{\cos(\theta)\cdot\cos(\omega)-\sin(\theta)\cdot\sin(\omega) & (-1)[\sin(\omega)\cdot\cos(\theta)+\sin(\theta)\cdot \cos(\omega)] \\ \sin(\theta)\cdot \cos(\omega)+\sin(\omega)\cdot \cos(\theta) & \cos(\omega)\cdot \cos (\theta)-\sin(\theta)\cdot \sin(\omega)} \\ \\
&= \mycolv{\cos(\theta+\omega) & -1\cdot(\sin(\theta+\omega)) \\ \sin(\theta+\omega) & \cos(\omega+\theta)}
\end{align}
$$
Assim sendo, obtemos uma matriz de rotação com ângulo $(\theta+\omega)$ que corresponde à multiplicação $A\cdot B$ solicitada na questão.

***

1. $(b)$ Tendo feita a multiplicação $A\cdot B$, apenas substituiremos $\theta$ por $\omega$ no resultado acima e obteremos o produto $B\cdot A$.
$$
\begin{align}
&=\mycolv{\cos(\omega)\cdot\cos(\theta)-\sin(\omega)\cdot\sin(\theta) & (-1)[\sin(\theta)\cdot\cos(\omega)+\sin(\omega)\cdot \cos(\theta)] \\ \sin(\omega)\cdot \cos(\theta)+\sin(\theta)\cdot \cos(\omega) & \cos(\theta)\cdot \cos (\omega)-\sin(\omega)\cdot \sin(\theta)} \\ \\
&=\mycolv{\cos(\omega+\theta) & (-1)\cdot \sin(\omega+\theta) \\ \sin(\omega+\theta) & \cos(\omega+\theta)}
\end{align}
$$
Como podemos ver, o resultado em si obtido é o mesmo fora algumas mudanças de ordem entre os ângulos $\theta,\omega$.

***

1. $(c)$ Tendo em vista que $A\cdot A^{-1}=I$, podemos tentar determinar a matriz inversa $A^{-1}$ da seguinte forma
$$
\begin{align}
\mycolv{\cos(\theta) & -\sin(\theta)\\ \sin(\theta) & \cos(\theta)}\mycolv{a_{11} & a_{12} \\ a_{21}  & a_{22}}&=\mycolv{1 & 0\\0 & 1} \\ \\
a_{11}\cos(\theta)-a_{21}\sin(\theta)&=1\tag{1} \\ \\
a_{12}\cos(\theta)-a_{22}\sin(\theta)&=0\tag{2} \\ \\
a_{11}\sin(\theta)+a_{21}\cos(\theta)&=0\tag{3} \\ \\
a_{12}\sin(\theta)+a_{22}\cos(\theta)&=1\tag{4}
\end{align}
$$
Podemos observar que nas expressões $(1)$ e $(4)$ só existe uma possibilidade para os coeficientes de $\cos(\theta)$ e $\sin(\theta)$, isto é, eles precisam resultar na identidade trigonométrica $\cos ^{2}(\theta)+\sin ^{2}(\theta)$. Assim sendo, realizando as seguintes substituições
$$
\begin{align}
a_{11}=\cos(\theta)\quad a_{21}=-\sin(\theta), \\ \\
(\cos(\theta))\cos(\theta)-(-\sin (\theta))\sin(\theta)=1\tag{1} \\ \\
\cos ^{2}(\theta)+\sin ^{2}(\theta)=1 \\ \\
a_{12}=\sin(\theta)\quad a_{22}=\cos(\theta),\\ \\
(\sin(\theta))\sin(\theta)+(\cos(\theta))\cos(\theta)=1\tag{4} \\ \\
\cos ^{2}(\theta)+\sin ^{2}(\theta)=1
\end{align}
$$
Por fim, podemos montar a matriz inversa $A^{-1}$.
$$
\begin{align}
A^{-1}=\mycolv{\cos(\theta) & \sin(\theta)\\ -\sin(\theta) & \cos(\theta)}
\end{align}
$$

***

1. $(d)$ Para verificar se a matriz $A$ possui colunas ortonormais, calcularemos o produto interno entre suas colunas, considerando cada uma delas como um vetor separadamente. Assim sendo, teremos
$$
\begin{align}
&=\mathbf{[}\cos(\theta)\quad \sin(\theta) \mathbf{]}\mycolv{-\sin(\theta)\\ \cos(\theta)} \\ \\
&=-\sin(\theta)\cos(\theta)+\sin(\theta)(\cos(\theta) \\ \\
&=0
\end{align}
$$
Desse modo, chegamos à conclusão que a matriz 

***

### $\texttt{Preciso acabar ainda..}$

2. $(a)$ Para determinar o espelho $u$, empregaremos a expressão para a matriz de projeção na expressão $Ex=y$. Assim sendo, suponha as coordenadas unitárias $u=(u_{1},u_{2})$.
$$
\begin{align}
\mycolv{2u_{1}^{2}-1 & 2u_{1}u_{2}\\ 2u_{1}u_{2} & 2u_{2}^{2}-1}\mycolv{5\\5}=\mycolv{1\\7} \\ \\
10u_{1}^{2}
\end{align}
$$

***

### $\texttt{Forma Alternativa.}$

2. $(a)$ Para determinar o vetor espelho $u$, faremos a soma entre $x$ e seu reflexo $y$ e encontraremos um vetor na reta de $u$. Finalmente, iremos normalizar o resultado obtido e teremos o vetor unitário do espelho.
$$
x+y=\mycolv{5\\5}+\mycolv{1\\7}=\mycolv{6\\12}
$$
Agora basta normalizarmos $\mycolv{6\\12}$, resultando em
$$
u=(6,12) \dfrac{1}{\sqrt{ 180 }}\to (1,2) \frac{1}{\sqrt{ 5 }}
$$
Por outro lado, a normal do espelho pode ser obtida invertendo as componentes de $u$ e atribuindo sinal negativo à primeira, tal como abaixo
$$
n=(-12,6) \dfrac{1}{\sqrt{ 180 }}\to(-2,1) \frac{1}{\sqrt{ 5 }}
$$
***

2. $(b)$ Para determinar a matriz de reflexão $E$, basta inserir os valores do vetor unitário $u$ na fórmula geral da matriz de reflexão, tal como abaixo
$$
\begin{align}
E=\mycolv{2u_{1}^{2}-1 & 2u_{1}u_{2}\\ 2u_{1}u_{2} & 2u_{2}^{2}-1}\implies\frac{1}{5}\mycolv{-3 & 4\\ 4 & 3}
\end{align}
$$
Agora vamos verificar se $x=E^{T}y$. Primeiramente, precisamos descobrir a transposta $E^{T}$ e, portanto, inverteremos as colunas e as linhas de acordo
$$
\begin{align}
E^{T}=\dfrac{1}{5}\mycolv{-3 & 4\\4 & 3}
\end{align}
$$
Para o caso da matriz de reflexão, a matriz transposta é a mesma que a original, pois os termos $a_{12}$ e $a_{21}$ são os mesmos. Nos resta verificar se $x=E^{T}y$ como farei abaixo
$$
\begin{align}
\dfrac{1}{5}\mycolv{-3 & 4\\ 4 & 3}\mycolv{1\\7}&=\mycolv{5\\5}? \\ \\
\dfrac{1}{5}(-3+28)=\dfrac{25}{5}&=5\;  \checkmark \\ \\
\dfrac{1}{5}(4+21)=\dfrac{25}{5}&=5\; \checkmark 
\end{align}
$$
Concluímos que a matriz transposta $E^{T}$ aplicada à reflexão $y$ resulta no vetor original $x$.

***

2. $(c)$ Para demonstrar que $E^{2}x=x$, calcularemos primeiramente $E^{2}$ da seguinte forma
$$
\begin{align}
\Big(\dfrac{1}{5}\Big)^{2}\mycolv{-3 & 4\\ 4 & 3}\mycolv{-3 & 4\\4 & 3}&=\dfrac{1}{25}\mycolv{9+16 & 12-12\\12-12 & 16+9} \\ \\
&=\dfrac{1}{25}\mycolv{25 & 0\\0 & 25}\to \mycolv{1 & 0\\0 & 1}=I
\end{align}
$$
Como previsto, obtemos a matriz identidade ao calcular o quadrado da matriz de reflexão. Desse modo, ao multiplicar $E^{2}$ pelo vetor $x$ retornaremos a $x$ novamente.
$$
\begin{align}
\mycolv{5\\5}\mycolv{1 & 0\\0 & 1}=\mycolv{5\\5}\quad    
\end{align}
$$
Ao calcular a matriz $E$, notamos que se trata de uma matriz simétrica, pois os termos $a_{12}$ e $a_{21}$ são os mesmos. Portanto, a matriz transposta $E^{T}$ também será a mesma, em função da simetria delas. Por definição, a matriz inversa é aquela que quando multiplicada pela original resulta na identidade $I$. Desse modo, percebemos que ao fazer $E^{2}$ chegamos à matriz identidade, ou seja, podemos concluir que a inversa é a própria matriz $E$. A relação entre a inversa, a transposta e a original é que todas são iguais quando trabalhamos com reflexão.

***

2. $(d)$ Os autovalores de $E$ podem ser descobertos tendo em mente a relação $\det(T-\lambda I)=0$ descrita na seção de [[Autovalores e Autovetores|autovetores e autovalores]]. Desse modo, teremos
$$
\begin{align}
E-\lambda I=\dfrac{1}{5}&\mycolv{-3 & 4\\4 & 3}-\lambda \mycolv{1 & 0\\0 & 1} \\ \\
=&\mycolv{-\dfrac{3}{5}-\lambda & \dfrac{4}{5}\\ \dfrac{4}{5} & \dfrac{3}{5}-\lambda} \\ \\
=\det&\mycolv{-\dfrac{3}{5}-\lambda & \dfrac{4}{5}\\ \dfrac{4}{5} & \dfrac{3}{5}-\lambda}=0
\end{align}
$$
Calculando o determinante da matriz, chegaremos à equação quadrática
$$
\begin{align}
\bigg(\dfrac{3}{5}-\lambda\bigg)\bigg(-\dfrac{3}{5}-\lambda\bigg)-\bigg(\dfrac{4}{5}\bigg)^{2}=0 \\ \\
\bigg(\lambda^{2}-\dfrac{9}{25}\bigg)-\bigg(\dfrac{16}{25}\bigg)=0 \\ \\
\lambda^{2}-\dfrac{25}{25}=0 \\ \\
\lambda^{2}=1 \\ \\
\lambda=\pm 1
\end{align}
$$
Desse modo, encontramos os autovalores $\lambda=1$ e $\lambda=-1$ para os quais temos autovetores associados. Com o objetivo de determiná-los, aplicaremos os autovalores encontrados na expressão $(E-\lambda I)v=0$ em que $v$ representa um vetor genérico do plano. Primeiramente, faremos $\lambda=1$.
$$
\begin{align}
&\mycolv{-\dfrac{3}{5}-1 & \dfrac{4}{5}\\ \dfrac{4}{5} & \dfrac{3}{5}-1}\mycolv{x\\y}=\mycolv{0\\0} \\ \\
&=\bigg(-\dfrac{8}{5}\bigg)x+\bigg(\dfrac{4}{5}\bigg)y=0\to-8x+4y=0 \\ \\
&=\bigg(\dfrac{4}{5}\bigg)x+\bigg(-\dfrac{2}{5}\bigg)y=0\to 4x-2y=0 \\ \\
&\therefore \boxed{y=2x}
\end{align}
$$
Do primeiro autovalor $\lambda=1$, encontramos a reta $y=2x$ correspondente à reta do vetor espelho $u$. Portanto se escolhermos $x=1$, obteremos o vetor $v=\mycolv{1\\2}$ para o qual podemos descrever o conjunto de autovetores $v'$ associados a um da seguinte forma
$$
\forall\; t\in\Bbb{R},(v'=vt)
$$
Por fim, determinaremos os autovetores referentes a $\lambda=-1$ de forma análoga
$$
\begin{align}
&\mycolv{-\dfrac{3}{5}+1 & \dfrac{4}{5}\\ \dfrac{4}{5} & \dfrac{3}{5}+1}\mycolv{x\\y}=\mycolv{0\\0} \\ \\
&=\bigg(\dfrac{2}{5}\bigg)x+\bigg(\dfrac{4}{5}\bigg)y=0\to 2x+4y=0 \\ \\
&=\bigg(\dfrac{4}{5}\bigg)x+\bigg(\dfrac{8}{5}\bigg)y=0\to 4x+8y=0 \\ \\
&\therefore\boxed{y=-\dfrac{x}{2}}
\end{align}
$$
Assim sendo, para o autovalor $\lambda=-1$ obtemos a reta $y=-\dfrac{x}{2}$ que corresponde à reta normal ao espelho. Se escolhermos $x=-2$ dessa vez, obteremos o vetor $u=\mycolv{-2\\1}$ para o qual poderemos enunciar o conjunto de autovetores $v''$ associados a $-1$ da seguinte forma
$$
\forall\; t\in\Bbb{R},(v''=ut)
$$
Ou seja, a proposição se estende para todos os vetores situados na reta $y=-\dfrac{x}{2}$.

***

3. As expressões para a reflexão do espelho $E_{1}=2uu^{t}-I$ e $E_{2}=I-2nn^{t}$, em que $u$ representa o vetor espelho e $n$ sua normal, são equivalentes entre si uma vez que derivam das mesmas fórmulas. Assim sendo, provaremos a igualdade de forma algébrica começando pela matriz $E_{1}$.
$$
\begin{align}
E_{1}&=2uu^{t}-I \\ \\
&=2\mycolv{u_{1}\\u_{2}}\mathbf{[}u_{1}\quad u_{2}\mathbf{]}-I \\ \\
&=2\mycolv{u_{1}^{2} & u_{1}u_{2}\\u_{1}u_{2} & u_{2}^{2}}-\mycolv{1 & 0\\0 & 1} \\ \\
&=\mycolv{2u_{1}^{2}-1 & 2u_{1}u_{2}\\2u_{1}u_{2} & 2u_{2}^{2}-1}
\end{align}
$$
Posto isso, realizaremos um cálculo semelhante para determinarmos matriz $E_{2}$.
$$
\begin{align}
E_{2}&=I-2nn^{t} \\ \\
&=I-2\mycolv{n_{1}\\n_{2}}\mycolv{n_{1} & n_{2}} \\ \\
&=\mycolv{1 & 0\\0 & 1}-2\mycolv{n_{1}^{2} & n_{1}n_{2}\\n_{1}n_{2} & n_{2}^{2}} \\ \\
&=\mycolv{1-2n_{1}^{2} & -2n_{1}n_{2}\\ -2n_{1}n_{2} & 1-2n_{2}^{2}}
\end{align}
$$
Por fim, basta substituir o vetor $n$ por um vetor normal ao espelho e em função deste mesmo, tal como $\mycolv{-u_{2} & u_{1}}^{t}$. Podemos demonstrar isso facilmente, pois
$$
\begin{align}
\langle u|n \rangle&= \mycolv{u_{1} & u_{2}}\mycolv{-u_{2}\\u_{1}}  \\ \\
&=-u_{1}u_{2}+u_{2}u_{1} \\ \\
&=0
\end{align}
$$
Posto isso, escolhendo $n=\mycolv{-u_{2} & u_{1}}^{t}$ e substituindo na matriz $E_{2}$ teremos
$$
\begin{align}
&=\mycolv{1-2(-u_{2})^{2} & -2(-u_{2})(u_{1})\\-2(-u_{2})(u_{1}) & 1-2(u_{1})^{2}}  \\ \\
&=\mycolv{1-2u_{2}^{2} & 2u_{1}u_{2}\\2u_{1}u_{2} & 1-2u_{2}^{2}}
\end{align}
$$
Como o vetor espelho $u$ é unitário, temos que $\|u_{1}\|=\sqrt{ u_{1}^{2}+u_{2}^{2} }=u_{1}^{2}+u_{2}^{2}=1$. Portanto, faremos a seguinte substituição
$$
\begin{align}
&=\mycolv{1-2(1-u_{1}^{2}) & 2u_{1}u_{2}\\2u_{1}u_{2} & 1-2(1-u_{2}^{2})}  \\ \\
&=\mycolv{2-u_{1}^{2} & 2u_{1}u_{2}\\2u_{1}u_{2} & 2u_{2}^{2}-1}\qquad \blacksquare  
\end{align}
$$
Por fim, deduzimos que a igualdade é válida $E_{1}=E_{2}$, concluindo a prova.

***

4. As demonstrações das propriedades do determinante se encontram na seção de [[Determinante]].

***