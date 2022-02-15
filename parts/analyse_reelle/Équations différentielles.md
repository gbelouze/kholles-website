```{math}
    \newcommand \sh {\textrm{sh}}
    \newcommand \ch {\textrm{ch}}
    \renewcommand \th {\textrm{th}}
    \newcommand \R {\mathbb{R}}
    \newcommand \C {\mathbb{C}}
    \newcommand \K {\mathbb{K}}
    \newcommand \Q {\mathbb{Q}}
    \newcommand \N {\mathbb{N}}
    \newcommand \Z {\mathbb{Z}}
    \newcommand \M {\mathcal{M}}
    \renewcommand \L {\mathcal{L}}
    \newcommand \B {\mathcal{B}}
    \newcommand \Vect {\textrm{Vect}}
    \renewcommand \S {\mathcal{S}}
    \renewcommand \P {\mathcal{P}}
```

# Équations différentielles

```{exercise}
:label: exo-254
Soit $a \in \R^*$ et $f \in \mathcal{C}^0(\R,\R)$, $T$-périodique. Montrer que l'équation $y'+ay=f$ admet une unique solution qui soit $T$-périodique.
```

```{solution} exo-254
:class: dropdown
La méthode de la variation des constantes amène
\begin{equation*}
y(x) = e^{-ax}(K + \int_{0}^x e^{at}f(t)dt)
\end{equation*}
Avec le changement de variable $s=t-T$ pour $y(x-T)$ on trouve
\begin{equation*}
 y(x)-y(x-T) = e^{-xT} (K + \int_0^T e^{aT}f(t)dt)
\end{equation*}
Ainsi $y$ est $T$-périodique si et seulement si $K = -\int_0^T e^{aT}f(t)dt$.
```


```{exercise}
:label: exo-255
Trouver les solutions $\mathcal{C}^2$ sur $\R$ de l'équation
\begin{equation*}
 y'' + y = \max(e^x,1)
\end{equation*}
vérifiant $y(0)=y'(0)=0$
```

```{solution} exo-255
:class: dropdown
Sur $\R^+$ la solution générale est $A\cos(x)+B\sin(x)+\frac{e^x}{2}$ d'où pour respecter les conditions au bord $y_{| \R^+} = \frac{1}{2}(e^x-cos(x)-sin(x))$.
Sur $\R^-$ la solution générale est $A\cos(x)+B\sin(x)+1$ d'où pour respecter les conditions au bord $y_{| \R^-} = 1-\cos(x)$. On vérifie enfin le bon raccord $y''(0)=0$.
```

```{exercise}
:label: exo-256
Résoudre $y' = |y-t|$.
```


```{solution} exo-256
:class: dropdown
Là où $y \geq t$ on a $y$ de la forme $t+1+Ke^t$. Là où $y \leq t$, on a $y$ de la forme $t-1+Ke^{-t}$. On remarque que dans tous les cas, $y(t)-t$ s'annule au plus une fois sur $\R$. Il ne peut donc y avoir au plus qu'un point de raccord. Ainsi trois situations se présentent

1. si $y \leq t$ pour tout $t$, on a $y = x - 1 - Ke^{-x}$ avec $K \geq 0$
1. si $y \geq t$ pour tout $t$, on a $y = x + 1 + Ke^x$ avec $K \geq 0$
1. sinon $y$ s'annule une seule fois, mettons en $t_0$, et alors $\forall t > t_0, \; y(t)=t+1-e^{t-t_0}$ et $\forall t \geq t_0, \; y(t) = t-1 + e^{t_0-t}$.

```

```{exercise}
:label: exo-257
Soit $f \in \mathcal{C}^1(\R^+, \R)$ telle que $f'+f$ bornée sur $\R^+$. Montrer que $f$ est bornée.
```

```{solution} exo-257
:class: dropdown
Soit $z = f' +f$. On écrit la solution générale de cette équation différentielle avec la variation de la constante. Il est alors évident que $f$ est bornée.
```

```{exercise}
:label: exo-258
Soit $\lambda \in \R$. Trouver les fonctions dérivables de $\R$ dans $\R$ vérifiant
\begin{equation*}
 f'(x) = f(\lambda - x)
\end{equation*}
```

```{solution} exo-258
:class: dropdown
$f$ est $\mathcal{C}^2$ et vérifie $f'' + f = 0$. Cela conduit à la solution générale $f = A\sin(x + \phi)$. La condition $f'(x) = f(\lambda - x)$ impose alors $\frac{\pi}{2} - \phi = \lambda + \phi \mod{2\pi}$. et finalement $f = A\sin(x + \frac{\pi}{4} - \frac{\lambda}{2})$.
```



```{exercise}
:label: exo-259
Soit $p \geq q$ deux fonctions de $\R$ dans $\R$. Soit $f$ une solution de $y'' + py = 0$ et $g$ une solution de $y'' + qy = 0$. Montrer que $f$ s'annule entre deux zéros de $g$.
```

```{solution} exo-259
:class: dropdown
Soit $a<b$ deux zéros consécutifs de $g$. On suppose par l'absurde que $f$ ne s'annule pas sur $[a,b]$. Quitte à changer $f$ en $-f$ on peut supposer que $f$ est strictement positive sur cet intervalle. De même on suppose que $g$ est strictement positive sur $]a,b[$. En particulier $g'(a) > 0$ et $g'(b) < 0$. Considérons alors le wronskien $\phi = fg'-f'g$. $\phi$ est dérivable et $\phi' = fg''-f''g = fg(p-q) \geq 0$.  Or $\phi(a) \geq 0$ et $\phi(b) \leq 0$. Par croissance de $\phi$ il vient $\phi_{|[a,b]}=0$. De là $\frac{g}{f}$ est constante sur $[a,b]$ et vaut $0$ en $a$ donc sur $[a,b]$. Absurde !
```


```{exercise}
:label: exo-260
Trouver les fonctions deux fois dérivables de $\R$ dans $\R$ vérifiant $\forall x \in \R$,
\begin{equation*}
 f''(x)-10f'(x)+29f(x) = 0
\end{equation*}
```

```{solution} exo-260
:class: dropdown
Le discrimant du polynôme caractéristique vaut $-16$. Les racines du polynôme sont donc $\lambda_1 = 5-2i$ et $\lambda_2 = 5+2i$. Les solutions de l'équation
sont donc
```


```{exercise}
:label: exo-261
Considérons l'équation différentielle $y'' + y = P$ où $P$ est un polynôme. Montrer que cette équation admet une unique solution polynômiale et expliciter cette solution. En déduire les solutions générales de l'équation.
```

```{solution} exo-261
:class: dropdown
L'unicité vient de ce que $\phi : Q \rightarrow Q''+Q$ est injective. On vérifie que $x \mapsto \sum \limits_{k=0}^n (-1)^k P^{(2k)}(x)$ est solution. La solution générale s'obtient en ajoutant la forme générale d'une solution à l'équation homogène.

Plus de détails :
**Unicité** Il s'agit de prouver l'injectivité de $\phi : Q \mapsto Q + Q''$. On peut par exemple remarquer que $\phi$ est un endormorphisme de l'espace des polynôme $\C[X]$, et qu'il suffit donc de regarder son noyau. Un argument sur le degré permet de conclure.
**Existence** On veut ici trouver une solution explicite $Q$ avec
\begin{align*}
Q + Q'' = P
\end{align*}
Une approche peut consister comme suit. On commence par $Q$ en fonction du reste. On écrit donc $Q = P - Q''$, et on cherche à se débarasser de $Q''$. En dérivant deux fois : $Q^{(2)} = P^{(2)} - Q^{(4)}$. Et on procède récursivement pour faire disparaître le terme en $Q^{(k)}$ à droite qui nous embête :
\begin{align*}
Q &= P - Q^{(2)} \\
&= P - P^{(2)} + Q^{(4)} \\
&= P - P^{(2)} + P^{(4)} - Q^{(6)} \\
& \ \, \vdots \\
\end{align*}
Cela fournit la solution explicitée plus haut.

```

```{exercise}
:label: exo-262
Résoudre l'équation différentielle $y'''-3y''+y'-3y = 0$
```

```{solution} exo-262
:class: dropdown
$z=y'-3y$ vérifie $z'' + z = 0$. De là $z= A\cos(t) + B \sin(t)$. On résoud pour $y$ à partir de là.
```

```{exercise}
:label: exo-263
Soit $y \in C^2(\R_+^*,\R)$ une solution de l'équation $(E) \; : \; x^2y''-y=x$. Montrer que $z=y(e^t)$ vérifie une certaine équation différentielle. En déduire la solution générale pour $(E)$.
```

```{solution} exo-263
:class: dropdown
$z' = e^ty'(e^t)$ puis
\begin{align*}
z'' &= e^{2t} y''(e^t) + e^ty'(e^t) \\
&= x^2y''(x) + z' \\
&= e^t + z + z'
\end{align*}
Et la résolution pour $z$ est classique.
```


```{exercise} lemme de Gronwall
:label: exo-264
Soit $f : \R_+ \rightarrow \R$ et $g : \R_+ \rightarrow \R_+$ continues et soit $A \geq 0$, tels que
\begin{equation*}
 \forall x \in \R_+^*, \quad f(x) \leq A + \int_0^x f(t)g(t)dt
\end{equation*}
Montrer que
\begin{equation*}
 \forall x \in \R_+^*, \quad f(x) \leq A\exp{\int_0^x g(t)dt}
\end{equation*}
```

```{solution} exo-264
:class: dropdown
On pose $F(t) = A + \int_0^x f(t)g(t)dt$. On a
\begin{align*}
\frac{f}{F} \leq 1 &\Rightarrow \frac{fg}{F} \leq g \\
&\Rightarrow \ln(F)' \leq g \\
&\Rightarrow \ln(F(x))-\ln(F(0)) \leq \int_0^x g(t)dt \\
&\Rightarrow F(x) \leq A\int_0^xg(t)dt \\
&\Rightarrow f \leq A\int_0^x g(t)dt
\end{align*}
```

```{exercise}
:label: exo-265
Soit $a,b \in \R \rightarrow \R$ continues et $(E) \; : \; y''= ay' + by$, et $y_0$ une solution non nulle de $(E)$.

1. Montrer que les zéros de $y_0$ sont isolés.
1. Montrer que les zéros de $y_0$ sont en nombre fini sur tout segment.
1. Soit $y_1$ une solution de $(E)$. Soit $x_0<x_1$ deux zéros de $y_0$. Montrer que si $y_1(x_0) = 0$, alors $y_0$ et $y_1$ sont liés, et sinon $y_1$ s'annule sur $]y_0, y_1[$.

```


```{exercise}
:label: exo-266
Résoudre l'équation fonctionnelle suivante d'inconnue une fonction $f$ dérivable.
\begin{equation*}
 \forall x,y \in \R, \quad f(x+y)=e^xf(y)+e^yf(x)
\end{equation*}
```

```{exercise}
:label: exo-267
Déterminer les fonctions $f : \R \rightarrow \R$ continues telles que $x \mapsto f(x) - \int_0^x tf(t) \; dt$ est constante.
```



































































































 