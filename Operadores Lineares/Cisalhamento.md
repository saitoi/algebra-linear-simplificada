# Cisalhamento

> **Definição.** Transformação linear que deforma uma figura geométrica mantendo sua área, mas alterando a forma e orientação dos objetos.

Dado um número real $\alpha$, definimos o operador do cisalhamento como

```math
\begin{align}
c_{\alpha}(x,y)=(x+\alpha y,y)\;\;&\equiv\textquotedblleft \text{Cisalhamento Horizontal}\textquotedblright \\
&\text{ou} \\ 
c_{\alpha}(x,y)=(x,\alpha x+y)\;\;&\equiv \textquotedblleft \text{Cisalhamento Vertical}\textquotedblright  
\end{align}
```

Ou seja, a matriz de cisalhamento possui duas formas distintas a depender do tipo de cisalhamento. Normalmente, trabalhamos com o cisalhamento horizontal como visto abaixo.

```math
\begin{align}
c_{\alpha}=\begin{bmatrix}1 & \alpha  \\0 & 1\end{bmatrix}
\end{align}
```
