---
aliases:
  - ed_1
tags:
  - ALA/trabalho
date: 2023-08-19
time: 01:46
---
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
### Nome: Pedro Henrique Honorio Saito

### DRE: 122149392

# Vetores e Produto Interno - Resolução

1. Tomando como referência a expressão para o produto interno: $\langle v_1|v_2\rangle=a_1a_2+b_1b_2$ , utilizaremos a seguinte notação para a composição dos vetores no plano:
$$
\begin{flalign*}
v_1&=(a_1,b_1) \\
v_2&=(a_2,b_2) \\
u&=(a_3,b_3)
\end{flalign*}$$
$$
\begin{flalign*}
(1)\;\;\langle u|v_1+v_2\rangle=\langle u|v_1\rangle+\langle u|v_2\rangle&& \\
\end{flalign*}
$$
- Segundo a operação básica de [[Operação Básicas com Vetores|soma entre vetores]], podemos concluir que a expressão $v_1+v_2$ resultará em $(a_1+a_2,b_1+b_2)$. Portanto, o produto interno dos vetores $u$ e $v_1+v_2$ terá o seguinte aspecto:$$
	\begin{flalign*}
	\langle u|v_1+v_2\rangle&=a_3\,(a_1+a_2)+b_3\,(b_1+b_2)\qquad\text{Pelo produto interno.}&& \\ \\
	&=a_3\,a_1+a_3\,a_2+b_3\,b_1+b_3\,b_2\quad\;\;\text{Pela propriedade distributiva do produto.}&& \\ \\
	&=\underbrace{a_3\,a_1+b_3\,b_1}_{\langle u|v_1\rangle}+\underbrace{a_3\,a_2+b_3\,b_2}_{\langle u|v_2\rangle}\quad\text{Reorganizando os termos..}&& \\ \\
	&\therefore\langle u|v_1\rangle+\langle u|v_2\rangle\quad\blacksquare
	\end{flalign*}
	$$
***
$$
\begin{flalign*}
(2)\;\;\langle u|\lambda v_2\rangle=\lambda\langle u|v_2\rangle&&
\end{flalign*}
$$
- Segundo a operação do [[Operação Básicas com Vetores|produto de um vetor por um escalar]],  $v_2$ será redimensionado para $(\lambda a_2,\lambda b_2)$. Portanto, o produto interno dos vetores $u$ e $\lambda v_2$ terá o seguinte aspecto:$$
	\begin{flalign*}
	\langle u|\lambda v_2\rangle&=a_3\,(\lambda a_2)+b_3\,(\lambda b_2)\quad\text{Pelo produto interno.}&& \\ \\ 
	&=\lambda\,(a_3a_2)+\lambda\,(b_3b_2)\quad\text{Pela propriedade associativa do produto.}&& \\ \\
	&=\lambda\,(\underbrace{a_3a_2+b_3b_2}_{\langle u|v_2\rangle})\quad\quad\text{Colocando }\lambda\text{ em evidência.}&& \\ \\
	&\therefore\;\lambda\,\langle u|v_2\rangle\quad\blacksquare
	\end{flalign*}
	$$
***
$$
\begin{flalign*}
(3)\;\;\langle v_1|v_2\rangle=\langle v_2|v_1\rangle&&
\end{flalign*}
$$
- A demonstração da propriedade de comutatividade dos vetores no produto interno pode ser feita por uma manipulação algébrica simples, aqui está a prova:$$
	\begin{flalign*}
	\langle v_1|v_2\rangle&=a_1\,a_2+b_1\,b_2\quad\text{Pelo produto interno.}&& \\ \\
	&=a_2\,a_1+b_2\,b_1\quad\text{Pela propriedade comutativa do produto.}&& \\ \\
	&=\underbrace{a_2\,a_1+b_2\,b_1}_{\langle v_2|v_1\rangle}\;\;\,\text{Encontramos a expressão do produto interno.}&& \\ \\
	&\therefore\langle v_2|v_1\rangle=\langle v_1|v_2\rangle\quad\blacksquare&&
	\end{flalign*}
	$$
***
$$
\begin{flalign*}
(4)\;\;\langle u|u\rangle\geq0&&
\end{flalign*}
$$
- Para demonstrar que o produto interno de um vetor com ele mesmo é no mínimo zero, podemos utilizar a propriedade do quadrado de números reais não nulos:$$
	\begin{flalign*}
	\langle u|u\rangle&=a_3\,a_3+b_3\,b_3\qquad\;\,\;\text{Pelo produto interno.}&& \\ \\
	&=(a_3)^2+(b_3)^2,\qquad\text{Pela propriedade do quadrado de reais não nulos, deduzimos que }a_3\geq0,\,b_3\geq0.\text{ Logo, temos $3$ hipóteses:}&& \\ \\
	&=(a_3=0\wedge b_3=0)\vee(a_3>0\wedge b_3=0)\vee(a_3>0\wedge b_3>0)&& \\ \\
	&\text{1. Se }a_3=0\text{ e }b_3=0,\text{ então pelo elemento neutro da soma temos que }0+0=0\text{, satisfazendo a proposição.}&& \\ \\
	&\text{2. Se }a_3>0\text{ e }b_3=0\text{ ou vice-versa, então novamente pelo elemento neutro da soma, temos que }a_3+0=a_3\text{ de modo que $a_3$ é positivo.}& \\ \\
	&\text{3. Se $a_3>0$ e $b_3>0$, então por fechamento temos que $a_3+b_3>0$, satisfazendo a proposição inicial.}&& \\ \\
	&\therefore\langle u|u\rangle\geq0\quad\blacksquare&&
	\end{flalign*}
	$$
***
$$
\begin{flalign*}
(5)\;\;\langle u|u\rangle=0\iff u=0&&
\end{flalign*}
$$
- Para demonstrar que o produto interno de um vetor com ele mesmo é zero se, e somente se, o vetor for nulo, provaremos os dois sentidos da implicação:
$$
\begin{flalign*}
&\underline{\langle u|u\rangle=0\implies u=0}&& \\ \\
&=\langle u|u\rangle=0\qquad\qquad\;\text{Partimos dessa suposição inicial. Logo, pela questão anterior obtemos:}&& \\ \\
&=(a_3)^2+(b_3)^2=0,\quad\text{Também sabemos que }a_3\geq0,\,b_3\geq0.&& \\ \\
&\text{Portanto, nos resta a hipótese de que $a_3=0$ e $b_3=0$. Desse modo, concluimos que se trata de um vetor nulo e $u=0$.}&& \\ \\
&\underline{u=0\implies\langle u|u\rangle=0}&& \\ \\
&=(a_3=0\wedge b_3=0)\quad\text{Partimos dessa suposição inicial. Logo, aplicando o produto interno:}&& \\ \\
&=\underbrace{0\cdot0+0\cdot0}_{\langle u|u\rangle}=0&& \\ \\
&\therefore\langle u|u\rangle=0\quad\blacksquare
\end{flalign*}
$$
***
2. A relação algébrica entre a norma e o produto interno do vetor $u$ consigo mesmo pode ser obtida por uma manipulação algébrica simples:$$
\begin{flalign*}
&\text{Norma do vetor }\mathbf u:\,\|u\|=\sqrt{(a_3)^2+(b_3)^2}&& \\ \\
&\text{Produto interno de }\mathbf u\text{ c/}\mathbf u:\,\langle u|u\rangle=(a_3)^2+(b_3)^2&& \\ \\
&\text{Podemos observar que a expressão }(a_3)^2+(b_3)^2\text{ é comum a ambas as soluções. Portanto, substituindo temos:}&& \\ \\
&\boxed{\|u\|=\sqrt{\langle u|u\rangle}}\quad\text{Encontramos a relação algébrica entre a norma e o produto interno.}&& \\ \\
\end{flalign*}
$$
***

3. Para encontrar o ângulo entre as retas especificadas, selecionaremos vetores referentes a cada reta e calcularemos o produto interno deles por meio da fórmula do cosseno. Aqui está a demonstração passo-a-passo:$$
\begin{flalign*}
&\text{Primeiramente, isolaremos o $y$ em ambas as equações e obteremos:}&& \\ \\
&=y_1=-\frac{2}{3}x_1&& \\ \\
&=y_2=-\frac{5}{2}x_2&& \\ \\
&\text{\textbf{Obs.} A notação $x_1,\,x_2$ e $y_1,\,y_2$ foi empregada para distinguir entre as expressões.}&& \\ \\
&\text{Como não há coeficientes lineares, deduzimos que as retas se cruzam na origem.}&& \\ \\
&\text{Portanto, podemos selecionar um ponto $x$ qualquer e teremos duas semirretas da origem $(0,0)$ até $(x,y_1)$ e $(x,y_2)$, nos proporcionando dois vetores. Assim sendo, suponha que escolhemos $(x=1)$:}&& \\ \\
&=y_1=-\frac{2}{3}\therefore\,v_1=(1,-\frac{2}{3})&& \\ \\
&=y_2=-\frac{5}{2}\therefore\,v_2=(1,-\frac{5}{2})&& \\ \\
&\text{\textbf{Obs.} A notação $v_1,\,v_2$ foi utilizada para diferenciar os vetores.}&& \\ \\
&\text{Cálculo do produto interno $\langle v_1|v_2\rangle$ usando duas expressões distintas:}&& \\ \\
&=1\cdot 1+(-\frac{2}{3})\cdot (-\frac{5}{2})=|v_1|\,|v_2|\cdot\cos(\theta)&& \\ \\
&=1+(-\frac{\cancel{2}}{3})\cdot (-\frac{5}{\cancel{2}})=|v_1|\,|v_2|\cdot\cos(\theta)&& \\ \\
\end{flalign*}
$$ $$
\begin{flalign*}
&\text{A norma $v_1,\,v_2$ será determinada abaixo:}&& \\ \\
&=\|v_1\|=\sqrt{(1)^2+(-\frac{2}{3})^2}=\sqrt{1+\frac{4}{9}}=\sqrt{\frac{13}{9}}\therefore\|v_1\|=\frac{\sqrt{13}}{3}&& \\ \\
&=\|v_2\|=\sqrt{(1)^2+(-\frac{5}{2})^2}=\sqrt{1+\frac{25}{4}}=\sqrt{\frac{29}{4}}\therefore\|v_2\|=\frac{\sqrt{29}}{2}&& \\ \\
&\text{Substituindo na expressão original:}&& \\ \\
&=1+\frac{5}{3}=\bigg(\frac{\sqrt{13}}{3}\bigg)\bigg(\frac{\sqrt{29}}{2}\bigg)\cdot\cos(\theta)&& \\ \\
&=\frac{8}{3}=\frac{\sqrt{377}}{6}\cdot\cos(\theta)&& \\ \\
&=\frac{16\sqrt{377}}{377}=\cos(\theta)&& \\ \\
&=\cos^{-1}(\frac{16\sqrt{377}}{377})=\theta&& \\ \\
&\therefore\;\boxed{34,5\textdegree\approx\theta}&&
\end{flalign*}
$$
***

4. Para demonstrar que a distância entre os pontos $P$ e $Q$ do plano é igual à norma do vetor $u-v$, empregaremos a seguinte notação:$$
\begin{align*}
&P=(x_1,\,y_1)\qquad&u=\mycolv{x_1\\y_1} \\
&Q=(x_2,\,y_2)\qquad&v=\mycolv{x_2\\y_2}
\end{align*}
$$ $$
\begin{flalign*}
&\text{Distância entre $P$ e $Q$ : $d=\sqrt{(x_1-x_2)^2+(y_1-y_2)^2}$}&& \\ \\
&\text{Vetor $u-v$ : $u-v=\mycolv{x_1-x_2\\y_1-y_2}$}&& \\ \\
&\text{Calculando a norma de $u-v$ : $\|u-v\|=\sqrt{\big(\underbrace{x_1-x_2}_{\mathbf x}\big)^2+\big(\underbrace{y_1-y_2}_{\mathbf y}\big)^2}$}&& \\ \\
&\text{Portanto, concluimos que $d=\|u-v\|$.}\quad\blacksquare
\end{flalign*}
$$

***
5. O conceito de esparsidade na Álgebra Linear se refere a vetores ou matrizes em que a maioria das entradas são nulas (zero).

	(a).  As entradas nulas indicam que a empresa não obteve lucro por um período de tempo consecutivo. Outrossim, os valores positivos ou negativos são indícios de lucro ou perda financeira se for o caso.

	(b). Revela que o investimento de muitas das ações não possui relevância e, portanto, não está sendo contabilizado. Por outro lado, a ausência de ações no portfólio pode ser indicada pelo zero.

	(c). Pode indicar que a cidade analisada passou por um período de seca,  poucas chuvas, no decorrer do ano ($n=365$).

	(d). Pode indicar que o senador votou nulo ou branco nas $n$ votações.

***

6. Ilustração e explicação dos vetores $v,\,w$ (sem coordenadas) conforme os requisitos solicitados:

$$
\begin{flalign*}
&\text{(a) $cv$ para todo $c\in\Bbb{R}$.}&& \\ \\
&\text{Considere o vetor $\bf \vec{v}$ pertencente a $\Bbb{R}^2$. Todavia, as propriedades descritas se estendem para todo $\Bbb{R}^n$.}&& \\    
\end{flalign*}
$$

```tikz
\begin{document}
\begin{tikzpicture}[scale=1.5]
    \draw[->, ultra thick] (0, 0) -- (3, 2);
    \node at (1.5, 1.5) {$\mathbf{\vec{v}}$};
    \end{tikzpicture}
\end{document}
```


Ao multiplicar um vetor $\bf \vec{v}$ por um escalar, estamos redimensionando suas componentes, isto é, estendendo ou reduzindo essas partes da seguinte forma:

$$
\begin{rcases}
\bf{\vec{v}}=\mycolv{x\cdot c\\y\cdot c\\\vdots\\n\cdot c}
\end{rcases}
\text{\;$n$ posições}
$$
Dividi a multiplicação por um escalar em três casos para facilitar a explicação:

1. **Expansão**: Refere-se ao produto de um vetor $\bf \vec{v}$ por um escalar $|c|>1$. Desse modo, a norma do vetor $cv$ aumentará proporcionalmente à $c$ juntamente da representação visual. Aqui está um exemplo:

```tikz
\begin{document}
\begin{tikzpicture}[scale=1.8]
    \draw[->, ultra thick] (0, 0) -- (3, 2);
    \draw[-, ultra thick] (0, -1) -- (3, 1);
    \draw[->, ultra thick, red] (3, 1) -- (4, 1.67);
    \node at (1.5, 1.5) {$\mathbf{\vec{v}}$};
    \node at (2.2, -0.4) {$\mathbf{\vec{v}}\cdot c$};
\end{tikzpicture}
\end{document}
```

2. **Redução**: Refere-se ao produto de um vetor $\bf \vec{v}$ por um escalar $|c|<1$. Posto isso, a norma do vetor $cv$ reduzirá proporcionalmente à $c$ juntamente da representação visual. Aqui está um exemplo:

```tikz
\begin{document}
\begin{tikzpicture}[scale=1.8]
    \draw[->, ultra thick] (0, 0) -- (3, 2);
    \draw[-, ultra thick] (0, -1) -- (2, 0.33);
    \draw[->, ultra thick, red, dotted] (2, 0.33) -- (3, 1);
    \node at (1.5, 1.5) {$\mathbf{\vec{v}}$};
    \node at (2.2, -0.4) {$\mathbf{\vec{v}}\cdot c$};
\end{tikzpicture}
\end{document}
```

3. **Inversão do sentido**: Refere-se ao produto de um vetor $\bf \vec{v}$ por um escalar $c<0$. Assim sendo, o sentido do vetor será invertido juntamente da representação visual. Aqui está um exemplo:

```tikz
\begin{document}
\begin{tikzpicture}[scale=1.8]
    \draw[->, ultra thick] (0, 0) -- (3, 2);
    \draw[->, ultra thick, red] (3, 1) -- (0, -1);
    \node at (1.5, 1.5) {$\Huge \mathbf{\vec{v}}$};  
    \node at (2.2, -0.4) {$\mathbf{\vec{\Huge v}}\cdot c$};
\end{tikzpicture}
\end{document}
```

De um modo geral, ao englobar todas as possibilidades do produto de um vetor $\bf \vec{v}$ por um escalar real $c$, obteremos uma reta.

```tikz
\begin{document}
\begin{tikzpicture}[scale=1.8]
    % Draw the x-axis
    \draw[->] (-2, 0) -- (2, 0) node[right] {$x$};
    % Draw the y-axis
    \draw[->] (0, -2) -- (0, 2) node[above] {$y$};
    % Draw the graph y = x
    \draw[domain=-1.5:1.5, smooth, variable=\x, ultra thick, blue] plot ({\x}, {\x}) node[right] {$y = x$};
\end{tikzpicture}
\end{document}
```

$$
\begin{flalign*}
&\text{(b) $w+cv$ para todo $c\in\Bbb{R}$.}&& \\ \\
&\text{Novamente, considere os vetores $\bf{ c\vec{v},\vec{w}}$ pertencentes a $\Bbb{R}^2$.}&& \\ \\
\end{flalign*}
$$
Ao somar o vetor $cv$ a um vetor constante $w$ estamos alterando o vetor resultante pois a lógica é semelhante. Dividiremos em $2$ casos:

1. Vetor $\mathbf{\vec{w}}$ linearmente dependente: Caso o vetor $\mathbf{\vec{w}}$ for um múltiplo de $\mathbf{\vec{v}}$ por um escalar, temos que o vetor resultante será apenas um prolongamento ou uma redução do original:

```tikz
\begin{document}

\begin{tikzpicture}
    % Vetor v
    \draw[->, ultra thick] (0,0) -- (3, 2);
    \node at (1.5, 1.5) {$\Huge \mathbf{\vec{v}}$};  
	\draw (3.09,0.7) node {$+$};
    
    % Vetor w
    \draw[->, ultra thick] (3.9, 0.1) -- (5.1, 0.9);
	\node at (4.5, 0.9) {$\Huge \mathbf{\vec{w}}$};
	\draw (5.65, 0.5) node {$=$};
	
    % Vetor resultante v+w
    \draw[->, ultra thick, red] (6.5,0) -- (10.7,2.8) node[midway, above left, red] {$\mathbf{\vec{v}} + \mathbf{\vec{w}}$};
\end{tikzpicture}

\end{document}
```

2. Vetor $\mathbf{\vec{w}}$ linearmente independente: Caso o vetor $\mathbf{\vec{w}}$ tiver autonomia em relação a $\mathbf{\vec{v}}$, temos que o vetor resultante será:

```tikz
\begin{document}
\begin{tikzpicture}
    % Vetor v
    \draw[->, ultra thick] (0,0) -- (3, 2);
    \node at (1.5, 1.5) {$\Huge \mathbf{\vec{v}}$};  
	\draw (3.09,0.7) node {$+$};
    
    % Vetor w
    \draw[->, ultra thick] (4.1, 0.1) -- (4.5, 1.6);
	\node at (4.7, 0.9) {$\Huge \mathbf{\vec{w}}$};
	\draw (5.3, 0.5) node {$=$};
	
    % Vetor resultante v+w
    \draw[->, ultra thick, red] (6.5,0) -- (9.9,3.5) node[midway, above left, red] {$\mathbf{\vec{v}} + \mathbf{\vec{w}}$};
	\draw[->, ultra thick, black, dotted] (6.5, 0) -- (9.5, 2);
	\draw[-, ultra thick, black, dotted] (9.5, 2) -- (9.9, 3.5);
\end{tikzpicture}
\end{document}
```

Novamente, ao englobar todas as possibilidades para $\mathbf{\vec{w}}$, teremos a formação de uma reta, tal como no exemplo abaixo:

```tikz
\begin{document}
\begin{tikzpicture}[scale=1.8]
    % Draw the x-axis
    \draw[->] (-2, 0) -- (2, 0) node[right] {$x$};
    % Draw the y-axis
    \draw[->] (0, -2) -- (0, 2) node[above] {$y$};
    % Draw the graph y = 3.5/3.4 * x
    \draw[domain=-1.5:1.5, smooth, variable=\x, ultra thick, red] plot ({\x}, {(3.5/3.4)*\x}) node[right] {$\mathbf{\vec{v}+\vec{w}}$};
\end{tikzpicture}
\end{document}
```

***
8. Definição de ambas as bibliotecas:

`NumPy`: Biblioteca fundamental para computação científica em Python, pois fornece suporte para arrays multidimensionais (denominados `ndarrays`) juntamente de funções matemáticas para sua utilização. Algumas características importantes incluem: 
- **Arrays multidimensionais.**
- **Broadcasting.**
- **Operações com Arrays.**
- **Integração com C/C++.**
- **Indexação e fatiamento avançado.**

`SciPy`: Fornece uma base sólida para análise numérica e científica em Python. Construída sobre a `NumPy` e oferece uma variedade de funcionalidades para resolver problemas complexos de matemática, estatística, otimização, dentre outros.

**Semelhanças:** Base em matrizes multidimensionais, a eficiência evidenciada pela redução no tempo de execução e otimização do desempenho com implementações em C e Fortran e, por fim, a integração entre as duas.

**Diferenças:** `SciPy` é mais abrangente e contém funcionalidades avançadas para lidar com problemas científicos e mais complexos em relação ao `NumPy`. Outrossim, o `SciPy` possui uma organização em módulos focando em uma área específica cada, tal como `scipy.optimize` para otimização e `scipy.stats` para estatística.
