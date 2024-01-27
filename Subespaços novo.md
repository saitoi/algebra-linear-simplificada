---
aliases: 
tags:
  - ALA
date: 2023-11-25
time: 12:51
complete:
---
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
# Subespaços novo

> $\textit{Definição.}$ Conjunto de vetores que satisfaz às propriedades de adição e multiplicação por escalar, formando assim uma estrutura linear dentro de um espaço vetorial.

Dado um sistema homogêneo qualquer $A\mathbf{x}=0$, o conjunto solução é dado por
$$
S_{A}=\{v\in\Bbb{R}^{n}|Av=0\}
$$
Com efeito, ambas as propriedades de adição e multiplicação oriundas dos [[Sistema Linear Homogêneo|sistemas homogêneos]] são aplicáveis de modo que denotamos o subconjunto $S_{A}$ de *subespaço*.

Nesse sentido, dizemos que um subconjunto não-vazio $U$ do $\Bbb{R}^{n}$ é um *subespaço* se, quaisquer que sejam os vetores $v,v' \in\Bbb{R}^{n}$ e o escalar $\lambda \in\Bbb{R}^{}$, temos que
$$
v+v' \in U\quad \text{e}\quad \lambda v\in U.
$$
- [i] Pela definição anterior, todo subespaço deve conter o 0, pois ele satisfaz ambas as propriedades descritas.

Por outro lado, também podemos definir *subespaços* por meio do conceito de [[Geradores|geradores]]. Considere os vetores $w_{1},\dots,w_{m}$ do $\Bbb{R}^{n}$ e o seguinte conjunto:
$$
W=\langle w_{1},\dots ,w_{m} \rangle
$$
composto por todas as combinações possíveis destes vetores. Para descobrirmos se um vetor do $\Bbb{R}^{n}$ pertence a $W$ verificamos se ele pode ser escrito como uma combinação linear de $w_{1},\dots,w_{m}$. Nesse sentido, se $v$ e $v'$ pertencem a $W$, então existem reais $a_{1},\dots,a_{m}$ w $b_{1},\dots,b_{m}$ tais que
$$
v=a_{1}w_{1}+\dots+a_{m}b_{m}\quad \text{e}\quad b'=b_{1}w_{1}+\dots+b_{m}w_{m}.
$$
Se somarmos esses vetores, obtemos
$$
v+v'=(a_{1}+b_{1})w_{1}+\dots+(a_{m}+b_{m})w_{m}
$$
o que nos permite concluir que $v+v'\in W$. Por fim, pela distributividade do produto por escalar,
$$
\lambda v=(\lambda a_{1})w_{1}+\dots+(\lambda a_{m})w_{m}
$$
também chegamos à conclusão de que $\lambda v\in W$ e, portanto, $W$ é um subespaço de $\Bbb{R}^{n}$.

## Operações com Subespaços

Tendo em vista que subespaços não são nada mais que conjuntos, podemos aplicar a aritmética de conjuntos aos subespaços a fim de gerar novos subespaços. Vamos investigar as operações de **interseção**, **união** e o conceito de **complementar** aplicados a subespaços.

### Interseção

Definimos a interseção de dois subespaços vetoriais $U$ e $U'$ como o conjunto de vetores que pertencem tanto a $U$ quanto $U'$. Nesse sentido, se um vetor $v$ pertence tanto ao subespaço $U$ quanto a $U'$, podemos afirmar que $v\in U\cap U'$. Com efeito as seguintes propriedades são válidas:

1. Se temos $v,w\in U\cap U'$, então $v+w\in U\cap U'$.
2. Se temos $v\in U\cap U'$ e $\lambda \in\Bbb{R}^{}$, então $\lambda v\in U\cap U'$.
3. A interseção entre dois subespaços quaisquer nunca será nula, pois $0\in U\cap U'$.

Por fim, temos que tratar da interseção de subespaços quando representada por meio de conjuntos. Com efeito, digamos que
$$
S_{A}=\{(x,y,z,w)\in\Bbb{R}^{4}|x+y+z+w=0\}\quad \text{e}\quad S_{B}=\{(x,y,z,w)\in\Bbb{R}^{4}|x+2y=z+3w=0\}.
$$
Tendo isso, a interseção entre ambos os subespaços corresponde a:
$$
S_{A}\cap S_{B}=\{(x,y,z,w)\in\Bbb{R}^{4}|x+y+z+w=x+2y=z+3w=0\}
$$
que equivale a reunir as expressões pertinentes a cada subespaço em um só conjunto de modo que o resultado será sempre 0 (como são sistemas homogêneos).

### União

Definimos a união de dois subespaços $U$ e $U'$ como a soma dos mesmos, isto é, a soma entre vetores pertencentes a cada subespaço individualmente. Por esse viés, se um vetor $v\in U$ e $v'\in U'$, então podemos afirmar que $v+v'\in U+U'$. Com efeito, as seguintes propriedades são válidas:

1. Novamente, as propriedades de soma e multiplicação por escalar são válidas.
2. Se temos $u\in U$ e considerando que $0\in U'$, então $u+0=u\in U+U'$. Logo, $U,U'\subseteq U+U'$.

Ademais, é útil verificarmos a interpretação de geradores no que diz respeito à soma de subespaços. Digamos que
$$
U=\langle w_{1},\dots,w_{k} \rangle \quad \text{e}\quad U'=\langle w_{1}',\dots w_{k}' \rangle.
$$
Como vimos anteriormente, tanto $U$ quanto $U'$ estão contidos em $U+U'$ de modo que
$$
w_{1},\dots,w_{k},w_{1}',\dots,w_{k}' \in U+U'.
$$
Por fim, há um caso especial de soma de subespaços para o qual designamos um nome próprio. Suponha $U,U'$ e $W$ subespaços do $\Bbb{R}^{n}$. Dizemos que $W$ é a *soma direta* de $U$ e $U'$ se
$$
W=U+U'\quad \text{e}\quad U\cap U'=\{0\}.
$$
Quando isso ocorre, dizemos que $W=U\oplus U'$. Em vista disso, considere a seguinte proposição:

$\textup{Proposição.}$ *Sejam $U,U'$ e $W$ subespaços do $\Bbb{R}^{n}$. Se $W=U\oplus U'$, então a união de uma base de $U$ com uma base de $U'$ produz uma base de $W$, de modo que $\textup{dim}(W)=\textup{dim}(U)+\textup{dim}(U')$.*

### Complementar

Dados dois subespaços $U$ e $U'$ do $\Bbb{R}^{n}$, dizemos que $U$ e $U'$ são *subespaços complementares* se, e  somente se,
$$
U+\overline{U}=\Bbb{R}^{n}\quad \text{e}\quad U\cap \overline{U}=\{0\}.
$$
Com efeito, a definição anterior sugere que $\Bbb{R}^{n}$ é resultado da *soma direta* entre $U$ e $\overline{U}$, de modo que $\overline{U}$ seria o *subespaço complementar* de $U$.

### Complemento Ortogonal

Definimos o complemento ortogonal de $U\in\Bbb{R}^{n}$ como sendo o conjunto de vetores do $\Bbb{R}^{n}$ que são ortogonais a todos os vetores de $U$, isto é,
$$
U^{\perp}=\{v\in \Bbb{R}^{n}|\langle v|u \rangle =0\; \text{ para todo }\; u\in U  \}.
$$
Tendo em vista que um dado subespaço $U$ do $\Bbb{R}^{n}$ admite um conjunto finito de geradores, se
$$
U=\langle u_{1},\dots,u_{m} \rangle
$$
e $v\in\Bbb{R}^{n}$ é ortogonal a cada um desses vetores, então
$$
\langle v|a_{1}v_{1},\dots,a_{m}u_{m} \rangle =a_{1}\langle v|u_{1} \rangle+\dots+a_{m}\langle v|u_{m} \rangle =0.
$$
Por fim, temos a seguinte proposição:

$\textup{Proposição.}$ *Se $U$ é um subespaço do $\Bbb{R}^{n}$, então:*

1. *$U^{\perp}$ é um complementar de $U$.*
2. $\Bbb{R}^{n}=U\oplus U^{\perp}$.
3. $(U^{\perp})^{\perp}=U$.

$\textup{Teorema Final.}$ *Todo subespaço do $\Bbb{R}^{n}$ pode ser definido por um conjunto de geradores ou como o conjunto solução de um sistema homogêneo.*

