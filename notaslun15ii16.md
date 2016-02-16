# Notas lunes 15II16
## Medios deformables
Habló de tensores y matrices. Dijo que los tensores con los que vamos
a trabajar son matrices.

Definió dos productos chistosos

$T:U \equiv T_{ij}U_{ji}$ y $T\cdot\cdot U \equiv T_{ij}U_{ji}$.

También definió el producto tensorial de dos vectores:

$$
\begin{matrix}
  1\\2\\3
\end{matrix}
\begin{matrix}
  4&5&6
\end{matrix}.
$$

O algo así.

### Transformación de una base

La transformación se hace a través de los cosenos
directores:
$$
a^r_k = \cos (\bar{x_k},x_i)
$$
la barrada es la nueva base.
$\bar{e_r} = a^s_r e_s$ y $e_s = a^r_s e_r$.
## Mecánica estadística

Construyó las caminatas aleatorias. ¿Cuál es la probabilidad
de que en $N$ pasos esté en el lugar $m$?

Primero definió las cantidades $n_1$ como el número de pasos
a la derecha y $n_2$ es el número a la izquierda que cumplen
la propiedad $n_1+n_2 = N$. Nótese que no hay referencia, no hay
orden, i.e., no nos importa si primero dio uno a la derecha u otro a
la izquierda; sólo nos interesa el total de pasos a la izquierda y a
la derecha.

¿De cuántas maneras se puede obtener $N = n_1 + n_2$?
Pues $N!/n_1! (N_n_1)!$.

Después como cada paso es un evento estadísticamente
independiente $p^{n_1}$ con $p$ la probabilidad de ir a la
derecha y $q$ la probabilidad de ir a la izquierda. La
probabilidad es $p^{n_1} q^{N-n_1}$. Por lo que la
distribución de probabilidad es:

$$W_N (n_1) = \binom{N,n_1} p^{n_1} q^{N-n_1}$$,

que es la probabilidad de $n_1$ pasos a la derecha, $n_2$ pasos a la
izquierda y de cuántas maneras se pueden dar. Cuando $p$ es
mayor que $q$ el máximo se va a la derecha de $N/2$ y lo
contrario.

Calculo el promedio de la distribución que recordamos está dada por:

$$\langle n_1 \rangle &= \sum_{n_1 = 0}^N n_1 P(n_1)
&= \sum_{n_1 = 0}^N \frac{n!}{n_1!(N-n_1)!}n_1 p^{n_1}q^{N-n_1}.$$
aquí utilizamos el trucazo que también apareció por ahí en cuántica:
$$
n_1 p^{n_1} = p \frac{\partial}{\partial p} p^{n_1}
$$
por lo que lo último nos queda
$$
= \sum \frac{N!}{n_1! (N-n_1)!} p \frac{\partial}{\partial p} p^{n_1}
q^{N-n_1}.
$$
sacamos la derivada
$$
= p\frac{\partial}{\partial p} \sum \frac{N!}{n_1!(N-n_1)!}
p^{n_1}q^{N-n_1} = p\frac{\partial}{\partial p}(p+q)^N = p N
(p+q)^{N-1} = pN.
$$
De la misma forma se obtiene que $\langle n_2 \rangle = Nq = N(1-p)$.

El segundo momento también se calcula con $\sum x_1^2 P(x_1)$ y ahora
usamos $n_1^2 p^{n_1} = n(n_1p^{n_1}) = n_1 \frac{\partial}{\partial
p}(p\frac{\partial}{\partial p}p^{n_1})$ y nos da $(Np)^2 + Np(1-p)$.
También $\langle n_2^2\rangle = N^2(1-q)^2 + Nq(1-q)$.

La __varianza__ está dada por
$$
\begin{align*}
  \sigma_{n_1}^2 &= \bar{(\Delta n_1)^2}\\
                 &= \bar{(n_1-\bar{n_1})^2}\\
                 &= \bar{n_1^2} - (\bar{n_1})^2 = Npq.
\end{align*}
$$

Un __gas ideal__ es aquel en el que las moléculas no
interaccionan.

El __macroestado__ es el estado termodinámico en equilibrio.
El estado mecánico del sistema es un microestado.

La mecánica estadística no busca demostrar/derivar la
termodinámica, «estamos muy lejor de ello», sino que busca
dar una descripción compatible con ella.

Ensamble, conjunto representativo, colectividad. Gibbs en
1900 introduce los __ensambles__.

Lo que tienen en común es el macroestado pero están en un
microestado, como cuando hablábamos del macroestado como los
que tuvieran el mismo número de monedas arriba y el
microestado las distintas configuraciones. El ensamble
__microcanónico__ es el que está aislado.

La probabilidad de que esté en cierto estado es $1/\Omega$
que no nos dijo cual era eso $\Omega$.

Consideró un volumen $V_0$ y lo separó en $V$ y $V'$.
Definió la probabilidad $p = V/V_0$ ya que consideró que es
lo mismo que el número de eventos __favorables__ sobre el
número de eventos __totales__. $q = V'/V_0 = V_0/V_0 - V/V_0
= 1 - V/V_0$. Se parece mucho al de las caminatas
aleatorias. Y nos preguntamos de cual es la $P(n)$ de que
$n$ moléculas se encuentren en $V$.
## Computación

Los `pull request` se actualizan al hacer `commit`.

`isodd` para los ciclos.

Fortran es la que tiene la libreria de álgebra lineal más rápida. Un
número se representa como $x = (-1)^{\sigma} 2^{2013 + e} m$ con $m$
la mantisa, $e$ el exponente y $\sigma$ el signo.


La preferencia para representar p.g. $12.3679$ es $1.23679 \times 10$
y se toma el exponente y demás. El entero más grande es $2^{53}-1$.

Funciones interesantes `prevfloat`. Para evitar la aritmética modular
se usa `BigInt`.
