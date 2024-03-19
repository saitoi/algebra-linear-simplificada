# Reflexão

> **Definição.** Transformação linear que mapeia um vetor para um vetor refletido com relação a um plano ou espelho.

## Fórmula Geral

**Demonstração.** Considere um espelho definido pelo vetor unitário $u$ e outro unitário perpendicular a este, definido por $n$. Se $v$ for um vetor do plano, sua reflexão $\text{R}(v)$ será:

```math
\begin{align*}
\text{R}(v)=\text{Proj}_{u}(\text{R}(v))+\text{Proj}_{n}(\text{R}(v))\tag{1}
\end{align*}
```

Ou seja, $\text{R}(v)$ corresponde à soma das projeções sobres $u,v$. Como a reflexão de $v$ é feita sobre o espelho $u$, as coordenadas com relação a $u$ permanecerão idênticas à da projeção, enquanto as coordenadas com base na normal $n$ serão invertidas. Matematicamente, temos:

```math
\begin{align*}
&\text{Proj}_{u}(\text{R}(v))=\text{Proj}_{u}(v) \\ \\
&\text{Proj}_{n}(\text{R}(v))=-\text{Proj}_{n}(v)
\end{align*}
```

Logo, fazendo a substituição na equação $1$ teremos:

```math
\text{R}(v)=\text{Proj}_{u}(v)-\text{Proj}_{n}(v)\tag{2}
```

Como também sabemos que $v=\text{Proj}_{u}(v)+\text{Proj}_{n}(v)$, obteremos então disso:

```math
\begin{align*}
\boxed{\text{R}(v)=v-2\,\text{Proj}_{n}(v)} \\ \\
=v-2\langle n|v\rangle\cdot n\;\;
\end{align*}
```

Por fim, deduzimos a fórmula para a reflexão do vetor $v$ com relação ao espelho $u$ dada pela expressão:

```math
\begin{align*}
\boxed{\text{R}(v)=v-2\langle\,n|v\,\rangle\cdot n}\tag{}
\end{align*}
```

De modo que $n$ representa um vetor normal ao espelho, sendo escolhido arbitrariamente.

## $\texttt{Matriz de reflexão.}$

Para determinar a matriz de reflexão, retornaremos à expressão $\textup{(2)}$ e, ao invés de substituirmos o termo $\text{Proj}_{u}(v)$, trocaremos $\text{Proj}_{n}(v)$ no lugar. Desse modo, teremos

```math
\begin{align}
\text{R}(v)&=\text{Proj}_{u}(v)+(-\text{Proj}_{n}(v))\tag{2} \\ \\
\text{R}(v)&=\textup{Proj}_{u}(v)+(\textup{Proj}_{u}(n)-v) \\ \\
\text{R}(v)&=2\cdot\textup{Proj}_{u}(v)-v
\end{align}
```

Posto isso, considere o vetor genérico $v=\begin{bmatrix}x\\y\end{bmatrix}$ e seu espelho $u=\begin{bmatrix}u_{1}\\u_{2}\end{bmatrix}$. Podemos então afirmar que

```math
\begin{align}
\text{R}(v)&=2\cdot \textup{Proj}_{u}(v)-v \\ \\
&=2\cdot\begin{bmatrix}u_1^2 & u_1u_2 \\ u_1u_2 & u_2^2\end{bmatrix}\begin{bmatrix}x\\y\end{bmatrix}-\begin{bmatrix}x\\y\end{bmatrix} \\ \\
&=\begin{bmatrix}x\\y\end{bmatrix}\bigg(2\begin{bmatrix}u_1^2 & u_1u_2 \\ u_1u_2 & u_2^2\end{bmatrix}-I\bigg) \\ \\
&=\begin{bmatrix}x\\y\end{bmatrix}\underbrace{\begin{bmatrix}2u_1^2-1 & 2u_1u_2 \\ 2u_1u_2 & 2u_2^2-1\end{bmatrix}}_{\texttt{matriz de reflexão}}\\ \\
\end{align}
```

Desse modo, a matriz de reflexão em relação ao espelho $u$, ao considerar um vetor genérico $v$ é dada por:

```math
\begin{align}
A=\begin{bmatrix}2u_1^2-1 & 2u_1u_2 \\ 2u_1u_2 & 2u_2^2-1\end{bmatrix}
\end{align}
```

## Propriedades

Uma matriz de reflexão também é..

1. Matriz quadrada.
2. Matriz ortonormal.
3. Matriz inversa.

4. A direção do vetor espelho $u$ corresponde à soma do vetor original $v$ com seu reflexo $R(v)$.
