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

# Arithmétique

```{exercise}
:label: exo-316
Montrer que la somme de deux nombres premiers consécutifs n'est jamais un produit de deux nombres premiers.
```

```{solution} exo-316
:class: dropdown
Si le premier est $2$, on vérifie à la main. Sinon $2$ divise la somme et $p_n + p_{n+1} = 2q$ donc $p_n < q < p_{n+1}$. Absurde.
```

```{exercise}
:label: exo-317
Montrer que $2^n$ divise $(3-\sqrt{5})^n + (3+\sqrt{5})^n$.
```

```{solution} exo-317
:class: dropdown
On note $u_n = (3-\sqrt{5})^n + (3+\sqrt{5})^n$. Cette suite doit vérifier une relation de récurrence d'ordre 2 dont $(3-\sqrt{5})$ et $(3+\sqrt{5})$ sont les racines. Cette relation doit donc être $u_{n+2} = 6u_{n+1} - 4u_n$. La récurrence est alors triviale.
```

```{exercise} nombre de Mersène
:label: exo-318
Les nombres de Mersène sont les $M_n = 2^n - 1$. Montrer que $M_n \textrm{ premier } \Rightarrow n \textrm{ premier}$.
```

```{solution} exo-318
:class: dropdown
Corollaire de $a-b$ divise $a^n - b^n$, en prenant $a = 2^p$, $n=q$ et $b=1$.
```

```{exercise}
:label: exo-319
Trouver $1000$ nombres consécutifs non premiers.
```

```{solution} exo-319
:class: dropdown
$1001! + k $ pour $k = 2, \ldots, 1001$.
```

```{exercise} nombre harmonique non entier
:label: exo-320
Montrer que $H_n = 1 + \frac{1}{2} + \ldots + \frac{1}{n}$ n'est pas entier.
```

```{solution} exo-320
:class: dropdown
On montre par récurrence que sa valuation $2$-adique est toujours strictement négative. $H_{n-1} = \frac{p_n}{2q_n}$ et $H_{n} = \frac{p_n}{2q_n} + \frac{1}{n} = \frac{np_n + 2q_n}{2nq_n}$ et on est assuré que $v_2(np_n + 2q_n) = \min{(v_2(n), v_2(2q_n))} < v_2(2q_n) + v_2(n) = v_2(2nq_n)$.
```

```{exercise}
:label: exo-321
Montrer que la somme de $n \geq 2$ impairs consécutifs n'est jamais un nombre premier.
```

```{exercise}
:label: exo-322
Calculer le dernier chiffre de $7^{\circ 7} = 7^{7^{7^{7^{7^{7^{7}}}}}}$.
```

```{solution} exo-322
:class: dropdown
$7^4 = 1 [10]$ puis $3^2 = 1 [4]$ puis $7^{\circ 5} = 1 \mod{2}$ donc $3^{7^{\circ 5}} = 3 \mod{4}$ donc $7^{\circ 6} = 3 \mod{4}$ donc $7^{\circ 7} = 7^3 \mod{10} = 3 \mod{10}$.
```

```{exercise}
:label: exo-323
Montrer que la somme de trois cubes consécutifs est divisible par $9$.
```

```{exercise}
:label: exo-324
Montrer que $a^2 + b^2 + c^2 + 1 \neq 0 \mod{8}$.
```

```{exercise}
:label: exo-325
Montrer que pour tout $n$, il existe des uniques $a_n,b_n$ tels que $(1+\sqrt{2})^n = a_n + b_n \sqrt{2}$. Calculer $a_n^2 - 2b_n^2$. En déduire que $a_n$ et $b_n$ sont premiers entre eux.
```

```{solution} exo-325
:class: dropdown
Existence acquise, unicité par irrationnalité de $\sqrt{2}$. Puis en remarquant que $(1-\sqrt{2})^n = a_n - b_n \sqrt{2}$, il vient $a_n^2 - 2b_n^2 = (-1)^n$. Enfin il suffit de remarquer que $a_n$ est impair pour conclure.
```

```{exercise}
:label: exo-326
Soit $a,b$ des entiers plus grands que $2$. Soit $n \in \N$. Montrer que si $p = a^n + b^n$ est premier, alors $n$ est une puissance de $2$.
```

```{solution} exo-326
:class: dropdown
On écrit $n = 2^k(2q+1)$. On a alors $p = (a^{2^k})^{2q+1} - (-b^{2^k})^{2q+1}$, ce qui se factorise par $a^{2^k} +b^{2^k}$.
```

```{exercise}
:label: exo-327
Soit $x_1, x_2, \ldots, x_n \in \Z$. Montrer qu'il existe $J \subset [\![ 1, n ] \! ]$ tel que $n$ divise $\underset{j \in J}{\sum} x_j$.
```

```{solution} exo-327
:class: dropdown
On se ramène dans $\Z/n\Z$. On prend $J_1, \ldots, J_n$ une suite croissante pour l'inclusion d'indices. On leur associe leur $n$ sommes correspondantes. Si l'une vaut $0$, c'est bon, sinon deux ont la même valeur, et la différence convient.
```

```{exercise}
:label: exo-328
Montrer que $13$ divise $3^{126} + 5^{126}$
```


```{exercise}
:label: exo-329
Montrer que $2012$ a un multiple qui ne s'écrit qu'avec des $4$.
```

```{solution} exo-329
:class: dropdown
$2012 = 503 \times 4$ et $503$ est premier. Il faut montrer que $503$ a un multiple qui ne s'écrit qu'avec des $1$, soit qu'il existe $m$ tel que $\frac{10^m - 1}{9} = 0 \mod{503}$. Or $9 \land 503 = 1$ donc il faut $m$ tel que $10^m = 1 \mod{503}$. C'est Fermat !
```

```{exercise}
:label: exo-330
Soit $(u_n)$ la suite de Fibonacci.

1. Montrer que $u_{n+m} = u_mu_{n+1} + u_{m-1}u_n$. En déduire que si $p | n$ alors $u_p | u_n$.
1. Montrer que $u_{n+1}u_{n-1} - u_n^2 = (-1)^n$
1. Montrer que $u_{p \land n} = u_p \land u_n$

```

```{solution} exo-330
:class: dropdown

1. Récurrence pour chaque question.
1. Récurrence.
1. Algorithme d'Euclide : il suffit de montrer que si $n = qp+r$, $u_p \land u_n = u_p \land u_r$. C'est la conséquence de la question $1$, et du fait que $u_n$ et $u_{n+1}$ sont premiers entre eux par question 2.

```



```{exercise}
:label: exo-331
Soit $n \in \N$. Caractériser les nilpotents de $\Z/n\Z$.
```


```{exercise}
:label: exo-332
Trouver les solutions de $x^2+y^2=3z^2$.
```

```{solution} exo-332
:class: dropdown
On regarde dans $\Z/3\Z$ et on montre qu'on peut diviser les solutions par $3$, donc il n'y a que $(0,0,0)$.
```

```{exercise}
:label: exo-333
Montrer que $\phi(n) \underset{n \rightarrow +\infty}{\rightarrow} +\infty$.
```

```{solution} exo-333
:class: dropdown
On note $q = \max(p_i^{\alpha_i})$. On a $\phi(n) \geq \frac{q}{2}$. Or à $N$ fixé il n'y a qu'un nombre fini d'entiers $n$ tels que $q \leq N$.
```


```{exercise}
:label: exo-334
Montrer que $\phi(n)$ est pair pour $n \geq 3$.
```

```{solution} exo-334
:class: dropdown
$-1$ est d'ordre $2$ et son ordre divise le cardinal de $(\Z/n\Z)^*$.
```

```{exercise}
:label: exo-335
On suppose $m \land n = 1$. Montrer que
\begin{equation*}
 m^{\phi(n)} + n^{\phi(n)} = 1 \mod{mn}
\end{equation*}
```

```{solution} exo-335
:class: dropdown
Par Euler c'est vrai modulo $m$ et modulo $n$ donc par le lemme chinois c'est vrai modulo $mn$.
```


```{exercise} Wilson
:label: exo-336
Soit $p \in \N \setminus \{ 0\}$. Montrer que
\begin{equation*}
 p \textrm{ premier } \Leftrightarrow (p-1)! + 1 = 0 \mod{p}
\end{equation*}
```

```{solution} exo-336
:class: dropdown
$(\Leftarrow)$  Par Bezout $p$ et $(p-1)!$ sont premiers entre eux.

$(\Rightarrow)$ On regarde $P=X^p-X$ dans $\mathbb{F}_p[X]$. Par raisonnement sur le degré ($\mathbb{F}_p$ est un corps) on a $P=\prod_{a \in \mathbb{F}_p}(X-a)$. Puis on identifie le coefficient devant $X$.
```


```{exercise}
:label: exo-337
Soit $b \in (\Z/p\Z)^*$ avec $p$ premier. Pour $k \in \N$, calculer
\begin{equation*}
 S_k = \sum_{a \in \Z/p\Z} a^k
\end{equation*}
```

```{solution} exo-337
:class: dropdown
pour $b \in \Z/p\Z$, on a $a \mapsto ba$ bijective donc $S_k = b^kS_k$. Puis si $k$ est multiple de $p-1$, $S_k = -1$ par Fermat. Sinon, il existe $b$ tel que $b^k \neq 1$ (on écrit $k = qp + r$ et on a $b^k = b^r$ donc au plus $r$ $b$ qui ne conviennent pas). De là $S_k = 0$.
```


```{exercise} Résidus quadratiques
:label: exo-338
Soit $p \geq 3$ premier. On dit que $a \in (\Z/p\Z)^*$ est un carré s'il existe $b \in \Z/p\Z$ tel que $a = b^2$.

1. Montrer qu'il y a $\frac{p-1}{2}$ carrés dans $(\Z/p\Z)^*$.
1. Montrer que $a$ est un carré si et seulement si $a^{\frac{p-1}{2}}=1$
1. En déduire que
    \begin{equation*}
    f_p \begin{cases}
    (\Z/p\Z)* \rightarrow &\{ -1, 1 \} \\
    x \mapsto &-1 \textrm{ si $x$ n'est pas un carré} \\
    & 1 \textrm{ sinon}
    \end{cases}
    \end{equation*}

    est un morphisme. Culture : c'est le seul non trivial et on note $(\frac{a}{b})=f_p(a)$. C'est le symbole de Legendre.

```

```{exercise} Suite résidus quadratiques
:label: exo-339
Soit $p$ un nombre premier de la forme $2^m -1$, avec $m \geq 3$.

1. Montrer que $p = 1 \mod{3}$.
1. Montrer qu'il existe $x \in \Z$ tel que $x^3=1 \mod{p}$ et $x \neq 1 \mod{p}$. En déduire que $x^2+x+1=0 \mod{p}$
1. Dans $\Z/p\Z$, montrer que $-1$ n'est pas un carré. Puis à l'aide de la question précédente, montrer que $-3$ est un carré. En déduire que $3$ n'est pas un carré.

```



```{exercise} Formule de Legendre
:label: exo-340
Soit $n \in \N$, $p$ premier. Montrer que
\begin{equation*}
 v_p(n!) = \sum_1^{\infty} \lfloor \frac{n}{p^k} \rfloor
\end{equation*}
```

```{exercise}
:label: exo-341
Soit $G$ un groupe commutatif fini, $a,b \in G$. Si $w(a) \land w(b) =1$, montrer que $w(ab)=w(a)w(b)$. En déduire que dans le cas général (plus d'hypothèse sur les ordres), il existe un élément $c \in G$ d'ordre le PPCM de $w(a)$ et $w(b)$. En déduire que pour $p$ premier, $(\Z/p\Z)^*$ est cyclique.
```

```{solution} exo-341
:class: dropdown
Soit $k$ l'ordre de $ab$. On a $(ab)^{w(a)w(b)} = 1$ donc $k | w(a)w(b)$.

Ensuite on écrit $1 = (ab)^{kw(a)} = b^{kw(a}$ donc $w(b) | kw(a)$. Puisque $w(a)$ et $w(b)$ sont premiers entre eux, on en déduit $w(b) | k$. De même  $w(a) | k$. Là encore, $w(a)$ et $w(b)$ étant premiers entre eux, $w(a)w(b) | k$, et finalement $k = w(a)w(b)$.

On écrit $w(a) = m = p_1^{\alpha_1}\ldots$ et $w(a) = n = p_1^{\beta_1}\ldots$.
On pose $\alpha'_i = \alpha_i$ si $\alpha_i \geq \beta_i$, $0$ sinon. De même on définit $\beta'_i$. Cela fournit naturellement $m'$ et $n'$. Remarquons que $m \lor n = m' \lor n'$. De plus $m' | m$ et $n' | n$. Les éléments $a' = a^{\frac{m}{m'}}$ et $b' = b^{\frac{n}{n'}}$ sont d'ordre premiers entre eux et ainsi $c = a'b'$ convient.

Puis pour la cyclicité, on a un élément d'ordre $m$ le ppcm de l'ordre de tous les éléments. En particulier (petit théorème de Fermat), $m | p-1$.  Mais chaque élément vérifie $x^{p-1}=1$ (petit théorème de Fermat) donc $p-1 | m$. Bref $p-1=m$.
```


















































































 