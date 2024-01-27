---
aliases:
  - base
  - mudanca_vetores
tags:
  - ALA
date: 2023-09-29
time: 16:17
complete: true
---
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
# Mudança de Base de Vetores

Considere a base canônica $\varepsilon=\{e_{1},e_{2}\}$ e outra base ortonormal $\beta=\{u_{1},u_{2}\}$ cujos vetores são
$$
u_{1}=(a_{11},a_{21})\quad \text{e}\quad u_{2}=(a_{12},a_{22})
$$
Posto isso, suponha um vetor $v$ cujas coordenadas, relativas à base ortonormal $\beta$, são
$$
(v)_{\beta}=(c_{1},c_{2})
$$
Por definição, o vetor $v$ pode ser descrito como $v=c_{1}u_{1}+c_{2}u_{2}$. Substituindo as coordenadas de $u_{1}$ e $u_{2}$ teremos
$$
\begin{align}
v&=c_{1}(a_{11},a_{22})+c_{2}(a_{12},a_{21}) \\ \\
&=\underbrace{\mycolv{c_{1}a_{11}+c_{2}a_{12} \\c_{1}a_{22}+c_{2}a_{21}}}_{(v)_{\varepsilon}}=\underbrace{\mycolv{a_{11} & a_{12} \\ a_{21} & a_{22}}}_{\textup{(id)}_{\beta\varepsilon}}\underbrace{\mycolv{c_{1} \\c_{2}}}_{(v)_{\beta}}\tag{1}
\end{align}
$$
Como pode perceber, denotamos a matriz $\textup{(id)}_{\beta\varepsilon}$ de $\textit{matriz de mudança de base}$ que corresponde a
$$
\begin{align}
\textup{(id)}_{\beta\varepsilon}=\mycolv{a_{11} & a_{12}\\ a_{21} & a_{22}}
\end{align}
$$
Usando essa notação, podemos escrever a equação $(1)$ como
$$
(v)_{\varepsilon}=\textup{(id)}_{\beta\varepsilon}\cdot(v)_{\beta}\tag{2}
$$
A notação $\textup{(id)}_{\beta\varepsilon}$ indica a matriz de transformação das coordenadas do vetor da base ortonormal $\beta$ para a convencional $\varepsilon$. Como podemos notar, a matriz de transformação equivale a
$$
\begin{align}
\textup{(id)}_{\beta\varepsilon}=\mycolv{| & | \\ (u_{1})_{\varepsilon} & (u_{2})_{\varepsilon}\\| & |}
\end{align}
$$
de modo que $\beta$ corresponde aos vetores $\{u_{1},u_{2}\}$ da base ortonormal. Por fim, podemos analisar o que acontece ao multiplicar a matriz $\textup{(id)}_{\beta\varepsilon}$ por sua transposta $\textup{(id)}_{\beta\varepsilon}^{t}$ obteremos
$$
\begin{align}
\textup{(id)}_{\beta\varepsilon}^{t}\textup{(id)}_{\beta\varepsilon}=\mycolv{\textemdash & u_{1}^{t} & \textemdash \\\textemdash & u_{2}^{t} & \textemdash}\mycolv{| & |\\ u_{1} & u_{2} \\| & |}=\mycolv{u_{1}^{t}u_{1} & u_{1}^{t}u_{2} \\u_{2}^{t}u_{1} & u_{2}^{t}u_{1}}
\end{align}
$$
No entanto, como $\beta$ se trata de uma base ortonormal, os vetores $u_{1}$ e $u_{2}$ satisfazem
$$
u_{1}^{t}u_{2}=\langle u_{1}|u_{2} \rangle =0\quad \text{e}\quad u_{i}^{t}u_{i}=\langle u_{i}|u_{i} \rangle =\|u_{i}\|^{2}=1,
$$
Para $i=1,2$. Substituindo na equação original teremos
$$
\textup{(id)}_{\beta\varepsilon}^{t}\textup{(id)}_{\beta\varepsilon}=I
$$
em que $I$ representa a matriz identidade. Posto isso, provamos que *a matriz de transformação entre duas bases é sempre uma matriz ortogonal.* Assim sendo, e se desejarmos fazer o contrário, isto é, partir de um vetor da base ortonormal para a base canônica. Bem, analisando a equação $(2)$ temos
$$
(v)_{\varepsilon}=\textup{(id)}_{\beta\varepsilon}\cdot(v)_{\beta}
$$
Multiplicando a expressão acima pela transposta $\textup{(id)}_{\beta\varepsilon}^{t}$ obteremos
$$
\textup{(id)}_{\beta\varepsilon}^{t}(v)_{\varepsilon}=\textup{(id)}_{\beta\varepsilon}^{t}\textup{(id)}_{\beta\varepsilon}\cdot(v)_{\beta}
$$
Podemos simplificar o lado direito obtendo
$$
\textup{(id)}_{\beta\varepsilon}^{t}(v)_{\varepsilon}=(v)_{\beta}
$$
Com efeito, podemos resumir tudo ao teorema abaixo.

$\textup{Teorema 3.1. }$ *Sejam $\varepsilon$ a base canônica e $\beta$ uma outra base ortonormal do plano. A matriz de mudança de base $\textup{(id)}_{\beta\varepsilon}$, obtida escrevendo em suas colunas as coordenadas dos vetores de $\beta$ relativamente à base canônica satisfaz:*
$$
\begin{flalign}
(i)\quad  & (v)_{\varepsilon}=\textup{(id)}_{\beta\varepsilon}(v)_{\beta}&& \\
(ii)\quad  &\textup{(id)}_{\varepsilon\beta}=\textup{(id)}_{\beta\varepsilon}^{t} && \\
(iii)\quad  &\textup{(id)}_{\beta\varepsilon}^{t}\textup{(id)}_{\beta\varepsilon}=I && \\
\end{flalign}
$$
