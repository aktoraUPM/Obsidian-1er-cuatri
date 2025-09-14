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
4. $f$ es **constante** enn $I$ si $f(x_{1}) = f(x_{2}), \forall x_{1},x_{2} \in I$, es decir, _es creciente y decreciente a la vez_.