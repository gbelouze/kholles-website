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

# Anneaux

```{exercise}
:label: exo-281
Soit $A,B$ deux anneaux commutatifs, et $f$ une application de $A$ vers $B$ qui préserve la somme, le carré et l'unité. On suppose de plus $2$ régulier dans $B$. Montrer que $f$ est un morphisme d'anneau. Trouver un contre-exemple si on ne suppose plus que $f$ préserve l'unité.
```

```{solution} exo-281
:class: dropdown
Il suffit de montrer quer $f$ préserve le produit. On prend $x,y \in A$. En écrivant $2xy = (x+y)^2-x^2-y^2$, on montre $2f(x)f(y) = 2f(xy)$ et on utilise la régularité de $2$. Pour le contre-exemple remarquons que $f(1)$ est toujours idempotent. Il faut donc se placer dans un anneau qui admet d'autre idempotent que $1$ et $0$, par exemple dans un anneau produit (prendre par exemple $\phi : A \rightarrow B$ un morphisme et $f:A\rightarrow B^2$ défini  par $f(a) = (\phi(a), 0)$).
```

```{exercise}
:label: exo-282
Soit $A$ un anneau commutatif. Montrer que $A$ possède un idempotent différent de $0$ et $1$ si et seulement si $A$ est isomorphe à un anneau produit $B\times C$ avec $B$ et $C$ des anneaux non nuls.
```

```{solution} exo-282
:class: dropdown
Le sens retour est trivial. Considérons $b$ différent de $0$ et de $1$ un idempotent de $A$, et notons $c = 1-b$. $c$ est également idempotent non trivial. Notons $B = Id(b)$ et $C = Id(c)$ et considérons le morphisme
\begin{align*}
\phi :
\begin{cases}
A &\rightarrow B \times C \\
x &\mapsto (bx, cx)
\end{cases}
\end{align*}
$\phi$ est clairement un morphisme et est bijectif de réciproque la somme. On peut munir $B$ et $C$ d'une structure d'anneau. Pour $B$ par exemple, il suffit de considérer que l'unité est $b$.
```

```{exercise}
:label: anneau-integre-fini
Soit $A$ un anneau intègre fini. Montrer que $A$ est un corps.
```

```{solution} anneau-integre-fini
:class: dropdown
Soit $a \in A \setminus \{ 0 \}$. Le morphisme $x \mapsto ax$ est injectif donc bijectif donc il existe un inverse $b$ à droite de $a$. De même il existe un inverse $c$ à gauche de $a$. Puis $1 = ca = c (ab) a = (ca)(ba) = ba$ donc $b=c$ et $A$ est un corps.
```

```{exercise}
:label: exo-284
Soit $A$ un anneau  dont les seuls idéaux sont les idéaux triviaux. Montrer que $A$ est un corps.
```

```{solution} exo-284
:class: dropdown
Pour $a \in A \setminus \{ 0 \}$ on a $Id(a) = A$ donc $1 \in Id(a)$ donc $a$ est inversible à gauche, à droite et avec le même raisonnement que dans l'exercice {ref}`anneau-integre-fini`, ce sont les mêmes inverses.
```

```{exercise}
:label: exo-285
Soit $A$ un anneau commutatif dont tous les idéaux sont premiers. Montrer que $A$ est un corps.
```

```{solution} exo-285
:class: dropdown
Soit $x \in A$. On regarde $Id(x^2)$ qui contient $x^2$ donc $x$, donc on peut écrire $x = x^2a$ pour un certain$a$, puis $x(1-xa)=0$. Il reste à remarquer que $\{ 0 \}$ est premier, donc $A$ est intègre. Ainsi $1=ax$.
```


```{exercise}
:label: exo-286
Soit $A$ un anneau intègre possèdant un nombre fini d'idéaux. Montrer que $A$ un est un corps.
```

```{solution} exo-286
:class: dropdown
Pour $a \in A \setminus \{ 0 \}$ on regarde les idéaux $I_n = a^nA$ qui forment une suite décroissante. Elle est donc stationnaire d'où l'existence de $m \in \N$ tel que $I_{m+1}=I_m$. De là il existe $x \in A$ tel que $a^{m+1}x = a^m$. Par intégrité, $x$ est inverse à droite de $a$. De même il existe un innverse à gauche et la conclusion suit.
```

```{exercise}
:label: exo-287
Soit $I_n$ une suite croissante d'idéaux de $\mathbb{K}[X]$ où $\mathbb{K}$ est un corps. Montrer que $(I_n)$ est stationnaire.
```

```{solution} exo-287
:class: dropdown
Facile quand on utilise le fait que $I_n = Id(P_n)$ pour un certain $P_n \in I_n$. La suite $deg(P_n)$ est alors décroissante donc stationnaire.
```

```{exercise}
:label: exo-288
Soit $A$ un anneau de Boole, i.e. $\forall a \in A, \; a^2=a$. Montrer que $A$ est commutatif. Indication : montrer que $\forall a \in A, \; a = -a$.
```

```{solution} exo-288
:class: dropdown
On a pour $a \in A$, $(a+a) = (a+a)^2 = a^2+a^2+a^2+a^2=a+a+a+a$ donc $a+a = 0$  soit $a=-a$. Puis pour $x,y \in A$, on regarde $(x+y)^2$. La conclusion suit facilement.
```


```{exercise}
:label: exo-289
Montrer que si $I$ est maximal, alors $I$ est premier.
```

```{solution} exo-289
:class: dropdown
Soit $x,y \in A$ tels que. On suppose $x \notin I$. On regarde l'idéal $J = I + Id(x)$ qui par maximalité de $I$ est égal à $A$. Il existe donc $i \in I, u \in A$ tels que $1 = i + ux$. De là $y = iy + uxy$. Mais $iy \in I$ et $uxy \in I$ donc $y \in I$.
```


```{exercise}
:label: exo-290

1. Soit $A$ un anneau, $u$ une unité de $A$ et $n$ un nilpotent qui commute avec $u$. Montrer que $u+n$ est encore une unité.
1. Soit $a,b$ deux éléments de $A$ tel que $1-ab$ soit inversible. Montrer que $1-ba$ est inversible.

```

```{solution} exo-290
:class: dropdown
\leavevmode

1. Intuition : $\frac{1}{1-x} = \sum x^k$. Déjà remarquer que $\frac{n}{u}$ est nilpotent, donc on peut se permettre de faire l'exercice pour simplement $u=1$. Avec l'intuition, on montre alors facilement que $\sum_{k \leq \mathcal{N}(n)} (-n)^k$ est bien l'inverse cherché (attention à montrer qu'il est inverse des deux côtés).
1. Pareil avec l'intuition, il faut regarder $1 + b\frac{1}{1-ab}a$ et vérifier qu'il s'agit bien de l'inverse cherché (des deux côtés !).

```

```{exercise}
:label: exo-291
Soit $A$ un anneau, et $a \in A$.

1. Montrer que l'ensemble des inverses à gauche de $a$ est en bijection avec $Ker(\cdot a)$ (noyau de l'homothétie).
1. On suppose $Ker(\cdot a)$ fini non vide. Soit $\kappa$ dans $Ker(\cdot a)$. Montrer qu'il existe $m>0$, tel que $\kappa = g^m \kappa$. *Indication : considérer $(a^n\kappa)$*.
1. Montrer que $1-ag \in Ker(g\cdot) \cap Ker(\cdot a)$.
1. En déduire que $a$ admet $0$, $1$ ou une infinité d'inverses à gauche.

```

```{solution} exo-291
:class: dropdown

1. On fixe $g_0$ inverse à gauche de $a$ (traiter le cas sans inverse à gauche séparément). On a
$ga = 1 \Leftrightarrow ga = g_0a \Leftrightarrow (g-g_0)a = 0 \Leftrightarrow g \in g_0 + Ker(\cdot a)$.

2. $(a^n\kappa)$ n'est pas injective.
3. Simple vérification
4. Il suffit de montrer le résultat sur $Ker(\cdot a)$. On le suppose non vide de taille fini. Alors avec les questions précédentes $Ker(g\cdot) \cap Ker(\cdot a) = \{ 0 \}$ donc $ag = 1$ donc $g$ est l'unique inverse de $a$.

```












































































 