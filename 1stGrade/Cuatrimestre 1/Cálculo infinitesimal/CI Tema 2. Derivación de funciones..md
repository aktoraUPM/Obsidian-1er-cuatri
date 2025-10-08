# 2.1 Derivada de una función
##### Derivada en un punto y derivabilidad
- Sea $f: (a,b) \longrightarrow \mathbb{R} : x_{0} \in (a,b)$. Se dice que $f$ es derivable en $x_{0}$ si $\exists \lim_\limits{ x \to x_{0} } \frac{f(x) - f(x_{0})}{x - x_{0}} \neq \pm \infty$, o lo que es lo mismo, $\lim_\limits{ h \to 0 } \frac{f(x_{0}-h) - f(x_{0})}{h}$.
- El valor de los límites anteriores es el **valor de la derivada en $x_{0}$**, y se denota por $f'(x_{0})$.
##### Función derivada
- Sea ${} D = \{x \in (a,b) : f$ es derivable en $x  \}$. La función $f' : \begin{array}{l} D \longrightarrow \mathbb{R} \\ x \longmapsto f'(x) \end{array}$ es la **función derivada de** $f$.
##### Interpretación geométrica
- $f'(x_{0})$ es la **pendiente** de la recta tangente a la gráfica de $f$ en el punto $\big(x_{0}, f(x_{0})\big)$, siendo la ecuación de tal recta $$ y - f(x_{0}) = f'(x_{0}) (x - x_{0}) $$
  *Ej.* $f(x) = \ln (x+1)$ para $x_{0} = 1.5$
```tikz
\usepackage{tikz}
\usepackage{pgfplots}

\begin{document}

\begin{tikzpicture}[scale=1.2]
% Axes
\begin{axis}[axis line style= {draw=gray}, xmin= 0, xmax=3, ymax=1.75, ymin=0, axis lines = middle, yticklabels=\empty, xticklabels=\empty]

% Curve
\addplot[color=red, thick, samples = 500, domain=0:3, restrict y to domain=-20:20]{ln(x+1)} node[below]{$f(x)$};
% Tangent line
\addplot[color=orange, thick, samples = 3, domain=0:3]
{0.4*x-1.5*0.4+ln(2.5)} node[above]{$y - f(x_0) = f'(x_0) (x-x_0) : x_0 = 1.5$};
% Tangency mark
\addplot[color=orange, mark=*] coordinates {(1.5, 0.9162)};

\end{axis}
\end{tikzpicture}

\end{document}
```
##### Reglas de derivación
- Sean $f,g$ funciones derivables en $x_{0}$.
	- **Regla del producto**: $(fg)' = fg' + f'g$.
	- **Regla del cociente**: $\displaystyle{\left( \frac{f}{g} \right)' = \frac{f'g - fg'}{g^{2}}}$ si $g(x_{0}) \neq 0$.
	- Derivada de una **suma**: $(f+g)' = f' + g'$.
	- Derivada de **función por escalar**: $(\lambda f)' = \lambda \cdot f'$.
- **Regla de la cadena**
	- Sean $I, J$ dos intervalos, y $f: I \longrightarrow \mathbb{R}, g: J \longrightarrow \mathbb{R}$ y $f(I) \in J$. Si $f$ es derivable en $x_{0} \in I$ y $g$ es derivable en $f(x_{0})$, entonces $g \circ f$ es derivable en $x_{0}$ y su valor es de $$ (g \circ f)'(x_{0}) = g'\big[f(x_{0}) \big] \cdot f'(x_{0}) $$
##### Teorema de la función inversa
- Sea $f$ una función continua e inyectiva en un intervalo $I$ y $J = f(I)$. Si $f$ es derivable en $x_{0}$, entonces $f^{-1}$ es derivable en $y_{0} = f(x_{0}) \in J$, y además $(f^{-1})'(y_{0}) = \displaystyle{\frac{1}{f'(x_{0})} = \frac{1}{f'(f^{-1}(y_{0}))}}$
##### Derivadas laterales
- Se dice que $f$ es **derivable por la derecha** (y respectivamente por la **izquierda**) si $\exists \lim_\limits{ x \to x_{0}^{+} } \frac{f(x) - f(x_{0})}{x - x_{0}} \neq \pm \infty$, (y respectivamente en $x \to x_{0}^{-}$), y se denota por $f'(x_{0}^{+})$ (y respectivamente $f'(x_{0}^{-})$ ).
- Existe la derivada **si y solo si** existen y coinciden sus derivadas laterales, es decir $$ \exists f'(x_{0}) \iff \exists f'(x_{0}^{-}), f'(x_{0}^{+}) : f'(x_{0}^{-}) = f'(x_{0}^{+}) $$
- Si $f$ es derivable en $x_{0}$, entonces **$f$ es continua en** $x_{0}$.
##### Lema de Fermat
>Si $f$ es derivable en $x_{0}$, y $f$ tiene un extremo local en $x_{0}$, entonces $f'(x_{0}) = 0$.
- Se dice que $x_{0}$ es un **punto crítico de** $f$ si esta es derivable en $x_{0}$ y $f'(x_{0}) = 0$.
- **Cololario**. Supongamos que $f$ tiene un extremo local en $x_{0}$. Entonces, solamente se cumple una de las siguientes afirmaciones:
	1. $x_{0}$ es un **punto crítico**.
	2. $x_{0}$ es uno de los extremos del intervalo $I$ estudiado.
	3. $f$ no es derivable en $x_{0}$.
---
# 2.2 Teoremas del valor medio (TVMs)
##### Teorema de Rolle
- Sea $f: [a,b] \longrightarrow \mathbb{R}$ continua y además derivable en $(a,b)$. Si $f(a) = f(b)$, entonces $\exists c \in (a,b) : f'(c) = 0$.
##### Teorema de Lagrange del valor medio
