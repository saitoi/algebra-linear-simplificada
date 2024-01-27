---
aliases:
  - gram-schmidt
tags:
  - ALA
  - P3
date: 2023-11-22
time: 18:56
complete:
---
# Algoritmo de Gram-Schmidt

> **Definição:** Método empregada para a ortogonalização de um conjunto de vetores (LI) em um espaço vetorial, transformando-os em um conjunto de vetores ortogonais entre si.

Dado um conjunto de vetores linearmente independentes, o algoritmo de Gram-Schmidt é aplicado para produzir um conjunto de vetores ortogonais que mantêm o mesmo subespaço. O processo ocorre da seguinte maneira:

1. Inicialmente, toma-se o primeiro vetor do conjunto linearmente independente $S$ e normaliza-se.
2. Em seguida, para cada vetor subsequente no conjunto, subtrai-se as projeções desse vetor nos vetores ortogonais já encontrados.
3. Feito isso, normaliza-se cada um desses vetores resultantes para obter um conjunto ortonormal que representa o mesmo espaço vetorial original, porém com vetores mutuamente ortogonais e de magnitude unitária.

$\textup{Algoritmo}$. *Dados vetores linearmente independentes $v_{1},\dots,v_{m}\in\Bbb{R}^{n}$, o algoritmo retorna uma base ortonormal do subespaço $\langle v_{1},\dots,v_{m} \rangle$*.

```c
gramSchmidt(Lista base) {
	Inicialize B como lista vazia;
	Atribua a u1 a normalização de v1;
	para i de 2 até m faça:
		calcule wi = vi - Proj(vi)_u1*u1 - ... - Proj(vi)_ui-1*ui-1;
		atribua a ui a normalização de wi;
		acrescente ui à B;
	retorne B.
}
```

Aqui está um exemplo da aplicação do processo de Gram-Schmidt:




