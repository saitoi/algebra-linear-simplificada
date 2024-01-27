---
aliases:
  - projection
tags:
  - ALA/Operadores
date: 2023-08-30
time: 17:00
complete: true
---
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
# Projeção
 
> $\textit{Definição.}$ Transformação de um vetor em um subespaço ou plano que envolve o alinhamento deste vetor com algum outro especificado.

### $\textup{Principais formas de projeção.}$

1. **Projeção ortogonal.** Projeção de um vetor $v$ sobre os vetores base do espaço, tal como $î$ e $ĵ$ por exemplo. Corresponde ao vetor resultante da projeção perpendicular de $v$ no subespaço. **Exemplo.** Considere a projeção do vetor $v$ sobre o eixo das abcissas no subespaço, tal como abaixo:
$$
\text{Proj}_{î}(v)=\big(\|v\|\cos\theta\big)\cdot î
$$
2. **Projeção não ortogonal.** Generalização da projeção ortogonal, isto é, envolve a projeção de um vetor $v$ no subespaço sem exigências de perpendicularidade. Consideramos um vetor $u$ sobre o qual realizamos a projeção nesse caso. **Exemplo.** Considere os vetores $v,u$ pertencentes ao subespaço $\Bbb{R}^n$ para algum $n\in\Bbb{N}$ de modo que $v$ será projetado sobre $u$.
$$
\text{Proj}_{u}(v)=\big(\|v\|\cos\theta\big)\cdot u
$$
É importante ressaltar que $u$ se trata de um vetor unitário e, caso contrário, devemos normalizá-lo.

## $\texttt{Fórmula geral.}$

Ao considerar uma projeção de $v$ sobre um vetor qualquer $u$ não unitário, teremos a seguinte expressão:
$$
\boxed{\text{Proj}_{u}(v)=\|v\|\cos\theta\cdot \dfrac{u}{\|u\|}}
$$
Como ja foi visto na seção de [[Produto Interno|produto interno]], podemos reescrever a fórmula acima empregando essa operação, da seguinte forma: ^2f5a98
$$
\begin{align}
\textup{Proj}_{u}(v)&=\underbrace{\|v\|\cos(\theta)}_{\langle v|\hat{u} \rangle }\cdot \underbrace{\dfrac{u}{\|u\|}}_{\hat{u}} \\
&=\langle v|\hat{u} \rangle \cdot\hat{u} \\ \\
\text{Proj}_{u}(v)&=\langle u|v\rangle\cdot u
\end{align}
$$
$\textbf{Obs.}$ Por questões de notação, escolhemos $u$ para representar o vetor unitário no lugar de $\hat{u}$ e consideramos que $\|\hat{u}\|=1$, pois se trata da norma do vetor unitário.

## $\texttt{Matriz de projeção.}$

A matriz que permite obter a transformação de um vetor $v$ qualquer do plano para sua projeção em $u$ pode ser obtida da seguinte forma.
$$
\begin{align*}
\text{Proj}_{\hat{u}}(v)&=\langle u|v\rangle\cdot u \\ \\
&=(u^T v)\cdot u \\ \\
&=\Bigg(\big[u_1,\,u_2\big]\mycolv{x\\y}\Bigg)\cdot\mycolv{u_1\\u_2}
\longrightarrow(u_1x+u_2y)\cdot\mycolv{u_1\\u_2} \\ \\
&=
\begin{bmatrix}
u_1^2x &+& u_1u_2y \\
u_1u_2x &+& u_2^2y
\end{bmatrix}\longrightarrow\underbrace{\mycolv{u_1^2 & u_1u_2 \\ u_1u_2 & u_2^2}}_{\texttt{matriz de projeção}}\cdot\mycolv{x\\y}
\end{align*}
$$
Posto isso, a matriz de projeção sobre $u$, considerando $u\in\Bbb{R}^2$, é dada pela fórmula abaixo:
$$
A_{T}=\mycolv{u_1^2 & u_1u_2 \\ u_1u_2 & u_2^2}
$$
> [!note] Matriz Inversa
> É importante ressaltar que a matriz de projeção não possui matriz inversa, pois o espaço total é reduzido uma dimensão e, portanto, não podemos reverter o processo.

## $\texttt{Projeção com transposta.}$

Podemos reformular a expressão da matriz de projeção para empregar a multiplicação entre matrizes ao invés do produto interno. Com vista disso, suponha um vetor $u=\mycolv{u_{1}\\u_{2}}$ unitário para o qual desejamos obter a matriz de projeção
$$
\begin{align}
A_{T}&=uu^{T} \\ \\
&=\mycolv{u_{1}\\u_{2}}\mathbf{[}u_{1}\quad  u_{2}\mathbf{]} \\ \\
&=\mycolv{u_{1}^{2} & u_{1}u_{2}\\u_{1}u_{2} & u_{2}^{2}}
\end{align}
$$
Como podemos ver, o produto entre $u$ e seu transposto $u^{T}$ resultou na matriz de projeção desejada.