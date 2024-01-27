---
aliases:
  - minimo_quadrados
tags:
  - ALA
date: 2023-11-27
time: 13:32
complete:
---
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
# Método dos Mínimos Quadrados

> $\textit{Definição.}$ *Também conhecida como **regressão linear**, consiste em um método para melhor aproximar um conjunto de dados por meio de uma função matemática, minimizando a soma dos quadrados das diferenças entre os valores observados e os valores preditos pela função.*

Neste contexto, precisamos encontrar a reta que mais se adequa a um conjunto arbitrário de pontos no espaço. Para isso, calculamos a diferença entre cada valor previsto pela função da regressão e seus valores reais, e então procuramos reduzir essas diferenças utilizando cálculos de derivadas parciais. Para entendermos melhor, aqui está uma descrição detalhada. Considere  a seguinte tabela:
![[Tabela Mínimos Quadrados.svg|center|150]]
1. De antemão, analisamos o banco de dados que fornece as correspondências entre os pontos $x_{i}$ e $y_{i}$ para os quais calcularemos a diferença dos mínimos quadrados.
2. Feito isso, calculamos a distância entre os valores previstos pela função de regressão e as imagens $y_{i}$ descritas na tabela e elevamos o resultado ao quadrado, tal como abaixo:
$$
\begin{align}
d=\sqrt{ (\Delta x)^{2}+(\Delta y)^{2} }.
\end{align}
$$
Como o $x$ não sofre variação, consideramos que $\Delta x=0$ e, portanto, segue que
$$
\begin{align}
&=\sqrt{ (\Delta y)^{2} } \\
&=\Delta y \\
d_{i}&=(ax_{i}+b)-y_{i} \\
d_{i}^{2}&=((ax_{i}+b)-y_{i})^{2}
\end{align}
$$
3. Feito isso, devemos somar o quadrado de cada distância de modo a obtermos uma função de duas variáveis $a$ e $b$ que compõem a função de regressão linear. Desse modo, teremos
$$
\begin{align}
F(a,b)&=\sum_{i=1}^{n}d_{i}^{2}(a,b) \\
&=((ax_{1}+b)-y_{1})^{2}+\dots+((ax_{n}+b)-y_{n})^{2}
\end{align}
$$
4. Por fim, nos resta calcular a derivada parcial com relação às variáveis $a$ e $b$ de $F(a,b)$ a fim de encontrarmos um sistema linear de duas equações.
$$
\begin{align}
\dfrac{{\partial F}}{\partial a}&=f_{1}(a,b)=0 \\
\dfrac{{\partial F}}{\partial b}&=f_{2}(a,b)=0
\end{align}
$$






