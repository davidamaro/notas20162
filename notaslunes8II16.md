## Física estadística
### Definiciones de probabilidad: ergodicidad y ensable}
Existen dos __principios de probabildiad__: uno es el
__clásico__ y el otro es el __estadístico__. Al
primero también se le llama __a priori__ porque este ya
conoce las probabilidades de los eventos simples. Al segundo
se le conoce también como __a posteriori__ porque para
conocer la probabilidad primero necesitamos conocer la
__frecuencia__ que es el número de __resultados
favorables__ obtenidos para un experimento sobre el número de
__resultados totales__, i.e., $F \equiv \displaystyle
\frac{n(N)}{N}$.

La única de las dos que toman en cuenta el __tiempo__ es la
estadística. Pero dado que es más fácil trabajar con la
clásica se formula el concepto de __ensamble__ que es
tomar un experimiento y realizarlo muchas veces __al
mismo tiempo__. También se introduce la hipótesis
__ergódica__, que nos dice que la probabilidad definida
utilizando el límite cuando $N\to\infty F$ es lo mismo que
obtener utilizar un ensamble con $N$ ejemplos.

El único sistema que se ha demostrado que se obtiene el
mismo resultado utilizando la probabilidad estadística y un
ensable es con el __billar__.

### Teoría de conjuntos
Siguió hablando de evento simple y dió sus ejemplos.
Además habló de escribir probabilidad usando conjuntos: si
dos eventos son __mutuamente excluyentes__ entonces la
probabilidad de que alguno, o ambos, ocurran es la suma. Si
no es así se tiene que utilizar teoría de conjuntos y vemos
que si $A \cup B = S$, entonces la probabilidad total es
$p(A) + p(B) - p(A\cup B)$ que quiere decir que es la
probabilidad de que ocurra $A$  y que ocurra $B$ pero que no
ocurran ambos.

Si $E_1$ y $E_2$ son dos eventos entonces, $p(E_1 E_2)$ es
la probabilidad de que ocurran ambos: $P(E_1 + E_2) = p(E_1)
+ p(E_2) - p(E_1 E_2)$. Por ejemplo, la probabilidad de que
salga un as es $4 1/52$ y que salga un rey es $4 1/52$, por
lo tanto la probabilidad de que salga un rey y un as es $8
1/52$.

Definió la probabilidad condicional como la probabilidad de
que obtengamos un evento una vez que otro a sido obtenido,
que se denota por $p(E_1|E_2)$. Los dos eventos son
independientes si $p(E_1|E_2) = p(E_1)$. Por eso se dice que
la probabilidad de que se cumple $E_1$ y $E_2$ es igual al
producto de la probabilidad de que obtengamos $E_1$ por la
probabilidad de obtener $E_2$ una vez obtenido $E_1$: $p(E_1
E_2) = p(E_2) p(E_2|E_1)$.

### Permutaciones y combinaciones
Queremos conocer de cuantas maneras podemos poner $r$
objetos de $n$ alineados en una fila utilizamos
permutaciones ya que este toma en cuenta el orden, p.g.,
$abc \neq bca$.

#### Aproximación de Stirling
% Revisar la notebook de Mathematica en donde tiene las
% otras aproximaciones.
Para ordenar $n$ objetos tenemos $n!$ formas de hacerlo. De
esta forma es necesario calcular el factorial de números más
o menos grandes. Para ello surge la aproximación de
Stirling, que aprimer orden (y el profesor comentó que es la
que vamos a utilizar es):
$$
  \log n! = \Sigma_{n=1}^N \log n \approx \int_{x=1}^n \log x
  \, dx = n \log n - (\log 1 - 1) \tilde n \log n -n,
$$
que al tomar exponenciales obtenemos $n! \approx n^n
\exp(-n)$. A segundo orden es $n! = \sqrt{2n\pi} n^n
\exp(-n)$.
% todo revisar la bibliografía para obtener una idea de
% demostrar el segundo orden.
