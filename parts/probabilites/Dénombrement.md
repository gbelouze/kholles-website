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

# Dénombrement

```{exercise}
:label: exo-243
Soit $S$ de cardinal $n \geq 2$ et soit $A_1,...,A_m$ des parties de $S$ vérifiant : $\forall x,y \in S$ avec $x \neq y$, il existe $i$ tel qu'on ait soit $x\in A_i, y\notin A_i$, soit $x \notin A_i, y\in A_i$. Montrer que $m \geq \log_2(n)$.
```

```{solution} exo-243
:class: dropdown
À chaque élément $x$ de $S$ on associe une clef $\phi(x) = (\mathds{1}_{x \in A_1}, \ldots, \mathds{1}_{x\in A_m})$. La condition de l'énoncé implique que $\phi$ est injective. Ainsi $|S| \leq |\{0,1\}^m|$, i.e. $n \leq 2^m$.
```

```{exercise}
:label: exo-244
Soit $E$ un ensemble de cardinal $n$. Dénombrer les $m$-uplets $(X_1, X_2, \ldots, X_m) \in \P(E)^m$ tels que $X_1 \subset X_2 \subset \ldots \subset X_m$.
```

```{solution} exo-244
:class: dropdown
Pour chaque élément, on a $m+1$ choix d'appartenance (à personne, au dernier, aux deux derniers, ..., à tout le monde), d'où $(m+1)^n$.
```


```{exercise}
:label: exo-245
Soit $E$ un ensemble de cardinal $n$, et soit $p \leq n$. Dénombrer les $m$-uplets $(X_1, X_2, \ldots, X_m) \in \P(E)^m$ tels que $\bigcap \limits_{i=1}^m X_i$ est de cardinal $p$.
```

```{solution} exo-245
:class: dropdown
À chaque élément on associe une clef d'appartenance à valeur dans $\{0,1\}^m$. Exactement $p$ éléments ont la clef $(1,1,\ldots,1)$. Il y a $2^m-1$ autres clefs possibles, d'où finalement ${n \choose p}(2^m-1)^{n-p}$.
```




```{exercise}
:label: exo-246
On dit que $(a_1,\ldots,a_p) \in \N^p$ est une $p$-décomposition de $n$ si $n=a_1+\ldots+a_p$. Si de plus $\forall i, a_i >0$, on parle de $p$-décomposition stricte. Dénombrer les $p$-décompositions et les $p$-décomposition stricte.
```

```{solution} exo-246
:class: dropdown
Pour les $p$-décompositions strictes. On écrit $n = 1+1+\ldots+1$ et on transforme $p-1$ "+" en séparation. On touve donc ${n-1 \choose p-1}$. Pour les $p$-décompositions, on a une bijection entre les $p$-décompositions et les $p$-décompositions strictes de $n+p$ et on trouve ${n+p-1 \choose p-1}$
```


````{exercise}
:label: exo-247
Soit $(a_i)$ une suite finie de $mn+1$ réels distincts. Montrer qu'il existe soit une sous-suite décroissante de longueur $m+1$, soit une sous-suite croissante de longueur $n+1$.
```{admonition} Indication
:class: tip
Considérer $\alpha_i$ la longueur de la plus grande sous-suite croissante finissant en $x_i$, et $\beta_i$ de la plus grande suite décroissante.```
```
````

```{solution} exo-247
:class: dropdown
$f(a_i) = (\alpha_i, \beta_i)$ est injective. Principe des tiroirs.
```


```{exercise}
:label: exo-248
Trouver une relation de récurrence sur le nombre d'involutions d'un ensemble à $n$ éléments. *Rappel : une involution est sa propre biijection réciproque.*
```

```{solution} exo-248
:class: dropdown
$u_{n+2} = u_{n+1} + (n+1)u_n$
```


```{exercise}
:label: exo-249
Une barrière circulaire est constituée de 17 poteaux dont 5 sont pourris. Montrer qu'il existe un ensemble de 7 poteaux consécutifs dont 3 sont pourris.
```

```{solution} exo-249
:class: dropdown
Soient $p_1, \ldots, p_{17}$ ces poteaux. À chaque poteau $p_i$, on associe l'ensemble $E_{p_i}$ qui est l'ensemble des 7 poteaux consécutifs commençant à $p_i$. Remarquons que tout poteau $p$ appartient à exactement 7 tels ensembles. On note également $E$ l'ensemble des poteaux pourris. Ensuite on définit
\begin{equation*}
    \phi : \; \begin{cases}
        [\![1, n]\!] \rightarrow \mathbb{N} \\
        i \longmapsto Card(E_{p_i} \cap E)
    \end{cases}
\end{equation*}
Supposons par l'absurde que pour tout $i$, $\phi(i) \leq 2$. On a alors
\begin{equation*}
 35 = \sum_{i=1}^{17} \phi(i)
\leq \sum_{i=1}^{17} 2 = 34
\end{equation*}
De là une contradiction.
```

```{exercise} Chemins du plan
:label: exo-250

1. Dénombrer le nombre de chemins de $\Z^2$ allant de $(0,0)$ à $(a,b)$ en n'effectuant que des déplacements vers le nord ou vers l'est.
1. Combien a-t-on de suite à valeurs entières de taille $b$ telle que $\forall n, |u_{n+1} - u_n| = 1$ ? Dans la suite, on considère des chemins n'effectuant que des déplacements NE ou SE.
1. Montrer que l'ensemble des chemins de $(a,\alpha)$ à $(b,\beta)$ qui passent par l'axe des abscisse a même cardinal que l'ensemble des chemins de $(a, -\alpha)$ à $(b, \beta)$ sans contrainte.
1. En déduire le nombre de chemins de $(a, \alpha)$ à $(b,\beta)$ qui ne passent pas par l'axe. Montrer que
\begin{equation*}
|\{ C_2 \neq 0, \ldots, C_{2n-2} \neq 0, C_{2n} = 0\} | = \frac{1}{2n-1}|C_{2n}=0| = |C_{2n-2}=0|- |C_{2n}=0|\end{equation*}
et
\begin{equation*}
|\{ C_2 \neq 0, \ldots, C_{2n-2} \neq 0, C_{2n} \neq 0\} | = |C_{2n}=0|
\end{equation*}

```

```{solution} exo-250
:class: dropdown

1. ${a+b \choose a}$
2. À faire

```


```{exercise}
:label: exo-251
En combien de façon peut-on paver un damier $2\times n$ avec des pièces $2 \times 1$ ?
```

```{solution} exo-251
:class: dropdown
Soit $C_n$ ce nombre. $C_1 = 1$, et $C_{n+2} = C_{n+1} + C_n$ donc c'est fibonacci.
```

````{exercise}
:label: exo-252
On note $F^{(n)}_p$ l'ensemble des parties de $[\![1,n]\!]$ ne contenant pas deux entiers consécutifs. Déterminer $|F^{(n)}_p|$.
```{admonition} Indication
:class: tip
Pour un élément $a_1 < a_2 < \ldots < a_p$ de $F^{(n)}_p$, considérer $b_k = a_k-k+1$.
```
````

```{solution} exo-252
:class: dropdown
L'indication donne une bijection entre $F_p^{(n)}$ et les suites de $p$ entiers de $[1, n-p + 1]$ strictement croissantes. On trouve donc ${n-p+1 \choose p}$
```


```{exercise}
:label: exo-253
Soit $\mathcal{P}$ un sous ensemble fini de $\mathbb{P}$ l'ensemble des nombres premiers, et $n = |\mathcal{P}|$. Soit $x_1, \ldots, x_{n+1}$ des entiers, dont les facteurs premiers sont contenus dans $\mathcal{P}$. Montrer qu'il existe un sous-ensemble $I$ non vide de $[\![1,n+1]\!]$ tel que $\prod_{i \in I} x_i$ soit un carré parfait.
```

```{solution} exo-253
:class: dropdown
Il suffit que la valuation $p$-adique du produit soit paire, pour tout $p \in \mathcal{P}$. On va procéder par récurrence.
**initialisation** Pour $n=1$, soit $x_1$ ou $x_2$ est de valuation $p_1$-adique paire et est un carré parfait, soit les deux ont une valuation $p_1$-adique impaire et leur produit est un carré parfait.
**récurrence** $X = \{x_1, \ldots, x_{n+1}\}$ sont donnés. On peut partitionner $X$ selon la parité de la valuation $p_n$-adique de ses éléments : $X = X_0 \sqcup X_1$.

Si $|X_1| \leq 1$, on peut choisir $n$-éléments dans $X_0$, et par hypothèse de récurrence extraire de ses $n$ éléments un produit dont la valuation $p_i$-adique est paire pour $i=1, \ldots, n-1$. De plus, la valuation $p_n$-adique de ce produit est paire par construction de $X_0$, le produit est donc un carré parfait.

Sinon on peut choisir $x, y \in X_1$. Par hypothèse de récurrence cela fournit $C_x$ (respectivement $C_y$) un sous ensembles de $X \setminus x$ (respectivement $X \setminus y$), tel que le produit $P_x$ de ses éléments est de valuation $p_i$-adique paire pour $i=1, \ldots, n-1$. Alors soit l'un des deux produits $P_x$ ou $P_y$ est de valuation $p_n$-adique paire, auquel cas ce produit est un carré parfait, soit les deux sont de valuation $p_n$-adique impaire. Dans ce dernier cas, on regarde $C = C_x \ XOR \  C_y$, c'est-à-dire que $C$ contient les éléments de $X$ qui sont dans $C_x$ ou dans $C_y$, mais pas les deux. Il suffit alors de remarquer que pour tout $p \in \mathcal{P}$, la parité du nombre d'éléments de valuation $p$-adique impaire est la même dans $C_x$ et dans $C_y$, et donc il y a un nombre pair de tels éléments dans leur $XOR$. Cela justifie que le produit des éléments de $C$ est un carré parfait.
```










































































 