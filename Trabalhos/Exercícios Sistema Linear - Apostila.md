---
aliases: 
tags:
  - ALA
date: 2023-10-18
time: 18:27
complete:
---
$\newcommand\mycolv[1]{\begin{bmatrix}#1\end{bmatrix}}$
# Exercícios Sistema Linear - Apostila

6. Mostre que a quantidade máxima de operações por linha necessárias para transformar uma matriz $n\times n$ dada em sua forma escada por eliminação gaussiana é igual a $\frac{n(n-1)}{2}$.

Faremos essa questão por recursão. De antemão, precisamos tratar do caso base, ou seja, quando o número de operações restantes é apenas uma que corresponde à matriz abaixo.
$$
\mycolv{a_{n-1,n-1} & a_{n-1,n} \\a_{n,n-1} & a_{n,n}}
$$
Dada essa matriz, nos resta eliminar o termo $a_{n-1,n-1}$. Como sabemos, podemos escolher o elemento $a_{n-1,n-1}$ como pivô e multiplicarmos a matriz pela elementar $L_{21}\Big(-\dfrac{a_{n,n-1}}{a_{n-1,n-1}}\Big)$ a fim de elementar o elemento desejado. Feito isso, teremos a matriz em sua forma escada (triangular superior).
$$
\begin{align}
\alpha&=-\dfrac{a_{n,n-1}}{a_{n-1,n-1}} \\ \\
&=\mycolv{a_{n-1,n-1} & a_{n-1,n} \\a_{n,n-1} & a_{n,n}}\cdot L_{21}(\alpha) \\ \\
&=\mycolv{a_{n-1,n-1} & a_{n-1,n} \\0 & a_{n-1,n}\cdot \alpha+a_{n,n}}
\end{align}
$$
Portanto, o caso base se trata de uma matriz $2\times 2$ para a qual conseguimos obter a solução facilmente. Tendo isso, 

Com efeito, suponha que para uma matriz de tamanho $k\times k$ em que $k=n-1$, conseguimos resolver o sistema por eliminação gaussiana. Precisamos determinar quantas operações serão realizadas ao total.

Tendo uma matriz $k\times k$ e completa (sem lacunas ou elementos nulos), começaremos eliminando todos os elementos abaixo do primeiro $a_{1,1}$ multiplicando a matriz original pelos elementares $L_{21}\cdot L_{31}\dots L_{k1}$ e realizando um total de $k-1$ operações. Tendo feito isso, repetiremos o processo para uma matriz $k-1\times k-1$ até retornarmos ao caso base.

Como pode perceber, o número de operações aumenta gradualmente da matriz $2\times 2$ de um para $k-1$ em $k\times k$ o que corresponde a um somatório de $1$ até $k-1$. Segundo a fórmula da soma dos termos de uma PA, temos que
$$
\begin{align}
\sum_{i=1}^{k-1}i&=\dfrac{(i_{1}+i_{n})n}{2} \\
&=\dfrac{(i_{1}+i_{k-1})(k-1)}{2} \\
&=\dfrac{(1+(k-1))(k-1)}{2} \\
&=\dfrac{k(k-1)}{2}\tag{1}
\end{align}
$$
Portanto, encontramos que o número de operações total para a matriz $k\times k$ corresponde à expressão $(1)$. Agora nos resta provar para a matriz de tamanho $n\times n$ que, por sua vez, teria o mesmo número de operações que  a matriz de tamanho $k$ porém acrescida de $n-1$. Ou seja, como $k=n-1$ iremos substituir na expressão $(1)$:
$$
\begin{align}
&=\dfrac{(n-1)((n-1)-1)}{2} \\
&=\dfrac{(n-1)(n-2)}{2}
\end{align}
$$
Acrescendo $n-1$ à expressão temos
$$
\begin{align}
&=\dfrac{(n-1)(n-2)}{2}+n-1 \\
&=\dfrac{{(n-1)(n-2)+2(n-1)}}{2} \\
&=\dfrac{{(n-1)((n-2)+2)}}{2} \\
&=\dfrac{{n(n-1)}}{2}\quad \blacksquare 
\end{align}
$$
Concluindo a prova desejada.