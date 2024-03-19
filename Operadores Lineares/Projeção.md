# Projeção

> **Definição:** Processo de mapear um ponto (ou vetor) em um espaço para o mais próximo em um dado subespaço.

## Fórmula Geral

Considere a projeção de um vetor $v$ sobre um vetor qualquer não unitário $u$, teremos a expressão:

$$
\boxed{\textup{Proj}_{u}(v)=\|v\|\cos \theta\cdot \frac{u}{\|u\|}}
$$

Como foi visto no [produto interno](/Operações%20com%20Vetores/Produto%20Interno.md), podemos reescrever a fórmula acima da seguinte forma:

```math
\begin{aligned}
\textup{Proj}_{u}(v) &= \underbrace{\|v\|\cos \theta}_{\langle v|\hat{u} \rangle} \cdot \frac{u}{\|u\|} \\ \\
\textup{Proj}_{u}(v) &= \langle v|\hat{u} \rangle \cdot \hat{u}
\end{aligned}
```


**Obs.** Considerando que $\hat{u}$ é um vetor unitário.

## Matriz de Projeção

Calculamos a matriz para transformação de um vetor qualquer do plano $v$ em sua projeção $u$ da seguinte forma:

```math
\begin{aligned}
\textup{Proj}_{\hat{u}}(v) &= \langle u|v \rangle \cdot v \\ \\
&= (u^{T}v) \cdot u \\\\
&= \left(\big[u_1, u_2\big] \begin{bmatrix}x\\y\end{bmatrix}\right) \cdot \begin{bmatrix}u_1\\u_2\end{bmatrix}
\longrightarrow (u_1x + u_2y) \cdot \begin{bmatrix}u_1\\u_2\end{bmatrix} \\ \\
&= 
\begin{bmatrix}
u_1^2x + u_1u_2y \\
u_1u_2x + u_2^2y
\end{bmatrix}
\longrightarrow \underbrace{\begin{bmatrix}u_1^2 & u_1u_2 \\ u_1u_2 & u_2^2\end{bmatrix}}_{\text{matriz de projeção}} \cdot \begin{bmatrix}x\\y\end{bmatrix}
\end{aligned}
```

Portanto, a matriz de projeção sobre $u$, considerando $u\in\Bbb{R}^{2}$ é dada por

$$
A_{T}={\begin{bmatrix}u_1^2 & u_1u_2 \\ u_1u_2 & u_2^2\end{bmatrix}}
$$

> [!note] Projeção não tem inversa!
> É importante notar que a matriz de projeção não possui inversa, pois o espaço total é reduzido a uma dimensão e, portanto, não podemos reverter o processo.

## Projeção e transposta

Podemos reformular a fórmula da matriz de projeção por meio do conceito de transposição. Podemos fazer isso da seguinte forma:

$$
\begin{aligned}
A_{T} &= uu^{T} \\\\
&= \begin{bmatrix}
u_{1}\\
u_{2}
\end{bmatrix} [u_{1}\quad  u_{2}]
\\ \\
&= \begin{bmatrix}
u_{1}^{2} & u_{1}u_{2}\\
u_{1}u_{2} & u_{2}^{2} \\
\end{bmatrix}
\end{aligned}
$$

Como podemos ver, partindo do produto $uu^{T}$, obtemos a fórmula da matriz de projeção.
