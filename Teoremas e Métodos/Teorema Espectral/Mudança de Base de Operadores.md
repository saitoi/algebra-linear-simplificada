# Mudança de Base de Operadores

Digamos que temos a base ortonormal $\beta=\{u_{1},u_{2}\}$ sendo $T$ um operador do plano. Supondo que conhecemos $(Tu_{1})_{\beta}$ e $(Tu_{2})_{\beta}$, a matriz do operador linear $T$ definida na base $\beta$ corresponde a

```math
\begin{align}
(T)_{\beta}=\begin{bmatrix}| & | \\(Tu_{1})_{\beta} & (Tu_{2})_{\beta} \\| & |\end{bmatrix}\tag{1}
\end{align}
```

Portanto,

```math
(Tv)_{\beta}=(T)_{\beta}(v)_{\beta}
```

Veremos como isso se aplica a um operador autoadjunto $T$ que tem $u_{1}$ e $u_{2}$ como autovetores unitários associados aos autovalores $\lambda_{1}$ e $\lambda_{2}$.

```math
T(u_{1})=\lambda_{1}u_{1}\quad \text{e} \quad T(u_{2})=\lambda_{2}u_{2}
```

Considerando $u_{1}$ e $u_{2}$ como os vetores unitários do plano, reescreveremos na base $\beta$,

```math
(T(u_{1}))_{\beta}=(\lambda_{1},0)\quad \text{e}\quad (T(u_{2}))_{\beta}=(0,\lambda_{2})
```

pois

```math
\lambda_{1}\cdot u_{1}=\lambda_{1}\cdot u_{1}+0\cdot u_{2}\quad \text{e}\quad \lambda_{2}\cdot u_{2}=0\cdot u_{1}+\lambda_{2}\cdot u_{2}
```

Implementando o conceito da expressão $(1)$, mas agora considerando os autovalores $\lambda_{1}$ e $\lambda_{2}$, teremos

```math
\begin{align}
(T)_{\beta}=\begin{bmatrix}| & | \\(T(u_{1}))_{\beta} & (T(u_{2}))_{\beta} \\| & |\end{bmatrix}=\begin{bmatrix}\lambda_{1} & 0\\0 & \lambda_{2}\end{bmatrix}
\end{align}
```

Que corresponde a uma matriz diagonal.

O próximo passo é calcular a matriz $T$ na base canônica, ou seja, $(T)_{\varepsilon}$ dado que conhecemos $(T)_{\beta}$. Isso só será possível se conhecermos as coordenadas do vetor de $\beta$ relativamente a $\varepsilon$, ou vice-versa. Bom, conhecemos o resultado das 
seguintes expressões:

```math
\begin{align}
(\textup{id})_{\beta\varepsilon}=\begin{bmatrix}| & | \\u_{1} & u_{2} \\| & |\end{bmatrix}\quad \text{e}\quad (\textup{id})_{\varepsilon\beta}=(\textup{id})_{\beta\varepsilon}^{t}  
\end{align}
```

Para elucidar o raciocínio da transformação de $(T)_{\varepsilon}$ em $(T)_{\beta}$ utilizaremos diagramas.

Precisamos encaixar os seguintes diagrama

![[Diagramas de Conversão de Base1.svg|350]]

Para que o resultado final fique semelhante à conversão de $(w)_{\varepsilon}$ para $(T(w))_{\beta}$.

![[Diagrama Completo.svg|700]]

A fórmula correspondente ao diagrama é interpretada da direita para esquerda, ou seja, teríamos

```math
(\textup{id})_{\beta\varepsilon}(T)_{\beta}(\textup{id})_{\varepsilon\beta}(w)_{\varepsilon}=(T)_{\varepsilon}(w)_{\varepsilon}
```

Eliminando $(w)_{\varepsilon}$ obteremos

```math
(\textup{id})_{\beta\varepsilon}(T)_{\beta}(\textup{id})_{\varepsilon\beta}=(T)_{\varepsilon}
```

- [i] Como podemos notar, acabamos caindo na expressão para a [[Mudança de Base de Operadores|decomposição espectral]] da matriz $(T)_{\varepsilon}$.
