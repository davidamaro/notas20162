# Notas
## Medios deformables

Hizo un repaso de calculo vectorial.

### Gradiente

Expresamos un vector $\vec{r}$ usando las coordenadas $q^i$ y luego calculamos
 $d\vec{r}$. Utilizando lo que aprendimos en termodinámica esto nos queda
$$
d\vec{r} = \frac{\partial \vec{r}}{\partial q^1} dq^1 +
\frac{\partial \vec{r}}{\partial q^2} dq^2 +
\frac{\partial \vec{r}}{\partial q^3} dq^3 = \frac{\partial \vec{r}}{\partial q^i} dq^i.
$$
Las derivadas respecto a $q^i$ las consideramos las bases y las nombramos $\vec{e}_i$.

Para cada una de estas derivadas, usamos la regla de la cadena con $q^i = q^i(x,y,z) = q^i(x_j)$.

Hacemos lo mismo con $\varphi = \varphi(q^1,q^2,q^3)$, i.e., calculamos
 $d\varphi$ y usando que $1 = \vec{e}_i\cdot\vec{e}^i$, obtenemos la expresión para el Gradiente.

 __Recuerda__ que el índice arriba que aparece en una derivada, es un índice abajo.

 Usando notación de Einstein $\nabla \equiv \hat{e}_i \frac{\partial}{\partial x_i}$.

 If any surface is defined by $φ(x) = \mathrm{constant}$, the unit normal to
the surface is determined from
$$
\hat{n}=\pm \frac{\nabla \varphi}{\vert \nabla \varphi\vert}, \qquad
\hat{n}=n_i\hat{e}_i,\qquad n_i=\frac{1}{\vert \nabla \varphi\vert}
\frac{\partial \varphi}{\partial x_i}
$$

El gradiente de un vector es:
$$
\nabla\mathbf{A} = \mathbf{\hat{e}}_j \frac{\partial}{\partial x_j}(A_i\mathbf{\hat{e}_i})=
A_{i,j}\mathbf{\hat{e}}_i\mathbf{\hat{e}}_j,
$$
con $A_{i,j} = \frac{\partial A_i}{\partial x_j}$.

El rotacional es

$$
\nabla\times\mathbf{A}=\varepsilon_{ijk} \mathbf{\hat{e}}_i A_{k,j}
$$

## Mecánica estadística

Comenzó haciendo un repaso de los conceptos más importantes de la clase pasada:

1. Microestado
  * Arreglo o configuración detallada.
  * Cada microestado es igualmente probable.
2. Macroestado
  * Propiedad física macroscópia que nos interesa describir.
  * Tiene asociados muchos microestados.
3. Variable aleatoria
  * Tiene un dominio (rango, espacio de muestreo, espacio muestral, espacio fase, etc...).
  * Tiene una $P_X(x_{\alpha})$ que se le llama __densidad de probabilidad__. Es la probabilidad de que $X$ tome el valor $x_{\alpha}$.

El nombre densidad de probabilidad viene del hecho de que si queremos encontrar
la probabilidad de que $X$ esté entre $x=a$ y $x=b$: $P(a\leq x\leq b) = \int_a^b dx\,P(x)$.

La conexión con la densidad de masa está dada por $\rho = M/V \to M=\rho V$,
tomando pequeños elementos $dM = \rho \, dV$ entonces, $M = \int \rho \, dV$.
También le pedimos la condición de normalización $\int P = 1$.

### Momentos

Se dijo algo sobre que al tener un equilibrio térmico las distribuciones son del
tipo gaussianas.

#### Promedio (primer momento)

$\langle X\rangle \equiv \bar{X} = \int x P(x) \, dS$.

#### Promedio (segundo momento)

$\langle x^2 \rangle \equiv \int P(x) x^2 \, dx$.

#### Varianza $\sigma_X^2$

La __varianza__ está definida como


Nos indica que tanto se aleja un valor posible del valor promedio.

No echó el choro sobre Boltzman que peleó contra todos en 1873.
$$
\begin{align}
\sigma_X^2 &= \langle x - \langle x \rangle^2\rangle\\
&= \int P(x) (x-\langle x \rangle)^2 \, dx\\
&= \int dx\, P(x) (x² - 2 x\langle x\rangle + \langle x \rangle^2)\\
&= \int P(x) x^2 dx - 2\langle x\rangle \int P + \langle x\rangle^2 \int P\\
&= \langle x^2\rangle - \langle x\rangle^2.
\end{align}
$$
La desviación estándar es la raíz de esto.

### Momento de orden $n$ y función característica

De manera similar,
$$
\chi(s) = \int P \exp(ixs) \, dx,\qquad P(x) = \frac{1}{2\pi} \int \chi(x) \exp(-ixs) \, ds,
$$

La __función característica__ es la transformada de Fourier de la densidad de probabilidad.
De la que a su vez podemos encontrar a la densidad de probabilidad:
$$
P(x) = \int P \exp(ixs) \, dx,\qquad P(x) = \frac{1}{2\pi} \int \chi(x) \exp(-ixs) \, ds,
$$
Por lo que $\chi(x) = \langle \exp(isx) \rangle$. Expandimos en serie de Taylor alrededor del 0:

$\chi(x) = \sum_n \frac{\chi^{(n)} (s=0)}{n!} s^n$. Le sacamos el promedio a esto y obtenemos que
$$
\chi(s) = \sum_n i^n \frac{\langle x^n\rangle s^n}{n!},
$$
por lo que $\langle x^n\rangle = \chi^{(n)}\vert_{s=0} / i^n$, hacemos el cambio $is \to t$ para tener que $\langle e^{isx}\rangle \to \langle e^{xt}\rangle = \int e^{tx} P dx$.

Expandimos la exponencial y encontramos los __momentos__ de distinto orden. La expansión
$$
M_x(t) = 1 + t \langle x\rangle + t^2/2! \langle x^2 \rangle + \cdots;
$$
se le conoce como la __función generadora de momentos__ y podemos ver al momento de orden $n$
como la derivada enésima de la función generador evaluada en $t=0$.
