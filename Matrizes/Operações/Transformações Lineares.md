---
aliases:
  - linear
  - transf
tags:
  - ALA
date: 2023-08-26
time: 13:14
---

# Transformações Lineares

> $\textit{Definição.}$ *Função que mapeia vetores de um espaço vetorial para vetores de outro espaço vetorial, de modo a preservar algumas propriedades fundamentais.*

**Propriedades fundamentais.** *Para quaisquer vetores $v$ e $u$, suponha uma transformação linear $T$ que parte de um espaço vetorial $V$ sobre um corpo $K$ 
para um espaço vetorial $W$ deve satisfazer as seguintes propriedades* :

1. Preservação da adição: $T(u+v)=T(u)+T(v)$.
2. Preservação do produto por escalar: $T(cu)=c\cdot T(u)$ para todo $c\in K$.

**Visualmente**, a transformação é dita linear se possui duas características principais:

1. Linhas permanecem linhas, sem curvatura.
2. A origem (vetor nulo) permanece fixo.

**Matriz de transformação linear.** A matriz composta pela conversão dos vetores unitários $\hat{i}$ e $\hat{j}$ é denominada matriz de transformação ou matriz de coeficientes.

Suponha que $T$ seja a transformação linear em questão. Se $T$ transforma $\mathbf{i}$ e $\mathbf{j}$ em $T(i)$ e $T(j)$ respectivamente, então a matriz resultante será:
$$
A=\big[T(i)\quad T(j)\big]
$$
De modo que as colunas serão as componentes $x$ e $y$ dos vetores base convertidos. Tendo em vista o exposto, para transformarmos um vetor $v$ do espaço vetorial $V$ para outro espaço $W$, basta multiplicarmos esse vetor pela matriz de transformação correspondente da seguinte forma:
$$
\mathbf{v}_{\in W}=\big[T(i)\quad T(j)\big]\cdot \mathbf{v}_{\in V}
$$

