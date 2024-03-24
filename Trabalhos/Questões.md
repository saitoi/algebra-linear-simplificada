# Questões.

![[Questões.jpg | 800]]

# Resolução.

1. Um outro vetor unitário na direção $u$, tendo em vista que $u=\begin{bmatrix}u_1\\u_2\end{bmatrix}$ e $\|u\|=1$ seria seu inverso $-u$ cujas componentes são $-u=\begin{bmatrix}-u_1\\-u_2\end{bmatrix}$ e a norma permaneceria sendo $\|-u\|=1$.

---

3. Segundo a fórmula da reflexão proposta pela Juliana teríamos, relembrando:

$$
\boxed{R(n)=2\,\text{Proj}_{u}(n)-n}
$$

Isto é, em relação ao vetor $n$ e considerando $u$ como espelho. Portanto, expandindo a expressão da projeção obteríamos:

$$
\begin{align*}
R(n)&=2\,\text{Proj}_{u}(n)-n \\ \\
&=2\,(u\cdot\cancel{\langle n|u\rangle}^{0})-n \\ \\
&=0-n \\ \\
&=n
\end{align*}
$$

---

4. As possíveis coordenadas de $n$ seriam $n=(-u_{2}, u_{1})$, pois para que o produto escalar resulte em zero basta que os vetores $n,u$ sejam ortogonais entre si.

Chegaremos a essa conclusão da forma descrita abaixo. Inicialmente, suponha que $n=\begin{bmatrix}a\\b\end{bmatrix}$.

$$
\begin{align*}
\langle n|u\rangle&=0 \\ \\
u_1\,a+u_2\,b&=0 \\ \\
u_1\,a&=-u_2\,b
\end{align*}
$$

Desse modo, podemos selecionar quaisquer $a,b$ desde que a condição descrita seja atendida. Escolhendo por exemplo $b=u_1$ teremos $a=\dfrac{-u_2(u_1)}{u_1}\therefore a=-u_2$.
