# Exercícios Collier.

2. Considerando o vetor $v=(2,3)$ em relação à base canônica, a sua representação na base ortonormal $\beta=\{\dfrac{1}{\sqrt{ 5 }}(1,2),\dfrac{1}{\sqrt{ 5 }}(2,-1)\}$ pode ser obtido de duas formas, apresentadas a seguir. Primeiramente, considere os vetores unitários da base ortonormal. 

```math
\begin{flalign}
&e_{1}=\dfrac{1}{\sqrt{ 5 }}\begin{bmatrix}1\\2\end{bmatrix}&& \\ \\
&e_{2}=\dfrac{1}{\sqrt{ 5 }}\begin{bmatrix}2\\-1\end{bmatrix}
\end{flalign}
```

Posto isso, podemos descrever o vetor $v$ por meio de uma combinação linear desses unitários. Desse modo, dados $a,b\in\Bbb{R}$ temos

```math
\begin{align}
(2,3)&=a\cdot\bigg(\dfrac{1}{\sqrt{ 5 }}(1,2)\bigg)+b\cdot\bigg(\dfrac{1}{\sqrt{ 5 }}(2,-1)\bigg) \\ \\
&=\bigg(\dfrac{a}{\sqrt{ 5 }},\dfrac{2a}{\sqrt{ 5 }}\bigg)+\bigg(\dfrac{2b}{\sqrt{ 5 }},\dfrac{-b}{\sqrt{ 5 }}\bigg)
\end{align}
```

Fazendo isso, teremos $2$ sistemas lineares como abaixo:

```math
\begin{align}
&\begin{cases}
2=\dfrac{a}{\sqrt{ 5 }}+\dfrac{2b}{\sqrt{ 5 }} \\ \\
3=\dfrac{2a}{\sqrt{ 5 }}-\dfrac{b}{\sqrt{ 5 }}
\end{cases} \\ \\
&\therefore \boxed{a=\dfrac{8}{\sqrt{ 5 }},b=\dfrac{1}{\sqrt{ 5 }}}
\end{align}
```

Por outro lado, poderíamos ter calculado a projeção de $v$ sobre cada vetor unitário da base ortonormal. Desse modo, as componentes $a,b$ corresponderiam ao produto interno de $v$ com os vetores unitários da questão.

```math
\begin{align}
v&=a\cdot(e_{1})+b\cdot(e_{2}) \\ \\
&=\langle v|e_{1} \rangle \cdot(e_{1})+\langle v|e_{2} \rangle \cdot(e_{2})
\end{align}
```

Este trecho reflete a substituição correta, transformando os vetores para a notação matricial padrão com o uso de matrizes.
