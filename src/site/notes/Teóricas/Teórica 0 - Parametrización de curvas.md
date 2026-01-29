---
{"dg-publish":true,"permalink":"/teoricas/teorica-0-parametrizacion-de-curvas/"}
---

# Curva
Una curva $\mathcal{C} \in \mathbb{R}^n$  es un conjunto que es imagen de una función  $\sigma : [a,b] \rightarrow \mathbb{R}^n$ y cuya  $\mathrm{Im(\sigma)= \mathcal{C}}$
llamamos a $\sigma$ **parametrización de la curva $\mathcal{C}$**.
$\mathcal{C}$ es continua y sobreyectiva.

Ejemplo
$\sigma:[a,b] \rightarrow \mathbb{R}²$
$\sigma(t) = (t,t²)$

Podemos observar que $\sigma(t)$ es continua porque $\sigma(t) = (f(t),g(t))$ y tanto $f$ como $g$ son continuas $\forall t \in \mathbb{R}$.

Observaciones: 
	1. $\sigma(t)$ **Siempre es acotada**
	2. La misma curva puede tener más de una parametrización
		1. Ejemplo 1 : 
			$\sigma:[0,1]\rightarrow \mathbb{R}²$
			$\sigma(t) = (t,t)$	
			![Figura0Teórica0.png](/img/user/Figuras/Figura0Te%C3%B3rica0.png)
		2. Ejemplo 2:
			$\sigma [0,\frac{1}{5}] \rightarrow \mathbb{R}²$
			$\sigma(t) = (5t,5t)$
			$x(t)=5t$ $y(t)=5t$ $x=y$ 
			![Figura0Teórica1.png](/img/user/Figuras/Figura0Te%C3%B3rica1.png)
		3. Ejemplo 3:
			$\sigma [1,2] \rightarrow \mathbb{R}²$
			$\sigma(t) = (t,t²)$
			![Figura2Teórica0.png](/img/user/Figuras/Figura2Te%C3%B3rica0.png)
			Si $\mathcal{C}$ es el gráfico de una función $f$ entonces siempre la puedo parametrizar por $\sigma(t,f(t))$
		4.Ejemplo 4: 
			$\sigma(t):[0,2\pi] \rightarrow \mathbb{R}²$
			$\sigma(t) = (\cos(t),\sin(t))$
			![Figura3Teórica0.png](/img/user/Figuras/Figura3Te%C3%B3rica0.png)
					
			 
---
## Curva Simple Abierta
Una curva $\mathcal{C}$ se dice *simple abierta* si no se corta a si misma.
Es decir, si ***admite una parametrización*** $\sigma(t)$ ***inyectiva en $[a,b]$***

$\sigma(t):[a,b] \rightarrow \mathbb{R}^n$ es simple abierta si:
No termina en el mismo punto en el que comienza. $\sigma(t_{i})= \sigma(t_{j}) \implies t_{i} = t_{j},\forall t\in[a,b]$

---
## Curva Simple Cerrada
Una curva $\mathcal{C}$ se dice *simple cerrada* si no se corta a si misma excepto en el punto donde empieza y termina.
Es decir, si ***admite una parametrización*** $\sigma(t)$ ***inyectiva en $[a,b)$***

$\sigma(t):[a,b] \rightarrow \mathbb{R}^n$ es simple cerrada si:
No termina en el mismo punto en el que comienza. $\sigma(t_{i})= \sigma(t_{j}) \implies t_{i} = t_{j},\forall t\in[a,b)$
$\wedge$
$\sigma(a) = \sigma(b)$
---
## Recta tangente
*Antes* : $y = f'(x)(x-x_{0})+f(x_{0})$
Ahora : ![Figura4Teórica0.png](/img/user/Figuras/Figura4Te%C3%B3rica0.png)
 $\mathcal{L}:\lambda(Q-P)+P$ además cuando $h\rightarrow 0$ , $\mathcal{L} \rightarrow$ recta tangente
La recta tangente en el punto $P_{0}$ : $\lambda\sigma'(t_{0}) + P_{0}$ 
Observemos que 
$\frac{1}{h}(Q-P_{0})= \frac{\sigma(t_{0}+h)- \sigma(t_{0})}{h}$ lo que es en realidad **un cociente incremental**.

Entonces si tomamos límite con h tendiendo a 0, obtenemos que
$\\lim_{ h \to 0 }{\frac{1}{h}(Q-P_{0})} = \sigma'(t_{0})$ ,  donde $\sigma'(t_{0})$ es el vector director de la recta tangente.
### Definición:
Sea $\mathcal{C}$ una curva que admite $\sigma:[a,b]\rightarrow \mathbb{R}²$ inyectiva en $[a,b]$ y diferenciable en $t_{0}\in [a,b]$ tal que $\sigma'(t_{0}) \neq \vec{0}$ entonces $\mathcal{C}$ tiene una recta tangente en $P_{0} = \sigma(t_{0})$ y viene dada por : $$
\mathcal{L}:\lambda\sigma'(t_{0})+ \sigma(t_{0})
$$
para $\lambda \in \mathbb{R}²$.

Proposición : 
Sea $\mathcal{C}$ parametrizada por $\sigma:[a,b]\rightarrow \mathbb{R}^n$ , $P_{0} \in \mathcal{C}$ y suponemos que $\mathcal{C}$ admite recta tangente en $P_{0}$. 
Entonces la recta tangente es **el límite de las rectas secantes a $\mathcal{C}$ que pasan por $P_{0}$ y $P\in\mathcal{C}$ cuando $P \rightarrow P_{0}$**



---
## Parametrización regular
Sea $\sigma[a,b] \rightarrow \mathcal{C} \subseteq \mathbb{R}^n$ parametrización de clase $C¹([a,b])$ (osea que tiene primer derivada y la misma es continua), $\sigma'(t) \neq \vec{0} \forall t \in [a,b]$ y cumple :
1. $\sigma$ inyectiva en $[a,b]$ , entonces $\sigma$ es una parametrización regular de una curva abierta.
2. $\sigma$ inyectiva en $[a,b)$, $\sigma(a) = \sigma(h)$ y $\sigma'(a) = k \sigma'(b)$ (iguales o linealmente dependientes) $\implies \sigma$ es parametrización regular de una curva cerrada.
La regularidad es una propiedad de la parametrización, no de la curva.

Ejemplo
$\sigma_{1}(t)=(t,t)$ y $\sigma_{2}(t)= (t³.t³)$ con $t \in [-1,1]$ .
Ambas parametrizan la misma curva y son $C¹$ en el intervalo cerrado pero una de ellas es regular y la otra no.
- $\sigma'_{1}(t) = (1,1)\neq (0,0) \forall t \in [-1,1]$ , por lo tanto $\sigma_{1}$ es regular✅
- $\sigma'_{2}(t)= (3t²,3t²) = (0,0)$ si t = 0, entonces no es regular en el intervalo cerrado ❌
### Definición : Curva suave
Una curva $\mathcal{C}$ es suave si para cada punto $P_{0}\in \mathcal{C}$ existe un entorno de $P_{0}$ tal que dicho entorno puede describirse como la unión de entornos parametrizables mediante parametrizaciones regulares.

![Figura5Teórica0.png](/img/user/Figuras/Figura5Te%C3%B3rica0.png)


### Definición: Reparametrización
- Sea $\mathcal{C}$ abierta simple
- Sea $\sigma:[a,b]\rightarrow \mathcal{C}$ param. regular de $\mathcal{C}$
- Sea $h:[c,d]\rightarrow[a,b]$ biyectiva y $C¹$ tal que $h'(t)\neq 0 \in \mathbb{R}$, entonces $\gamma : [c,d] \rightarrow \mathcal{C}$ , $\gamma(s) = \sigma(h(s))$ se llama **reparametrización de $\sigma$**

Obs: Si $\sigma$ es regular $\gamma$ debe serlo también.

Proposición: La recta tangente **no depende de la parametrización que se elija.**

Demo : 
- Dadas $\sigma_{1}$ y $\sigma_{2}$ parametrizaciones regulares de una curva abierta simple
- Sea $h$ $C¹$ tal que $\sigma_{1}= \sigma \circ h$
Recta tangente en $P_{0} = \sigma(t_{0})$ = $\sigma_{2}\circ h(t_{0}) = \sigma_{2}(h(t_{0}))=\sigma(t_{1})$  es
$\sigma_{1}(t_{0}) + \sigma_{1}'(t_{0})\lambda$ =
= $P_{0} + \sigma_{2}'(h(t_{0}))h'(t_{0})\lambda$ 
$=P_{0} + \sigma_{2}'(t_{1})h'(t_{0})\lambda$ 
$=\sigma_{2}(t_{1})+\sigma_{2}'(t_{1})h'(t_{0})\lambda$
$=\sigma_{2}(t_{1})+\sigma_{2}'(t_{1})\beta$  donde $\beta \in \mathbb{R}$

Observación: Dadas dos parametrizaciones regulares de $\mathcal{C} \implies \sigma_{2}(t) = \sigma_{1}(h(t))$ para algún $h$

Final Teórica 1
[[Apunte principal Análisis Matemático II\|Apunte principal Análisis Matemático II]]

Siguiente teórica: [[Teóricas/Teórica 1 - Longitud de arco\|Teórica 1 - Longitud de arco]]

Práctica vinculada:
[[]]