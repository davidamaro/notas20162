# Notas
## Medios
## Mecánica estadística

Recordó que el promedio es $Np$, con $N$ el número de partículas y $p$ la
probabilidad de que se encuentre en el volúmen $V$. Pensamos en la desviación
estándar. Se comentó que las fluctuaciones en la densidad (que es la variación
  respecto al valor promedio) son debidas a fenómenos como la disperisón.

Observó que la __varianza__ aumenta cuando el número de partículas aumenta. La
desviación estándar va como $\approx \sqrt{N}$. Pero este valor crece mucho, por
lo que definimos la __desviación estándar relativa__ (relativa al _promedio_)
como
$$
\sigma_p \equiv \sigma/\mu = \frac{1}{\sqrt{N}}
 \left(\frac{q}{p}\right)^{1/2}\approx\frac{1}{\srqt{N}}.
$$
Podemos notar que cuando $N\to\infty$ esta se va a cero que tiene sentido ya que
las variaciones deberían disminuir cuando aumenta el número de partículas. Las
fluctuaciones son pequeñas comparadas con el 1, _p.g._, para $N=10^{20}$
la $\sigma_p$ va como $1/10^{10}$.

Se hace la importante observación de que con esto asociamos a la densidad o el
número de partículas que son una cantidad macroscópia se le puede asociar un concepto
matemático, estadístico, como lo es el promedio del número de partículas (supongo que en un
  lado del volumen).

Como observamos que en una vecindad cerca del máximo de la distribución no cambia
mucho, trabajamos con el logaritmo: $\ln W(n) = \ln N! - \ln n! - \ln (N-n)! + n\ln p
+(N-n)\ln q$. Dado que las variaciones son pequeñitas podemos considerar $n\in\mathbb{R}$,
así que derivamos para encontrar el máximo. Este resulta ser igual a $\tilde{n} = Np$
(en la derivación se usa $p+q=1$ y que el logaritmo es una función multiplicativa).
Después se expande en serie de Taylor, se desprecian términos de orden tres y que el
valor de la segunda derivada evaluada en el máximo es $-1/Npq$. Se obtiene que
$\ln W(n) = \ln \tilde{W} - \frac{(n-\tilde{n})^2}{2Npq}$ y la exponenciamos.

La normalizamos utilizando la teoría de integrales gaußianas. Se obtiene que la
integral es $\tilde{W} \sqrt{\pi/(1/2Npq)} = 1$, por lo que $\tilde{W} = \frac{1}{\sqrt{2\pi Npq}}$.

Tomando en cuenta el promedio $\mu$ y la desviación estándar se escribe $P(n)$ como
$$
P(n) = \frac{1}{\sqrt{2\pi\sigma^2}}e^{-(n-\mu)^2/2\sigma^2}.
$$
Obtenemos el resultado de que en equilibrio termodinámico se formula en términos
de una distribución gaußiana.

### Caminata aleatoria

__Problema__. Después de dar $n+1$ pasos, encontrar la probabildad de que se encuentre
en la posición $m$. $P(m,n+1) \to P(t,n)$ cuando tenemos una distribución que depende
de un parámetro determinista (el tiempo) y otro estocástico (el número de pasos) se
le denomina __proceso estocástico__.
