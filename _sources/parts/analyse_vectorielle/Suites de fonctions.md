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

# Suites de fonctions

```{exercise}
:label: exo-407
Déterminer les $\alpha$ tels que $f_n(x)= n^{\alpha}\cos^n(x)\sin(x)$ converge uniformément sur $[0;\frac{\pi}{2}]$.
```

```{solution} exo-407
:class: dropdown
Il y a convergence en $0$ vers $0$. Puis $\forall x \in ]0;\frac{\pi}{2}], \;|\cos(x)| < 1$ donc $f_n(x) \rightarrow 0$. Bref il y a CVS vers $0$. Puis on calcule
\begin{align*}
f'_n(x) &= n^{\alpha}(-n\cos^{n-1}(x)\sin^2(x)+\cos^{n+1}(x)) \\
&= n^{\alpha}\cos^{n-1}(x)(-n+(n+1)\cos^2(x))\\
\end{align*}

s'annule en $x_n = \arctan{\frac{1}{\sqrt{n}}}$. où $f_n$ est maximum. En inégrant le développement limité du DL de $\arctan$ on trouve
\begin{equation*}
 \arctan(x) \underset{0}{=} x + O(x^3)
\end{equation*}
D'où
\begin{align*}
f_n(x_n) &= \left (\frac{1}{\sqrt{n}}+O(\frac{1}{n^{3/2}}) \right )(1-\frac{x_n^2}{2}+O(x_n^4))^nn^{\alpha} \\
&\sim \frac{e^{-1/2}}{\sqrt{n}}n^{\alpha}
\end{align*}
Et ainsi $\sup f_n \rightarrow 0$ si et seulement si $\alpha < \frac{1}{2}$.
```


```{exercise} Une limite classique
:label: exo-408
Soit $f_n(x) = \frac{x^n}{n!}e^{-x}$ sur $\R^+$. Déterminer le mode de convergence de $f$.
```

```{solution} exo-408
:class: dropdown
Après dérivation, $f_n$ admet son maximum en $n$ et $f_n(n) = \frac{n^n}{n!}e^{-n}$. Avec Stirling $f_n(n)\rightarrow 0 = f_{+\infty}$. Il y a bien CVU.
```


```{exercise}
:label: exo-409
Soit $f_n$ une famille de fonction de $X$ un ensemble vers $\R$, toutes bornées et telles que $(f_n)$ converge uniformément vers $f:X\rightarrow \R$.

1. Montrer que $f$ est bornée.
1. Montrer que $\sup_X f_n \rightarrow \sup_X f$.

```

```{solution} exo-409
:class: dropdown

1. Immédiat
1. On prend $n_{\varepsilon}$ tel que $\forall n \geq n_{\varepsilon}, \; ||f-f_n||_{\infty} < \varepsilon$.

```

```{exercise}
:label: exo-410
Déterminer l'adhérence de $\mathcal{C}_C(\R,\C)$ fonctions continues à support compact dans $(\mathcal{C}(\R,\C), ||.||_{\infty}$ espace des fonctions continues. Autrement dit trouver l'ensemble des fonctions continues $f$ telle qu'il existe une suite $(f_n)$ stationnaires à $0$ en $\infty$ qui converge uniformément vers $f$.
```

```{solution} exo-410
:class: dropdown
On montre que ce sont les fonctions nulles en $\infty$.

Si $(f_n) \in (\mathcal{C}_C(\R,\C))^{\N}$ CVU vers $f$, alors en choisissant $f_n$ proche de $f$ à $\varepsilon$ près, il vient que $|f|$ est plus petite que $\varepsilon$ en $\infty$.

Si $f \rightarrow 0$ en $\infty$, alors on prend $f_n$ égale à $f$ sur $[-n,n]$ puis qui "descend être stationnaire en $0$". Il vient $||f-f_n||< 2 \underset{|x|\geq n}{\sup} |f|$ et le membre gauche tend vers $0$ quand $n$ tend vers $+\infty$.
```


\end{document}