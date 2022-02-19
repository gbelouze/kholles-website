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

# Taylor-Young

```{exercise}
:label: exo-198
Soit $f : \R \rightarrow \R$ une fonction $\mathcal{C}^{\infty}$ et $\lambda > 0$ telles que $\forall n$
\begin{align*}
f^{(n)}(0) &= 0 \\
||f^{(n)}||_{\infty} &\leq  \lambda^n n!
\end{align*}
Montrer que $f$ est nulle.
```

```{exercise}
:label: exo-199
Soit $f : \R^+ \rightarrow \R$ de classe $\C^{\infty}$ telle que $f(0) = \lim_{\infty} f = 0$. Montrer qu'il y a une suite $(a_n)$ strictement croissante telle que $f^{(n)}(a_n) = 0$ pour tout $n$.
```

```{solution} exo-199
:class: dropdown
Par récurrence sur $n$, l'initialisation étant acquise avec $a_0=0$. Supposons donc donnés $a_0 < a_1 < \ldots < a_n$ tels que $f^{(k)}(a_k) = 0$, et par l'absurde que $f^{(n+1)}$ ne s'annule pas sur $[a_n, +\infty[$, par exemple est positive (quitte à remplacer $f$ par $-f$). Choisissons $a>a_n$, ainsi $f^{(n)}$ est strictement croissante sur $[a, +\infty[$. On écrit 
\begin{equation*}
f(a + x) - \sum_{k=0}^{n-1} \frac{f^{(k)}(a)x^n}{n!} = \frac{f^{(n)}(c_x)x^{n}}{n!}
\end{equation*}
 et puisque $f \underset{x \rightarrow+\infty}{\rightarrow} 0$, il vient $f(c_x) \underset{x \rightarrow +\infty}{\rightarrow} 0$ ce qui est impossible, car $f^{(n)}$ est globalement minoré sur $[a, +\infty[$ par $f^{(n)}(a) > 0$.
```

```{exercise}
:label: exo-200
Soit $f : \R \rightarrow \R$ un application $\mathcal{C}^{\infty}$. On note
\begin{equation*}
 M_k = || f^{(k)} ||_{\infty}
\end{equation*}

1.
    On suppose $M_0$ et $M_2$ finis. Montrer
    \begin{equation*}
    M_1 \leq \sqrt{2M_1M_2}
    \end{equation*}
2. 
    On suppose $M_0$ et $M_n$ finis. Montrer
    \begin{equation*}
     \forall k \in [\![0, n]\!], M_k \leq 2^{k(n-k)/2} M_0^{1-k/n}M_n^{k/n}
    \end{equation*}
3. 
    La constante $\sqrt{2}$ est-elle optimale ?

```

```{solution} exo-200
:class: dropdown

1.
    On écrit classiquement
    \begin{align*}
    f(x + h) &= f(x) + f'(x)h + f''(x)\frac{h^2}{2} \\
    f'(x) &= \frac{f(x+h)-f(x)}{h} + \frac{f''(x)h}{2}\\
    &\leq \frac{2M_0}{h} + \frac{M_2 h}{2}
    \end{align*}
    La borne est minimisée en $h = \sqrt{2\frac{M_0}{M_2}}$, et vaut $2\sqrt{M_0M_2}$. C'est bien mais ce n'est pas suffisant. On utilise la fameuse idée de la pseudo dérivée seconde en regardant à gauche et à droite de $x$
    \begin{align*}
    f(x + h) &= f(x) + f'(x)h + f''(c_1)\frac{h^2}{2} \\
    f(x - h) &= f(x) + f'(x)h + f''(c_2)\frac{h^2}{2} \\
    \frac{f(x + h) - f(x-h)}{2} &= f'(x)h + \frac{f''(c_1)+f''(c_2)}{2}\frac{h^2}{2} \\
    |f'(x)| &\leq \frac{M_0}{h} + \frac{M_2 h}{2}
    \end{align*}
    Et c'est gagné.
2. 
    Par récurrence, mais c'est pas facile.
3. 
    La réponse est oui. On va chercher à maximiser $M_1$ pour $M_0$ et $M_2$ fixés. S'il n'y pas la contrainte de $M_2$, on fait bouger $f'$ très vite (un pic d'intégrale petite) pour atteindre des grandes valeurs tout en contraignant $f$. Avec $M_2$ on contrôle la vitesse de variation de $f'$, mais on a donc tout intérêt à pousser les contraintes au maximum, c'est-à-dire de prendre $f''$ en créneau égale à $M_2$ puis $-M_2$. On fait le calcul et ça marche. Mais la fonction n'est que $\mathcal{C}_1$ donc on smooth $f''$ de plus en plus proche de la fonction en créneau. In fine on se rapproche de $\sqrt{2}$ arbitrairement proche.

```

```{exercise}
:label: exo-201
Soit $f:[0,1]\rightarrow \R$ de classe $\mathcal{C}^2$ vérifiant $f(0)=f'(0)=f'(1)=0$ et $f(1)=1$. Montrer qu'il existe $c\in[0,1]$ tel que $|f''(c)|\geq 4.$. La constante $4$ est elle optimale ?
```

```{solution} exo-201
:class: dropdown
On regarde ce qu'il se passe en $\frac{1}{2}$, en écrivant
\begin{align*}
f(1/2)  = f(0 + 1/2) &= f(0) + 1/2f'(0) + \frac{f''(c_1)}{8} \\
f(1/2)  = f(1 - 1/2) &= f(1) - 1/2f'(1) + \frac{f''(c_2)}{8} \\
\end{align*}
Et on conclut en considérant la première formule si $f(1/2) > 1/2$, la deuxième sinon.

La constante est optimale, pour cela on prend deux bouts de parabole entre $0$ et $1/2$ puis entre $1/2$ et $1$ (la dérivée seconde est un créneau valant $4$ puis $-4$).
```


































































 