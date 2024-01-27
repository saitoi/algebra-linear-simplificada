---
aliases: 
tags:
  - ALA
date: 2023-11-27
time: 09:14
complete:
---
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
# Estudo Dirigido Subespaços

1. $(a)$ 

***

2. $(a).$ Após a aplicação do processo do Gram-Schmidt, encontramos que o subespaço gerado por $a_{1}$ e $a_{2}$ é equivalente ao gerado pelos vetores ortogonalizados $q_{1}$ e $q_{2}$. Por esse viés, a distância entre o vetor $a_{3}$ e o plano descrito anteriormente corresponde à diferença entre $a_{3}$ e sua projeção sobre nesse subespaço. Denotando de $d$ a distância que desejamos encontrar e de $\beta^{*}_{2}$ o conjunto formado pelos vetores ortogonalizados até $q_{1}$ e $q_{2}$, teremos
$$
\begin{align}
d&=a_{3}-\textup{Proj}_{\beta^{*}_{2}}(a_{3})\beta^{*}_{2} \\
d&=a_{3}-\langle a_{3}|q_{1} \rangle -\langle a_{3}|q_{2} \rangle.
\end{align}
$$
$(b).$ O tamanho ou norma de $a_{1}$ pode ser obtido facilmente ao considerarmos que $q_{1}$ corresponde à normalização de $a_{1}$. Nesse sentido, podemos deduzir que como
$$
q_{1}=\dfrac{a_{1}}{\|a_{1}\|},
$$
tendo em vista que se trata da primeira ortogonalização. Temos que
$$
\|a_{1}\|=\dfrac{a_{1}}{q_{1}}.
$$
$(c).$ O tamanho da projeção de $a_{3}$ sobre o plano gerado  