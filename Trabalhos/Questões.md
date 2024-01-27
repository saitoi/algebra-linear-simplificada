---
aliases:
  - questoes
tags:
  - Exercícios
date: 2023-09-10
time: 22:35
complete:
---
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
### Nome: Pedro Henrique Honorio Saito

### DRE: 122149392

# $\texttt{Questões.}$

![[Questões.jpg | 800]]

# $\texttt{Resolução.}$

1. Um outro vetor unitário na direção $u$, tendo em vista que $u=\mycolv{u_1\\u_2}$ e $\|u\|=1$ seria seu inverso $-u$ cujas componentes são $-u=\mycolv{-u_1\\-u_2}$ e a norma permaneceria sendo $\|-u\|=1$.
---
3. Segundo a fórmula da reflexão proposta pela Juliana teríamos, relembrando:
$$
\boxed{R(n)=2\,\text{Proj}_{u}(n)-n}
$$
Isto é, em relação ao vetor $n$ e considerando $u$ como espelho. Portanto, expandindo a expressão da projeção obteríamos:
$$
\begin{align*}
R(n)&=2\,\text{Proj}_{u}(n)-n \\ \\
&=2\,(u\cdot\cancel{\langle n|u\rangle}^{0})-n \\ \\
&=0-n \\ \\
&=n
\end{align*}
$$
***
4. As possíveis coordenadas de $n$ seriam $n=\mycolv{-u_2\\u_1}$, pois para que o produto escalar resulte em zero basta que os vetores $n,u$ sejam ortogonais entre si.

Chegaremos a essa conclusão da forma descrita abaixo. Inicialmente, suponha que $n=\mycolv{a\\b}$.
$$
\begin{align*}
\langle n|u\rangle&=0 \\ \\
u_1\,a+u_2\,b&=0 \\ \\u_1\,a&=-u_2\,b
\end{align*}
$$
Desse modo, podemos selecionar quaisquer $a,b$ desde que a condição descrita seja atendida. Escolhendo por exemplo $b=u_1$ teremos $a=\dfrac{-u_2(u_1)}{u_1}\therefore a=-u_2$. 
***
5. 