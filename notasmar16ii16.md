# Notas martes 16/II/16
## Física nuclear y subnuclear
Inicio hablando de la distribución de carga. Definió el factor de forma como la
transformada  de Fourier de la densidad.

El factor de forma está dado por
$$
\begin{align}
F(\vec{q}) &= \int d\vec{r} \, e^{i\vec{q}\cdot\vec{r}/\hbar} \, \rho(r)\\
&= \int r^2 dr d\cos\vartheta d\varphi \, e^{iqr\cos\vartheta} \rho(r)\\
&= \frac{4\pi\hbar}{q} \int dr \, r\rho(r) \sin\left(\frac{qr}{\hbar}\right).
\end{align}
$$
Se expande en serie de Taylor para $qr/\hbar \ll q$ y obtenemos que el primer
término es la condición de normalización y el segundo es proporcional al _mean
square root_ del radio. De la que se deduce la ecuación:
$$
\langle r^2 \rangle_{ch} = - 6\hbar^2 \frac{dF}{dq^2}\vert_{q=0},
$$
evaluarlo en $q=0$ mata al término de orden cuarto y se evalúa en el origen.

Una delta de Dirac correspondería a la dispersión de Rutherford.

Se tiene la relación
$$
\langle r^2\rangle^{1/2}_{ch} = 0.94 A^{1/3} \,\mathrm{fm},
$$
en donde $A$ es el número de nucleones. Este valor no debe sorprendernos porque
tenemos que el volumen debe tener cierta relación con el número de nucleones.

El radio está dado por $R=\sqrt{5/3} \langle r^2\rangle^{1/2}_{ch}.

También $R = \Gamma_0 A^{1/3}$ con $\Gamma_0 = 1.2\,\mathrm{fm}$. Es el radio
del núcleo.

$7 \, \mathrm{fm}$ es el radio promedio de los núcleos pesados.

Probó varias distribuciones de carga. En particular la que tiene la forma:
$\rho = \rho_0$ cuando $r\leq R$ y cero en el resto. El valor de $\rho_0$ se puede
calcular utilizando la __normalización__, en este caso nos da
$$
\rho_0 = \frac{3}{4\pi R^3}.
$$
El factor de forma queda dado por:
$$
\frac{3}{b^2} (\sin b - b\cos b), \quad b=qR/\hbar. Obtenemos que el valor de
$\langle r^2\rangle = 3R^2/5$ distinto al radio del núcleo.

La distribución de Fermi está dada por:
$$
\rho(r) = \frac{N}{1+\exp\bigl((r-c)/a\bigr)}
$$
En los datos vemos que al inicio hay cierta discrepancia, esto es debido a que
formalmente la transformada de Fourier toma todo el rango de $q$ pero nosotros
sólo podemos trabajar con un $q_0\neq\infty$.

## FAMC

La notación es __s__ harp, __p__ rincipal, __d__ iffuse y __f__ undamental.
Después se sigue hasta
que se salta la __j__ porque algunos lenguajes no la pueden distinguir.

El magneton de Bohr va como $\mu_B = e\hbar/2mc$.
