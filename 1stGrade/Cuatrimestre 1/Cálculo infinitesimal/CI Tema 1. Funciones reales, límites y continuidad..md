# 1.1 Funciones reales
##### Definiciones
1. Una **función real** (de variable real) en una variable es una función de la forma $f: A \longrightarrow \mathbb{R}$, donde $A \subset \mathbb{R}$.
2. Sea $f: A \longrightarrow \mathbb{R}$, la **gráfica de f** es un subconjunto de $\mathbb{R} \times \mathbb{R} = \mathbb{R}^{2}$, y se define como $\mathrm{Graf}(f) = \{ (x, f(x)) : x \in \mathrm{Dom}(f) \}$.
3. Sea $f: A \longrightarrow \mathbb{R}$ una función real y $k \in \mathbb{R} \backslash \{0\}$.
	1. La función $f(x+k)$ tiene la misma gráfica que $f$ pero **desplazada horizontalmente**, tantas unidades a la izquierda como $k$ (por lo que hacia la derecha si $k<0$).
	2. La función $f(x) + k$ tiene la misma gráfica que $f$ pero **desplazada verticalmente** tantas unidades como $k$.
	3. La función $|f(x)|$ tiene la misma gráfica que $f$ pero con sus **valores negativos espejados en el eje $X$**, es decir, convertidos a positivo.
###### Inciso sobre la función valor absoluto
1. $|f(x)|$ se define como la distancia de $f$ al 0 en la recta real, de la siguiente forma: $$
|f(x)| = \left\{ \begin{array}{l}
f(x) \text{ si } x \leq 0 \\
-f(x) \text{ si } x > 0
\end{array} \right. $$
2. Dada una desigualdad $|f(x)| \leq a$, para despejar $x$, basta con comprender que tanto $x$ como $-x$ serán menores o iguales a $a$, por lo que se puede escribir de la forma $-a \leq |f(x)| \leq a$.
	_Ej._ $|x-4| \leq 3 \implies -3 \leq x+4 \leq 3 \implies -7 \leq x \leq -1$.
3. **Desigualdad triangular**. $|x| \pm |y| \leq |x| + |y|$
4. **Desigualdad triangular inversa**. $\Big||x| - |y| \Big| \leq |x| + |y|$
##### Operaciones con funciones.
Sean $f,g$ funciones reales y $\lambda \in \mathbb{R}$.
1. **Suma**. $(f+g)(x) = f(x) + g(x), \forall x \in \mathrm{Dom}(f) \cap \mathrm{Dom}(g)$.
2. **Producto**. $(f \cdot g) = f(x) \cdot g(x), \forall x \in \mathrm{Dom}(f) \cap \mathrm{Dom}(g)$.
3. **Producto por escalar**. $(\lambda f)(x) = \lambda f(x), \forall x \in \mathrm{Dom}(f)$.
4. **Composición**. $(f \circ g)(x) = f(g(x)), \forall x \in \mathrm{Dom}(f) \cap \mathrm{Dom}(g)$.
	- _Ej._ $f(x) = x^{3} + 1, g(x) = \sqrt{ x } \implies (f \circ g)(x) = (\sqrt{ x })^{3} + 1, (g \circ f)(x) = \sqrt{ x^{3} + 1 }$.
	- No es **conmutativa**. $(f \circ g) \neq (g \circ f)$.
	- ***CUIDADO AL DOMINIO***. $\mathrm{Dom}(f \circ g) = \{\text{"Teniendo en cuenta los dominios de las funciones originales"\}}$.
##### Comprobar si una función es inyectiva
Ver [[CI Tema 0. Preliminares#Funciones inyectivas, sobreyectivas y biyectivas]].
- $f$ es inyeciva si $f(x) = f(y) \implies x = y$. Partiendo de esta definición se puede **comprobar** si una función es inyectiva. 
- _Ej:_$$
f(x) = \frac{x+1}{x-1} \implies \frac{x_{1} + 1}{x_{1} - 1} = \frac{x_{2}+1}{x_{2}-1} \implies (x_{1}+ 1)(x_{2} - 1) = (x_{2}+1)(x_{1}-1) \implies \cancel{x_{1}x_{2}} + x_{2} - x_{1} \cancel{-1} = \cancel{x_{1}x_{2}} +x_{1} -x_{2} \cancel{-1} \implies 2x_{1} = 2x_{2} \implies x_{1} = x_{2} \; \;\text{ La función es inyectiva.}$$
- También se puede comprobar a través de la **gráfica** de una función, si cualquier **recta horizontal** corta, como máximo, un solo punto de la gráfica.
##### Crecimiento y decrecimiento
Sea $f$ una función real e $I \in \mathrm{Dom}(f)$ un intervalo.
1. $f$ es **creciente** en $I$ si $f(x_{1}) \leq f(x_{2}), \forall x_{1},x_{2} \in I : x_{1} \leq x_{2}$.
2. $f$ es **decreciente** en $I$ si $f(x_{1}) \geq f(x_{2}), \forall x_{1},x_{2} \in I : x_{1} \leq x_{2}$.
3. Si en las definiciones anteriores se da que $f(x_{1}) \neq f(x_{2})$, se dice que $f$ es **estrictamente** creciente o decreciente, respectivamente.
4. $f$ es **constante** en $I$ si $f(x_{1}) = f(x_{2}), \forall x_{1},x_{2} \in I$, es decir, _es creciente y decreciente a la vez_.
##### Acotación de funciones
Ver [[CI Tema 0. Preliminares#Acotación de intervalos]]
Sea $f: \mathrm{Dom}(f) \longrightarrow \mathbb{R}$ y $A \subset \mathrm{Dom}(f)$.
- $f$ está **acotada superiormente** en $A$ si $\exists M \in \mathbb{R} : f(x) \leq M, \forall x \in A$. $M$ es una **cota superior de $f$**.
- $f$ está **actoada inferiormente en $A$** si $\exists m \in \mathbb{R} : f(x) \geq M, \forall x \in A$. $m$ es una **cota inferior** de $f$.
- $f$ está acotada si lo está **inferior y superiormente**.
##### Extremos
Sea $f$ una función real y $a \in \mathrm{Dom}(f)$.
- $a$ es un **máximo global** si $f(x) \leq f(a), \forall x \in \mathrm{Dom}(f)$.
- $a$ es un **mínimo global** si $f(x) \geq f(a), \forall x \in \mathrm{Dom}(f)$.
- $a$ es un **máximo relativo** si $\exists \delta > 0 : f(x) \leq f(a),  \forall x \in (a - \delta, a + \delta)$.
- $a$ es un **mínimo relativo** si $\exists \delta > 0 : f(x) \geq f(a),  \forall x \in (a - \delta, a + \delta)$.
##### Simetrías
Sea $f$ una función real y $P \in \mathbb{R} \backslash \{0\}$.
- $f$ presenta **simetría par** si $f(x)=f(-x), \forall x \in \mathrm{Dom}(f)$.
- $f$ presenta **simetría impar** si $f(x) = -f(-x), \forall x \in \mathrm{Dom}(f)$.
- $f$ es **periódica** si $f(x) = f(x+P), \forall x \in \mathrm{Dom}(f)$, y se llama **periodo** a $P$.
---
# 1.2 Límites de funciones
##### Definición de límite
Sea $f: \mathrm{Dom}(f) \longrightarrow \mathbb{R}$, $I \subset \mathrm{Dom}(f), x_{0} \in I, y_{0} \in \mathbb{R}$.
- Se dice que el **límite de $f$ cuando $x \to x_{0}$** es $y_{0}$, denotado como $\lim_\limits{ x \to x_{0}} f(x) = y_{0}$, si se cumple que $$
\forall \varepsilon, \exists \delta : 0 < \left| x - x_{0} \right| < \delta \implies 0 < \left| f(x) - y_{0} \right| < \varepsilon 
$$
- *Ej. 1.* Comprobar que $\displaystyle{\lim_\limits{ x \to 0 } \frac{3x + 1}{2}} = \frac{1}{2}$.
	1. Formular la pregunta: sustituir valores concretos en la definición del límite.
	Sea $\forall \varepsilon > 0$, ¿$\exists\delta > 0 : 0< |x - 0| < \delta \implies 0 < \left| \frac{3x + 1}{2} - \frac{1}{2} \right| < 0$? $$ \begin{gather} \left| \frac{3x+1}{2} - \frac{1}{2} \right| = \left| \frac{3x}{2} \right| = \frac{3}{2} |x| \implies \frac{3}{2} |x| < \varepsilon \implies |x| < \frac{2\varepsilon}{3}, \text{recordando que } 0 < |x| < \delta \\ \end{gather} $$
	2. $\left. \begin{array}{l} |x| < \frac{2\varepsilon}{3} \\ |x| < \delta \end{array} \right\}$, Es necesario ahora tomar un valor arbitrario de $\delta$ para continuar, así que lo más sencillo es suponer que $\delta = \frac{2\varepsilon}{3}$, pues ya se sabe que es también menor que $|x|$.
	3. Para comprobar entonces que todo esto cumple la existencia de $\varepsilon$, basta con retomar la expresión recién obtenida.
	$$ |x| < \frac{2}{3} \varepsilon \implies \left|\frac{3x+1}{2} - \frac{1}{2} \right| = \frac{3}{2} |x| < \cancel{\frac{3}{2}} \cancel{\frac{2}{3}} \varepsilon$$
- *Ej. 2*. Des Comprobar que $\lim_\limits{ x \to 1 } (x^{2}+2x+1) = 4$.
	1. Sea $\forall \varepsilon > 0$, ¿$\exists \delta > 0 : 0 < |x-1| < \delta \implies 0 < |(x^{2}+2x+1) - 4| < \varepsilon$? Transformamos un poco el segundo valor absoluto para acotarlo y así encontrar un $\varepsilon$. $$ | x^{2}+2x+1 - 4 | = | x^{2}+1-3 | = | x-1 |\cdot | x+3 | $$
	2. Supongamos ahora $| x-1 | < 1$, sencillamente para acotar esta parte del producto obtenido. Entonces, $$ | x-1 | < 1 \implies -1 < x-1 < 1 \implies 0 < x < 2 \implies 3 < x+3 < 5 \implies 3 < | x+3 | < 5 $$
	3. Tomando esta expresión, queda también acotado $| x+3 |$, y podemos seguir hasta acotar el producto obtenido en el paso 1. $$ | x+3 | < 5 \implies | x-1 | \cdot | x+3 | < 5 | x-1 | < \varepsilon \implies | x-1 | < \frac{\varepsilon}{5}$$
	4. Entonces:
		1. Si $| x-1 | < \delta \leq 1$, entonces $| x+3 | < 5$
		2. Para que $| x-1 | \cdot | x+3 | < \varepsilon$, partiendo de $5 | x-1 | < \varepsilon$, entonces $| x-1 | < \frac{\varepsilon}{5}$.
		3. Ya que seguimos buscando que $| x-1 | < \delta$, (véase desde un punto de vista algebraico, olvidando si $| x-1 |$ pertenece a $x$, $y$, $\delta$ o lo que sea, meramente el término $| x-1 |$), y en vista de los dos pasos anteriores, entonces $\delta = \mathrm{min}\left( 1, \frac{\varepsilon}{5} \right)$.
	5. Dado, entonces, que $\delta = \mathrm{min}\left( 1, \frac{\varepsilon}{5} \right)$, se comprueba, siguiendo la pregunta inicial formulada en el paso 1, que tal $\delta$ implica $0 < | x^{2}+2x-3 | < \varepsilon$. $$ | x^{2}+2x-3 | = | x-1 | \cdot | x+3 | < 5| x-1 | < \cancel{5} \frac{\varepsilon}{\cancel{5}} = \varepsilon$$
##### Límites laterales
Sea $f: \mathrm{Dom}(f) \longrightarrow \mathbb{R}$, $I \subset \mathrm{Dom}(f)$, $x_{0} \in I$ e $y_{0} \in \mathbb{R}$.
- Se define el **límite lateral por la izquierda** como $\lim_\limits{ x \to x_{0}^{-} } f(x) = y_{0}$ si se cumple que $$\forall \varepsilon > 0, \exists \delta > 0 : 0 < x_{0} - x < \delta \implies 0 < y_{0} - f(x) < \varepsilon$$
  Y el **límite lateral por la derecha** como $$ \forall \varepsilon > 0, \exists \delta > 0 : 0 < x - x_{0} < \delta \implies 0 < f(x) - y_{0} < \varepsilon $$
- **Teorema.** $\exists \lim_\limits{ x \to x_{0} } f(x) \iff \left\{ \begin{array} l\exists \lim_\limits{ x \to x_{0}^+ } f(x) \\ \exists \lim_\limits{ x \to x_{0}^- } f(x) \end{array} \right.$
##### Límites y el infinito
Sea $f: \mathrm{Dom}(f) \longrightarrow \mathbb{R}$, $I \subset \mathrm{Dom}(f)$ y $x_{0} \in I, y_{0} \in \mathbb{R}$.
1. Se dice que:
	- **$\lim_\limits{ x \to x_{0} } f(x) = + \infty$** si $\forall M \in \mathbb{R}$, $\exists \delta > 0$ tal que si $0 < | x - x_{0} | < \delta$, entonces $f(x) > M$.
	- **$\lim_\limits{ x \to x_{0} } f(x) = - \infty$** si $\forall m \in \mathbb{R}$, $\exists \delta > 0$ tal que si $0 < | x - x_{0} | < \delta$, entonces $f(x) > m$.
2. Si $I$ no está acotado superiormente,
	- $\lim_\limits{ x \to \infty } f(x) = y_{0}$ si $\forall \varepsilon, \exists k \in \mathbb{R}$ tal que si $x > k$ entonces $| f(x) - y_{0} | < \varepsilon$.
	- $\lim_\limits{ x \to \infty } f(x) = + \infty$ si $\forall M \in \mathbb{R}$, $\exists k \in \mathbb{R}$ tal que si $x > k$, entonces $f(x) > M$.
	- $\lim_\limits{ x \to \infty } f(x) = - \infty$ si $\forall m \in \mathbb{R}$, $\exists k \in \mathbb{R}$ tal que si $x > k$, entonces $f(x) < m$.
	- De forma análoga, se definen $\lim_\limits{ x \to - \infty } f(x) =$ todos los casos anteriores.
##### Propiedades cualitativas
1. Si el límite existe, este **es único**.
2. Si $\exists \lim_\limits{ x \to x_{0} } f(x) = y_{0}$, entonces $f(x)$ está acotada en un intervalo centrado en $x_{0}$.
3. Si además de la condición 2, se cumple que $y_{0} \neq 0$, entonces existe un intervalo centrado en $x_{0}$ en el que $f(x)$ conserva el signo de $y_{0}$.
##### Propiedades algebraicas
Sea $\lambda \in \mathbb{R}$ y supongamos que existen ${} \lim_\limits{ x \to x_{0} } f(x) \in \mathbb{R} {}$ y $\lim_\limits{ x \to x_{0} } g(x) \in \mathbb{R}$.
1. ${} \lim_\limits{ x \to x_{0} } (f + g)(x) = \lim_\limits{ x \to x_{0} } f(x) + \lim_\limits{ x \to x_{0} } g(x) {}$
2. $\lim_\limits{ x \to x_{0} } \lambda f(x) = \lambda \lim_\limits{ x \to x_{0} } f(x)$
3. $\lim_\limits{ x \to x_{0} } (f \cdot g)(x) = \lim_\limits{ x \to x_{0} }f(x) \cdot \lim_\limits{ x \to x_{0} }g(x)$
4. $\lim_\limits{ x \to x_{0} }\left( \frac{f}{g} \right)(x) = \frac{\lim_\limits{ x \to x_{0} } f(x)}{\lim_\limits{ x \to x_{0} }g(g)}$ sólo si $\lim_\limits{ x \to x_{0} } g(x) \neq 0$
5. $\lim_\limits{ x \to x_{0} } f^{g}(x) = \lim_\limits{ x \to x_{0} }f(x)^{\lim_\limits{ x \to x_{0} } g(x)}$
##### Infinitésimos
1. Se dice que $f$ es un **infinitésimo** en $a \in \mathbb{R}$ si $\lim_\limits{ x \to a } f(x) = 0$.
2. Si $f$ es un infinitésimo en $a$, y $g(x)$ es otra función acotada en un intervalo que contiene a $a$, entonces $\lim_\limits{ x \to a } f(x) \cdot g(x) = 0$.
	*Ej.* $\lim_\limits{ x \to 0 } x \sin\left( \frac{1}{x} \right)$. Observamos que $\nexists \lim_\limits{ x \to 0 } \sin\left( \frac{1}{x} \right)$; como $f$ es un infinitésimo en $0$ y ${} \sin\left( \frac{1}{x} \right) {}$ está acotada en ${} \{a,b \in \mathbb{R}, a < 0 < b \} {}$, entonces $\lim_\limits{ x \to 0 } x \sin\left( \frac{1}{x} \right) = 0$.
##### Ramas infinitas y asíntotas
1. Se dice que una curva recorre una **rama infinita** cuando la distancia de sus puntos al origen tiende a $\infty$ cuando $x,y \to \infty$.
2. Se dice que una recta $r$ es **asíntota** de una rama infinita cuando la distancia de los puntos de la rama a $r$ tiende a $0$ al tender a $\infty$ los puntos de dicha rama.
3. **Asíntotas verticales de $f$** son las rectas $x = x_{0}$, tal que $\lim_\limits{ x \to x_{0}^\pm } = \pm \infty$.
4. **Asíntotas oblicuas de $f$** son las rectas $y = mx + n$, donde $m = \lim_\limits{ x \to +\infty } \frac{f(x)}{x}$, y, por su parte, $n = \lim_\limits{ x \to +\infty } \big[ f(x) - mx \big]$. Si $m=0$, se dice que $y = n$ y que esta es una **asíntota horizontal**.
	*Ej.* Encontrar las asíntotas de $f(x) = \frac{2x^{2}}{x-1}$ y clasificarlas.
	- Asíntotas verticales: al ser $f$ un cociente de polinomios $\frac{P(x)}{Q(x)}$, se darán en $x : Q(x) = 0$, es decir, $x-1 = 0 \implies x = 1$.
	- Asíntotas oblicuas: $$ \begin{gather} m = \lim_\limits{ x \to +\infty } \frac{f(x)}{x} = \lim_\limits{ x \to +\infty } \frac{2x^{2}}{x^{2} - x} = \frac{\infty}{\infty} : \mathrm{INDET} \\ \text{L'Hôpital} \to \lim_\limits{ x \to +\infty } \frac{4x}{2x} = 2 = m \\ n = \lim_\limits{ x \to +\infty } \big[ f(x) - mx \big] = \lim_\limits{ x \to +\infty } \left( \frac{2x^{2}-2x(x+1)}{x+1} \right) = 2 = n \end{gather} $$ $$ y = mx + n = 2x + 2 $$
##### Cálculo de límites
1. Existen ciertos resultados que suponen una **indeterminación** en matemáticas en lo que a límites se refiere. Estos son $$ \begin{array}{c|c|c|c|c|c|c} \frac{0}{0} & \frac{\infty}{\infty} & 0^{0} & 0^{\infty} & 1^{\infty} & \infty^{0} & \infty - \infty \end{array} $$
2. Para solventar estos resultados, existen diversas técnicas.
	1. **Dividir por $(x-a)^{k}$. Para $\frac{0}{0}$**. Sean $P(x), Q(x)$ polinomios tales que $\lim_\limits{ x \to a } P(x) =$ $= \lim_\limits{ x \to a } Q(x) = 0$. Entonces $$ \lim_\limits{ x \to a } \frac{P(x)}{Q(x)} = \frac{0}{0} \implies \lim_\limits{ x \to a } \frac{\cancel{(x-a)^k} P_{1}(x)}{\cancel{(x-a)^k} Q_{1}(x)} = \frac{P_{1}(x)}{Q_{1}(x)}, \text{ si } Q_{1}(x) \neq 0$$
	2. **Dividir por $x$ a la potencia más grande**. $\lim_\limits{ x \to \pm \infty } \frac{P(x)}{Q(x)} = {\left\{ \begin{array}{l} 0 \text{ si } grado(P) < grado(Q) \\ \pm \infty \text{ si } grado(P) = grado(Q) \\ \displaystyle{\frac{a_{P}}{a_{Q}}} \text{ si } grado(P) > grado(Q) \end{array} \right.}$
	   donde $a_{P}, a_{Q}$ son los máximos coeficientes de $P$ y $Q$, respectivamente. Se puede aplicar esta regla o dividir cada término por $x^{n}$, siendo $n$ el exponente más grande entre $P(x)$ y $Q(x)$.
	   Esto funciona también para composiciones en las que haya **funciones exponenciales**.
	3. **Operar utilizando las expresiones conjugadas si hay radicales**. Para $\frac{0}{0}$ seguro, intuyo que para $\frac{\infty}{\infty}$ también.
	4. **Definición de $e$ en indeterminaciones $1^{\infty}$**: Hacer mototrucos con la función para que llegue a  $e = \lim_\limits{ x \to +\infty } \left( \frac{1}{f(x)} + 1 \right)^{f(x)}$.
	   *Ej.* $\lim_\limits{ x \to +\infty } \left( \frac{x+7}{x+3} \right)^{x+5}$ $$ \begin{gather} \lim_\limits{ x \to +\infty } \left( \frac{x+7}{x+3} \right)^{x+5} (=1^\infty) = \lim_\limits{ x \to +\infty } \left( 1 + \frac{x+7}{x+3} - 1 \right)^{x+5} = \lim_\limits{ x \to +\infty } \left( 1 + \frac{4}{x+3} \right)^{x+5} = \\ = \lim_\limits{ x \to +\infty } \left( 1 + \frac{1}{\frac{x+3}{4}} \right)^{ \frac{4}{x+3} \frac{x+3}{4} (x+5)} = \lim_\limits{ x \to +\infty } e^{\frac{4}{x+3}(x+5)} = e^{\lim_\limits{ x \to +\infty } \frac{4}{x+3}(x+5)} = e^{\lim_\limits{ x \to +\infty }  \frac{4x+20}{x+3}} = e^{4} \end{gather} $$
	5. **Regla de L'Hôpital**. Sean $f$ y $g$ dos funciones derivables tales que cumplan que $\lim_\limits{ x \to a }f(x) = \lim_\limits{  x \to a } g(x) = \{-\infty, 0, +\infty\}$. Si $\exists \lim_\limits{ x \to a } \left( \frac{f}{g} \right)(x) \implies \lim_\limits{ x \to a } \frac{f(x)}{g(x)} = \lim_\limits{ x \to a } \frac{f'(x)}{g'(x)}$.
	6. **Regla tomando logaritmos**. Válida para $0^0$, $1^\infty$ y $\infty^{0}$.  *Nota:  ${} \ln(x) \implies \log(x) {}$ y $\log(x) \implies \log_{10}(x)$*.
	   _Ej._ $\lim_\limits{ x \to 0^+ } x^{\frac{2}{3 - \log(x)}} (=0^0)$. $$ \lim_\limits{ x \to 0^+ } x^{\frac{2}{3 - \log(x)}} = \lim_\limits{ x \to 0^+ } e^{\log\left( x^{\frac{2}{3-\log(x)}} \right)} = \lim_\limits{ x \to 0^+ } e^{\frac{2}{3-\log(x)} \cdot \log(x)} = e^{\lim_\limits{ x \to 0^+ }\frac{2 \log(x)}{3-\log (x)}} \overset{*}\implies e^{2}$$
	   $$ \overset{*}\implies \lim_\limits{ x \to 0^+ } \frac{2 \log x}{3 - \log x} \left( = \frac{\infty}{\infty} \right)\overset{L'H} = \lim_\limits{ x \to 0^+ } \frac{\frac{2}{x}}{\frac{1}{x}} = \lim_\limits{ x \to 0^+ } \frac{2 \cancel{x}}{\cancel{x}} = 2 \overset{*}\implies $$
---
# 1.3 Continuidad de funciones
##### Definición
Sea $I$ un intercalo de extremos $a,b: a < b$:
- $f: I \longrightarrow \mathbb{R}$ es **continua** en $x_{0} \in (a,b)$ si $\lim_\limits{ x \to x_{0} } f(x) = f(x_{0})$, o lo que es lo mismo, $$ \forall \varepsilon > 0, \exists \delta > 0 : 0 < |x - x_{0}| < \delta \implies 0 < |f(x) - f(x_{0})| < \varepsilon$$
- $f$ es **continua en** $a$ (y respectivamente en $b$) si $\exists f(a)$ (o $f(b)$) tal que ${} \lim_\limits{ x \to a^{+} } f(x) = f(a) {}$ (y respectivamente para ${} \lim_\limits{ x \to b^{-} } f(x) = f(b) {}$).
- $f$ es continua en $I$ si lo es para $\forall x \in I$.
##### Propiedades locales
Si $f$ es continua en $x_{0}$
- $f$ está acotada en un intervalo que contiene a $x_{0}$.
- Si $f(x_{0}) \neq 0$, entonces $f$ conserva el signo de $f(x_{0})$ en un intervalo que contiene a $x_{0}$.
##### Propiedades algebraicas
Sean $f$ y $g$ continuas en $x_{0}$ y $\lambda \in \mathbb{R}$
- La suma de $f+g$ es continua en $x_{0}$.
- $\lambda f$ es continua en $x_{0}$.
- $fg$ es continua en $x_{0}$.
- $f \circ g$ es continua en $x_{0}$ si $f$ es continua en $g(x_{0})$.
- $f/g$ es continua en $x_{0}$ si $g(x_{0}) \neq 0$.
- si $\exists f^{-1}(x)$ entonces $f^{-1}(x)$ es continua en $x_{0}$.
##### Discontinuidades
Sea $f: I \longrightarrow \mathbb{R}$ y $x_{0} \in I$. Se dice que $f$ es **discontinua en** $x_{0}$ si no es continua en $x_{0}$. Más aún,
- $f$ tiene en una **discontinuidad finita en $x_{0}$** si $f$ está acotada en un intervalo que contiene a $x_{0}$. Se clasifican en:
	- **Discontinuidad evitable** de $f$ en $x_{0}$ si $\exists f(x_{0})$ y $\exists \lim_\limits{ x \to x_{0} } f(x) \neq \pm \infty$, pero $\lim_\limits{ x \to x_{0} } f(x) \neq f(x_{0})$. 
	- **Discontinuidad de salto finito** si $\exists \lim_\limits{ x \to x_{0}^{-} } f(x) \neq \exists \lim_\limits{ x \to x_{0}^{+} } f(x) \neq \pm \infty : \lim_\limits{ x \to x_{0}^{-} } \neq \lim_\limits{ x \to x_{0}^{+} }$. Al número $s = \lim_\limits{ x \to x_{0}^{+} } - \lim_\limits{ x \to x_{0}^{-} }$ se lo denomina **salto**.
	- **Discontinuidad oscilatoria finita**. Por lo general, si no cumple ninguna de las anteriores.
		*Ejemplo ilustrativo:* $$ \begin{cases} \sin\left( \frac{1}{x} \right) \text{ si } x\neq 0 \\[7px] 0 \text{ si } x = 0 \end{cases} $$
```tikz
\usepackage{tikz}
\usepackage{pgfplots}

\begin{document}

\begin{tikzpicture}[scale=1.25]
\begin{axis}[xmin= -1.5, xmax=1.5, axis lines = middle, yticklabels=\empty, xticklabels={\empty,-1,\empty,\empty,\empty,1,\empty}]
\addplot[color=red, thick, samples = 500]{sin((1/x)r)};
\end{axis}
\end{tikzpicture}

\end{document}
```
- $f$ tiene una **discontinuidad infinita en** $x_{0}$ si $\nexists I$ donde la función esté acotada.
	- **Discontinuidad infinita pura** (o **polo**) si $\lim_\limits{ x \to x_{0} } f(x) = \pm \infty$.
	- **Discontinuidad de salto infinito** si $\pm \infty = \lim_\limits{ x \to x_{0}^{\pm} } f(x) \neq \lim_\limits{ x \to x_{0}^{\mp} } f(x) = \{ \mp \infty, \lambda \in \mathbb{R} \}$.
	- **Discontinuidad oscilatoria infinita**, por lo general si no satisface ninguna de las anteriores. *Ejemplo ilustrativo*.$$ \begin{cases} \frac{1}{x} \sin\left( \frac{1}{x} \right) \text{ si } x \neq 0 \\[7px]  0 \text{ si } x = 0 \end{cases} $$
```tikz
\usepackage{tikz}
\usepackage{pgfplots}

\begin{document}

\begin{tikzpicture}[scale=1.25]
\begin{axis}[xmin= -1.5, xmax=1.5, ymax=20, ymin=-20, axis lines = middle, yticklabels=\empty, xticklabels={\empty,-1,\empty,\empty,\empty,1,\empty}]
\addplot[color=red, thick, samples = 500]{(1/x)*sin((1/x)r)};
\end{axis}
\end{tikzpicture}

\end{document}
```
##### Teoremas en relación a la continuidad
- **Bolzano**. Si $f$ es continua en $[a,b]$ y $f(a) \cdot f(b) < 0$, entonces $\exists c \in (a,b) : f(c) = 0$.
- **Darboux** o **Teorema del Valor Medio (TVM)**. Si $f$ es continua en el intervalo $I$, entonces $f(I)$ es un intervalo. Más aún, si $I = [a,b]$, entonces $f$ recorre todos los valores entre el máximo y el mínimo ($a$ y $b$).
- **Weierstrass**. Si $f$ es continua en $[a,b]$, entonces $f$ alcanza el máximo y el mínimo en $[a,b]$, es decir, $\exists x_{M}, x_{m} : f(x_{m}) \leq f(x) \leq f(x_{M}), \forall x \in [a,b]$.
---
