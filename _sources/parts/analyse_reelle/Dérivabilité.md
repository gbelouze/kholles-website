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

# Dérivabilité


```{exercise}
:label: exo-176
Soit $f \; : \; \mathbb{R} \longrightarrow \mathbb{R}$ dérivable et $a \in \mathbb{R}$. Déterminer $\underset{x \longrightarrow a}{\lim}\frac{xf(a)-af(x)}{x-a}$.
```

```{solution} exo-176
:class: dropdown
\begin{align*}
\frac{xf(a)-af(x)}{x-a} &= \frac{(a+x-a)f(a)-af(x)}{x-a}  \\
&= a\frac{f(a)-f(x)}{x-a} + f(a) \\
&\longrightarrow f(a)-af'(a) \\
\end{align*}
```


```{exercise}
:label: exo-178
Montrer que la fonction
\begin{equation*}
f : x \mapsto
\begin{cases}
0 \textrm{ si $x\leq 0$} \\
e^{-\frac{1}{x}} \textrm{ sinon}
\end{cases}
\end{equation*}
est $\mathbb{C}^{\infty}$ et à dérivées en $0$ nulles.
\begin{remarque}
La fonction précédente est un bon contre-exemple à plusieurs fausses propriétés :

- Son développement de Taylor en $0$ à tout ordre est nul mais elle n'est pas nulle sur un voisinage de $0$.
- Elle est $\mathcal{C}^{\infty}$ et nulle sur un intervalle mais pas nulle partout.
\end{remarque}
```

```{solution} exo-178
:class: dropdown
Par récurrence, il existes des polynômes $P_n$ et $Q_n$ tels que
\begin{equation*}
 f^{(n)} = \frac{P_n}{Q_n} e^{-\frac{1}{x}}
\end{equation*}
```


```{exercise}
:label: exo-179
Soit $f$ dérivable de $[a,b]$ dans $\R$, et telle que $f(a)=f(b)=0$, et soit $X=(x,0)$ un point de l'axe des abscisses hors le segment $[a,b]$. Montrer qu'il existe une tangente à la courbe de $f$ qui passe par $X$.
```

```{solution} exo-179
:class: dropdown
Graphiquement, on voit qu'il faut maximiser (ou minimiser selon la position de $c$ et le signe de $f$) $\mu(c) = \frac{f(c)}{c-x}$. Soit donc $c \in [a,b]$ qui maximise (ou minimise...) $\mu$. En dérivant $\mu$ il vient $f'(c) = \frac{f(c)}{c-x}$, d'où le résultat.
```

```{exercise}
:label: exo-180
Soit $P$ un polynôme de degré $n$, montrer que l'équation $P(x)=e^x$ admet au plus $n+1$ solutions.

*Variante* Soit $P$ un polynôme de degré $n$, montrer que l'équation $P(x) = \ln(x)$ admet au plus $n+1$ solution sur $\R_+^*$.
```

```{solution} exo-180
:class: dropdown
Par récurrence en utilisant Rolle. Pour la variante, on peut se ramener à un segment avant la récurrence.
```

```{exercise}
:label: exo-181
Soit $f$ de $\R$ dans $\R$ vérifiant $f^2+(1+f')^2 \leq 1$. Montrer que $f$ est nulle.
```

```{solution} exo-181
:class: dropdown
Nécessairement $f' \leq 0$ donc $f$ est décroissante. Puis par l'absurde si $f$ est non nulle en $a$, et par disjonction de cas sur le signe de $f(a)$, soit $f$ tend vers $+\infty$ en $-\infty$, soit $f$ tend vers $-\infty$ en $+ \infty$, d'où la contradiction.
```

```{exercise}
:label: exo-182
Soit $f$ $\mathcal{C}^{\infty}$ et $P$ un polynôme de degré impair tels que
$\forall x \in \R, \forall n \in \N$,
\begin{equation*}
 |f^{(n)}(c)| \leq |P(x)|
\end{equation*}
Montrer que $f$ est nulle.
```

```{solution} exo-182
:class: dropdown
$P$ s'annule, par exemple en $0$. Alors toutes les dérivées de $f$ en $0$ sont nulles.

Avec égalité de Taylor-Lagrange, la conclusion vient tout de suite (pour tout $x$, pour tout $n$ il existe $c$ entre $0$ et $x$ tel que $f(x) = \frac{x^{n+1}}{(n+1)!} f^{(n+1)}(c)$ qui tend vers $0$ quand $n$ tend vers l'infini).

Sinon l'inégalité suffit aussi.
```

```{exercise}
:label: exo-183
Soit $f \in \mathcal{C}^2(\R, \R)$ telle que $f$ est bornée par $M_0$ et $f''$ est bornée par $M_2$. Montrer que $f'$ est bornée par $2\sqrt{M_0M_2}$.
```

```{solution} exo-183
:class: dropdown
On a $f(x+h)=f(x) + hf'(x)+\frac{h^2}{2}f''(c)$ pour un certain $c$, ce qui amène $|f'| \leq \frac{2M_0}{h} + \frac{hM_2}{2}$. On prend le minimum du membre de droite pour $h$.
```



```{exercise}
:label: exo-184
Soit $f:[-1,1] \rightarrow \R$ $\mathcal{C}^1$, deux fois dérivable sur $]-1,1[$, telle que $f(-1)=-1$, $f(0)=0$ et $f(1)=1$. Montrer qu'il existe $c \in ]-1,1[$ tel que $f(c)=0$.
```

```{solution} exo-184
:class: dropdown
Rolle appliqué à $\phi(x)=f(x)-x$ fournit $a<0<b$ tels que $\phi(a)=\phi(b)=0$. D'où $f'(a)=f'(b)$ puis l'existence du $c$ recherché.
```

```{exercise}
:label: exo-185
Soit $f$ dérivable telle que $f(0)=0$. Montrer que $S(n)=\sum_{k=1}^n f(\frac{k}{n^2})$ admet une limite quand $n \rightarrow + \infty$ et la déterminer.
```

```{solution} exo-185
:class: dropdown
On écrit $f(x) = xf'(0) + o(x)$. En fixant $N$ tel que le petit $o$ est plus petit que $\epsilon x$ lorsque $x \in [0,\frac{1}{N}]$, on a $\forall n \geq N$,
\begin{equation*}
 |S(n) - f'(0)\sum_{k=1}^n \frac{k}{n^2} | \leq \varepsilon \sum_{k=1}^n \frac{k}{n^2} \leq \frac{\varepsilon}{2}
\end{equation*}
Or
\begin{align*}
S(n) &= \sum_{k=1}^n \frac{k}{n^2} \\
&= \frac{1}{n^2} \frac{n(n+1)}{2} \\
\underset{n \rightarrow +\infty}{\longrightarrow} \frac{1}{2}
\end{align*}
Ainsi la limite de $S(n)$ existe et vaut $\frac{f'(0)}{2}$.
```

```{exercise}
:label: exo-186
Soit $f$ définie sur un intervalle ouvert contenant $0$, continue sur $I$. On suppose que $\exists \underset{x \rightarrow 0}{\lim} \frac{f(2x)-f(x)}{x} = 0$. Montrer que $f$ est dérivable en $0$.
```

```{solution} exo-186
:class: dropdown
Soit $\varepsilon > 0$, pour $x$ suffisamment petit, on a $\forall n$, $|f(\frac{x}{2^n})-f(\frac{x}{2^{n+1}})| \leq \varepsilon |\frac{x}{2^{n+1}}|$. De là $|f(x)-f(\frac{x}{2^{n}})| \leq \varepsilon x $ puis $|f(x)-f(0)| \leq \varepsilon x$. Il vient que $\exists f'(0)=0$.
```


```{exercise}
:label: exo-187
Soit $f = \R_+ \rightarrow \R$ une fonction continue, dérivable sur $\R_+^*$ telle que $f(0)= \lim_{+\infty} f = 0$. Montrer qu'il existe $c \in \R_+^*$ tel que $f'(c)=0$.
```

```{solution} exo-187
:class: dropdown
Si $f$ est identiquement nulle c'est bon. Sinon soit $c \in \R_+^*$ tel que $f(x) \neq 0$, par exemple $f(c)>0$. Alors par le TVI, il existe $a<c<b$ tels que $f(a)=f(b)=\frac{f(c)}{2}$. Par Rolle, $f'$ s'annule entre $a$ et $b$.
```

```{exercise}
:label: exo-188
Quelle est la nature de la suite $u_n=\sin(\ln(n))$ ?
```

```{solution} exo-188
:class: dropdown
On montre qu'on peut extraire deux sous-suite convergente vers deux valeurs différents. Soit $x_k = \exp(k\pi)$, $y_k = \exp(k\pi + \frac{\pi}{2})$, $n_k = \lceil x_k \rceil$ et $m_k = \lceil y_k \rceil$. Avec l'inégalité des accroissements finis, on a
\begin{equation*}
 |\ln(x_k)-\ln(n_k)| \leq \frac{|n_k-x_k|}{|x_k|} \leq \exp{-k\pi}
\end{equation*}
Puis une deuxième application du IAF :
\begin{equation*}
 |\sin(\ln(x_k))-\sin(\ln(n_k))| \leq |\ln(x_k)-\ln(n_k) | \leq \exp{-k\pi}
\end{equation*}
Ainsi les $u_{n_k}$ converge vers $0$. De même $u_{m_k}$ converge vers $1$. Ainsi $u_n$ ne converge pas.
```

```{exercise}
:label: exo-189
Voir exercice 30 à la page \url{http://www.bibmath.net/ressources/index.php?action=affiche&quoi=bde/analyse/unevariable/derivee&type=fexo}
```


```{exercise}
:label: exo-190
Soit $f : \R \rightarrow \R$ de classe $\C^{\infty}$ et bornée.

1. Pour $k \geq 2$, on suppose que $f^{(k)}$ s'annule un nombre fini de fois. Montrer alors que pour tout $1 \leq p < k$, $f^{(p)}$ tend vers $0$ en $\pm \infty$.
1. En déduire que $f^{(k)}$ s'annule au moins $k-1$ fois.

```

```{solution} exo-190
:class: dropdown
La propriété suivante se montre par récurrence. Soit $k \geq 1$ tel qu'il existe $\varepsilon > 0$ et $A$ tel que $x > A \Rightarrow |f^{(k)}(x)| > \varepsilon$. Alors pour tout $h \geq 0$, $|f(A+h)| \geq \varepsilon h^k + P(h)$ avec $P$ un polynôme de degré inférieur ou égal à $k-1$.

En particulier, aucune dérivée de $f$ ne vérifie l'hypothèse de la propriété, sans quoi $f$ ne serait pas bornée en $+\infty$.

Pour $k\geq 2$, si $f^{(k)}$ s'annule un nombre fini de fois, alors $f^{(k-1)}$ est monotone en $+\infty$. D'après la remarque précédente, $f^{(k-1)}$ ne peut diverger en $+\infty$, donc est bornée (en $+\infty$), donc converge. Encore une fois d'après la remarque précédente, la limite doit être $0$. Puisque $f^{(k-1)}$ est monotone en $+\infty$ et converge vers $0$, elle est de signe constant en $+\infty$. On montre donc récursivement que $f^{(p)}$ tend vers $0$ en $+\infty$ pour tout $1 \leq p <k$.

Puis on effectue des Rolle successifs. On utilise les zéros en $\pm \infty$ donc il s'agit de Rolle généralisé.
```

```{exercise}
:label: exo-191
Soit $f : \R\rightarrow\R$ dérivable, et $a \in \R$ tel que $f'(a) \neq 0$.

1. Montrer qu'il existe un voisinage $V$ de $a$ tel que $\forall x \in V \setminus \{a\}$, $f(x) \neq f(a)$.
1. Si $f'$ est continue en $a$, montrer qu'il existe un voisinage $V$de $a$ tel que $f_{|V}$ soit injective. Et si $f'$ n'est pas continue en $a$ ?

```
```{solution} exo-191
:class: dropdown

1. Pour tout $\varepsilon > 0$, il existe un voisinage $V$ tel que $x \in V \setminus \{ a \} \Rightarrow |\frac{f(x)-f(a)}{x-a} - f'(a)| \leq \varepsilon $. Avec $\varepsilon = \frac{f'(a)}{2}$ on a $|f(x) - f(a)| \geq |\frac{f'(a)}{2}(x-a)| > 0$.
1. Si $f'$ est continue en $a$, $f'$ est de signe strictement constant sur un voisinage de $a$, donc $f$ y est strictement monotone donc injective. Un contre-exemple est fourni par $x \mapsto x^2\sin(\frac{1}{x}) + \alpha x$ en $0$ pour n'importe quel $|\alpha| < 1$.

```

```{exercise}
:label: exo-192
Soit $f : \R\rightarrow\R$ dérivable. Montrer que $|f|$ admet en tout point une dérivée à droite et à gauche.
```
```{solution} exo-192
:class: dropdown
On regarde en $0$, le reste se fait pareil. Si $f(0) \neq 0$, $f$ est dérivable en $0$. Sinon $f(0) = 0$, et on regarde $f(x)/x$ pour $x > 0$ tendant vers $0$. S'il existe $a>0$ tel que $f$ est de signe constant sur $]0, a[$ c'est gagné, sinon $f'(a) = 0$ et c'est gagné.
```

```{exercise}
:label: exo-193
Soit $f : \R\rightarrow\R$ dérivable telle que $f' \underset{x \rightarrow + \infty}{\rightarrow} l$. Monter que $\frac{f(x)}{x} \underset{x \rightarrow + \infty}{\rightarrow} l$. Que dire de la réciproque ?
```

```{solution} exo-193
:class: dropdown
Soit $(x_n) \rightarrow +\infty$. Le TAF nous donne $\alpha_n \in [x_n, x_{n+1}]$ tel que $f(x_{n+1}) = f(x_n) + f'(\alpha_n)(x_{n+1} - x_n)$. On écrit alors
\begin{align*}
f(x_n) - f(x_0) &= \sum_{k=1}^n f(x_k) - f(x_{k-1})\\
&= \sum_{k=1}^n f'(\alpha_k)(x_k - x_{k-1})\\
&= \sum_{k=1}^n l(x_k - x_{k-1}) + \sum_{k=1}^n (f'(\alpha_k) - l)(x_k - x_{k-1})\\
&= l(x_n - x_0) + \sum_{k=1}^n o(x_k - x_{k-1})\\
&= l(x_n-x_0) + o(x_n)
\end{align*}
Et le résultat suit directement. Pour la réciproque, on regarde par exemple $x \mapsto x + \cos(e^x)$.
```

```{exercise} {$f'$ vérifie la propriété des valeurs intermédiaires}] \
:label: exo-194
Soit $f :[a,b] \rightarrow \R$ dérivable.

1. On suppose que $\forall x \in [a,b]$, $f'(x) \neq 0$. Montrer que $f'$ est de signe constant.
1. Dans le cas général, montrer que $f'([a,b])$ est un intervalle.

```

```{solution} exo-194
:class: dropdown

1. Si $f$ n'est pas injective, Rolle nous donne une dérivée nulle, donc $f$ est injective, continue donc monotone.
1. Soit $c < d$ et $\alpha \in [f(c), f(d)]$. La contraposée de la question précédente, appliquée à $f(x) - \alpha x$, fournit $\gamma$ tel que $f'(\gamma) - \alpha = 0$. Ainsi, $f'([a,b])$ est convexe, donc est un intervalle.

```


```{exercise}
:label: exo-195
Soit $f:[a,b] \rightarrow \R$ tel que $f'(a) = f'(b)$. Montrer qu'il existe $c \in ]a,b[$ tel que $f'(c) = \frac{f(c) - f(a)}{c-a}$.
```

```{solution} exo-195
:class: dropdown
Graphiquement, on voit qu'il faut maximiser $\phi : x \mapsto \frac{f(x) - f(a)}{x-a}$. Cette fonction est continue sur $]a,b]$, prolongeable par continuité en $a$ par $f'(a)$. $\phi$ est donc bornée et atteint sa borne $\sup$ en $c \in ]a,b[$ (les bornes sont correctement ouvertes car $\phi(a) = \phi(b)$). $\phi$ est dérivable sur $]a,b[$, de dérivée $\frac{(x-a)f'(x) - (f(x) - f(a))}{(x-a)^2}$. Or $\phi'(c) = 0$, ce qui donne exactement la condition recherchée.
```


```{exercise}
:label: exo-196
Soit $f : \R \rightarrow \R$ telle que $\forall a,b \in \R$, 
\begin{equation*}
 f(b) - f(a) = (b-a)f'(\frac{a+b}{2})
\end{equation*}

Montrer que $f$ est un polynôme de degré inférieur ou égal à $2$.
```

```{solution} exo-196
:class: dropdown
$f'(x) = \frac{f(x+1) - f(x-1)}{2}$ est dérivable, donc récursivement $f$ est $\mathcal{C}^{\infty}$. Ensuite on dérive l'expression de l'énoncé d'abord par rapport à $a$, puis par rapport à $b$.
```

```{exercise}
:label: exo-197
Soit $n\in \N$, $n \geq 2$, et $a,b \in \R$. Montrer que l'équation $x^n +ax + b = 0$ admet au plus 2 racines réelles distinctes si $n$ est pair, 3 si $n$ est impair.
```

```{solution} exo-197
:class: dropdown
Notons $P = X^n + aX +b$. $P''$ admet $0$ comme unique racine, donc par Rolle $P$ admet au plus $3$ racines distinctes. Si $P$ en admet $3$, elles sont de multiplicité $1$ (sinon $P'$ admet au mois $3$ racines et donc $P''$ au moins $2$), et $P$ ne peut pas tendre vers $+\infty$ en $\pm \infty$, donc $n$ est impair.
```







