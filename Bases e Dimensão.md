---
aliases:
  - LI_LD
tags:
  - ALA
  - P3
date: 2023-11-25
time: 13:31
complete:
---
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
# Bases e Dimensão

> $\textit{Definição de Base.}$ *Um conjunto finito de geradores $\beta$ de um subespaço $U$ é uma base se nenhum de seus vetores pode ser escrito como combinação de linear*.

Por esse viés, o subespaço gerado ao removermos um dos vetores de $\beta$ não é mais igual a $U$.

*Definição da base canônica..*

Suponha $w_{1},\dots,w_{m}$ geradores de um subespaço $U\in\Bbb{R}^{n}$. Considere então que
$$
G=\{w_{1},\dots,w_{m}\}
$$
*não* é uma base de $U$. Pela definição anterior de base, um ou mais desses vetores pode ser escrito como uma combinação linear dos demais. Reordenando os vetores, iremos supor que o *vetor impostor* é $w_{m}$. Logo, existem números reais $a_{1},\dots,a_{m-1}$ tais que
$$
w_{m}=a_{1}w_{1}+\dots+a_{m-1}w_{m-1}.
$$
Podemos reformular isso da seguinte forma
$$
a_{1}w_{1}+\dots+a_{m-1}w_{m-1}-w_{m}=0.
$$
Portanto, deduzimos que existe uma combinação linear dos vetores pertencentes ao conjunto $G$ que resulte em 0 *sem que todos os coeficientes da combinação sejam nulos*. Um conjunto de vetores com essa propriedade é dito **linearmente dependente**.

Por outro lado, um conjunto de vetores é considerado **linearmente independente** quando nenhum dos vetores desse conjunto pode ser expresso como uma combinação linear dos demais.

Para melhor entendermos a relação entre base, subespaço e a dimensão $\Bbb{R}^{n}$ aqui está uma ilustração representativa:

![[Bases, Geradores e Subespaços.svg|center|450]]

## Dimensão

> $\textit{Definição de Dimensão.}$ *Refere-se ao número de vetores independentes necessários para formar um espaço vetorial ou a quantidade de direções distintas que um espaço pode se estender*.

$\textup{Teorema.}$ *Se $U$ é um subespaço do $\Bbb{R}^{n}$, então*

1.  *U admite uma base.*
2. *Quaisquer duas bases de $U$ têm a mesma quantidade de elementos.*
3. *Qualquer subconjunto linearmente independente de $U$ pode ser completado para uma base de $U$.*

Segundo o teorema, a quantidade de elementos de um subespaço $U\neq∅$ do $\Bbb{R}^{n}$ não depende da base escolhida, mas apenas do subespaço $U$. Isso nos permite associar $U$ à quantidade de elementos de qualquer uma de suas bases ao qual denominamos de *dimensão*.

$\textup{Corolário.}$ *Se $U\subseteq W$ são subespaços do $\Bbb{R}^{n}$, então $\textup{dim}(U)<\textup{dim}(W)$.*

