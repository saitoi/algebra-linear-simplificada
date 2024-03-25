# Operação Básicas com Vetores

> **Definição.** Refere-se às operações aritméticas que podem ser realizadas com grandezas vetoriais.

## Soma

A soma de dois vetores gera vetor com magnitude equivalente à soma das magnitudes originais e direção determinada pela junção de suas componentes. Podemos representar a soma de vetores de <u>forma algébrica</u> e <u>visual</u>.

- **Representação algébrica.** Podemos tratar da soma de vetores de forma algébrica. Suponha os vetores $v$ e $u$ ambos pertencentes a $\Bbb{R}^n$, aqui está a interpretação algébrica:

```math
\begin{align*}
v=\begin{bmatrix}x_1\\y_1\\\vdots\\n_1\end{bmatrix}\qquad
&u=\begin{bmatrix}x_2\\y_2\\\vdots\\n_2\end{bmatrix} \\ \\
v+u\coloneqq\begin{bmatrix}x_1\\y_1\\\vdots\\n_1\end{bmatrix}+\begin{bmatrix}x_2\\y_2\\\vdots\\n_2\end{bmatrix}&=\begin{bmatrix}x_1+x_2\\y_1+y_2\\\vdots\\n_1+n_2\end{bmatrix}
\end{align*}
```

- **Visualização.** Por outro lado, podemos tratar da soma de vetores com uma representação visual caso os vetores forem perceptíveis no plano cartesiano, ou seja, $v,u\in\Bbb{R}^n,(\,\forall\;n<4)$. Suponha os vetores $v$ e $w$ pertencentes a $\Bbb{R}^2$, aqui está a visualização da soma deles:

*Vou adicionar a imagem..*

2. **Subtração de vetores.** Operação semelhante à soma de vetores, no entanto o vetor que está sendo subtraído terá seu sentido invertido. Por sua vez, a alteração feita modificará a representação visual de acordo.

- **Representação algébrica.** A ilustração algébrica da subtração entre vetores é semelhante à soma, porém as componentes são subtraídas (é claro 🥱). Considerando os mesmos vetores $u$ e $v$, aqui está a representação:

```math
v-u\coloneqq\begin{bmatrix}x_1\\y_1\\\vdots\\n_1\end{bmatrix}-\begin{bmatrix}x_2\\y_2\\\vdots\\n_2\end{bmatrix}=\begin{bmatrix}x_1-x_2\\y_1-y_2\\\vdots\\n_1-n_2\end{bmatrix}
```

- **Visualização.** A representação visual da subtração de vetores pode ser feita da seguinte forma:

Assim como a visualização da soma, a representação da subtração de vetores com o código TikZ requer um ambiente LaTeX compatível para ser visualizada corretamente.

3. **Produto interno.** Já temos uma seção reservada para o [produto interno](Produto%20Interno.md).

4. **Produto vetorial.** Já temos uma seção reservada para o [produto vetorial](Produto%20Vetorial.md).
