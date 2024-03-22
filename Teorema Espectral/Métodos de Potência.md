# Métodos de Potência

> **Definição.** Algoritmo iterativo baseado no cálculo de potências sucessivas de um operador que, por sua vez, converge para um autovetor.

Seja $T$ um operador autoadjunto do plano, cujos autovalores não são nulos. Dado um vetor unitário $u_{0}$ qualquer, definimos a sequência $u_{0},u_{1},\dots$ recursivamente pela expressão abaixo

```math
u_{i}=\dfrac{T(u_{i-1})}{\|T(u_{i-1})\|}\tag{1}
```

**Lema.** *Sejam $v_{1}$ e $v_{2}$ vetores não nulos do plano. Se $v_{1}$ é múltiplo de $v_{2}$, então as normalizações de $v_{1}$ e $v_{2}$ são iguais, a menos o sinal. Em particular, se $a>0$, as duas normalizações são iguais.*

**Lema.** *Se $T$ é um operador linear autoadjunto cujos autovalores não são nulos e $u_{0}$ é um vetor do plano, então*

```math
u_{i}=\dfrac{T^{i}(u_{0})}{\|T^{i}(u_{0})\|}
```

$\textup{Demonstração.}$ Retornando à expressão $(1)$, denotaremos o inverso da norma de $T(u_{j})$ de $n_{j}$, agora substituindo na equação teremos

```math
u_{i}=n_{i-1}T(u_{i-1})\quad \text{e}\quad u_{i-1}=n_{i-2}T(u_{i-2}).
```

Substituindo a segunda igualdade na primeira teremos

```math
u_{i}=n_{i-1}n_{i-2}T^{2}(u_{i-2}).
```

Mas $u_{i-2}=n_{i-3}T(u_{i-3})$ de modo que

```math
u_{i}=n_{i-1}n_{i-2}T^{2}(n_{i-3}T(u_{i-3}))
```

Repetindo esse argumento repetidas vezes, obteremos finalmente

```math
u_{i}=n_{i-1}n_{i-2}\dots n_{0}T^{i}(u_{0}).
```

Portanto, como $n_{j}>0$, então pelo lema, $u_{i}$ é igual à normalização de $T^{i}(u_{0})$.

**Teorema** *Seja $T$ um operador autoadjunto do plano cujos autovalores distintos $\lambda_{1}$ e $\lambda_{2}$ satisfazem $\lvert \lambda_{1} \rvert>\lvert \lambda_{2} \rvert$. Se $u_{0}$ é um vetor unitário que não é um autovetor associado a $\lambda_{2}$, então a sequência $u_{0},u_{1},\dots$ definida na expressão $(1)$ tende a um autovetor de $T$ associado a $\lambda_{1}$.*

**Demonstração.** Sejam $w_{1},w_{2}$ autovetores unitários de $T$ associados aos autovalores $\lambda_{1}$ e $\lambda_{2}$. Como partimos do pressuposto que $\lambda_{1}\neq \lambda_{2}$, os vetores $w_{1}$ e $w_{2}$ são ortogonais. Logo, $\beta=\{w_{1},w_{2}\}$ é uma base ortonormal do plano e podemos fazer

```math
u_{0}=a_{1}w_{1}+a_{2}w_{2}
```

com $a_{1},a_{2}\in\Bbb{R}$. Sabemos que $a_{1}\neq 0$ pois estamos supondo que $u_{0}$ não é um múltiplo de $w_{2}$. Posto isso,

```math
T^{i}(w_{1})=T^{i-1}(T(w_{1}))=T^{i-1}(\lambda_{1}w_{1})=\lambda_{1}T^{i-1}(w_{1})
```

pois $w_{1}$ é um autovetor associado a $\lambda_{1}$. Repetindo o mesmo argumento

```math
T^{i}(w_{1})=\lambda_{1}T^{i-1}(w_{1})=\lambda_{1}T^{i-2}(T(w_{1}))=\lambda_{1}T^{i-2}(\lambda_{1}w_{1})=\lambda_{1}^{2}T^{i-2}(w_{1})
```

E, por fim, chegamos à conclusão

```math
T^{i}(w_{1})=\lambda_{1}^{i}w_{1}\quad \text{e}\quad T^{i}(w_{2})=\lambda_{2}^{i}w_{2}
```

Assim, aplicando $T^i$ a $u_0$, obtemos

```math
T^{i}(u_{0})=T^{i}(a_{1}w_{1}+a_{2}w_{2})=a_{1}T^{i}(w_{1})+a_{2}T^{i}(w_{2})=a_{1}\lambda_{1}^{i}w_{1}+a_{2}\lambda_{2}^{i}w_{2}
```

Como $\lvert \lambda_{1} \rvert > \lvert \lambda_{2} \rvert$, o termo $a_{1}\lambda_{1}^{i}w_{1}$ domina $a_{2}\lambda_{2}^{i}w_{2}$ para $i$ grande. Isso implica que $u_i$, a normalização de $T^i(u_0)$, converge para o autovetor $w_{1}$ associado a $\lambda_{1}$, conforme $i$ tende ao infinito.

*Continua na apostila do Collier..*

