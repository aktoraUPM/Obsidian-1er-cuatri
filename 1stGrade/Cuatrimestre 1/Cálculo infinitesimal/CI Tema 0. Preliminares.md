# 0.1 Conjuntos
### Conceptos básicos
1. Colección de objetos, en este caso matemáticos.
2. A cada objeto de un conjunto se lo denomina _elemento_.
	**Nomenclatura**: $x$ es elemento del conjunto $Y$, entonces se dice que $x \in Y$.
	_Ejemplo de conjuntos_: $Y = \{1,4,8,15\}$, $X = \{x : x \textrm{ es par} \} = \{x : x=2k, k \in \mathbb{R} \}$
3. **Conjunto vacío** $\emptyset$. Conjunto que no tiene elementos.
4. Sean $A$ y $B$ dos conjuntos, se dice que $A$ es subconjunto de $B$, ($A \subset B$) si cualquier elemento $x(A)$ cumple que $x \in B$.
5. $A$ y $B$ son iguales ($A = B$) si $\left\{ \begin{array}{r} A \subset B \\ B \subset A \end{array} \right.$
6. Sean $A$ y $X$ dos conjuntos tales que $A \subset X$. Entonces, el complementario de $A$ en $X$ es el conjunto de elementos de $X$ que no están en $A$.
	$A^c = \{x \in X : x \notin A \}$

##### Proposición y demostración
- Sean $A$ y $B$ dos conjuntos en $X$, si se cumple que $A \subset B$, entonces $B^c \in A^c$.
- $A \subset B$. Sea $x \in B^c \Rightarrow x \in X$, $x \notin B$. Como $A \subset B$, entonces $x \in X$ pero $x \notin A$, por lo que $x \in A^c$
### Operaciones de conjuntos
1. ***Unión.*** $A \cup B$ es el conjunto de los elementos que pertenecen a $A$ o a $B$.
	$A \cup B = \{ x \in X : x \in A \textrm{ ó } x \in B \}$
2. ***Intersección*** $A \cap B$ es el conjunto de los elementos que pertenecen a $A$ y a $B$.
	$A \cap B = \{ x \in X : x \in A \textrm{ y } x \in B \}$
	Si $A \cap B = \emptyset$, entonces $A$  y $B$ son **disjuntos**. 
3. ***Diferencia***. Sean $A,B \subset X$. Entonces $A \backslash B$, la diferencia de $A$ menos , son los elementos de $A$ que no están contemplados en $B$.
	$A \backslash B = \{x \in X : x \in A \textrm{ y } x \notin B \}$
	**Proposición y demostración**
	- Sean $A$ y $B$ dos conjuntos, entonces se cumple que $A \backslash B = A \cap B^c$. Es necesario entonces, demostrar que $A \backslash B \subset A \cap B^c$ y que $A \backslash B \supset A \cap B^c$. 
	- Sea $x \in A \backslash B$ $\Leftrightarrow x \in A \textrm{ y } x \notin B$ $\Leftrightarrow x \in A \cap B^c$.
4. ***Producto cartesiano***. $A \times B$ es el conjunto de pares **ordenados** denotados como $(a, b)$, tales que $a \in A$ y $b \in B$.
	$A \times B = \{ (a,b) : a \in A, b \in B \}$
	_Ejemplo:_ $A = \{1, 2\}$, $B=\{2, 3\}$. Entonces $A \times B = \{(1,2), (1,3), (2,2), (2,3) \}$. Como los pares deben ser ordenados, entonces, por ejemplo, $(3,2) \notin A \times B$, ya que $3 \in B$ y $2 \in A$ (aunque en este caso también esté en $B$)

5. ***Leyes de Morgan***. $\left\{ \begin{array}{l} (A \cup B)^c = A^c \cap B^c \\ (A \cap B)^c = A^c \cup B^c \end{array} \right.$
	Sea $x \in (A \cup B)^c$ $\Leftrightarrow x \notin A \textrm{ y } x \notin B$ $\Leftrightarrow x \in A^c \textrm{ y } x \in B^c$ $\Leftrightarrow x \in A^c \cap B^c$
	Sea $x \in (A \cap B)^c$ $\Leftrightarrow x \notin A \textrm{ ó } x \notin B$ $\Leftrightarrow x \in A^c \textrm{ ó } x \in B^c$ $\Leftrightarrow x \in A^c \cup B^c$
---
# 0.2 Correspondencias y funciones
##### Correspondencia
1. Una correspondencia $f$ de $A$ y $B$ es una **terna** $(A, B, G_f)$, donde $A$ y $B$ son conjuntos y $G_f$ es un subconjunto $A \times B$. Se denomina $f: A \longrightarrow B$.
2. El conjunto de los elementos de $A$ que forman parte de la primera coordenada de de los elementos de $G_f$ es el **dominio** de $f$.
3. El conjunto $G_f$ es la **gráfica** de $f$.
	_Ejemplo_. Considerando $f : A \longrightarrow B$, $A=\{1, 2, 3\}$, $B = \{a, b, c\}$ y $G_f = \{(1,a), (2,b), (2,c), (3,c) \}$, $G_f$ es el "diccionario" (al estilo *Python*), que correlaciona valores de $A$ con otros de $B$ de forma unidireccional.
##### Función
- Sean $A$ y $B$ dos conjuntos, una función $f$ de $A$ en $B$, es una correspondencia que asocia a cada $x \in A$ una **única** correspondencia a un elemento $y \in B$ tal que $(x,y) \in G_f$. El elemento $y$ unívocamente asociado se denomina por $f(x)$, y es el valor que toma $f$ en $x$. Otra notación es $$f: \begin{array}{} A \longrightarrow B \\ a \longmapsto b \end{array}$$
##### Imágenes de funciones
Sea $f: A \longrightarrow B$ una función, $S \subset A$ y $T \subset B$.
1. La **imagen de $f$ por $S$** es $f(S) = \{ f(x) : x \in S \}$.
2. La **imagen inversa** o **preimagen** de $f$ por $T$ es $f^{-1} (T) = \{x \in A : f(x) \in T\}$.
3. La **imagen de** $f$ es $f(\mathrm{Dom}(f)) = \mathrm{Im}(f)$.
4. _Ejemplo._
	$f: \begin{array}{} A \longrightarrow B \\ a \longmapsto d \\ b \longmapsto d \\ c \longmapsto e \end{array}$ ; $\; \begin{array}{l} \text{Sea} S=\{a, b\} \Rightarrow f(S) = \{d\} \\ \text{Sea} T = \{d, e\} \Rightarrow f^{-1} (T) = \{a, b, c\} \end{array}$
##### Funciones inyectivas, sobreyectivas y biyectivas
Sea $f: A \longrightarrow B$ una función, $A = \{a, b, c\}$ y $B = \{1,2,3\}$
1. $f$ es una función **inyectiva** si dados cualesquiera $x,y \in \mathrm{Dom}(f) : x \neq y$, se tiene $f(x) \neq f(y)$; o lo que es lo mismo, si $f(x) = f(y)$ entonces $x = y$.
	_Ej. de función inyectiva suponiendo $B = \{1,2,3,4\}$_ $$
f: \begin{array}{l}
a \mapsto 1 \\
b \mapsto 3 \\
c \mapsto 2
\end{array}$$
	Si $f$ es inyectiva, se llama función inversa de $f$ a $f^{-1}: \mathrm{Im}(f) \longrightarrow A$ tal que $f^{-1}(y) = x$
2. $f$ es una función **sobreyectiva** si $B = \mathrm{Im}(f)$.
	_Ej. de función sobreyectiva suponiendo $B = \{1,2\}$._ $$
f: \begin{array}
l a \mapsto 1 \\
b \mapsto 1 \\
c \mapsto 2
\end{array}
$$
3. $f$ es **biyectiva** si es tanto inyectiva como sobreyectiva.
	_Ej. de función biyectiva suponiendo $B = \{1,2,3\}$_ $$
f: \begin{array}
l a \mapsto 1 \\
b \mapsto 3 \\
c \mapsto 2
\end{array}
$$
---
# 0.3 Conjuntos numéricos
##### Conjuntos numéricos relevantes
1. $\mathbb{N} = \{1,2,3 \dots\}$ Números naturales.
2. $\mathbb{Z} = \{-2, -1, 0, 1, 2\dots\}$ Número enteros.
3. $\mathbb{Q} = \displaystyle{\left\{ \frac{p}{q} : x,y \in \mathbb{Z}, q \neq 0, \mathrm{mcd}(p,q) = 1 \right\}}$. Números racionales.
4. $\mathbb{I}$ Números irracionales. No se pueden expresar como racionales. Ej. $\sqrt{ 2 }$, $\pi$, $e$.
5. $\mathbb{R} = \mathbb{Q} \cup \mathbb{I}$.
##### Intervalos
Sean $a,b \in \mathbb{R} : a < b$.
1. Intervalo **abierto**. $(a,b) = \{x \in \mathbb{R} : a < x < b\}$
2. Intervalo **cerrado**. $[a,b] = \{x \in \mathbb{R} : a \leq x \leq b\}$
3. Intervalo **semiabierto** o **semicerrado**.$\left\{ \begin{array}l [a,b) \\ (a,b]\end{array} \right.$
##### Acotación de intervalos
Sea $A \subset \mathbb{R}$.
1. $A$ está acotado **superiormente** si $\exists M \in \mathbb{R} : a \leq M, \forall a \in A$, y se dice que $M$ es una **cota superior**. A la cota superior más pequeña se lo denomina **supremo de $A$, $\textrm{ sup}(A)$**. Si $\mathrm{sup}(A) \in A$, se dice que es un **máximo**, denotado como $\mathrm{max}(A)$.
2. Igualmente, $A$ está acotado **inferiormente** si $\exists n \in \mathbb{R} : n \leq a, \forall a \in A$, y $n$ es una **cota inferior**. La cota inferior más grande posible es el **ínfimo**, $\mathrm{inf}(A)$, y si $\mathrm{inf}(A) \in A$, entonces es el **mínimo de $A$**.
3. $A$ está **acotado** si lo está superior e inferiormente.
---
