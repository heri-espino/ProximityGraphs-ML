Sí, pero solo en un sentido limitado: **las coordenadas polares habrían producido rápidamente otra fórmula para el volumen**, aunque no una fórmula más sencilla que la que obtuvimos para dimensión arbitraria.

Normalicemos los sitios como

\[
p=0,\qquad q=e_1,\qquad \lVert p-q\rVert=1,
\]

y escribamos un punto en coordenadas esféricas centradas en \(p\):

\[
z=r\omega,\qquad r\geq 0,\qquad \omega\in\mathbb S^{d-1}.
\]

Si \(\theta\) es el ángulo entre \(\omega\) y \(e_1\), entonces

\[
\lVert z-p\rVert=r,
\qquad
\lVert z-q\rVert
=
\sqrt{r^2+1-2r\cos\theta}.
\]

La región stepping-stone queda descrita por

\[
r^\alpha+
\left(r^2+1-2r\cos\theta\right)^{\alpha/2}
\leq 1.
\]

Podemos despejar el ángulo:

\[
\cos\theta
\geq
c_\alpha(r)
:=
\frac{1+r^2-(1-r^\alpha)^{2/\alpha}}{2r},
\qquad 0<r\leq1.
\]

Por tanto, para cada radio \(r\), las direcciones permitidas forman un casquete esférico de apertura

\[
\theta_\alpha(r)=\arccos c_\alpha(r).
\]

Esto da la fórmula polar

\[
a_{d,\mathrm{SS}}(\alpha)
=
\sigma_{d-2}
\int_0^1
r^{d-1}
\left(
\int_0^{\theta_\alpha(r)}
\sin^{d-2}\varphi\,\mathrm d\varphi
\right)
\mathrm dr,
\]

donde \(\sigma_{d-2}\) es el área de la esfera unitaria \(\mathbb S^{d-2}\).

En el plano se simplifica bastante:

\[
a_{2,\mathrm{SS}}(\alpha)
=
2\int_0^1
r\,
\arccos\left(
\frac{1+r^2-(1-r^\alpha)^{2/\alpha}}{2r}
\right)
\mathrm dr.
\]

Esa sí es una fórmula unidimensional relativamente corta.

Sin embargo, en dimensión general el integral angular introduce una beta incompleta:

\[
\int_0^{\theta}\sin^{d-2}\varphi\,\mathrm d\varphi
=
\frac12
B_{\sin^2\theta}
\left(\frac{d-1}{2},\frac12\right).
\]

Además, \(c_\alpha(r)\) contiene una resta numéricamente delicada cerca de \(r=0\):

\[
1-(1-r^\alpha)^{2/\alpha}.
\]

Por eso nuestra parametrización fue mejor para el objetivo del artículo. Aprovecha la **simetría axial** alrededor de la recta \(pq\): cada corte perpendicular es una bola de dimensión \(d-1\), y su volumen es simplemente

\[
\kappa_{d-1}y(x)^{d-1}.
\]

Más aún, las variables \(u\) y \(t\) que utilizamos son las distancias a los dos sitios. Es decir, nuestra construcción es esencialmente una parametrización mediante **distancias focales**, más adaptada a una región definida por

\[
\lVert z-p\rVert^\alpha+\lVert z-q\rVert^\alpha\leq1
\]

que las coordenadas polares ordinarias, las cuales privilegian un solo centro.

Polares sí serían particularmente cómodas en casos especiales:

\[
\alpha=2
\quad\Longrightarrow\quad
R_2(\theta)=\cos\theta,
\]

porque la región es la bola de Gabriel, y

\[
\alpha\to\infty
\quad\Longrightarrow\quad
R_\infty(\theta)=\min\{1,2\cos\theta\},
\]

que describe la lente del relative-neighborhood graph.

Entonces, la conclusión precisa es:

\[
\boxed{
\begin{aligned}
&\text{Polares: fórmula alternativa rápida y útil como verificación;}\\
&\text{cortes axiales + distancias focales: fórmula más explícita y estable}\\
&\text{para }d\geq2\text{ y }\alpha\text{ general.}
\end{aligned}}
\]

No elegimos un camino innecesariamente complicado: para el resultado general y la cuadratura estable, el método del artículo era más adecuado.