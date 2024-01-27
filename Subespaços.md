---
aliases: 
tags:
  - ALA
  - P3
date: 2023-11-01
time: 21:04
complete:
---
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
# Subespaços

> $\textit{Definição.}$ Conjunto de vetores que satisfaz às propriedades de adição e multiplicação por escalar, formando assim uma estrutura linear dentro de um espaço vetorial.

As propriedades de adição e multiplicação mencionadas anteriormente, estão descritas abaixo. Considerando o subconjunto $\mathrm{H}\in\Bbb{R}^{n}$, poderemos chamá-lo de subespaço dadas as seguintes condições:

1. $u,v\in\mathrm{H}\implies u+v\in\mathrm{H}$.
2. $\lambda \in\Bbb{R}^{}\implies \lambda u\in\mathrm{H}$.

- Verificar essa informação:
> Ao trabalhar com um sistema de três ou mais variáveis, precisamos isolar algumas delas e por em função das outras.

### <span style="color:#ff0000">Preciso melhorar a parte abaixo.</span>

Como saber se um sistema linear é homogêneo:

1. Está escrito na forma $Ax=0$.

## $\texttt{Operações com Subespaços.}$

**Interseção.** Refere-se ao conjunto de todos os vetores que pertencem simultaneamente a dois ou mais subespaços vetoriais. Suponha a interseção entre os subespaços $U$ e $U'$ juntamente de um vetor $u$ pertencente a ambos subespaços:
$$
u\in U\land u\in U'\iff u\in U\land U'
$$
Repare que dessa forma, se $u,v\in U\land U'$, então
$$
\begin{flalign}
&1.\;  u\in U\land u\in U'&& \\
&2.\;  v\in U\land v\in U'&&
\end{flalign}
$$
Logo, chegamos à conclusão que: $u+v\in U\land u+v\in U'\to u+v\in U\land U'$.

O mesmo vale se $\lambda \in\Bbb{R}^{}$ e $(x)$ então, $\lambda u\in U\land \lambda u\in U'$. Com isso, mesmo que $U\land U'$ é também um subespaço. **Exemplo**: Encontre $U\land U'$, sabendo que
$$
\begin{align}
U=&\{(x,y,z,w)\in\Bbb{R}^{4}|x+y+z+w=0\} \\ \\
U'=&\{(x+y+z+w)\in\Bbb{R}^{4}|x+2y=z+3w=0\}
\end{align}
$$

**União**: Refere-se ao conjunto de todos os vetores que pertencem a pelo menos um dos subespaços vetoriais considerados, podendo ser dado pela soma:
$$
U+U'=\{u+u'|u\in U\; \text{e}\; u'\in U'\}
$$
Para calcular a soma, basta encontrar os geradores de cada subespaço.

**Exercício**: Encontre os geradores de $U$ e $U'$ do exemplo anterior e a partir deles uma base para $U+U'$.

**Complementar**: Refere-se ao conjunto de todos os vetores que estão no espaço vetorial subjacente, mas não estão no subespaço em questão, podendo ser dado pela seguinte expressão:
$$
U^{t}=\{v\in\Bbb{R}^{n}|\langle v|u \rangle =0\; \forall\; u\in U \}
$$
Como empregamos o produto interno, vale lembrar suas [[Produto Interno|propriedades]].