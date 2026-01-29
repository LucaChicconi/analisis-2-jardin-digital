---
{"dg-publish":true,"permalink":"/practicas/practica-0-repaso-integrales/","tags":["repaso-integrales"]}
---

Teórica vinculada : [[Teóricas/Teórica 0 - Parametrización de curvas\|Teórica 0 - Parametrización de curvas]] (fue el mismo día, en realidad ésta práctica no tocó los temas de la teórica sino que se hizo un repaso de integrales)

## Principio de Cavalieri (Cálculo de volúmenes)
![Figura0Práctica0.png](/img/user/Figuras/Figura0Pr%C3%A1ctica0.png)

### Método de las secciones o de Cavalieri:
Permite calcular volúmenes de sólidos que cumplan con ciertas condiciones.

Sea $S$ un sólido y $Px$ con $a \leq x \leq b$ una familia de planos paralelos tales que :
1. $S$ está limitado entre $a$ y $b$
2. El área de la sección de $S$ al cortarlo con el plano $Px$ es $A(x)$
entonces

$$
Volumen = V(s) = \int_{a}^b{A(x)dx}
$$

Ejercicio 1 : 
Hallar el volumen del siguiente sólido de revolución:

![Ejercicio1Práctica0.png](/img/user/Figuras/Ejercicio1Pr%C3%A1ctica0.png)

$x\in[a,b]$

Simple

$$V(S)= \int_{a}^b{\pi*[f(x)]²dx}$$
Listo. Luego queda (una vez sepas cuál es $f(x)$) hallar la primitiva y evaluar.

Ejercicio 2:
Encontrar el volumen de la región obtenida al girar la gráfica de la parábola $y = -x²+2x+3$ con $x\in[-1,3]$ al rededor del eje $x$.

![Ejercicio2Práctica0.png](/img/user/Figuras/Ejercicio2Pr%C3%A1ctica0.png)

Aclaración : El eje verde es el eje x, el rojo es el y, el azul es el z. El sólido realiza la vuelta completa, en el gráfico no se ve así por que sino tapaba los ejes!
$$y = -x²+2x+3$$
$$y-3 = -x²+2x$$
Completamos cuadrados
$$y-3-1=-x²+2x-1 = -(x-1)²$$
Recordando la ecuación canónica de la parábola:
$$(x-k) - 4p(y-k)$$
tenemos que
$$y-4 = -(x-1)² \implies vértice=(1,4)$$
Esto sirvió para darse una noción geométrica de cómo es el sólido.

Ahora aplicamos Cavalieri para calcular el volumen

$$\int_{-1}^{3}{(-x²+2x+3)²dx}  = \frac{512\pi}{15}$$

## Cambio de variable

### Teorema
Sean $D$ y $D^*$ de $\mathbb{R}²$, sea $T$ una aplicación diferenciable $T$ de $D*$ con imagen $D$, es decir $T(D*)=D$ y sea $f$ una función con valores reales, $f:D\rightarrow \mathbb{R}$. 
La idea es transformar $\int \int_{D}f(x,y)dA$ en una integral definida en $D*$ donde podamos integrar $f\circ T$ más fácil.

Supongamos que $D*$ está en el plano $uv$ y $D$ está en el plano $xy$. Se define la aplicación $T$ por medio de 
$$T(u,v) = (x(u,v),y(u,v),z(u,v))$$ $$(u,v)\in D*$$
Sin embargo, lamentablemente

$$\iint_{D}f(x,y)\,dx\,dy \neq \iint_{D*}f(x(u,v),y(u,v))\,du\,dv$$
Hace falta algún factor de conversión para que las integrales sean iguales.
La razón de ésto está detrás de $dxdy$ y $dudv$ (Los elementos de área o volumen en integrales triples)
Lo que pasa es que estamos cambiando la escala con la que medimos, ya sea en tamaño o forma. 
![Figura1Práctica0.png](/img/user/Figuras/Figura1Pr%C3%A1ctica0.png)

Fijate cómo al medir con distintas "reglas" la misma distancia no da lo mismo.

Acá es donde entra en juego el **Jacobiano**,algo así como el factor de conversión.

$$\mathcal{J} = \det(D_{T})$$
donde $D_{T}$ es la matriz diferencial total de T.

Entonces queda que 

$$\iint_{D}f(x,y)dxdy = \iint_{D*}{f(x(u,v),y(u,v))|\mathcal{J}|}\,du\,dv$$


### Coordenadas polares

$(x,y) = (r\cos(\theta),r\sin(\theta))$
$\mathcal{J} = r$
Entonces 
$$\iint_{D}{f(x,y)dxdy} = \iint f(r\cos\theta , r\sin\theta)r \,dr\,d\theta$$
### Coordenadas cilíndricas
$(x,y,z) = (r\cos\theta,r\sin\theta,z)$
$|\mathcal{J}|$ = r 😁

Entonces
$$\iiint_{W}f(x,y,z)\,dx\,dy\,dz = \iiint_{W^*}f(x(r,\theta,z),y(r,\theta,z),z(r,\theta,z))*r \,dr\,d\theta\,dz$$
### Coordenadas esféricas
$(x,y,z) = (\rho \sin \phi \cos \theta,\rho \sin \phi \sin \theta , \rho \cos \phi)$
$\rho >0, \phi\in[0,\pi],\theta\in[0,2\pi)$

$\|\mathcal(J)| = \rho² \sin \phi$
![Figura2Práctica0.png](/img/user/Figuras/Figura2Pr%C3%A1ctica0.png)

$$\iint_{W}f(x,y,z)dxdydz = \iiint_{W^*}f(\rho \sin \phi \cos \theta,\rho \sin \phi \sin \theta ,\rho \cos \phi)*\rho²\sin \phi \,d\rho \,d\phi \,d\theta$$

Ejercicio 3:
Hallar el volumen de la región W limitada por las superficies
$$z = x²+y² , z = 10-x²-2y²$$

![Ejercicio3Práctica0.png](/img/user/Figuras/Ejercicio3Pr%C3%A1ctica0.png)

(tip para graficar a mano)
De $z = 10-x²-2y²$ vemos que $z-10 = -(x²+y²)$ entonces sabemos que uno de los paraboloides está hacia abajo y tiene su vértice en $z=10$ y el otro es un paraboloide. 

Entonces para hallar el volumen debemos hacer
$$V(W)= \iiint_{W}1\,dx\,dy\,dz$$
Aplicando el cambio de variable nos queda:
$$\iiint_{x²+y²}^{10-x²-2y²}dz\,dy\,dx$$
Te desafío a intentar hallar los limites de integración de y (Dibujá como se vería la intersección de las superficies desde arriba osea contemplando sólo los ejes x e y). Vas a ver que lo que queda es extremadamente rancio de integrar. Así que pasemos directamente a **Coordenadas Cilíndricas $(r,\theta,z)$**
Tenemos: 
- La ecuación canónica de una elipse : $$\frac{x²}{a²}+\frac{y²}{b²} = 1$$
- Que $2x²+3y²=10 \implies \frac{x²}{5}+\frac{y²}{\frac{10}{3}}= 1$

Entonces vemos que nuestro $a= \sqrt{5 }$ y $b= \sqrt{ \frac{10}{3} }$
De esta manera podemos reescribir 

$$x = a*r\cos \theta = \sqrt{ 5 }r \cos \theta$$
$$y = b*r\sin \theta = \sqrt{ \frac{10}{3} }r\sin \theta$$Es decir 
$$\mathcal{T}(r,\theta,z)=\left( \sqrt{ 5 }*r\cos \theta,\sqrt{ \frac{10}{3}}*r\sin \theta ,z\right)$$
con $r \in [0,1]$ y $\theta \in [0,2\pi]$

Entonces, luego de integrar en z con los extremos que teníamos, podemos proceder con la siguiente integral.

Ah , el modulo del Jacobiano CREO que es $\sqrt{ \frac{10}{3} }*r$

$$\iint_{D}{10-x²-2y²-x²-y^2}dA$$
Y luego del cambio de variables nos queda ésto
$$\int_{0}¹{\int_{0}^{2\pi}{[(1-r²)*r]dr\,d\theta}}$$
Lo cual te podes encargar vos de checkear si efectivamente da lo que me dio a mí
$$\pi*30\sqrt{ \frac{10}{3} }$$
Al profe le dio otra cosa pero yo ya estaba cansado como para checkear