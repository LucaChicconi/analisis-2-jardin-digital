---
{"dg-publish":true,"permalink":"/teoricas/teorica-1-longitud-de-arco/"}
---

Anterior : [[Teóricas/Teórica 0 - Parametrización de curvas\|Teórica 0 - Parametrización de curvas]]

- Sea $\mathcal{C}$ una curva y $\sigma:[a,b]\rightarrow \mathcal{C} \subseteq \mathbb{R}^n$ parametrización regular de $\mathcal{C}$.
- Sea $\pi$ partición de $[a,b]$ , $\pi : a=t_{0}<t_{1}<t_{2}<\dots<t_{n} = b$ consideramos que $t_{i+1}-t_{i}= \frac{b-a}{n}$
$\pi$ induce una partición de $\mathcal{C}$
$P:{P_{0},P_{1},\dots,P_{n}}$ partición de $\mathcal{C}$


### Definición: Longitud de poligonal con puntos en P

$L(P) = \sum_{i=0}^{n-1} \lvert \lvert P_{i+1}-P_{i} \rvert \rvert$ donde $P_{i} = \sigma(t_{0})$

### Definición: Curva rectificable
Decimos que una curva $\mathcal{C}$ es rectificable si
$$\exists M>0 /L(P)\leq M$$
Para toda partición de $\mathcal{C}$.

Entonces existe un **supremo de p partición de $\mathcal{C}$** y lo definimos como
$$Long(\mathcal{C})= sup L(c)$$
### Proposición: 
Sea $\mathcal{C}$ una curva abierta simple suave. Entonces $\mathcal{C}$ es rectificable. Más aún : Si $\sigma:[a,b]\rightarrow\mathcal{C},\sigma\in C¹$ es una parametrización regular de $\mathcal{C}$, entonces la longitud es

$$Long(\mathcal{C})= \int_{a}^b \lvert \lvert \sigma'(t)\,dt \rvert  \rvert $$
Observar que ésta definición de longitud no depende de la parametrización que elijamos.

Ejemplo: Sea $\mathcal{C}$ 
![Figura0Teórica1.png](/img/user/Figuras/Figura0Te%C3%B3rica1.png)
$\sigma(t)=\cos t,\sin t)$  con $t\in\left[ -\frac{\pi}{2},\frac{\pi}{2} \right]$
$\sigma'(t) = (-\sin t, \cos t) \neq (0,0) \forall t$
$\lvert \lvert \sigma'(t) \rvert \rvert =\sqrt{ \sin²(t)+\cos²(t) } = 1$
$Long(\mathcal{C}) = \int_{-\frac{\pi}{2}}^{\pi/2}1dt = \frac{\pi}{2}+\frac{\pi}{2} = \pi$

A continuación tuvimos un comentario de la demo de ésto:
Como $\mathcal{C}$ es suave puedo considerar $\sigma:[a,b]\rightarrow  \mathcal{C}$ regular tomamos $\pi$ partición de $[a,b]$ y $P$ la partición de $\mathcal{C}$ inducida por $\pi$

$$L(P)= \sum_{i=0}^{n-1}\lvert \lvert P_{i+1}-P_{i} \rvert  \rvert = \sum_{i=0}^{n-1} \lvert  \lvert \sigma_{t_{i}+1}-\sigma(t_{i}) \rvert  \rvert $$
Por Teorema de Lagrange (creo) se simplifica a:
$$L(P) = \sum_{i=0}^{n-1}\lvert \lvert \sigma'(t^*)(t_{i+1}-t_{i}) \rvert  \rvert $$
Como sabemos que $(t_{i+1}-t_{i})>0$ lo podemos sacar "de factor común" de la sumatoria, dejándonos con
$$L(P)=\left( \sum_{i=0}^{n-1} \lvert  \lvert \sigma'(t^*) \rvert  \rvert  \right)* (t_{i+1}-t_{i})$$
Lo cual es efectivamente una suma de Riemann [https://es.wikipedia.org/wiki/Suma_de_Riemann](Suma de Riemann)

Eso significa que si tomamos límite con n tendiendo a infinito obtenemos 
$$\lim_{ n \to \infty }L(P) = \int_{a}^{b}\sigma'(t)dt $$
Que es lo que queríamos probar!

### Definición : curva regular a trozos
Sea $\sigma[a,b]\rightarrow \mathbb{R}^n$,decimos que $\sigma$ es regular a trozos si existe una partición de $[a,b]$ 
$$a= t_{0} <t_{1}<\dots<t_{n}= b$$
tal que $\sigma |_{[t_{i,t_{i+1}}]}$ es regular.

### Definición : curva suave a trozos
Una curva $\mathcal{C}$ es suave a trozos si admite una parametrización regular a trozos.

Observación : Si $\mathcal{C}$ es suave a trozos, entonces $Long(\mathcal{C})= \sum Long(\mathcal{C}_{i})$ donde $\mathcal{C}_{i} = \mathrm{Im}(\sigma_{[t_{i},t_{i+1}]})$

### Función de Longiutd de arco

Sea $\mathcal{C}$ abierta, simple y suave y $\sigma:[a,b]\to\mathcal{C}$ una parametrización regular. Definimos $g(a,t):[a,b]\to \mathbb{R}$ como 
$$g(a,t) = \int_{a}^{t}\lvert \lvert \sigma'(s) \rvert  \rvert ds $$

Observación: $g$ mide la longitud de la curva desde $\sigma(a)$ hasta $\sigma(t)$
![Figura1Teórica1.png](/img/user/Figuras/Figura1Te%C3%B3rica1.png)

**Propiedades de g**
1. Si $t>a \implies g(a,t)>0 (\sigma'\neq \vec{0})$
2. Si $a<t<s\leq b \implies g(a,s) = g(a,t)+g(t,s)$
	Entonces g es estrictamente creciente
3. $g(a,t) = \int_{a}^{t}\lvert \lvert \sigma'(s) \rvert \rvert ds$
	Por TFC: ${\frac{\partial g}{\partial t}}(a,t) = \lvert  \lvert  \sigma'(t) \rvert \rvert$
4. Como $sigma$ es regular entonces $g'\neq 0 \forall t \in[a,b]$ y $\sigma'\neq \vec{0}$

Observación: Por lo anterior podemos asegurar que existe $g⁻1$
$$g^{- 1 }\to[a,b]$$
$$\mathcal{l}= Long (\mathcal{C})$$
y además $(g^{-1})' \neq 0$. Recordemos que en el teorema de la función inversa [https://es.wikipedia.org/wiki/Teorema_de_la_funci%C3%B3n_inversa](Teorema de la función inversa)
$$(g^{-1})'= \frac{1}{g'(g^{-1}(t))}$$
Ahora sea $\gamma :[a,l]\to \mathcal{C} \subseteq \mathbb{R}^{n}$ , $\gamma(s) = \sigma(g^{-1}(s))$ es parametrización regular de la curva $\mathcal{C}$ (Porque $\sigma$ es regular y g' es biyectiva)

Si $f(t)=\int_{0}^{t}\lvert \lvert \gamma'(s) \rvert \rvert ds$, $f:[0,l]\to \mathbb{R}$
![Teórica1Figura2.png](/img/user/Figuras/Te%C3%B3rica1Figura2.png)

$f$ mide la longitud de arco desde $\gamma_{0}$ hasta $\gamma_{l}$, más aún $f(t)=t$

*Efectivamente, normalizamos la velocidad en la que recorremos la curva. Ahora lo hacemos a velocidad constante. Ésto se conoce como reparametrizar por longitud de arco.*

Más aún, $f(t)=t$. Veamos que $f(t) = t$:
$\gamma'(s)$ es por regla de la cadena igual a $\sigma'(g^{-1}(s)*\frac{1}{g'(g^{-1}(s))})$
$$\lvert \lvert \gamma'(S) \rvert  \rvert = \lvert  \lvert \sigma'(g'(s)) \rvert  \rvert * \lvert\frac{1}{g'(g^{-1}(s))}\rvert  $$
$$= \lvert  \lvert \sigma'(g^{-1}(s)) \rvert  \rvert * \frac{1}{g'(g^{-1}(s))}$$
$g'=\lvert \lvert \sigma' \rvert \rvert$ asi que...
$$= 1$$
$\implies f(t)=\int_{0}^{t}\lvert \lvert \gamma'(S) \rvert \rvert ds = \int_{0}^{t}1ds = t$

### Definición :
Ésto, como te dije antes, se llama parametrización por longitud de arco de $\mathcal{C}$