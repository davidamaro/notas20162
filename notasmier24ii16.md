# Notas
## Medio deformables
Un esfuerzo es fuerza por unidad de área.

## Mecánica estadística
El objetivo de la mecánica estadística es obtener las propiedades
termodinámicas utilizando propiedades microscópicas.
El sistema sobre el que se trabaja es el siguiente:

1. $N$ partículas $\sim 10^{23}$.
2. La dinámica de las partículas es clásica.
3. Están encerradas en un volumen $V$.
4. Las paredes son térmicamente aisladas.
5. Paredes rígidas.
6. Paredes impermeables.
7. Las partículas se les considera puntuales[^1]

El volumen en el que están encerradas las partículas está definido por
$V$, $E$ y $N$. Bajo estas condiciones no hay intercambio de energía.

La _ley cero_ de la termodinámica nos dice que dado un _tiempo característico_
se alcanza el estado de _equilibrio_. Este es el __macroestado__, i.e., el
__macroestado__ está caracterizado por $E$, $V$ y $N$.

¿Cuáles son los microestados? y ¿cómo los puedo describir?

Clasicamente la descripción de cada partícula está dada por su _posición_ y su _momento_. Por lo tanto, cada partícula tiene _seis grados de libertad_; todo el sistema tiene $6\times10^{23}$ grados de libertad.[^2]

La __hamiltoniana[^3]__ del sistema es

$$ H(\vec{r},\vec{p}) = \sum \frac{p_i^2}{2m}+
\frac{1}{2} \sum_{i\neq j} V(|\vec{r_i}-\vec{r_j}|).
$$

__NOTA__ $\vec{r}$ y $\vec{p}$ son variables estocástica.

Cada _punto_ del _espacio de muestreo_ es un _microestado_. El espacio de muestreo es lo mismo que el _espacio fase_ o también _espacio $\Gamma$_.

__NOTA__ suponemos que los valores que los valores de $p$ y $q$ son tantos que los tratamos como _continuos_. Todo este conjunto está _contenido_ en una __hipersuperficie__ dada por $E=\mathrm{constante}$.

Utilizamos las ecuaciones de Hamilton.

Encerramos en un hipervolumen _diferencia_ centrado en $(p,q)$. Nos preguntamos _¿Cuál es la probabilidad de que un microestado esté en un infinitesimal de volumen?_.

Se considera la función de densidad de $N$ cuerpos: $f_N$

$$
f_N(q,p,t) \, dqdp,
$$

es igual a la probabilidad de encontrar $N$ cuerpos __simultaneamente__ en el espacio infinitesimal $dqdp$ alrededor del $(q,p)$ al tiempo $t$.

Se le impone una condición de normalización: $\int f_N \, dqdp = 1$.

Ver [aquí](http://itp.uni-frankfurt.de/~valenti/WS13-14/all_1314_chap7.pdf) la deducción de la __ecuación de Liouville__. Simplemente añado, para convencerme observé que $d\vec{S} \cdot \vec{j}$ tiene las dimensiones correctas de partículas por unidad de tiempo.

La ecuación a la que se llegó en el curso es:

$$
\frac{\partial f_N}{\partial t} + \{f_n, H\} =0.
$$

[^1]: Es decir, no tienen grados de libertad internos de rotación.
[^2]: Cada segundo se dan $\sim 10^{19}$ colisiones, lo que crea otro microestado.
[^3]: NO es cuántica.
