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

# Convexité, inégalité arithmético-géométrique

```{exercise}
:label: exo-268
Soit $a_1, a_2, \ldots, a_n$ des réels positifs tels que $\prod a_i = 1$. Montrer que
\begin{equation*}
 \prod_{i=1}^{n}(2+a_i) \geq 3^n
\end{equation*}
et donner le cas d'égalité.
```

```{solution} exo-268
:class: dropdown
$a_1 =a_2 = \ldots = a_n = 1$ est un cas d'égalité. Cela conduit à utiliser l'inégalité arithmético-géométrique avec $1, 1, a_i$ ce qui donne $\frac{2+a_i}{3} \geq a_i^{\frac{1}{3}}$. De là suit l'inégalité. Le cas d'égalité est celui de l'IAG, donc uniquement pour les $a_i$ tous égaux à 1.
```

```{exercise}
:label: exo-270
Soit $f : \R \rightarrow \R $ continue telle que $\forall x, y$,
\begin{equation*}
 f(\frac{x+y}{2}) \leq \frac{f(x)+f(y)}{2}
\end{equation*}
Montrer que $f$ est convexe.
```

```{solution} exo-270
:class: dropdown
Vrai pour tous les diadiques puis densité des diadiques.
```

```{exercise}
:label: exo-271
Soit $(x_1, \ldots, x_n)$ des réels strictement positifs

    1. Montrer que $\frac{x_1}{x_2} + \ldots + \frac{x_{n-1}}{x_n} + \frac{x_n}{x_1} \geq n$
    1. Montrer que $\sum_{i,j = 1}^n \frac{x_i}{x_j} \geq n^2$.

```


```{solution} exo-271
:class: dropdown

    1. Concavité de $\ln$ : $\ln(\frac{1}{n}\sum \frac{x_i}{x_{i+1}}) \geq \frac{1}{n} \sum \ln(\frac{x_i}{x_{i+1}}) =0$
    1. Cas $n=2$ de l'inégalité précédente pour toute paire $i,j$.

```

```{exercise}
:label: exo-272
Soit $f :[a,b] \rightarrow \R$ continue telle que
\begin{equation*}
 \forall x \in ]a,b[, \; \exists \varepsilon > 0, \; f(x) = \frac{1}{2}(f(x+\varepsilon)+f(x-\varepsilon))
\end{equation*}
Montrer que $f$ est convexe. En considérant $-f$, en déduire qu'elle est affine.
```

```{solution} exo-272
:class: dropdown
Notons $\Delta_x(y) = \frac{f(x)-f(y)}{x-y}$.
On raisonne par l'absurde et on suppose disposer de $u < v < w$ tels que $\Delta_u(v) > \Delta_u(w)$. On regarde alors $h : x \mapsto f(x)-f(u) -(x-u)\Delta_u(w)$ qui possède la même propriété que $f$ et de plus vérifie $h(u)=h(w)=0$ et $h(v)>0$. En considérant $y = \inf \{x \; | \; h(x) = \sup h \}$ on obtient une contradiction. Ensuite le même raisonnement appliqué à $-f$ montre que $f$ est concave. De là $f$ est à la fois convexe et concave, elle est donc affine.
```

```{exercise}
:label: exo-273
Soit $x_1, \ldots, x_n$ des réels strictement positifs. Pour $\alpha > 0$ on pose $M_{\alpha}(x_i) = (\frac{1}{n}\sum_ix_i^{\alpha})^{\frac{1}{\alpha}}$. Montrer que si $0 < \alpha < \beta$, alors $M_{\alpha} \leq M_{\beta}$. Déterminer $\lim_{\alpha \rightarrow 0} M_{\alpha}$ et $\lim_{\alpha \rightarrow +\infty} M_{\alpha}$
```

```{solution} exo-273
:class: dropdown

Tout d'abord $\alpha \leq 1 \leq \beta \Rightarrow M_{\alpha} \leq M_1 \leq M_{\beta}$. La première inégalité (resp. la deuxième) vient de ce que $x \mapsto x^{\gamma}$ est concave (resp. convexe) lorsque $\gamma \leq 1$ (resp. $\gamma \geq 1$).

Ensuite dans le cas général, on écrit
\begin{align*}
M_{\alpha}(x_1, \ldots, x_n) &= M_1(x_1^{\alpha}, \ldots, x_n^{\alpha})^{\frac{1}{\alpha}} \\
&\leq M_{\beta/\alpha}(x_1^{\alpha}, \ldots, x_n^{\alpha})^{\frac{\alpha}{\beta}\frac{1}{\alpha}} \\
&= M_{\beta}(x_1, \ldots, x_n)
\end{align*}

En factorisant par $\max(x_i)$, clairement $M_\alpha(x_i) \underset{\alpha \rightarrow + \infty}{\rightarrow} \max(x_i)$.
Pour la limite en $0$ on écrit $x_i = e^{t_i}$ et
\begin{align*}
M_\alpha(x_i) &= \left ( \frac{1}{n} \sum e^{t_i\alpha} \right )^{1/\alpha} \\
&= (1 - \alpha \frac{\sum t_i}{n} + o(\alpha))^{1/\alpha} \\
&= e^{\sum t_i / n + o(1)} \\
&\underset{\alpha \rightarrow 0}{\rightarrow} e^{M_1(\ln(x_i))}
\end{align*}

```

```{exercise}
:label: exo-274
Soit $f : \R \rightarrow ]0,+\infty[$. Montrer que $\ln(f)$ est convexe si et seulement si $\forall a > 0$, $f^a$ est convexe.
```

```{solution} exo-274
:class: dropdown
($\Rightarrow$) $\ln(f^a) = a\ln(f)$ est convexe. Or $\exp$ est convexe croissante donc $f^a = \exp(\ln(f^a))$ est convexe.

($\Leftarrow$) On a $f^a$ convexe $\Rightarrow$ $\forall b>a$ $f^b$ convexe. Toute l'information de l'hypothèse se trouve donc pour $a$ petit, d'où l'idée de faire tendre $a$ vers $0$. Fixons $x, y, \lambda$. Notons $X = \ln(f(x))$, $Y=\ln(f(y))$ et $ Z = \ln(f(\lambda x + (1-\lambda) y))$. On exprime la convexité de $f^a$ :
\begin{equation*}
\forall a > 0, \quad e^{aZ} \leq \lambda e^{aX} + (1-\lambda)e^{aY}
\end{equation*}
De là $\phi : a \mapsto \lambda e^{aX} + (1-\lambda)e^{aY} - e^{aZ} $ est positive sur $\R^*+$. Mais $\frac{\phi(a)}{a} \underset{a \rightarrow 0}{\rightarrow} \lambda X + (1-\lambda) Y - Z$. D'où finalement $\lambda X + (1-\lambda) Y - Z \geq 0$, ce qui est la condition souhaitée.
```

```{exercise}
:label: exo-275
Montrer que pour tout $x > 1$, on a
\begin{equation*}
x^n-1 \geq n(x^{\frac{n+1}{2}}-x^{\frac{n-1}{2}})
\end{equation*}
```

```{solution} exo-275
:class: dropdown
On factorise par $x-1$ : on veut donc montrer
\begin{equation*}
 \sum_{k=0}^{n-1}x^k \geq nx^{\frac{n-1}{2}}
\end{equation*}
On utilise la convexité de $y \mapsto \exp(y\ln(x))$ et on écrit
\begin{align*}
\frac{1}{n}\sum_{k=0}^{n-1}x^k
&= \sum_{k=0}^{n-1}\frac{1}{n}e^{k\ln(x)} \\
&\geq  \exp(\ln(x)(\frac{1}{n}\sum_{i=0}^{n-1}i))\\
&\geq x^{\frac{n-1}{2}}
\end{align*}
```

```{exercise}
:label: exo-276
(Éventuellement la première question peut juste servir d'indication)
Soit $f:\R\rightarrow\R$ convexe.

    1. On suppose que $\lim_{+\infty}f = 0$, montrer que $f$ est positive.
    1. On suppose que $f$ admet une asymptote. Montrer que la courbe est toujours au dessus de l'asymptote.

```

```{solution} exo-276
:class: dropdown

1. Sinon on peut trouver $x,y$ tels que $\Delta_x(y) > 0$.
1. On regarde la différence de $f$ et de son asymptote, qui reste convexe et on utilise la question 1.

```

```{exercise}
:label: exo-277
Soit $f:\R\rightarrow\R$ convexe. Montrer que $\frac{f(x)}{x}$ admet une limite dans $\R \bigcup \{+\infty\}$ lorsque $x$ tend vers $+\infty$.
```

```{solution} exo-277
:class: dropdown
Par croissance des cordes, on a $\frac{f(x)-f(0)}{x}$ croissante. Cela conclut.
```

```{exercise}
:label: exo-278
Soit $f : \R^+ \rightarrow \R$ positive, bornée, de classe $\mathbb{C}^2$ telle que $f \leq f''$.

    1. Montrer que $f$ est convexe et décroissante.
    1. Montrer que $f$ et $f'$ tendent vers 0 en $+\infty$.
    1. Soit $g$ et $h$ définies par $g(x)=f(x)e^{x}$ et $h(x)=(f'(x)+f(x))e^{-x}$ pour $x\geq 0$. Étudier les variations de $g$ et le signe de $h$.
    1. En déduire que pour $x \geq 0$, on a $f(x) \leq f(0)e^{-x}$.

```

```{solution} exo-278
:class: dropdown

    1. La convexité vient de ce que $f'' \geq 0$. $f'$ est croissante. Si elle n'est pas tout le temps négative, $f$ diverge en $+\infty$.
    1. $f$ et $f'$ convergent par monotonie. Donc $f'$ converge vers $0$ (sinon $f$ ne converge pas). Puis si $f$ converge vers une limite strictement positive, $f''$ reste grande et donc $f'$ diverge.
    1. On a $h' = (f''-f)e^{-x} \geq 0$. Donc $h$ est croissante et $h \underset{+\infty}{\rightarrow} 0$, donc $h$ est toujours négative. Il suit que $g$ est décroissante.
    1. Immédiat

```

```{exercise}
:label: exo-279
Montrer que pour tout $a,b,x,y > 0$, on a
\begin{equation*}
 x\ln{\frac{x}{a}}+y\ln{\frac{y}{b}} \geq (x+y)\ln{\frac{x+y}{a+b}}
\end{equation*}
```

```{solution} exo-279
:class: dropdown
$f : x \mapsto x\ln{x}$ est convexe d'où
\begin{equation*}
 f(\frac{a}{a+b}\frac{x}{a}+\frac{b}{a+b}\frac{y}{b}) \leq \frac{a}{a+b}f(\frac{x}{a}) + \frac{b}{a+b}f(\frac{y}{b})
\end{equation*}
```

```{exercise}
:label: exo-280
Montrer qu'une fonction sur un intervalle ouvert est convexe si et seulement si elle s'écrit comme le $\sup$ d'une famille de fonctions affines.
```

```{solution} exo-280
:class: dropdown
Soit $f$ définie sur $I$ affine. Par croissance des pentes il existe pour tout $y \in I$, $\underset{x \rightarrow x^-}{\lim} \frac{f(y)-f(x)}{y-x}$, que l'on note $a(y)$. On note $f_y : x \rightarrow f(y)+a(y)(x-y)$ (la tangente à gauche). On a $f = \sup_{y \in I} f_y$.
Réciproquement, on montre qu'un tel $\sup$ est convexe.
```











































































 