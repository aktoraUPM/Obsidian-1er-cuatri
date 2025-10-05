# 2.1 Nociones básicas
##### Vector posición
- Es necesario un **sistema de referencia** $(O,xyz)$. Generalmente:
	- $\vec{r} = (x,y,z)$ es un vector cualquiera de **posición** en el espacio, en este caso, por ejemplo, $(3,4,4)$.
	- La base del sistema viene dada por los vectores unitarios $(\vec{i}, \vec{j}, \vec{k})$, que suponen una base ortonormal.
	- El producto escalar de $\vec{r} \cdot \vec{i}$ es la proyección de $\vec{r}$ sobre $\vec{i}$, es decir, la descomposición en $x$ de $\vec{r}$.
	- Se puede escribir $\vec{r}$ como $\vec{r} = | \vec{r} | \cdot \vec{u}_{r}$, donde $\vec{u}_{r}$ es el **unitario** en la dirección de $\vec{r}$ y $| \vec{r} |$ el módulo de $\vec{r}$. 
```tikz
\usepackage{tikz}
\usepackage{tikz-3dplot}

\begin{document}

% Angulo de vista (elevación, rotación)
\tdplotsetmaincoords{70}{110}

\begin{tikzpicture}[tdplot_main_coords, scale=1.25]

  % Dibujar ejes
  \draw[->] (0,0,0) -- (5,0,0) node[anchor=north east]{$x$};
  \draw[->] (0,0,0) -- (0,5,0) node[anchor=north west]{$y$};
  \draw[->] (0,0,0) -- (0,0,4) node[anchor=south]{$z$};

  % Segmentos auxiliares de r
  \draw[dashed, gray] (3,0,0) -- (3,4,0);
  \draw[dashed, gray] (0,4,0) -- (3,4,0);
  \draw[dashed, gray] (3,4,0) -- (3,4,4);

  % Vector r = (3,2,2)
  \draw[->, thick, red] (0,0,0) -- (3,4,4) node[anchor=south west]{$\vec{r}$};
  
  % Proyección de r sobre i
  \draw[->, thick, red!60] (0,0,0) -- (3,0,0) node[anchor=south east]{$\vec{r} \cdot \vec{i}$};
  
  % Segmentos auxiliares de u_r
  \draw[dashed, gray] (0.468,0,0) -- (0.468,0.625,0);
  \draw[dashed, gray] (0,0.625,0) -- (0.468,0.625,0);
  \draw[dashed, gray] (0.468,0.625,0) -- (0.468,0.625,0.625);
  
  % Unitario u_r = (0.468, 0.625, 0.625)
  \draw[->, thick, red!30] (0,0,0) -- (0.468, 0.625, 0.625) node[above]{$\vec{u}_r$};

  % Base ortonormal
  \draw[->, thick, cyan] (0,0,0) -- (1,0,0) node[below]{$\vec{i}$};
  \draw[->, thick, cyan] (0,0,0) -- (0,1,0) node[above]{$\vec{j}$};
  \draw[->, thick, cyan] (0,0,0) -- (0,0,1) node[left]{$\vec{k}$};
  
  % Puntos auxiliares
  \filldraw[gray] (3,0,0) circle (0.5pt);
  \filldraw[gray] (0,4,0) circle (0.5pt);
  \filldraw[red]  (3,4,4) circle (0.2pt);

\end{tikzpicture}

\end{document}

\end{document}
```
- **Órbita y trayectoria**.
	- La **órbita** es el conjunto de puntos en el espacio que ocupa un móvil en su movimiento. Se expresa en forma de ecuación general, $F(x,y) = 0$.
	- La **trayectoria** es cualquier determinación *paramétrica* de la órbita, $\left\{ \begin{array} l x(p) = f_1(p) \\ y(p) = f_2(p) \\ z(p) = f_{3}(p) \end{array} \right.$, donde $p$ es un parámetro. Es común utilizar el **tiempo** $t$ como parámetro.
##### Vector velocidad
- Existen varios vectores para indicar la velocidad, que es el cambio de posición respecto al tiempo.
	- **Velocidad media** del móvil en un periodo de tiempo $\Delta t$. $\vec{v}_{med} = \displaystyle{\frac{\Delta \vec{r}}{\Delta t} = \frac{\vec{r}(t_{2})-\vec{r}(t_{1})}{t_{2} - t_{1}}}$.
	- **Velocidad instantánea**, en un momento $t$ preciso. $\vec{v}_{inst} = \vec{v}(t) = \displaystyle{ \frac{d \vec{r}}{dt} }$.
	- Para un vector $\vec{r}$, $\vec{r}(t) = x(t)\vec{i} + y(t)\vec{j} + z(t)\vec{k} = \big(x(t), y(t), z(t) \big)$, tenemos el vector $\vec{v} = \frac{d\vec{r}}{dt} = \frac{d}{dt} (x \vec{i}, y \vec{j}, z \vec{k}) = \left(  \frac{dx}{dt}, \frac{dy}{dt}, \frac{dz}{dt} \right) = (v_{x}, v_{y}, v_{z})$.
	- Se define el **vector unitario tangente** o **paralelo** (notación Zemanski) como el vector $\vec{u}_{t} = \frac{\vec{v}}{| \vec{v} |}$, con el que ponemos que $\vec{v} = | \vec{v} | \cdot \vec{u}_{t}$.
##### Vector aceleración
- De nuevo, existen varios vectores implicados en la indicación de la aceleración, la variación de la velocidad respecto al tiempo.
	- **Aceleración media** en un periodo de tiempo $\Delta t$. $\vec{a}_{med} = \displaystyle{\frac{\Delta \vec{v}}{\Delta t} = \frac{v(t_{2}) - v(t_{1})}{t_{2} - t_{1}} }$
	- **Aceleración instantánea** en un momento $t$. $\vec{a}_{inst} = \vec{a} (t) = \displaystyle{ \frac{d\vec{v}}{dt} = \frac{d^{2}\vec{r}}{dt^{2}} }$
- Se define $\vec{a}$ como la siguiente suma: $$ \vec{a} = \frac{d\vec{v}}{dt} = \frac{d}{dt} (\vec{u}_{t} + | v |) = \left( \frac{d|v|}{dt} \right) \vec{u}_{t} + \left( \frac{d\vec{u}_{t}}{dt} \right) |v| $$
- Los vectores $u_{t}$ y $\frac{d}{dt} u_{t}$ son, sin excepción, perpendiculares, ya que en efecto, su producto escalar también lo es: $$ \frac{d}{dt} (\vec{u}_{t} \cdot \vec{u}_{t}) \overset{\vec{u}_{t} \cdot \vec{u}_{t} = 0} = 0 = \left( \frac{d\vec{u}_{t}}{dt} \right) \vec{u}_{t} + \vec{u}_{t} \left( \frac{d\vec{u}_{t}}{dt} \right) = 2\left[ \left( \frac{d\vec{u}_{t}}{dt} \right) \cdot \vec{u}_{t} \right] = 0 $$
  Con ello, se define el **vector unitario normal** $\vec{u}_{n}$ como $$ \vec{u}_{n} = \frac{\displaystyle{ \frac{d\vec{u}_{t}}{dt} }}{\displaystyle{ \left| \frac{d\vec{u}_{t}}{dt} \right|  }}$$
  Y con ello, $\vec{a} = \vec{a}_{t} + \vec{a}_{n}$, donde $\left\{\begin{array}{l} \vec{a}_{t} = a \vec{u}_{t} = \frac{dv}{dt} \vec{u}_{t} \\ \vec{a}_{n} = v \left( \frac{d\vec{u}_{t}}{dt} \right) \vec{u}_{n} \end{array} \right.$ son las **componentes intrínsecas de la aceleración**.
  Se añade $\vec{u}_{n}$ al término de $\vec{a}_{n}$ para poder expresarlo en función de una base ortonormal, no aporta nada al término ${} v \frac{d\vec{u}_{t}}{dt} {}$, de forma que se expresa: $$ \vec{a} = a_{t}\vec{u}_{t} + a_{n} \vec{u}_{n} $$
##### Radio de curvatura y circunferencia osculatriz
- En el caso del plano, una trayectoria se puede aproximar por una sucesión infinita de arcos de circunferencia. Esta circunferencia se denomina **circunferencia osculatriz**.
- Así, para cualquier trayectoria, $a_{n}$ es la correspondiente a un **movimiento circular**, por lo que ${} a_{n} = \displaystyle{ \frac{v^{2}}{R} } \implies \vec{a}_{n} = \displaystyle{ \frac{v^{2}}{R} \vec{u}_{n}} {}$, donde $R$ es el radio de la circunferencia osculatriz, o **radio de curvatura**, y el centro al que apunta es el **centro de curvatura**.
---
# 2.2 Integración de las ecuaciones del movimiento
- La intención de la cinemática es obtener $\vec{r}$, y en ocasiones esto será a partir de vectores derivados de este mismo, como $\vec{a}$ o $\vec{v}$. Para ello, es necesario integrar sus ecuaciones.
- Por lo general y por el momento, se restringirá a movimientos unidireccionales con una sola $\vec{a}$. Tomamos, entonces, $\vec{a}(t) = a_{x}(t) \vec{i}, \; \vec{v}(t) = v_{x}(t) \vec{i}, \; \vec{r} (t) = x(t) \vec{i}$. Partiendo de que $\vec{a} = \frac{d\vec{v}}{dt}$, $$ \vec{a} = a_{x} \vec{i} = \frac{d}{dt} (v_{x} \vec{i}) \implies \frac{dv_{x}}{dt} = a_{x} \implies dv_{x} = a_{x} \, dt$$ Ahora, se puede comenzar a integrar. $$ \begin{gather} \int_{v_{x}(t_{0})}^{v(x)(t)} dv_{x} = \int_{t_{0}}^{t} a_{x}(t) \, dt \\[7px] v_{x}(t) - v_{x}(t_{0}) = \int_{t_{0}}^{t} a_{x} \, dt \\[7px] v_{x}(t) = v_{0}(t) + \int_{t_{0}}^{t} a_{x} \, dt \end{gather} $$
- Por su parte, para $\vec{r} = \frac{d}{dt}\vec{v} \implies x(t) = \frac{d}{dt} v_{x}(t)$, $$ \begin{gather} \int_{x(t_{0})}^{x(t)} dx = \int_{t_{0}}^{t}v_{x}(t) \, dt = \int_{t_{0}}^{t} \left[ v_{x}(t_{0}) + \int_{t_{0}}^{t} a_{x}(t) \,dt \right] \,dt \\[7px] x(t) = x(t_{0}) + \underbrace{v_{x}(t_{0}) (t-t_{0})}_{v(t_{0}) = cte} + \iint_{t_{0}}^{t} a_{x} \,(dt)^{2} \end{gather} $$
- Poniendo como caso particular $a_{x} = 0$, $$ \begin{gather} \boxed{v_{x}(t) = v_{x}(t_{0}) + a_{x}(t-t_{0})} \\[7px] x(t) = x(t_{0}) + v_{x}(t_{0})(t-t_{0}) + \int_{t_{0}}^{t} a_{x}(t-t_{0}) \,dt   = \boxed{x(t_{0}) + v_{x}(t-t_{0}) + \frac{1}{2}a(t-t_{0})^{2}} \end{gather} $$
---
# 2.3 Movimiento circular general
##### Magnitudes cinemáticas angulares
- **Posición angular** $\varphi$. Ángulo de $\vec{r}$ con un eje coordenado. (SI) $[\varphi] = rad = \frac{m}{m} = 1$. 
- **Velocidad angular** $\omega = \frac{d \varphi}{dt}$.  ${} [\omega] = rad \, s ^{-1} {}$.
- **Aceleración angular** $\alpha = \frac{d \omega}{dt} = \frac{d^{2} \varphi}{dt^{2}}$. $[\alpha] = rad \, s ^{-2}$.
##### Relación entre magnitudes cinemáticas lineales y angulares
- Determinada por la condición $l = \varphi R \implies v = \frac{d \varphi}{dt} R = \omega R \implies a = \frac{d \omega}{dt} R = \alpha R$ 
##### Distintos movimientos angulares
- **Movimiento circular general**. Donde $\alpha = \alpha (t)$.
- **Movimiento circular uniforme**. Donde $\alpha (t) = 0 \implies \frac{d \omega}{dt} = 0$. En este, se definen una serie de magnitudes adicionales.
	- **Periodo** $T = \frac{2\pi}{\omega}$, $[T] = s$.
	- **Frecuencia** $f = \frac{1}{T}$, $[f] = s ^{-1} = \text{Hz}$.
---
# 2.4 Movimiento relativo. Transformaciones de Galileo
##### Interacción de varios sistemas de referencia
- En la mecánica clásica, se toman **el tiempo y el espacio como absolutos**, lo que implica que sea quien sea el espectador, este va a ver siempre los **mismos cambios en espacio y en tiempo** que cualquier otro observador en algún punto del espacio.
- Considerando dos sistemas de referencia $SR_{1}$ y $SR_{2}$, se da que:
	1. $\vec{r}_{1} = \vec{r}_{12} + \vec{r}_{2}$, siendo $\vec{r}_{12}$ el vector de **posición relativo** de $SR_{2}$ frente a $SR_{1}$. De esto se concluye que, efectivamente, el espacio es absoluto.
	2. $\displaystyle{ \frac{d \vec{r}_{1}}{dt_{1}} = \vec{v}_{1} = \vec{v}_{12} + \vec{v}_{2} = \vec{v}_{12} + \frac{d\vec{r}_{2}}{dt_{2}} }$, y el tiempo es absoluto, $t_{1} = t_{2} = t \implies \vec{v}_{1} = \vec{v}_{12} + \vec{v}_{2}$.
	3. De forma análoga a la velocidad, $\vec{a}_{1} = \vec{a}_{12} + \vec{a}_{2}$.
```tikz
\usepackage{tikz}
\usepackage{tikz-3dplot}

\begin{document}

% Ángulo de vista
\tdplotsetmaincoords{70}{110}

\begin{tikzpicture}[tdplot_main_coords, scale=2.5]

  % Ejes del sistema S (fijo)
  \draw[->] (0,0,0) -- (3,0,0) node[anchor=north east]{$x_1$};
  \draw[->] (0,0,0) -- (0,3,0) node[anchor=north west]{$y_1$};
  \draw[->] (0,0,0) -- (0,0,2) node[anchor=south]{$z_1$};
  \filldraw[gray!60] (0,0,0) circle (0.8pt) node[above left]{$O_1$};

  % Origen del sistema S': O'
  \coordinate (Oprime) at (0.5,2,1.5);

  % Vector de posición relativa entre S y S'
  \draw[->, thick, red] (0,0,0) -- (Oprime) node[midway, above left]{$\vec{r}_{12}$};

  % Ejes del sistema S' (móvil)
  \draw[->, thick, blue!30] (Oprime) -- ++(1,0,0) node[anchor=north east]{$x_2$};
  \draw[->, thick, blue!30] (Oprime) -- ++(0,1,0) node[anchor=north west]{$y_2$};
  \draw[->, thick, blue!30] (Oprime) -- ++(0,0,1) node[anchor=south]{$z_2$};
  % Etiqueta de O'
  \filldraw[blue!35] (Oprime) circle (0.8pt) node[below right]{$O_2$};
  
  % Punto P
  \filldraw[green] (2,1.5,0.5) circle (0.8pt) node[below left]{$P$};

  % Vector r_1 y r_2
  \draw[->, red!50] (0,0,0) -- (2,1.5,0.5) node[midway, below left]{$\vec{r}_1$};
  \draw[->, blue!20] (Oprime) -- (2,1.5,0.5) node[midway, below right]{$\vec{r}_2$};

  % Punto marcado en el origen de S'
  % \filldraw[red] (Oprime) circle (1.2pt);

\end{tikzpicture}

\end{document}

```
##### Caso de interés: movimiento relativo uniforme entre $SR$
- En este caso, $\frac{d\vec{v}_{12}}{dt} = \vec{a}_{12} = 0$.
- Relevancia: las **leyes de la mecánica** son **iguales** en los dos sistemas de referencia.
	La mecánica Newtoniana se basa en las **aceleraciones** en sus leyes, y en este caso particular, $\vec{a}_{1} = \underset{0}{\cancel{\vec{a}_{12}}} + \vec{a}_{2} = \vec{a}_{2}$.
- En un caso **general**, las ecuaciones de transformación toman la siguiente forma. $$ \begin{gather} \vec{r}_{1} = \vec{r}_{12} + \vec{r}_{2} \overset{*}{=} [\vec{r}_{12}(t_{0}) + \vec{v}_{12}(t - t_{0})] + r_{2}(t) \\[7px] \overset{*}{=} \vec{v}_{12} = \frac{d\vec{r}_{12}}{dt} \implies \int_{\vec{r}(t_{0})}^{\vec{r}(t)} d\vec{r}_{12} = \int_{t_{0}}^{t} \vec{v}_{12}(t) \:dt \implies \vec{r}_{12}(t) - \vec{r}_{12}(t_{0}) = \vec{r}_{12}(t_{0}) + \vec{v}_{12}(t - t_{0}) \overset{*}{=}\end{gather} $$
---
# 2.5 Leyes de Newton
### 2.5.1 Nociones básicas y enunciado de las leyes
##### Concepto de fuerza
- Magnitud vectorial utilizada para **cuantificar la interacción entre dos sistemas**.
- Obedecen el álgebra vectorial, por lo que un sistema de fuerzas da lugar a una **fuerza resultante** $F = \sum\limits_{i = 1}^{n} F_{i}$.
##### Primera ley: Ley de inercia
>Un cuerpo sometido a **ninguna interacción** mantiene **constante** su **vector velocidad**. $$ \vec{F} = 0 \iff \vec{v} = \text{cte} \iff \vec{a} = 0 $$
- Establece en qué sistemas de referencia son válidas las leyes de Newton: los **sistemas de referencia inerciales SRI**.
  Si, por ejemplo, en un sistema se puede apreciar cambio en otro sistema sin que a este segundo, aparentemente, lo afecte ninguna fuerza, se dirá que no es un SRI, y que por tanto no se pueden aplicar las leyes de Newton sobre él.
##### Masa inerte y segunda ley
- El concepto de inercia se ve reflejado en la **masa inerte**, la magnitud escalar que lo cuantifica.
- En un SRI, la masa inerte de las partículas es la **constante de proporcionalidad** entre la **fuerza** aplicada al cuerpo y la **aceleración** que este experimenta. $$ \vec{F} = m \vec{a} $$
##### Tercera ley
>Dos partículas con interacción de contacto ejercen fuerzas **la una sobre la otra**, de igual módulo y dirección, pero de distinto sentido.
##### Fuerzas notables de la mecánica
1. **Fuerzas internas**. Entre elementos de del propio sistema, en contraposición a las **externas**, entre elementos del sistema y el resto del universo.
2. **Fuerzas de ligadura**. Representan restricciones al movimiento del sistema.
	- **Fuerza normal** de un plano. Reacción entre un 
	- **Tensión** de una cuerda
3. **Fuerzas de rozamiento**.
	- **Rozamiento estático**. No implica desplazamiento relativo entre las superficies en contacto. No tiene valor fijo, pero sí valor máximo. $$ F_{R}^{(e)} = \mu_{e} N $$
	  Donde $\mu_{e}$ es el **coeficiente de rozamiento estático**, y $N$ la fuerza de reacción normal entre superficies en contacto.
	- **Rozamiento dinámico**. Implica desplazamiento relativo entre las superficies en contacto. $$ F_{R} = \mu N = \mu_{d} N$$
	  Tal que $\mu$ ó $\mu_{d}$ es el **coeficiente de rozamiento dinámico**.