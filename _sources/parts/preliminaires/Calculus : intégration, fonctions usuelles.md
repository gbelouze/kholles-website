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

# Calculus : intégration, fonctions usuelles


```{exercise}
:label: exo-1
\begin{equation*}
 I = \int_0^1 \frac{xdx}{1+\sqrt{x}}
\end{equation*}
```

```{exercise}
:label: exo-2
\begin{equation*}
 I = \int_0^{\pi/3} \frac{\sin^3(x)dx}{\sqrt{\cos(x)}}
\end{equation*}
```

```{exercise}
:label: exo-3
\begin{equation*}
 I = \int_0^1 \frac{e^{2x}dx}{\sqrt{e^x+1}}
\end{equation*}
```



```{exercise}
:label: exo-4
Soit $f$ une application continue périodique de $\R$ dans $\R$. Trouver une condition nécessaire et suffisante pour que les primitives de $f$ soient périodiques.
```
```{solution} exo-4
:class: dropdown
$f$ est $T$-périodique. Soit $\lambda = \int_0^T f$. On a $F(x+nT) = F(x) + n\lambda$. Si $\lambda \neq 0$, $F$ est non bornée, continue, donc non périodique. Réciproquement, si $\lambda = 0$, $F$ est $T$-périodique.
```



```{exercise} Wallis
:label: exo-5
Calculer $W_n = \int_0^{\pi/2} cos^n(x) dx$.
```

```{solution} exo-5
:class: dropdown
\begin{align*}
\int_0^{\pi/2}cos^{n+2}(x) dx &= W_n - \int_0^{\pi/2} cos^n(x)sin^2(x) dx \\
&= W_n + \frac{1}{n+1} \left ( [cos_{n+1}sin]_0^{\pi/2} - \int_0^{\pi/2} cos_{n+2}(x)dx \right ) \\
W_{n+2} &= \frac{n+1}{n+2}W_n
\end{align*}
Leading to
 \begin{align*}
W_{2n} &= \frac{1\times3\times\ldots\times(2n-1)}{2\times4\times\ldots\times2n}W_0 \\
&= \frac{(2n)!}{4^n(n!)^2}W_0 \\
&= \frac{(2n)!}{4^n(n!)^2} \frac{\pi}{2}
\end{align*}
et
\begin{align*}
W_{2n+1} &= \frac{2\times4\times\ldots\times2n}{3\times5\times\ldots\times(2n+1)}W_1 \\
&= \frac{4^n(n!)^2}{(2n+1)!}\\
\end{align*}
```



```{exercise}
:label: exo-6
Montrer qu'une fonction $f: \mathbb{R} \rightarrow \mathbb{R}$ se décompose de façon unique comme somme d'une fonction paire et d'une fonction impaire.
```

```{solution} exo-6
:class: dropdown
$f(x) = \frac{f(x)+f(-x)}{2} +  \frac{f(x)-f(-x)}{2}$ pour l'existence. $f = p + i$ donne $f(x)+f(-x) = p(x) + p(-x) = 2p(x)$ pour l'unicité.
```



```{exercise}
:label: exo-7
On se donne $a \in ]0, 2 \pi [$. Calculer $\prod \limits_{k=0}^n \cos(\frac{a}{2^k})$.
```

```{solution} exo-7
:class: dropdown
On part de $\sin(2a) = 2\sin(a)\cos(a)$ pour avoir
\begin{equation*}
 \sin(2^na) = 2^n\sin(a)\prod_{k=0}^{n-1}\cos(2^ka)
\end{equation*}
D'où $\prod \limits_{k=0}^n \cos(\frac{a}{2^k}) = \frac{sin(2^na)}{2^n}$.
```



```{exercise}
:label: exo-8
Montrer que dans un triangle ABC, $\frac{\sin{\hat{a}}}{a}=\frac{\sin{\hat{b}}}{b}=\frac{\sin{\hat{c}}}{c}$.
```

```{solution} exo-8
:class: dropdown
On projette $C$ pour avoir un segment de longueur $h$ vérifiant $\sin(a) = \frac{h}{b}$ et $\sin(b) = \frac{h}{a}$ d'où le résultat.
```



```{exercise}
:label: exo-9
Résoudre dans $\mathbb{R}$ l'équation
\begin{equation*}
 \arctan(x) + \arctan(2x) = \frac{\pi}{4}
\end{equation*}
```

```{solution} exo-9
:class: dropdown
En prenant la tangente on a
\begin{align*}
\frac{\tan(\arctan(x)) + \tan(\arctan(2x))}{1-\tan(\arctan(x))\tan(\arctan(2x))} &= 1 \\
\frac{3x}{1-2x^2} &= 1\\
2x^2+3x-1&=0 \\
x = \frac{-3\pm\sqrt{17}}{4}
\end{align*}
On note $x_1 = \frac{-3-\sqrt{17}}{4} < 0$ et $x_2 = \frac{-3+\sqrt{17}}{4} > 0$.  En remontant les implications, on a $\arctan(x_i) + \arctan(2x_i) = \frac{\pi}{4} \mod{\pi}$.

Remarquons que $\phi : x \mapsto \arctan(x) + \arctan(2x)$ est négative sur $\R_-$, positive sur $\R_+$, et comprise entre $-\pi$ et $\pi$. Ainsi $\phi(x_1) < 0$ donc $x_1$ n'est pas solution de l'équation initiale. D'autre part, $\phi(x_2) \in [0, \pi]$. La seule valeur possible est $\phi(x_2) = \pi/4$. $\frac{-3+\sqrt{17}}{4}$ est l'unique solution de l'équation.
```



```{exercise} Formule de Machin
:label: exo-10
Montrer la formule
\begin{equation*}
 \frac{\pi}{4} = 4\arctan(\frac{1}{5})-\arctan(\frac{1}{239})
\end{equation*}
```

```{solution} exo-10
:class: dropdown
On passe par les complexes
\begin{align*}
Arg(\frac{(5+i)^4}{239+i}) &= Arg((5+i)^4(239-i)) \\
&= Arg((24+10i)^2(239-i)) \\
&= Arg((476 +480i)(239-i)) \\
&= Arg(114244 + 114244i) \\
&= Arg(1+i)\\
&= \frac{\pi}{4}
\end{align*}
```




```{exercise}
:label: exo-11
Donner le nombre de solutions de $\tan(x) + \tan(2x) +\tan(3x)+\tan(4x)=a$  dans $[0, \pi]$ selon $a\in\R$.
```

```{solution} exo-11
:class: dropdown
Les points limites sont $\frac{\pi}{2}, \frac{\pi/4}, \frac{3\pi}{4}, \frac{\pi}{6}, \frac{5\pi}{6}, \frac{\pi}{8}, \frac{3\pi}{8}, \frac{5\pi}{8}, \frac{7\pi}{8}$. Par ailleurs, $f(0)=f(\pi)=0$, $f$ est strictement croissante sur chaque intervalle de définition, bref l'équation possède $9$ solutions si $a \neq 0$ et $10$ si $a=0$
```



```{exercise}
:label: exo-12

1. Résoudre pour $x \in [0,2\pi]$, l'équation $\cos(3x)=\sin(2x)$.
1. En déduire une expression des $\cos$ et $\sin$ de $\{ \frac{3\pi}{10}, \frac{\pi}{10}, \frac{\pi}{5} \}$.

```

```{solution} exo-12
:class: dropdown

1.
     \begin{align*}
    \cos(3x) = \sin(2x) &\Leftrightarrow \cos(3x) = \cos(\pi/2-2x) \\
    &\Leftrightarrow \begin{cases}
    3x = \pi/2-2x \mod{2\pi} \\
    3x = 2x - \pi/2 \mod{2\pi}
    \end{cases} \\
    &\Leftrightarrow \begin{cases}
    x = \pi/10 \mod{2\pi/5} \\
    x = 3\pi/2 \mod{2\pi}
    \end{cases} \\
    \end{align*}
    Les solutions dans $[0, 2\pi]$ sont $\frac{\pi}{10}, \frac{\pi}{2}, \frac{9\pi}{10}, \frac{13\pi}{10}, \frac{3\pi}{2}, \frac{17\pi}{10}$.
2.
    On commence par factoriser $\cos(3x)$
    \begin{align*}
    \cos(3x) &= \Re(e^{3ix}) \\
    &= \Re((\cos(x) + i\sin(x))^3) \\
    &= 4\cos^3(x)-3\cos(x)
    \end{align*}
    Ainsi $x_1 = \pi/10$ et $x_2 = 13\pi/10$ vérifient

    \begin{align*}
    4\cos^3(x)-3\cos(x) &= 2\cos(x)\sin(x)\\
    4 (1-\sin^2(x))-2\sin(x)-3 &= 0 \\
    \end{align*}
    Et de là $X_1 = \sin(\pi/10)$ et $X_2 = \sin(13\pi/10) = -\sin(3\pi/10)$ sont les 2 racines de $4X^2 + 2X -1$
    De là
    \begin{align*}
    \sin(\pi/10) &=  \frac{\sqrt{5}-1}{4}\\
    \sin(3\pi/10) &=  \frac{\sqrt{5}+1}{4}\\
    \end{align*}
    Et ensuite ça déroule.
```



```{exercise}
:label: exo-13
Montrer que $\arctan(\frac{1}{\sqrt{x}}) = \arcsin(\frac{1}{\sqrt{x+1}})$ pour $x >0$.
```

```{solution} exo-13
:class: dropdown
On passe à la tangente
\begin{align*}
\tan(\arcsin(\frac{1}{\sqrt{x+1}})) &= \frac{\sin(\arcsin(1/\sqrt{x+1}))}{\sqrt{(1-\sin^2(\arcsin(1/\sqrt{x+1})))}}\\ &= \frac{1/\sqrt{x+1}}{\sqrt{1-1/(x+1)}} \\
&= \frac{1}{\sqrt{x}} \\
&= \tan(\arctan(\frac{1}{\sqrt{x}}))
\end{align*}
```



```{exercise}
:label: exo-14
Montrer que $\frac{1}{\sh(x)} = \frac{1}{th(\frac{x}{2})} - \frac{1}{th(x)}$. En déduire une expression simple de $\sum \limits_{k=0}^n \frac{1}{\sh(2^kx)}$.
```



```{exercise}
:label: exo-15
Soit $\forall a,b,x \in \R_+^*$, $a<b$,
\begin{equation*}
0 < b e^{-ax}-a e^{-bx} < b-a
\end{equation*}
```

```{solution} exo-15
:class: dropdown
$be^{-ax} - ae^{-bx} > be^{-ax} - ae^{-ax} > 0$. De l'autre côté, on dérive $f'(x) = ab(e^{-bx}-e^{-ax}) < 0$ donc $f(x)<=f(0) = b-a$.
```



```{exercise}
:label: exo-16
Étudier la monotonie sur $\R_+^*$, pour $a,b$ réels, de $\frac{\ln(1+ax)}{\ln(1+bx)}$.
```

```{solution} exo-16
:class: dropdown
Sans perte de généralité, $a<b$. On dérive deux fois.
```



```{exercise}
:label: exo-17
Soit $n \in \N$. Trouver une primitive de $\frac{1}{x \ln(x) \ln(\ln(x)) \ldots \ln^{\circ n}(x)}$.
```

```{solution} exo-17
:class: dropdown
$ln^{\circ n}(x)$ par récurrence.
```



```{exercise}
:label: exo-18
Calculer $\int \limits_0^1 \frac{1}{(1+x^2)^2}dx$.
```



```{exercise}
:label: exo-19
Trouver une primitive de $\frac{1}{\sqrt{-x^2+x+1}}$.
```

```{solution} exo-19
:class: dropdown
\begin{align*}
\int^t \frac{1}{\sqrt{1+x-x^2}} dx &= \int^t \frac{1}{\frac{\sqrt{5}}{2}\sqrt{-(\frac{2(x-1/2)}{\sqrt{5}})^2+1} } dx \\
&= \int^{2(u-1/2)/\sqrt{5}} \frac{1}{\sqrt{1-u^2}}du \\
&= \arcsin(\frac{2u-1}{\sqrt{5}})
\end{align*}
```



```{exercise}
:label: exo-20
Calculer $I = \int \limits_0^{\frac{\pi}{2}} \ln (\sin (x)) dx$. On pourra introduire $J = \int \limits_0^{\frac{\pi}{2}} \ln (\cos (x)) dx$.
```


```{solution} exo-20
:class: dropdown
Par un changement de variable évident, $I=J$. Donc $2I = I+J = \int_0^{\frac{\pi}{2}} \ln(\sin(2x)/2)dx = -\ln(2)\frac{\pi}{2} + \frac{1}{2}\int_0^{\pi} \ln(\sin(x))dx = -\ln(2)\frac{\pi}{2} + I$ d'où 
\begin{equation*}
I = -\ln(2)\frac{\pi}{2}
\end{equation*}

```



```{exercise}
:label: exo-21
Soit $f : \R \rightarrow \R$, telle que le graphe de $f$ possède deux centres de symétrie distincts. Montrer que $f$ peut se décomposer comme somme d'une fonction affine et d'une fonction périodique.
```

```{solution} exo-21
:class: dropdown
Quitte à retirer la bonne fonction affine à $f$, on peut supposer que les deux centres de symétrie sont situés sur l'axe des $x$, respectivement en $a$ et en $b$. Soit $x \in \R$. On a
\begin{align*}
f(x) &= f(b-(b-x)) \\
&= f(2b-x) \\
&= f(a - (a-2b + x)) \\
&= f(x + 2(a-b) )
\end{align*}
Donc $f-\delta$ est $a-b$ périodique avec $\delta$ affine.
```



```{exercise}
:label: exo-22
Soit $a>b$ des réels. Déterminer une condition nécessaire et suffisante pour que le système
\begin{equation*}
\begin{cases}
    \ch(x) + \ch(y) = a \\
    \sh(x) + \sh(y) =b
\end{cases}
\end{equation*}
admette au moins une solution.
```



```{exercise}
:label: exo-23
Soit $f : \R \rightarrow \R$, on suppose que $f \circ f$ est croissante et que $f \circ f \circ f$ est strictement décroissante.

Montrer que f est strictement décroissante.
```

```{solution} exo-23
:class: dropdown
$f\circ f$ est strictement croissante, sinon $f \circ f \circ f$ n'est pas strictement décroissante.

Soit $a<b$, $f(f(f(a)))< f(f(f(b)))$ donc par croissance de $f\circ f$, $f(a) < f(b)$.
```



```{exercise}
:label: exo-24
Calculer exactement $\sin(\frac{1}{2} \arcsin(\frac{3}{4}))$.
```



```{exercise} formule de Hutton
:label: exo-25
Montrer la formule
\begin{equation*}
\frac{\pi}{4} = 2 \arctan(\frac{1}{3})+\arctan(\frac{1}{7})
\end{equation*}
```

```{solution} exo-25
:class: dropdown
Par les complexes ou bien avec les formules de trigonométrie.
```





































































 