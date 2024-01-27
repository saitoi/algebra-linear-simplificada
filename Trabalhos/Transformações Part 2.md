---
aliases:
  - trab3
  - part2
tags:
  - Exercícios
date: 2023-09-11
time: 13:26
complete:
---
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
### Nome: Pedro Henrique Honorio Saito

### DRE: 122149392

# Transformações Lineares - Parte 2

1. A transformação corresponde ao cisalhamento horizontal e sua matriz possui a seguinte fórmula geral:
$$
M=\mycolv{1 & \alpha\\ 0 & 1}
$$
Em que $\alpha$ refere-se à constante de cisalhamento ao longo do eixo $x$. Posto isso, escolheremos o vetor $v=\mycolv{-3\\3}$ juntamente de sua transformação $v'=\mycolv{-6\\3}$ e determinaremos o coeficiente $\alpha$ com base nisso. Temos que,
$$
\begin{align*}
&\mycolv{1 & \alpha\\ 0 & 1}\cdot\mycolv{-3\\3}=\mycolv{-6\\3} \\ \\
&\begin{cases}
1\cdot(-3)+3\cdot(\alpha)=-6 \\ \\
0\cdot(-3)+3\cdot(1)=3
\end{cases} \\ \\
&-1+\alpha=-2 \\ \\
&\qquad\;\;\,\boxed{\alpha=-1}
\end{align*}
$$
Portanto, a matriz resultante será descrita abaixo:
$$
M=\mycolv{1 & -1\\ 0 & 1}
$$
Podemos concluir que o vetor unitário $\hat{j}$ sofre uma alteração no eixo $x$, inclinando-o no sentido anti-horário, ou seja, no segundo quadrante. Desse modo, a figura como um todo segue a orientação desses vetores da base como observamos.

***

2. A matriz $\mycolv{0 & 1 \\ 1 & 0}$ é responsável pela reflexão dos vetores no plano cartesiano em relação à reta $y=x$, tendo em vista que as coordenadas de cada vetor são invertidas entre si. Suponha a aplicação dessa matriz sobre um vetor qualquer $v=\mycolv{x\\y}$, teremos:
$$
\mycolv{0 & 1\\ 1 & 0}\cdot\mycolv{x\\y}=\mycolv{y\\x}
$$
Realizando os cálculos, notamos que as coordenadas do vetor original $v$ foram invertidas após a transformação. Graficamente, o espelho da reflexão é a reta $y=x$, pois os pontos situados nessa reta não modificam suas coordenadas após a reflexão justamente porque suas componentes já são iguais. Aqui está uma ilustração da reflexão:

```tikz
\begin{document}
\begin{tikzpicture}[scale=1.8]
    % Draw the x-axis
    \draw[->] (-2, 0) -- (2, 0) node[right] {$x$};
    % Draw the y-axis
    \draw[->] (0, -2) -- (0, 2) node[above] {$y$};
	% v1
	\draw[->, ultra thick] (0,0) -- (1.5, 0.5) node[above] {$v_1$};
	% R(v1)
	\draw[->, ultra thick, dotted, red] (0,0) -- (0.5, 1.5) node[above] {$R(v_1)$};
    % Draw the graph y = x
    \draw[domain=-1.5:1.5, smooth, variable=\x, ultra thick, blue] plot ({\x}, {\x}) node[right] {$y = x$};
\end{tikzpicture}
\end{document}
```

***

3. O conjunto de vetores cuja direção não varia após a transformação são denominados de autovetores e, no caso apresentado, estão contidos na reta $y=x$ e $y=-x$. Em primeiro lugar, vimos que os vetores contidos na reta $y=x$ não sofrem alteração pois suas coordenadas já são iguais, desse modo nos resta tratar dos pontos situados em $y=-x$. Sabemos que se um vetor qualquer possui uma inclinação de $\theta\degree$ em relação ao espelho, a rotação envolve apenas girá-lo $\theta\degree$ no sentido oposto.    
Nesse sentido, como os pontos pertencentes à reta $y=-x$ são ortogonais ao espelho $y=x$, o ângulo de inclinação $\theta$ corresponde a $90\degree$. Assim sendo, ao rotacioná-lo $90\degree$ no sentido oposto teremos uma rotação total de $180\degree$ e, portanto, o vetor permanecerá na mesma reta (mesma direção), no entanto no sentido oposto.

***

4. O conjunto de vetores cuja direção não varia após a aplicação da matriz $\mycolv{-1 & 0\\ 0 & 1}$ são todos os vetores contidos nas retas abcissas e ordenadas, ou seja, $x=0$ e $y=0$, respectivamente. Chegamos a essa conclusão da seguinte forma:
$$
\begin{align*}
\mycolv{-1 & 0\\0 & 1}\cdot\mycolv{x\\y}=\lambda\mycolv{x\\y}& \\ \\
-1\cdot(x)+0\cdot(y)=\lambda\,x\tag{1}& \\ \\
0\cdot(x)+1\cdot(y)=\lambda\,y\tag{2}& \\ \\
-x=\lambda\,x\qquad y=\lambda\,y \\ \\
\underbrace{\lambda=-1}_{\mycolv{0\\?}}\qquad\quad\underbrace{\lambda=1}_{\mycolv{?\\0}}
\end{align*}
$$
Traduzindo, se $\lambda$ for $-1$, então a solução terá o formato: $v=\mycolv{0\\n}$ para todo $n\in\Bbb{R}$.    
Por outro lado, se $\lambda$ for igual a $1$, então a solução terá o formato: $v=\mycolv{n\\0}$ novamente para todo $n\in\Bbb{R}$.

***

5. Considerando a matriz de transformação $A=\mycolv{-2 & 2\\ 0 & 2}$, devemos encontrar os autovetores que satisfazem a expressão abaixo:
$$
A\mathbf{v}=\lambda\mathbf{v}
$$
Em que $\mathbf{v}$ seria um vetor qualquer com componentes $\mathbf{v}=\mycolv{x\\y}$. Substituindo teremos:
$$
\begin{align*}
&\mycolv{-2 & 2\\0 & 2}\cdot\mycolv{x\\y}=\mycolv{x\\y}\lambda \\ \\
&\begin{cases}
\lambda x=-2x+2y \\ \\
\lambda y=0x+2y
\end{cases} \\ \\
&\underbrace{\lambda=2}_{\mycolv{x\\2x}}\qquad\underbrace{\lambda\neq2}_{\mycolv{x\\y}\forall\,x,y\neq0}
\end{align*}
$$
Posto isso, temos duas possibilidades para o sistema linear, quando $\lambda=2$ e quando $\lambda\neq2$. Para o primeiro caso encontramos a solução padrão $y=2x$ e para o segundo todos os vetores do plano satisfazem a condição, com exceção do vetor nulo $\mycolv{0\\0}$.
***

6. A matriz de transformação $\mycolv{2 & 4 \\ 1 & 2}$ é responsável pelo achatamento ou redução em uma dimensão do conjunto de vetores originais, resultando na perda de informações. Essa alteração ocorre pois a matriz em questão possui colunas linearmente dependentes, ou seja, ela contém informações redundantes e, portanto, seu determinante é igual a zero. Como o cálculo do determinante resulta em zero, o escalonamento resultará na perda da área ou do volume (depende da dimensão que trabalhamos) da figura original. Por exemplo, se tivermos uma área, ela será reduzida a uma reta (uma única direção) e se tivermos um volume, este será planificado.

***

7. A matriz de transformação responsável por esticar o espaço do eixo das abcissas em $2$ unidades e das ordenadas em $2.5$ unidades está descrito abaixo:
$$
A=\mycolv{2 & 0\\0 & 2.5}
$$
Nesse sentido, nos resta multiplicar a matriz $A$ por uma que rotacione o espaço em $45\degree$ no sentido anti-horário e, por fim, compor uma matriz única que realize todas as operações necessárias de vez. Nesse sentido, a matriz de rotação que gira o plano no sentido anti-horário em $45\degree$ pode ser obtida pela operação:
$$
\begin{align*}
p_{45\degree}&=\mycolv{\cos(45\degree) & -\sin(45\degree)\\\sin(45\degree) & \cos(45\degree)} \\ \\
&=\mycolv{\frac{\sqrt{2}}{2} & -\frac{\sqrt{2}}{2}\\\frac{\sqrt{2}}{2} & \frac{\sqrt{2}}{2}} \\ \\
\therefore\;(p_{45}\cdot A)&=\mycolv{\frac{\sqrt{2}}{2} & -\frac{\sqrt{2}}{2}\\\frac{\sqrt{2}}{2} & \frac{\sqrt{2}}{2}}\cdot\mycolv{2 & 0\\0 & 2.5} \\ \\
&=\underbrace{\mycolv{\sqrt{2} & -2.5\cdot(\frac{\sqrt{2}}{2})\\\sqrt{2} & 2.5\cdot(\frac{\sqrt{2}}{2})}}_{\texttt{matriz final}}
\end{align*}
$$

***

8. A matriz $M$ definida por $\mycolv{0 & -1\\1 & 0}\cdot\mycolv{1 & 0\\0 & 0}$ equivale à transformação única $\mycolv{0 & 0\\1 & 0}$ obtida ao realizar a multiplicação. Nesse sentido, ao realizar a multiplicação da matriz $M$ por um vetor genérico $v=\mycolv{x\\y}$ teremos o seguinte resultado:
$$
\mycolv{0 & 0\\1 & 0}\cdot\mycolv{x\\y}=\mycolv{0\\x}
$$
Ou seja, a componente $x$ do vetor transformado é anulada e, por fim, substitui a posição do $y$. Chegamos a conclusão que a transformação possui determinante zero de modo que todos os vetores do plano são mapeados para a reta vertical $(0, n)$ para todo $n\in\Bbb{R}$.

***

9. Se a letra $\textup{M}$ for transformada pela matriz $\mycolv{1 & 0\\3 & 2}$, ela aumentará de tamanho e terá seus lados esticados em cada lado. Podemos comprovar essa hipótese considerando um vetor genérico $v=\mycolv{x\\y}$ e verificando as alterações realizadas sobre ele da seguinte forma:
$$
\mycolv{1 & 0\\3 & 2}\cdot\mycolv{x\\y}=\mycolv{1\cdot(x)+0\cdot(y)\\3\cdot(x)+2\cdot(y)}=\mycolv{x\\3x+2y}
$$
Posto isso, notamos que a primeira coordenada ($x$) permanece inalterada, enquanto a segunda é esticada em $2$ vezes e incrementada pelo fator $3x$. Nesse sentido, se $x$ for positivo para um dado vetor da letra $\textup{M}$, teremos um escalonamento positivo no eixo das ordenadas e, caso for negativo, teremos a componente $y$ reduzirá proporcionalmente.

***

10. Para determinar os efeitos da matriz $\mycolv{a & 1\\c & 1}$ sobre os vetores que compõe a letra $\textup{M}$ teremos que analisar as funções das incógnitas $a,c$ durante a transformação. Aqui estão algumas informações para iniciarmos a análise:
- Valor de $a$ afetará a escala na direção horizontal (eixo $x$).
- Valor de $c$ afetará a escala na direção vertical (eixo $y$).   

1. ${a,c>1}$ : Ampliará o espaço na direção correspondente ($x,y$).
2. $0<a,c<1$ : Reduzirão o espaço na direção correspondente ($x,y$).
3. $a,c<0$ : Provocarão reflexões ao longo dos eixos correspondentes.

***

11. $\textbf{Resposta:}$ Não daria o mesmo resultado, pois a multiplicação de matrizes não é comutativa.    
$\textbf{Explicação:}$ As matrizes de transformação responsáveis pela reflexão e rotação, quando multiplicadas em ordens distintas, não possuem o mesmo resultado.    
- Podemos comprovar isso considerando um vetor $v=\mycolv{1\\1}$ e as operações descritas.    
1. Rotação de $45\degree$: Resulta no vetor $\mycolv{0\\\sqrt{2}}$ após a rotação.
2. Reflexão em torno de $x$ : Obtemos o vetor $\mycolv{0\\-\sqrt{2}}$ como consequência.    
- Agora faremos as operações inversas.
1. Reflexão em torno de $x$ : Obtemos o vetor $\mycolv{1\\-1}$ com a reflexão.
2. Rotação de $45\degree$: Teremos o vetor $\mycolv{\sqrt{2}\\0}$ ao final dessa operação.

***

12. A matriz de transformação $M$ se trata de uma matriz de rotação de $90\degree$ no sentido anti-horário, desse modo ela terá o seguinte formato:
$$
M=\mycolv{0 & -1\\ 1 & 0}
$$
Ao elevar a matriz de rotação $M$ ao quadrado teremos o resultado:
$$
 M^2 = \begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix} \cdot \begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix} = \begin{bmatrix} (-1)(-1) + (-1)(0) & (-1)(-1) + (-1)(0) \\ (1)(-1) + (0)(1) & (1)(0) + (0)(1) \end{bmatrix} = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}
$$
Obtemos a matriz identidade em $\Bbb{R}^2$ que não ocasiona mudanças no vetor origem. Por outro lado, a matriz $M$ elevada ao cubo resultará em:
$$
M^3 = M \cdot M^2 = \begin{bmatrix}
0 & -1 \\
1 & 0
\end{bmatrix} \cdot
\begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix} =
\begin{bmatrix}
(0)(1) + (-1)(0) & (0)(0) + (-1)(1) \\
(1)(1) + (0)(0) & (1)(0) + (0)(1)
\end{bmatrix} =
\begin{bmatrix}
0 & -1 \\
1 & 0
\end{bmatrix}
$$
Retorna à mesma condição da matriz inicial $M$ e realiza a rotação em $90\degree$ no sentido anti-horário. Por fim, a matriz $M$ à quarta potência será:
$$
M^4 = M^2 \cdot M^2 = \begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix} \cdot
\begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix} =
\begin{bmatrix}
(1)(1) + (0)(0) & (1)(0) + (0)(1) \\
(0)(1) + (1)(0) & (0)(0) + (1)(1)
\end{bmatrix} =
\begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix}
$$
Retornamos à matriz de $M^2$ como vimos anteriormente, isto é, a matriz identidade. O resultado obtido em cada um dos casos é previsível e as contas não são necessárias pois os únicos termos que irão alterar são $a_{12}$ e $a_{21}$, isto é, $-1$ e $1$, respectivamente. Quando elevados a uma potência par, o resultado será $1$, enquanto quando são elevados a uma potência ímpar, teremos $-1$ ou $1$ dependendo do termo original.

***

13. Para encontrar o núcleo da matriz $\mycolv{-2 & 2\\0 & 2}$, consideramos um vetor genérico $\mycolv{x\\y}$ e sua imagem $\mycolv{0\\0}$ como foi mencionado. Assim sendo, teremos:
$$
\begin{align*}
\mycolv{-2 & 2\\0 & 2}\cdot\mycolv{x\\y}=\mycolv{0\\0} \\ \\
-2x+2y=0 \\ \\
0x+2y=0 \\ \\
\therefore \boxed{x,y=0}
\end{align*}
$$
Como podemos observar, o único vetor que convergiu para o $\mycolv{0\\0}$ foi o próprio vetor nulo.

***

14. O núcleo da matriz $\mycolv{-3 & 1\\6 & -2}$ possui infinitas soluções, pois a matriz em questão possui colunas linearmente dependentes. Se tentarmos realizar o cálculo encontraremos uma fórmula geral:
$$
\begin{align*}
\mycolv{-3 & 1\\6 & -2}\cdot\mycolv{x\\y}=\mycolv{0\\0} \\ \\
-3x+y=0\tag{1} \\ \\
6x-2y=0\tag{2} \\ \\
\boxed{y=3x}\text{\quad ou\quad}\mycolv{x\\3x}
\end{align*}
$$
Ou seja, a solução compreende todos os vetores situados na reta $y=3x$ ou cujas componentes são $\mycolv{x\\3x}$.

***

15. O núcleo da matriz $\mycolv{-3 & 1\\2 & -2}$ pode ser obtido da mesma forma que no exercício (13). Posto isso, consideraremos um vetor genérico $\mycolv{x\\y}$e a imagem como sendo o vetor nulo.
$$
\begin{align*}
\mycolv{-3 & 1\\2 & -2}\cdot\mycolv{x\\y}=\mycolv{0\\0} \\ \\
-3x+y=0\tag{1} \\ \\
2x-2y=0\tag{2} \\ \\
\therefore\boxed{x,y=0}
\end{align*}
$$

Portanto, o núcleo da matriz compreende apenas o vetor nulo $\mycolv{0\\0}$.

***

16. Para determinar todos os vetores contidos no contradomínio da transformação, suponha um vetor $v=\mycolv{x\\y}$ para o qual aplicaremos a matriz $A=\mycolv{-3 & 1\\2 & -2}$. Teremos,
$$
\begin{align*}
\mycolv{3 & 1\\ 6 & -2}\cdot\mycolv{x\\y}=\mycolv{-3x+y\\2x-2y} \\ \\
\end{align*}
$$
Portanto, a imagem da matriz transformação $A$ corresponde a todos os vetores do formato $v=\mycolv{-3x+y\\2x-2y}$ para todos $x,y\in\Bbb{R}$. Como estamos tratando de uma matriz com determinante não nulo, a imagem também corresponderia a todos os vetores contidos em $\Bbb{R}^2$ sem problemas.

***

17. Faremos um processo semelhante ao item anterior para analisar todos os vetores contidos no contradomínio da transformação $\mycolv{-3 & 1\\2 & -2}$, considerando sempre o vetor genérico $\mycolv{x\\y}$. Teremos,
$$
\begin{align*}
\mycolv{-3 & 1\\2 & -2}\cdot\mycolv{x\\y}=\mycolv{-3x+y\\2x-2y} \\ \\
\end{align*}
$$
O contradomínio da transformação mencionada corresponde ao plano $\Bbb{R}^2$, pois a matriz de transformação não possui colunas linearmente dependentes e, por consequência, nenhuma dimensão do plano é reduzida. Por outro lado, a imagem da transformação também equivale ao plano $\Bbb{R}^2$ como determinante é não nulo.

***

18. Como podemos constatar, o núcleo das matrizes de transformação que possuem com colunas linearmente dependentes corresponde a um conjunto de soluções, tal como o item (14). Isso implica que vetores distintos podem resultar no nulo, ou seja, temos infinitas soluções. Por outro lado, nas matrizes de transformação com posto completo, o núcleo da matriz equivale apenas ao vetor nulo que, por sua vez, já está contido implicitamente no núcleo de uma transformação linear.

