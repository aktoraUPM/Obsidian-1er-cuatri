## 1. Introducción
##### Objetivo
Aplicar información sobre las relaciones que se pueden restablecer entre magnitudes físicas
##### Aplicaciones
1. Establecer distintos sistemas de unidades
2. Comprobar la consistencia de fórmulas.
3. Obtención de relaciones entre magnitudes físicas.
4. Base para la formulación empírica de resultados: saber qué variables manipular en un experimento).
5. Construcción de modelos a escala. ya que las distintas magnitudes pueden no escalarse de forma lineal.
---
## 2. Definiciones previas
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
## 3. Principio de homogeneidad dimensional
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
##### **Principio de homogeneidad dimensional**
>*«Las ecuaciones de la física deben ser dimensionalmente homogéneas, lo que implica que los dos miembros de la igualdad tienen la misma dimensión».*
## 4. Sistemas de unidades coherentes
- Un sistema de unidades es coherente con un conjunto de leyes físicas cuando estas se verifican al sustituir sustituir en cada caso particular los símbolos por sus respectivas medidas concretas.
	_Ej._ Considerando $F = ma$, un sistema coherente sería el SI, que utiliza como unidades $(N,m,kg,s)$; tomando que una fuerza de $1N$ ejerce, sobre $1kg$ de masa, una aceleración de $1m/s^{2}$, entonces se cumple que $F = ma \Rightarrow 1N = 1kg \cdot 1m/s^{2}$.
	Si, sin embargo, se utilizase el **kilopondio** $kp$ como unidad de fuerza, daría lugar al sistema $(kp,m,kg,s)$, que es incoherente, puesto que partiendo de que $1kp = \displaystyle{\frac{1}{9.8N}}$, no es cierto que $F = ma \Rightarrow 1kp = \displaystyle{\frac{1}{9.8N}} = 1kg \cdot 1m/s^{2}$.
