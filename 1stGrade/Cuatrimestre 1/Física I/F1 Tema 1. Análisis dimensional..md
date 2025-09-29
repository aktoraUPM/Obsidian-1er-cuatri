# 1.1. Introducción
##### Objetivo
Aplicar información sobre las relaciones que se pueden restablecer entre magnitudes físicas
##### Aplicaciones
1. Establecer distintos sistemas de unidades
2. Comprobar la consistencia de fórmulas.
3. Obtención de relaciones entre magnitudes físicas.
4. Base para la formulación empírica de resultados: saber qué variables manipular en un experimento).
5. Construcción de modelos a escala. ya que las distintas magnitudes pueden no escalarse de forma lineal.
---
# 1.2. Definiciones previas
###### Magnitud física
- Concepto / idea / construcción mental físicos que pueden expresarse numéricamente en términos de uno o más patrones. "Todo lo que puede ser medido".
###### Cantidad
- Estado de una magnitud física al aplicarse a un objeto particular.
###### Unidad de una magnitud
- Cantidad arbitrariamente elegida de una magnitud, denotada como $U_A$ ó $(A_0)$.
###### Medida de una cantidad
- Dada una cantidad $(A)$, su medida en la unidad $U_A$ es el número real definido por $$\frac{(A)}{U_{0}} = A \Longleftrightarrow (A) = A \cdot U_{A}$$
  Dadas dos unidades distintas $U_1$ y $U_2$ de una misma cantidad $(A)$, se puede expresar dicha cantidad como $$(A) = A_{1} U_{1} = A_{2} U_{2} \Longleftrightarrow \frac{A_1}{A_{2}} = \frac{U_{2}}{U_{1}}$$
  Conocida una de las unidades, se puede conocer una medida en función de la otra.
---
# 1.3. Principio de homogeneidad dimensional
##### Postulado
- Un **postulado** es una **ley fundamental de la física**, que puede recogerse de forma que consista en una **relación de proporcionalidad** (no una ecuación) entre determinadas **potencias** (ni sumas ni restas) de las cantidades que intervienen en un fenómeno. Como ejemplo, la ley de la gravitación universal en forma de postulado vendría a ser:$$
 F \propto \frac{M_{1} M_{2}}{r^{2}}
$$
##### Ecuación de la física
- Las **ecuaciones de la física** son relaciones de igualdad entre distintas potencias de las cantidades que intervienen en un fenómeno físico. En la gravitación universal: $$
F = G \frac{M_{1} M_{2}}{r^{2}}
$$
##### Constantes
- Ajustan y definen la proporcionalidad entre los dos miembros de una ecuación física.
- Pueden ser **específicas o universales**, según si dependen de los detalles del sistema en cuestión, como $k$ en la ley de Hooke $F = k \cdot \Delta x$, o se aplican a cualquier sistema, como $G$ en la gravitación universal (Véase [[#Ecuación de la física]]).
- Pueden ser **dimensionales o adimensionales**. Si son dimensionales, dependen del sistema de unidades utilizado, como $G$. Si son adimensionales, ya que no dependen de un sistema, se puede escoger uno que tome una constante adimensional como la unidad; estas constantes se denominan **espúreas**.
##### Dimensión y base dimensional
- Una **dimensión** es la propiedad común a todas las cantidades de una misma [[#Magnitud física]], desde el punto de vista de la propiedad como tal, siendo la magnitud la forma en la que se posibilita su expresión numérica.
- Una **base dimensional** es el conjunto de dimensiones utilizadas como referencia y construcción de otras dimensiones en el mismo sistema. Por ejemplo, la base dimensional de la mecánica newtoniana es $(M,L,T)$, masa, longitud y tiempo; en termodinámica, se amplia esta a $(M,L,T,\theta)$, masa, longitud, tiempo y temperatura; en electrostática, $(M,L,T,Q)$, etcétera.
##### Principio de homogeneidad dimensional
>*«Las ecuaciones de la física deben ser dimensionalmente homogéneas, lo que implica que los dos miembros de la igualdad tienen la misma dimensión».*
---
# 1.4. Sistemas de unidades coherentes
- Un sistema de unidades es coherente con un conjunto de leyes físicas cuando estas se verifican al sustituir sustituir en cada caso particular los símbolos por sus respectivas medidas concretas.
	_Ej._ Considerando $F = ma$, un sistema coherente sería el SI, que utiliza como unidades $(N,m,kg,s)$; tomando que una fuerza de $1N$ ejerce, sobre $1kg$ de masa, una aceleración de $1m/s^{2}$, entonces se cumple que $F = ma \Rightarrow 1N = 1kg \cdot 1m/s^{2}$.
	Si, sin embargo, se utilizase el **kilopondio** $kp$ como unidad de fuerza, daría lugar al sistema $(kp,m,kg,s)$, que es incoherente, puesto que partiendo de que $1kp = \displaystyle{\frac{1}{9.8N}}$, no es cierto que $F = ma \Rightarrow 1kp = \displaystyle{\frac{1}{9.8N}} = 1kg \cdot 1m/s^{2}$.
##### Ecuación de dimensiones de una magnitud
- Utilizando una base dimensional, por ejemplo, la ordinaria de la mecánica $(M,L,T)$, la **fórmula dimensional** de una magnitud $X$ se escribe como $[X] = M^{a} L^{b} T^{c}$, donde $a,b,c \in \mathbb{R}$.
- Para una magnitud adimensional, la ecuación de dimensiones será $[X] = 1$.
	Nota de clase: **dimensiones de una integral**. Sabiendo la suma de Riemann: $$\displaystyle{\int} f(x) \; dx = \lim_\limits{ \Delta x \to 0 }\sum_\limits{x_{i}} f(x_{i}) \; \Delta x \implies \left[ \displaystyle{\int} f(x) \; dx\right] = [f(x)] \; [x]$$
---
# 1.5. Introducción al cálculo de errores
##### Definiciones
- **Error**. Imprecisión en base a la medida más pequeña que un aparato es capaz de hacer.
- **Medida directa**. Aquella hecha a base de compararla con una patrón unitario.
- **Medida indirecta**. Aquella obtenida a través de calcularla como función de otras medidas directas.
##### Expresión de errores
- Se expresan como **intervalos**, de forma que la medida $a$ será expresada como $(a - \Delta a, a + \Delta a)$ más comúnmente expresado como $a \pm \Delta a$, siendo $\Delta a$ el denominado **error** de la medida.
- Se tomará como como $\Delta a$ al mayor de los errores posibles, véase el siguiente punto: [[#Tipos de error]].
##### Tipos de error
- **Por fuente del error**
	1. **Sistemático**. Errores cometidos por una estrategia de medición incorrecta. Hacen tender las medidas bien por exceso o bien por defecto. Es difícil saber que se están cometiendo, pero de saberse, basta con compensar el exceso o defecto producido.
	2. **Instrumentales**. Causados por la precisión del instrumento. Se denomina también **incertidumbre** del aparato.
	3. **Aleatorios / Accidentales**.  Se distribuyen aleatoriamente. Precisamente por ello, si se repite numerosas veces un experimento, estadísticamente se verán compensados unos con otros.
	4. Si las medidas realizadas se ciñen de forma cercana a la medida real (sin error), se dice que esta medida es **precisa**.
- **Por cuantificación**
	1. **Absoluto**. Medida propia del error. Dada como una estimación $\pm \Delta x$
	2. **Relativo**. Comparando el error con la medida total. $\varepsilon = \frac{\Delta x}{x}, \Delta x = | x_{real} - x |$.
##### Expresión de resultados
La medida $X$ se expresa a través del propio valor medido $x$ y el error $\Delta x$ que esta puede acarrear. $$ \boxed{X = x + \Delta x} $$
- El error $\Delta x$:
	- No es preciso, es una **aproximación**; por ello, se expresa con **una sola cifra significativa**. Se redondea dicha cifra con el criterio de siempre (5+↑, 4-↓).
	  _Ej:_ ${} \Delta x = 0.00569 \implies \Delta x = 0.006 {}$
	- **No debe superar la incertidumbre del instrumento de medida**.
- La medida $x$:
	- Se redondea a partir de la magnitud del error. _Ej:_ $X = 256.5 \pm 10 \implies 260 \pm 10$.
	- Si la medida es **única**, el error y la magnitud son los medidos directamente, pero si se hacen **varias medidas** $x_{1}, x_{2},x_{3} \dots x_{n}$ se tomará el valor más representativo, que es la **media aritmética** $\overline{x}$. $$ \overline{x} = \frac{\sum^i_\limits{i=1} \; x_{i}}{n} $$
	  Mientras, la el error tendrá también una naturaleza estadística, dependiente de $n$, representada por el **error cuadrático medio (ECM)**. $$ \Delta x = \sqrt{\frac{1}{n(n-1)} \cdot \sum^n_\limits{i = 1} \big[(x_{i} - \overline{x})^2\big]}$$
	  En la calculadora, se puede calcular en el menú `Estadística` como $\Delta x = \displaystyle{\frac{s_{x}}{\sqrt{n}}}$
---
# 1.6 Medidas indirectas
Una medida indirecta $f$ es la obtenida matemáticamente en función de otras tantas hechas directamente, tal que $f(x,y,z)$. Así, las medidas $x,y,z$ tienen sus propios errores experimentales que se acumulan a la hora de calcular $f$.
##### Cálculo de propagación de errores
Para calcular el error propagado $\Delta f$, existen distintas opciones.
- **Cálculo por diferenciales**. Apto para cualquier función. A partir de la diferenciación de toda la función $f$, $$ df(x,y,z) = \left( \frac{\partial f}{\partial x} \right) dx + \left( \frac{\partial f}{\partial y} \right) dy + \left( \frac{\partial f}{\partial z} \right) dz $$
  Se puede sustituir cada diferencial por su respectivo **incremento**, obteniendo así la **regla de cálculo para la propagación de errores**. $$ \Delta f(x,y,z) = \left( \frac{\partial f}{\partial x} \right) \Delta x + \left( \frac{\partial f}{\partial y} \right) \Delta y + \left( \frac{\partial f}{\partial z} \right) \Delta z $$
- **Método de los logaritmos**. Apto en caso de que $f$ sea una función monomia, es decir, de la forma $f(x,y,z) = x^{a} y^{b} z^{c}$. $$ \Delta f = | a | \frac{\Delta x}{x} + | b | \frac{\Delta y}{y} + | c | \frac{\Delta z}{z} $$
---
