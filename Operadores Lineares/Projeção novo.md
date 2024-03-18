# Projeção

> **Definição:** Processo de mapear um ponto (ou vetor) em um espaço para o mais próximo em um dado subespaço.

## Fórmula Geral

Considere a projeção de um vetor $v$ sobre um vetor qualquer não unitário $u$, teremos a expressão:

$$
\boxed{\textup{Proj}_{u}(v)=\|v\|\cos \theta\cdot \frac{u}{\|u\|}}
$$

Como foi visto no [[Produto Interno|produto interno]], podemos reescrever a fórmula acima da seguinte forma:

$$
\textup{Proj}_{u}(v)=\underbrace{\|v\|\cos \theta}_{\langle v|u \rangle }\cdot \frac{u}{\|u\|}
$$