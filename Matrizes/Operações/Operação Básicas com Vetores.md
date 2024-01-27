---
aliases:
  - operacoes
tags:
  - ALA/operações
date: 2023-08-19
time: 03:11
complete: true
---

$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
# Operação Básicas com Vetores

> $\textit{Definição.}$ Refere-se às operações aritméticas que podem ser realizadas com grandezas vetoriais.

Principais operações que podem ser realizadas com vetores:

1. **Soma de vetores**. A soma de dois vetores resulta em um vetor cuja magnitude equivale à soma das magnitudes dos vetores originais e a direção é determinada junção das componentes dos vetores.

- **Representação algébrica.** Podemos tratar da soma de vetores de forma algébrica, isto é, representando a soma das componentes individuais dos vetores. Suponha os vetores $v$ e $u$ ambos pertencentes a $\Bbb{R}^n$, aqui está a interpretação algébrica:

$$
\begin{align*}
v=\mycolv{x_1\\y_1\\\vdots\\n_1}\qquad
&u=\mycolv{x_2\\y_2\\\vdots\\n_2} \\ \\
v+u\coloneqq\mycolv{x_1\\y_1\\\vdots\\n_1}+\mycolv{x_2\\y_2\\\vdots\\n_2}&=\mycolv{x_1+x_2\\y_1+y_2\\\vdots\\n_1+n_2}
\end{align*}
$$

- **Visualização.** Por outro lado, podemos tratar da soma de vetores com uma representação visual caso os vetores forem perceptíveis no plano cartesiano, ou seja, $v,u\in\Bbb{R}^n,(\,\forall\;n<4)$. Suponha os vetores $v$ e $w$ pertencentes a $\Bbb{R}^2$, aqui está a visualização da soma deles:


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

2. **Subtração de vetores.** Operação semelhante à soma de vetores, no entanto o vetor que está sendo subtraído terá seu sentido invertido. Por sua vez, a alteração feita modificará a representação visual de acordo.

- **Representação algébrica.** A ilustração algébrica da subtração entre vetores é semelhante à soma, porém as componentes são subtraídas (é claro 🥱). Considerando os mesmos vetores $u$ e $v$, aqui está a representação:

$$
v-u\coloneqq\mycolv{x_1\\y_1\\\vdots\\n_1}-\mycolv{x_2\\y_2\\\vdots\\n_2}=\mycolv{x_1-x_2\\y_1-y_2\\\vdots\\n_1-n_2}
$$

- **Visualização.** A representação visual da subtração de vetores pode ser feita da seguinte forma:

```tikz
\begin{document}
\begin{tikzpicture}
    % Vetor v
    \draw[->, ultra thick] (0,0) -- (3, 2);
    \node at (1.5, 1.5) {$\Huge \mathbf{\vec{v}}$};  
	\draw (3.09,0.7) node {$-$};
    
    % Vetor w
    \draw[->, ultra thick] (4.1, 0.1) -- (4.5, 1.6);
	\node at (4.7, 0.9) {$\Huge \mathbf{\vec{w}}$};
	\draw (5.3, 0.5) node {$=$};
	
    % Vetor resultante v+w
    \draw[->, ultra thick, red] (6.5,0) -- (9.1,0.5) node[midway, below right, red] {$\mathbf{\vec{v}} - \mathbf{\vec{w}}$};
	\draw[->, ultra thick, black, dotted] (6.5, 0) -- (9.5, 2);
	\draw[-, ultra thick, black, dotted] (9.5, 2) -- (9.1, 0.5);
\end{tikzpicture}
\end{document}
```

3. **Produto interno.** Possui uma seção reservada para a descrição do Produto Interno. Aqui está uma breve explicação.

![[Produto Interno#$ ;$]]

4. **Produto vetorial.** Possui uma seção reservada para a descrição do [[Produto Vetorial|produto vetorial]].

