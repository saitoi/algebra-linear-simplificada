---
aliases:
  - trab2
  - part1
tags:
  - ALA/trabalho
date: 2023-08-30
time: 13:11
---
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
### Nome: Pedro Henrique Honorio Saito

### DRE: 122149392

# Transformações Lineares Parte 1

1. Ao implementar a matriz de transformação $\begin{bmatrix} \frac{1}{3} & 0 \\ 0 & \frac{1}{3} \end{bmatrix}$ no programa, notamos que os pontos convergem para a origem $(0,0)$, tal como em um encolhimento. Por outro lado, a matriz $\begin{bmatrix} 3 & 0 \\ 0 & \frac{1}{3} \end{bmatrix}$ realiza o papel oposto, isto é, estica os pontos do plano e afasta-os da origem.

***

2. A matriz solicitada que expande o espaço em $2$ unidades no eixo $x$ e em $2.5$ unidades no eixo $y$ está representada abaixo:
$$
A=
\begin{bmatrix}
2 & 0 \\
0 & 2.5
\end{bmatrix}
$$
A matriz mencionada funciona da forma correta, pois ao realizar a multiplicação matriz-vetor obteremos o resultado abaixo. De antemão, suponha o vetor $v$ pertencente ao espaço vetorial original com as componentes $(a,b)$.
$$
A\cdot v\equiv
\begin{bmatrix}
2 & 0 \\
0 & 2.5
\end{bmatrix}
\cdot\mycolv{a\\b}
=
\begin{bmatrix}
2\cdot a+0\cdot a\,\\
\,\,\;\;0\cdot b+2.5\cdot b\,
\end{bmatrix}
=\mycolv{2a\\2.5b}
$$

***

3. Para descobrir os fatores $\lambda$ responsáveis pela ação de "encolhimento" ou "esticamento" dos pontos no plano, analisaremos as questões anteriores separadamente:
$$
\begin{flalign*}
1)\quad&\text{ Considerando a matriz $\begin{bmatrix} \frac{1}{3} & 0 \\ 0 & \frac{1}{3} \end{bmatrix}$, o fator $\lambda$ responsável pelo encolhimento é $\frac{1}{3}$, uma vez as componentes $x$ e $y$ são multiplicadas por esse fator.}&& \\ \\
2)\quad&\text{ Considerando a matriz $\begin{bmatrix}2 & 0 \\0 & 2.5\end{bmatrix}$, devemos multiplicar cada componente por fatores distintos, isto é, $x$ por 2 e $y$ por 2.5.} \\ \\
&\text{ Assim sendo teríamos $\lambda_x=2$ e $\lambda_y=2.5$\,.}
\end{flalign*}
$$

***

4. A matriz de transformação que projeta qualquer vetor do plano na direção $\mathbf{v}=\mycolv{v_1\\v_2}$ pode ser obtida pelo produto $\mathbf{v}\cdot\mathbf{v}^T$, isto é, considerando $\mathbf{v}$ como um vetor unitário.
$$
\mathbf{v}\cdot\mathbf{v}^T=\mycolv{v_1\\v_2}\cdot\mathbf{[}v_1\;\; v_2\mathbf{]}
\;\therefore\;A=
\begin{bmatrix}
v_1^2 & v_1v_2 \\
v_1v_2 & v_2^2
\end{bmatrix}
$$

***



4. $\text{(a).}$ O vetor $\mathbf{u}=\mycolv{2\\1}$ projetado sobre o vetor $\mathbf{v}=\mycolv{-1\\2}$ corresponde à seguinte transformação:
$$
\text{P}_\mathbf{v}(u)=\mycolv{0\\0}
$$
**Explicação.** Primeiramente, empregaremos a seguinte fórmula para projeção: $\boxed{\text{P}_{\mathbf{v}}(u)=\langle\mathbf{u}\,|\,\hat{\mathbf{v}}\rangle\cdot\hat{\mathbf{v}}}$. De antemão, teremos que normalizar o vetor $\mathbf{v}$ que será feito abaixo:
$$
\begin{flalign*}
&\text{1.\quad Encontrando a norma do vetor:\quad}\|\text{v}\|=\sqrt{(-1)^2+(2)^2}=\sqrt{5}&& \\
\end{flalign*}
$$
$$
\begin{flalign*}
&\text{2.\quad Deduzindo o vetor unitário:\quad}\text{v}_\text{unit}=\dfrac{\text{v}}{\|\text{v}\|}=\mycolv{-\frac{1}{\sqrt{5}}\\\frac{2}{\sqrt{5}}}&&
\end{flalign*}
$$
$$
\begin{flalign*}
&\text{3.\quad Calculando o produto interno entre }\mathbf{u}\text{ e }\hat{\mathbf{v}}\text{: }\langle\mathbf{u}\,|\,\hat{\mathbf{v}}\rangle=\mycolv{-\frac{1}{\sqrt{5}}\\\frac{2}{\sqrt{5}}}\cdot\mycolv{2\\1}
=-\dfrac{2}{\sqrt{5}}+\dfrac{2}{\sqrt{5}}=0&&
\end{flalign*}
$$
$$
\begin{flalign*}
&\text{4.\quad Multiplicando o produto interno pelo vetor unitário }\hat{\mathbf{v}}\text{: }\langle\mathbf{u}\,|\,\hat{\mathbf{v}}\rangle\cdot\hat{\mathbf{v}}=0\cdot\mycolv{-\frac{1}{\sqrt{5}}\\\frac{2}{\sqrt{5}}}=0&& \\ \\
\end{flalign*}
$$
Por fim, concluímos que a projeção $\text{P}_\text{v}(u)$ corresponde ao vetor nulo, como foi visto acima.

***

4. $\text{(b).}$ O ângulo entre os vetores $\mathbf{u}$ e $\hat{\mathbf{v}}$ é um ângulo reto $(90\degree)$. Segundo a definição de produto interno, podemos expressá-lo da seguinte forma:
$$
\langle\,u|v\,\rangle=\|u\|\cdot\|v\|\cdot\cos(\theta\degree)
$$
Desse modo, como sabemos que os vetores em questão são ortogonais temos que $\cos(90\degree)=0$ e, portanto, a fórmula da projeção resultará em zero.
Podemos demonstrar que o ângulo entre os vetores é reto facilmente, como será feito abaixo:
$$
\begin{flalign*}
&\text{1.\quad Sabemos que o produto interno entre }\mathbf{u}\text{ e }\hat{\mathbf{v}}\text{ é nulo de acordo com a questão anterior.}&& \\ \\
&\text{2.\quad Aplicando esse dado na fórmula do produto interno teremos:\quad}0=\|u\|\cdot\|v\|\cdot\cos(\theta\degree)\;\therefore\;\frac{0}{\|u\|\|v\|}=\cos(\theta\degree).&& \\ \\
&\text{3.\quad Portanto, como $\cos(\theta\degree)=0$, nos resta a opção de $\theta=90\degree$.}
\end{flalign*}
$$

***

4. $\text{(c).}$ Como foi calculado no terceiro passo da questão $\text{4. (a)}$, o produto interno entre $\mathbf{u}$ e $\hat{\mathbf{v}}$ vale zero. Porém, recapitulando temos:
$$
\langle\mathbf{u}\,|\,\hat{\mathbf{v}}\rangle=\mycolv{-\frac{1}{\sqrt{5}}\\\frac{2}{\sqrt{5}}}\cdot\mycolv{2\\1}
=-\dfrac{2}{\sqrt{5}}+\dfrac{2}{\sqrt{5}}=0
$$
***

5. Para determinar a reflexão do vetor $\mathbf{u}$ em torno de $\mathbf{v}$, visualizaremos esses dois vetores no plano juntamente de $R(u)$ da seguinte forma:

```tikz
\begin{document}
\begin{tikzpicture}[scale=1.7]
    % Eixos
    \draw[->] (-3,0) -- (3,0) node[right] {$x$};
    \draw[->] (0,-3) -- (0,3) node[above] {$y$};
    
    % Vetores
    \draw[->,red,thick] (0,0) -- (-1,2) node[midway, below left] {$\mathbf{v} = (-1, 2)$};
    \draw[->,blue,thick] (0,0) -- (2,1) node[midway, below right] {$\mathbf{u} = (2, 1)$};
    \draw[->,black,thick,dashed] (0,0) -- (-2, -1) node[midway, below right] {R($\mathbf{u}$)};
    
    % Ângulo reto
    \draw[thick] (-0.13,0.25) arc (135:45:0.4);
    \node at (0.18,0.6) {$90^{\circ}$};
    
    % Pontos de origem
    \fill (0,0) circle (1pt) node[below right] {Origem};
\end{tikzpicture}
\end{document}
```

Assim sendo, a matriz necessária para a reflexão do vetor $\mathbf{u}$ corresponde a $A=\begin{bmatrix}-\frac{3}{5} & -\frac{4}{5} \\ -\frac{4}{5} & \frac{3}{5}\end{bmatrix}$. Podemos obtê-la por meio da seguinte expressão:
$$
\boxed{R=I-\dfrac{2}{{\|v\|}^2}\mathbf{v}\cdot\mathbf{v}^T}
$$
Em que,    
- $I$ corresponde à matriz identidade $\begin{bmatrix}1 & 0\\ 0 & 1\end{bmatrix}$.
- $\|v\|$ equivale à norma do vetor $\mathbf{v}$.
- $\mathbf{v}\cdot\mathbf{v}^T$ traduz para a matriz de projeção em torno de $\mathbf{v}$.

Por fim, o ângulo entre o vetor $\mathbf{u}$ e $\mathbf{v}$ é o mesmo que entre $R(\mathbf{u})$ e $\mathbf{v}$. Por outro lado, temos a seguinte relação entre os ângulos de $\mathbf{u}$ e seu reflexo $R(\mathbf{u})$:

```tikz
\begin{document}
\begin{tikzpicture}[scale=1.7]
    % Eixos
    \draw[->] (-3,0) -- (3,0) node[right] {$x$};
    \draw[->] (0,-3) -- (0,3) node[above] {$y$};
    
    % Vetores
    \draw[->,red,thick] (0,0) -- (-1,2) node[midway, below left] {$\mathbf{v} = (-1, 2)$};
    \draw[->,blue,thick] (0,0) -- (2,1) node[midway, below right] {$\mathbf{u} = (2, 1)$};
    \draw[->,black,thick,dashed] (0,0) -- (-2, -1) node[midway, below right] {R($\mathbf{u}$)};
    
    % Ângulo reto
    \draw[thick] (-0.13,0.25) arc (135:45:0.4);
    \node at (0.18,0.6) {$90^{\circ}$};
    
    % Ângulo entre u e x
    \draw[thick] (0.6,0) arc (0:26.57:0.6);
    \node at (0.6,0.155) {$-$};
    
    % Ângulo oposto ao ângulo entre u e x
    \draw[thick] (-0.6,0) arc (180:206.57:0.6);
    \node at (-0.58,-0.15) {$-$};
    
    % Pontos de origem
    \fill (0,0) circle (1pt) node[below right] {Origem};
\end{tikzpicture}
\end{document}
```
