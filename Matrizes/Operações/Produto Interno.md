---
aliases:
  - escalar
  - interno_produto
tags:
  - ALA/operações
date: 2023-08-27
time: 10:50
complete: true
---
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
# Produto Interno

> $\textit{Definição.}$ *Operação matemática que associa duas grandezas vetoriais a um escalar (número real).*
## $\;$
Dados dois vetores $v$ e $u$ pertencentes a um espaço vetorial $\Bbb{R}^n,(\,\forall n\in\Bbb{N})$. A expressão para o produto interno é definida como:

$$
\boxed{v\cdot u=|v|\cdot|u|\cdot\cos\theta\degree}
$$

Por outro lado, quando tratamos das coordenadas dos vetores no produto interno obtemos outra expressão para determinação das componentes do vetor resultante. Aqui está a representação abaixo:

$$
\begin{align}
&v=\mycolv{v_{1}\\v_{2}\\\vdots\\v_{n}}\qquad u=\mycolv{u_{1}\\u_{2}\\\vdots\\u_{n}} \\ \\
\langle v|u \rangle&=\sum_{i=1}^{n}(v_{i}\cdot u_{i}) \\  \\
\langle v|u \rangle &=v_{1}u_{1}+v_{2}u_{2}+\dots+v_{n}u_{n}
\end{align}
$$
Por fim, podemos enxergar o produto interno de outra forma, isto é, como a multiplicação de duas matrizes. Considere os vetores $v=\mycolv{x\\y}$ e $u=\mycolv{u_{1}\\u_{2}}$, or produto deles resultaria em:
$$
\begin{align}
\langle v|u \rangle &=v^{T}\cdot u \\ \\
&=\mycolv{x & y}\cdot\mycolv{u_{1}\\u_{2}} \\ \\
&=x\cdot u_{1}+y\cdot u_{2}
\end{align}
$$

## $\text{Notação}$ 

Dados os dois vetores mencionados, o produto interno pode ser expresso de $2$ formas:
1. Notação de ponto: $v\cdot u$
2. Notação de Bra-ket: $\langle v|u \rangle$

## $\textup{Propriedades.}$

Considerando os vetores anteriores, aqui estão algumas propriedades do produto interno.

1. $\textup{Distributiva.}\; \langle v|u_{1}+u_{2} \rangle=\langle v|u_{1} \rangle+\langle v|u_{2} \rangle$
2. $\textup{Comutativa.}\; \langle v|u \rangle=\langle u|v \rangle$
3. $\textup{Norma.}\; \langle u|u \rangle=\|u\|^{2}$
4. 
