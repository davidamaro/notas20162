# Notas
## Física nuclear y subnuclear
Escribió la solución a la ecuación de Schrödinger en coordenadas esféricas. Esta solución es una onda plana en dichas coordenadas. Obtuvo ciertas relaciones y las usó para simplificar la expresión con la que trabajaría.

Una vez que obtuvo esto hizo un repaso de dispersión en mecánica cuántica.

### Repaso dispersión

Comenzó hablando de el ángulo de dispersión $\vartheta$. Luego habló de la dispersión de Rutherford que lo más interesante es  la forma en la que obtiene la expresión ya que al usar

Aproxima las funciones esféricas de Bessel por una función oscilante. Dicha función oscilante al sustituir en la aproximación de Born el potencial coulombiano se obtiene una integral de 0 a $\infty$ del seno la cual no existe, por lo que se hace el truco de hacer que el potencial coulombiano tenga ahora un decaimiento exponencial lo que provoca que ahora la función sí exista (después se toma el límite cuando el término exponencial se hace uno).

Habló de la sección eficaz: después de la dispersión nos queda una onda plana y una onda circular que tiene una dirección radial que forma un ángulo de dispersión. Cuando proyectamos este valor obtenemos una relación que tiene la siguiente forma:
$$
d\sigma = \hat{e}_r j dA = d\Omega.
$$

Lo que vamos a medir es:
$$
\vec{j} \cdot \vec{i}_r \, dA.
$$

### Sección eficaz para la dispersión de Rutherford

#### Sección eficaz

La aproximación es
$$
\lim_{kr\to\infty} j_l (kr) = -\frac{1}{2ikr}
\left[
\exp\bigl(-i(kr-l\pi/2)\bigr)-
\exp\bigl(i(kr-l\pi/2)\bigr)
\right] \approx \sin (kr - l\pi/2)
$$

La solución a la ecuación de Schrödinger es
$$
\begin{align}
\psi(\vec{r}) = \exp(i\vec{k}\cdot\vec{r}) &=
4\pi \sum_{l=0}^{\infty} \,
\sum_{m=-l}^l i^l j_l(kr) Y_{lm}^*(\vec{k}) Y_{lm}(\vec{r})\\
&=
\sum_l (2l+1) i^l j_l(kr) P_l(\cos \vartheta)\\
&\to
\frac{i}{2k} \sum_{l=0}^{\infty} (2l+1) i^l
\left[
\frac{\exp\bigl(-i(kr-l\pi/2)\bigr)}{r}-
\frac{\exp\bigl(i(kr-l\pi/2)\bigr)}{r}
\right]
\end{align}
$$

Debemos notar que podemos interpretar los términos de la exponencial como ondas entrantes y salientes. La ecuación anterior nos indica que la onda saliente no es afectada por el objetivo. Para tomar en cuenta esto se le añade un término $S_l(k)$ para que tome en cuenta esto. De esta forma la solución nos queda (al sumar y restar un cero tramposo):
$$
\exp(i \vec{k} \cdot \vec{r})+
\frac{i}{2k} \sum_l (2l+1)\frac{1-S_l(k)}{r}e^{-il\pi/2} i^l P_l(\cos \vartheta) e^{ikr}
= \exp(i \vec{k} \cdot \vec{r})+ f(\vartheta) \exp(ikr)/r
$$
La identidad es:
$$
\sum_m Y_{lm}^* (\vec{k}) Y_{lm}(\vec{r}) = \frac{2l+1}{4\pi} P_l(\cos \vartheta).
$$

### Operador de flujo

Recordando las clases de Relatividad y más específicamente la ecuación de Klein-Gordon, el Operador de flujo está dado por:

$$
\vec{j} = \frac{\hbar}{2im}(\psi^* \vec{\nabla} \psi - \psi \vec{\nabla}\psi^*).
$$

Para la onda plana obtenemos $\hbar \vec{k}/m$.

Para la onda saliente obtenemos hasta orden que no tiene rápidas oscilaciones que pueden ser despreciadas:
$$
= \frac{\hbar \vec{k}}{m} + \frac{\hbar k}{m} \vec{i}_r \vert f(\vartheta)\vert^2 \frac{1}{r^2} + \cdots.
$$

Por lo tanto, lo que nosotros queremos medir está dado por
$$
\frac{\hbar k}{m} \frac{\vert f(\vartheta)\vert^2}{r²} r^2 \, d\Omega.
$$

La sección eficaz está dada por
$$
d\sigma = \frac{\vec{j}\cdot\vec{i}_r \, dA}{\hbar k/m} = \vert f(\vartheta)\vert^2 \,d\Omega
$$
### Aproximación de Born
La aproximación de Born está dada por
$$
f(\vec{q}) = - \frac{m}{2\pi\hbar^2} \int V(\vec{r})\exp(i\vec{q}\cdot\vec{r}/\hbar) \, d\vec{r},
$$
en donde, $\vec{q} = \vec{k}-\vec{k'}$ de la que al elevar al cuadrado y suponer que $k=k'$ obtenemos la relación con el ángulo $\vartheta$.
Básicamente la aproximación de Born es de la forma $\psi_i V \psi_f$. $q=2k\sin \vartheta/2$.

Escribimos algunos pasos:
$$
\begin{align}
f(\vec{q}) &= -\frac{m}{2\pi\hbar^2} \int V(r) e^{\frac{iqr\cos\vartheta}{\hbar}} \,d^3r\\
&= -\frac{m}{2\hbar^2 i} \int V(r) e^{\frac{iqr\cos\vartheta}{\hbar}} \,r r^2 dr d\cos\vartheta d\varphi\\
&=-\frac{2m}{\hbar q} \int_0^{\infty} dr\, rV(r)\sin\frac{qr}{\hbar}; \quad V(r)\to \frac{Z_1 Z_2 e^2}{r}\exp(-r/a) = -\frac{2m Z_1 Z_2 e^2}{q^2+(\hbar/a)^2},
\end{align}
$$
tomando el límite para $a$ grande:
$$f(q)=-\frac{2mZ_1Z_2e^2}{q^2}.$$
Por lo tanto, la sección eficaz es
$$
\frac{d\sigma}{d\Omaga}\vert_{R} = \vert f(\vartheta) \vert^2 = \frac{4m^2(Z_1Z_2 e^2)^2}{q^4}.
$$

El el número de partículas que cruzas la sección de área $dA$ que
subtiende un ángulo sólido $d\Omega$. El flujo incidente es $\hbar
k/m$.

La parte de dispersión, está [aquí](http://www.nucleares.unam.mx/~bijker/subnuclear/Extra02.pdf)
__Nota__. Sigo sin ver por qué se va el término $i^l$ en la expresión para $f(\vartheta)$.
