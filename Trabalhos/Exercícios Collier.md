---
aliases: 
tags:
  - Exercícios
date: 2023-09-16
time: 14:42
complete:
---
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
# $\texttt{Exercícios Collier.}$

2. Considerando o vetor $v=\mycolv{2\\3}$ em relação à base canônica, a sua representação na base ortonormal $\beta=\Bigg\{\dfrac{1}{\sqrt{ 5 }}(1,2),\dfrac{1}{\sqrt{ 5 }}(2,-1)\Bigg\}$ pode ser obtido de duas formas, apresentadas a seguir. Primeiramente, considere os vetores unitários da base ortonormal. 
$$
\begin{flalign}
&e_{1}=\dfrac{1}{\sqrt{ 5 }}\mycolv{1\\2}&& \\ \\
&e_{2}=\dfrac{1}{\sqrt{ 5 }}\mycolv{2\\-1}
\end{flalign}
$$
Posto isso, podemos descrever o vetor $v$ por meio de uma combinação linear desses unitários. Desse modo, dados $a,b\in\Bbb{R}$ temos
$$
\begin{align}
(2,3)&=a\cdot\bigg(\dfrac{1}{\sqrt{ 5 }}(1,2)\bigg)+b\cdot\bigg(\dfrac{1}{\sqrt{ 5 }}(2,-1)\bigg) \\ \\
&=\bigg(\dfrac{a}{\sqrt{ 5 }},\dfrac{2a}{\sqrt{ 5 }}\bigg)+\bigg(\dfrac{2b}{\sqrt{ 5 }},\dfrac{-b}{\sqrt{ 5 }}\bigg)
\end{align}
$$
Fazendo isso, teremos $2$ sistemas lineares como abaixo:
$$
\begin{align}
&\begin{cases}
2=\dfrac{a}{\sqrt{ 5 }}+\dfrac{2b}{\sqrt{ 5 }} \\ \\
3=\dfrac{2a}{\sqrt{ 5 }}-\dfrac{b}{\sqrt{ 5 }}
\end{cases} \\ \\
&\therefore \boxed{a=\dfrac{8}{\sqrt{ 5 }},b=\dfrac{1}{\sqrt{ 5 }}}
\end{align}
$$
Por outro lado, poderíamos calculado a projeção de $v$ sobre cada vetor unitário da base ortonormal. Desse modo, as componentes $a,b$ corresponderiam ao produto interno de $v$ com os vetores unitários da questão.
$$
\begin{align}
v&=a\cdot(e_{1})+b\cdot(e_{2}) \\ \\
&=\langle v|e_{1} \rangle \cdot(e_{1})+\langle v|e_{2} \rangle \cdot(e_{2})
\end{align}
$$
