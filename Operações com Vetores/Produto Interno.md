# Produto Interno

> **Definição.** *Operação matemática que associa duas grandezas vetoriais a um escalar (número real).*

Dados dois vetores $v$ e $u$ pertencentes a um espaço vetorial $\Bbb{R}^n,(\,\forall n\in\Bbb{N})$. A expressão para o produto interno é definida como:

$$
\boxed{v\cdot u=|v|\cdot|u|\cdot\cos\theta\degree}
$$

Por outro lado, quando tratamos das coordenadas dos vetores no produto interno obtemos outra expressão para determinação das componentes do vetor resultante. Aqui está a representação abaixo:

$$
\begin{align}
&v=\begin{bmatrix}v_{1}\\v_{2}\\\vdots\\v_{n}\end{bmatrix}\qquad u=\begin{bmatrix}u_{1}\\u_{2}\\\vdots\\u_{n}\end{bmatrix} \\ \\
\langle v|u \rangle&=\sum_{i=1}^{n}(v_{i}\cdot u_{i}) \\  \\
\langle v|u \rangle &=v_{1}u_{1}+v_{2}u_{2}+\dots+v_{n}u_{n}
\end{align}
$$

Por fim, podemos enxergar o produto interno de outra forma, isto é, como a multiplicação de duas matrizes. Considere os vetores $v=\begin{bmatrix}x\\y\end{bmatrix}$ e $u=\begin{bmatrix}u_{1}\\u_{2}\end{bmatrix}$, o produto deles resultaria em:

$$
\begin{align}
\langle v|u \rangle &=v^{T}\cdot u \\ \\
&=\begin{bmatrix}x & y\end{bmatrix}\cdot\begin{bmatrix}u_{1}\\u_{2}\end{bmatrix} \\ \\
&=x\cdot u_{1}+y\cdot u_{2}
\end{align}
$$

## Notação 

Dados os dois vetores mencionados, o produto interno pode ser expresso de $2$ formas:
1. Notação de ponto: $v\cdot u$
2. Notação de Bra-ket: $\langle v|u \rangle$

## Propriedades

Considerando os vetores anteriores, aqui estão algumas propriedades do produto interno.

1. **Distributiva.** $\langle v|u_{1}+u_{2} \rangle=\langle v|u_{1} \rangle+\langle v|u_{2} \rangle$
2. **Comutativa.** $\langle v|u \rangle=\langle u|v \rangle$
3. **Norma.** $\langle u|u \rangle=\|u\|^{2}$
