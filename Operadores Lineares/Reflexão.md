---
aliases:
  - reflection
  - reflexao
tags:
  - ALA/Operadores
date: 2023-09-01
time: 16:18
complete: true
---
 $\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
# Reflexão

> $\textit{Definição.}$ Transformação linear que mapeia um vetor para um vetor refletido com relação a um plano ou espelho.

## $\texttt{Fórmula geral.}$

$\mathbf{Demonstração.}$ Considere um $\textit{espelho}$ definido pelo vetor unitário $u$ e outro unitário perpendicular a este, definido por $n$. Se $v$ for um vetor do plano e $\text{R}(v)$ seu reflexo com relação ao espelho $u$, temos que 
$$
\begin{align*}
\text{R}(v)=\text{Proj}_{u}(\text{R}(v))+\text{Proj}_{n}(\text{R}(v))\tag{1}
\end{align*}
$$
Ou seja, a reflexão de $v$ corresponde à soma das projeções sobres $u,v$ os quais formam uma base ortonormal no plano. Como a reflexão de $v$ é feita sobre $u$, podemos afirmar que as coordenadas em relação a $u$ permanecerão idênticas a da projeção, enquanto a componente da normal $n$ será invertida. Portanto, teríamos
$$
\begin{align*}
&\text{Proj}_{u}(\text{R}(v))=\text{Proj}_{u}(v) \\ \\
&\text{Proj}_{n}(\text{R}(v))=-\text{Proj}_{n}(v)
\end{align*}
$$
Logo, fazendo a substituição na equação $1$ teremos:
$$
\text{R}(v)=\text{Proj}_{u}(v)-\text{Proj}_{n}(v)\tag{2}
$$
Como também sabemos que $v=\text{Proj}_{u}(v)+\text{Proj}_{n}(v)$, obteremos então disso:
$$
\begin{align*}
\boxed{\text{R}(v)=v-2\,\text{Proj}_{n}(v)} \\ \\
=v-2\langle n|v\rangle\cdot n\;\;
\end{align*}
$$
Por fim, deduzimos a fórmula para a reflexão do vetor $v$ com relação ao espelho $u$ dada pela expressão:
$$
\begin{align*}
\boxed{\text{R}(v)=v-2\langle\,n|v\,\rangle\cdot n}\tag{}
\end{align*}
$$
De modo que $n$ representa um vetor normal ao espelho, sendo escolhido arbitrariamente.
$\mathbf{Obs.}$ Possíveis escolhas para $n$ seriam

## $\texttt{Matriz de reflexão.}$

Para determinar a matriz de reflexão, retornaremos à expressão $\textup{(2)}$ e, ao invés de substituirmos o termo $\text{Proj}_{u}(v)$, trocaremos $\text{Proj}_{n}(v)$ no lugar. Desse modo, teremos
$$
\begin{align}
\text{R}(v)&=\text{Proj}_{u}(v)+(-\text{Proj}_{n}(v))\tag{2} \\ \\
\text{R}(v)&=\textup{Proj}_{u}(v)+(\textup{Proj}_{u}(n)-v) \\ \\
\text{R}(v)&=2\cdot\textup{Proj}_{u}(v)-v
\end{align}
$$
Posto isso, considere o vetor genérico $v=\mycolv{x\\y}$ e seu espelho $u=\mycolv{u_{1}\\u_{2}}$. Podemos então afirmar que
$$
\begin{align}
\text{R}(v)&=2\cdot \textup{Proj}_{u}(v)-v \\ \\
&=2\cdot\mycolv{u_1^2 & u_1u_2 \\ u_1u_2 & u_2^2}\mycolv{x\\y}-\mycolv{x\\y} \\ \\
&=\mycolv{x\\y}\bigg(2\mycolv{u_1^2 & u_1u_2 \\ u_1u_2 & u_2^2}-I\bigg) \\ \\
&=\mycolv{x\\y}\bigg(2\mycolv{u_1^2 & u_1u_2 \\ u_1u_2 & u_2^2}-\mycolv{1 & 0 \\ 0 & 1}\bigg) \\ \\
&=\mycolv{x\\y}\underbrace{\mycolv{2u_1^2-1 & 2u_1u_2 \\ 2u_1u_2 & 2u_2^2-1}}_{\texttt{matriz de reflexão}}\\ \\
\end{align}
$$
Desse modo, a matriz de reflexão em relação ao espelho $u$, ao considerar um vetor genérico $v$ é dada por:
$$
\begin{align}
A=\mycolv{2u_1^2-1 & 2u_1u_2 \\ 2u_1u_2 & 2u_2^2-1}
\end{align}
$$
## $\texttt{Propriedades da matriz de reflexão.}$

Aqui estão algumas propriedades para identificar matrizes de reflexão.

1. A matriz de reflexão deve ser quadrada, isto é, o número de linhas é igual ao número de colunas.
2. A matriz deve ser ortogonal, suas linhas e colunas são vetores unitários perpendiculares entre si.
3. Quando multiplicada por si mesma deve resultar na matriz identidade $I$.
4. A direção do vetor espelho $u$ corresponde à soma do vetor original $v$ com seu reflexo $R(v)$.