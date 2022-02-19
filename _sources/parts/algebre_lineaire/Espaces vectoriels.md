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

# Espaces vectoriels


```{exercise}
:label: exo-342
Montrer que la commutativité de la loi $+$ est une conséquence des autres axiomes de la structure d'espace vectoriel.
```

```{solution} exo-342
:class: dropdown
Soit $u,b$ deux vecteurs. On a
\begin{align*}
0 &= u + (v-v) - u \\
&= (u+v) -v -u \\
&= (u+v) + (-1)u + (-1)v \\
&= (u+v)+(-1)(v+u) \\
&= (u+v)-(v+u)
\end{align*}
d'où $u+v = v+u$.
```


```{exercise} lemme de Schur
:label: exo-343
Soit $E$ un espace vectoriel et $u \in \L(E)$. On suppose que $\forall x \in E, \; \exists \lambda_x \in \mathbb{K} \; u(x) = \lambda_xx$. Montrer que $u$ est une homothétie.
```

```{solution} exo-343
:class: dropdown
Soit $x,y \in E$ non nuls. On va montrer que $\lambda_x = \lambda_y$. S'il existe $\mu \in \mathbb{K}$, $x=\mu y$, alors on a
\begin{align*}
\lambda_y y &= u(y) \\
&= \lambda_x \mu x \\
&= \lambda_x y
\end{align*}
d'où $\lambda_x=\lambda_y$. Sinon on regarde $z=x+y$.
\begin{align*}
\lambda_z (x+y) &= \lambda_x x + \lambda_y y  \\
(\lambda_z-\lambda_x) x = (\lambda_y-\lambda_z) y \\
\end{align*}
Et il suit de la liberté de $(x,y)$ que $\lambda_x=\lambda_z=\lambda_y$.
```


```{exercise}
:label: exo-344
Déterminer $\alpha$ tel que
\begin{equation*}
F_{\alpha} = \{ (x,y) \in R^2 \; | \; x^2 + \alpha xy + y^2 = 0 \}
\end{equation*}
soit un sous espace vectoriel de $\R^2$.
```

```{solution} exo-344
:class: dropdown
Soit $x$ non nul fixé. $x^2 + \alpha xy + y^2 = 0$ admet une solution réelle si et seulement si $\alpha^2 \geq 4$. Ainsi, pour $\alpha \in ]-2,2[$, $F_{\alpha} = \{ (0,0) \}$ convient. On vérifie que $|\alpha| = 2$ convient également. Puis si $\alpha^2 > 4$, il existe deux solutions distinctes $y_1, y_2$ à $x$ non nul fixé. Si $F_{\alpha}$ est un espace vectoriel, alors $(x-x, y_1-y_2 ) \in F_{\alpha}$mais cela est absurde.
```

```{exercise}
:label: sevcomplementaire
Soit $F$ un sous-espace vectoriel strict de $E$. Déterminer $\Vect(E \setminus F)$.
```

```{solution} sevcomplementaire
:class: dropdown
Soit $a \in E \setminus F$ non nul. Soit $x\in E$. Si $x \in E \setminus F$, alors $x \in \Vect(E \setminus F)$. Sinon $x = x+(a-a) = (x+a)-a$. Mais $x+a \notin F$ (sans quoi $a \in F$) et $-a \notin F$, donc $x \in \Vect(E \setminus F)$. Bref $\Vect(E \setminus F) = E$.
```

```{exercise}
:label: exo-346
Soit $E = \C^0(\R,\R)$. Pour $a \in \R$ on note $E_a = \{f \in E \; | \; f(a)=0 \}$. Montrer que pour tout $a$, $E_a$ est un sous-espace vectoriel de $E$. Soit $a\neq b$. Que dire de $E_a + E_b$?
```

```{solution} exo-346
:class: dropdown
$E_a+E_b=E$.
```

```{exercise}
:label: exo-347
Soit $E$ un espace vectoriel et $F$ un sous-espace non trivial de $E$. Déterminer l'ensemble des endomorphismes s'annulant sur le complémentaire de $F$.
```

```{solution} exo-347
:class: dropdown
Soit $u$ un tel endomorphisme. $Ker(u)$ est un sous-espace vectoriel s'annulant sur $E\setminus F$, donc sur $\Vect(E \setminus F)$. Or avec {ref}`sevcomplementaire`, cet ensemble est $E$ lui-même. Donc seul l'endomorphisme nul convient.
```

```{exercise}
:label: exo-348
Soit $E,F$ deux $\R$-espaces vectoriels, $u \in \L(E,F)$ et $V,W$ deux sous-espaces vectoriels de $E$. Montrer
\begin{equation*}
u(V) \subset u(W) \Leftrightarrow V \subset W + Ker(u)
\end{equation*}
```

```{solution} exo-348
:class: dropdown
Le sens retour est immédiat. Montrons le sens direct. Soit $v \in V$. Il existe $w \in W$ tel que $u(v)=u(w)$, i.e. $v-w \in Ker(u)$. Il suit $v = w+z$ avec $z \in Ker(u)$, d'où le résultat.
```


```{exercise} Suite des noyaux itérés
:label: noyau_itere

1. Soit $E$ un espace vectoriel, $u\in \L(E)$ et $n \in \N$ tel que $Ker(u^n)=Ker(u^{n+1})$. Montrer que pour tout $m \geq n$, $Ker(u^n)=Ker(u^m)$
1. Voir {ref}`noyau_itere_suite`

```

```{solution} noyau_itere
:class: dropdown

1. Par récurrence, $x \in Ker(u^{n+k+1}) \Leftrightarrow u^k(x) \in Ker(u^{n+1}) \Leftrightarrow u^k(x) \in Ker(u^n) \Leftrightarrow x \in Ker(u^{n+k})$
1. Soit $(d_k)$ la suite des dimensions de $Ker(u^k)$. On remarque $Ker(u^k) \subset Ker(u^{k+1})$, ce qui se traduit par le fait que $(d_k)$ est croissante. De plus $d_n = n$, et pour tout $m \geq n$, $d_m=n$, et pour tout $m<n$, $d_m < n$. Ensuite, si $(d_k)$ n'est pas strictement croissante sur $[\![0, n-1]\!]$, avec la question 1 $(d_k)$ est stationnaire et n'atteint pas $n$, ce qui est absurde. Donc $(d_k)$ est strictement croissante sur $[\![0, n-1]\!]$, à valeur dans $[\![0, n-1]\!]$. Il n'y a qu'une seule possibilité : $d_k = k$ pour $k \leq n$.

```

```{exercise}
:label: exo-350
Soit $E$ un espace vectoriel et $\mathcal{F} = (F_i)_{i \in I}$ une famille de sous-espace vectoriels de $E$. On suppose $\mathcal{F}$ filtrante, i.e. $\forall i,j, \; \exists k$ tel que $F_i \cup F_j \subset F_k$. Montrer que $\bigcup_{i \in I} F_i$ est un sous-espace vectoriel de $E$.
```

```{solution} exo-350
:class: dropdown
Il contient $0$. Puis soit $x,y \in \bigcup_{i \in I} F_i$. Il existe $i,j$ tels $x \in F_i$ et $y \in F_j$. De là $x,y \in F_k$ puis $x + \alpha y \in F_k \subset \bigcup_{i \in I} F_i$. Cela conclut.
```

```{exercise}
:label: exo-351
Montrer que si un $\K$-espace vectoriel $E$ est réunion d'une famille finie de sous-espaces différents de $E$, alors le corps $\K$ est fini.
```

```{solution} exo-351
:class: dropdown
Soit $E_1, \ldots, E_n$ des sous-espaces propres de $E$ de réunion $E$, et (quitte à éliminer les redondances) tels qu'aucun d'entre eux ne soit inclus dans la réunion des autres. Soit alors $u$ un vecteur de $E_1$ qui ne soit pas dans la réunion des autres, et $v \notin E_1$. On regarde le sous-espace affine $v + \K u$. Il contient au plus un élément dans chaque $E_i$, et est disjoint de $E_1$, donc $\K$ contient au plus $n-1$ éléments.
```

```{exercise}
:label: exo-352
Soit $E$ l'espace vectoriel des fonctions de $[0,1]$ dans $\R$ et $p_a : x \mapsto |x-a|$. Déterminer le sous-espace vectoriel engendré par les $p_a$ pour $a \in [0,1]$.
```

```{solution} exo-352
:class: dropdown
Clairement ce sous-espace est inclus dans l'ensemble $\mathcal{A}$ des fonctions affines par morceaux continues, avec un nombre fini de morceaux. Montrons que le sev recherché est exactement $\mathcal{A}$. On représente une fonction $f$ de $\mathcal{A}$ par les $n$ points $(a_i, f(a_i))$ de rupture de pente, ainsi que $f(0)$ et $f(1)$. On raisonne par réccurrence sur $n$.

Pour $n=1$, on résoud un système linéaire à trois inconnues.

Pour $n \geq 2$, on peut retirer la fonction $f$ correspondant aux $n-1$ premiers points de représentation, puis utiliser le cas $n=2$.
```

```{exercise}
:label: exo-353
Montrer que deux formes linéaires de même noyau sont colinéaires
```

```{solution} exo-353
:class: dropdown
Il s'agit de trouver une combinaison linéaire annulant $\phi$ et $\psi$. Fixons $a$ et remarquons astucieusement pour $x \in E$ que $\phi(x)\phi(a) - \phi(x)\phi(a) = 0$, soit $x\phi(a) - \phi(x)a \in Ker(\phi)$ donc $x\phi(a) - \phi(x)a \in Ker(\psi)$, i.e. $\psi(a)\phi - \phi(a)\psi = 0$. Il suffit alors de choisir $a$ qui n'annule pas une des deux fonctions. Si cela n'est pas possible, elles sont toutes deux nulles donc a fortiori colinéaires.
```



```{exercise}
:label: exo-354
Exhiber un endomorphisme d'un espace vectoriel injectif et non surjectif, puis surjectif mais non injectif.
```

```{solution} exo-354
:class: dropdown
Les tapis roulants de $\R^{\N}$
```

```{exercise}
:label: exo-355
Montrer que le produit de nilpotent n'est pas nécessairement nilpotent.
```

```{solution} exo-355
:class: dropdown
Les tapis roulants de $\R^n$.
```

```{exercise}
:label: exo-356
Soit $n \geq 1$ et $\K$ un corps fini de cardinal $q \geq 2$

1. Déterminer le nombre de droites de $\K^n$.
1. Déterminer le nombre de plans de $\K^n$. (CORRECTION MISSING)

```

```{solution} exo-356
:class: dropdown
1.
    Notons $\mathcal{D}$ l'ensemble des droites. Une droite est de la forme $\K x$ avec $x$ un vecteur non nul. Il est naturel de regarder
    \begin{align*}
    \phi : \begin{cases}
    K^n \setminus \{0\} &\rightarrow \mathcal{D} \\
    x &\mapsto \K x
    \end{cases}
    \end{align*}
    L'application $\phi$ est par construction surjective. Regardons le nombre d'antécédents d'un éléments de $\mathcal{D}$.
    \begin{align*}
    \phi(x) = \phi(y) &\Longrightarrow \K x = \K y\\
    &\Longrightarrow y = 1y \in \K x\\
    &\Longrightarrow \exists k \in \K^*, \; y = k x
    \end{align*}
    Réciproquement, il est évident que $x = k y$ pour $k$ non nul implique $\phi(x) = \phi(y)$. Ainsi tout élément de $\mathcal{D}$ possède exactement $q-1$ antécédent par $\phi$. Ainsi
    \begin{equation*}
     |\mathcal{D}| = \frac{|\K^n \setminus \{ 0\}|}{|K^*|} = 1 + q +\ldots + q^{n-1}
    \end{equation*}
2.
    à faire
```


```{exercise}
:label: noyau_itere_suite
Soit $E$ de dimension $n$ et $u \in \L(E)$ nilpotent d'indice $n$. On note $F_k = Ker(u^k)$. Calculer $d_k=dim(F_k)$ pour tout $k$.
```

```{solution} noyau_itere_suite
:class: dropdown
Voir {ref}`noyau_itere`
```

```{exercise}
:label: exo-358
Soit $E,F$ des espaces vectoriels de dimension finie et $u \in \L(E,F)$. Montrer qu'il existe $v \in \L(F,E)$ tel que $u \circ v \circ u = u$.
```

```{exercise}
:label: exo-359
Montrer que la famille des fonctions $x \rightarrow \cos(\lambda x)$ avec $\lambda \in \R^{+}$ est libre.
```

```{solution} exo-359
:class: dropdown
Ce sont des vecteurs propres de l'application $f \longmapsto -f''$. Sinon dériver $n$ fois en $0$ et faire tendre $n$ vers $+ \infty$.
```

```{exercise}
:label: exo-360
Même exercice avec $x \rightarrow \exp(\lambda x)$.
```

```{exercise}
:label: supplementaire_existe
Soit $U$ et $V$ des s.e.v. de $E$ un espace vectoriel de dimension fini.. Montrer que $U$ et $V$ ont un supplémentaire commun si et seulement si $dim(U) = dim(V)$.
```

```{solution} supplementaire_existe
:class: dropdown
Un sens est trivial. On raisonne par récurrence décroissante sur $dim(U)=dim(V)$. Si $dim(U)=dim(E)$ c'est fini. On suppose le résultat vrai pour tout sous espace de dimension plus grande que $k$. Soit $e \in E \setminus (U \cup V)$. On considère $U' = U + Vect(e)$ et $V'=V+Vect(e)$. Par hypothèse de récurrence, il existe $S$ supplémentaire commun à $U'$ et $V'$. De là $S+Vect(e)$ est supplémentaire commun à $U$ et $V$.
```


```{exercise}
:label: exo-362
Déterminer le rang de la famille des vecteurs $X_{i,j} = e_i-e_j \in \R^n$.
```

```{solution} exo-362
:class: dropdown
Il est majoré par $n$. Il est minoré par $n-1$ avec les $X_{1,j}$. Puis on remarque $X_{j,k} = X_{1,k}-X_{1,j}$. D'où un rang de $n-1$.
```

```{exercise}
:label: exo-363
Soit $a_0<a_1<\ldots<a_N$.

1. Montrer que l'espace $E$ des fonctions continues sur $[a_0,a_N]$ affines par morceaux pour la subdivision $a_0, \ldots, a_N$ est de dimension $N+1$.
1. Déterminer une base de $E$.

```

```{solution} exo-363
:class: dropdown
Isomorphisme évident avec $\R^{N+1}$ par $f \mapsto (f(a_0), \ldots, f(a_N))$.
```

```{exercise}
:label: exo-364
Soit $E$ un espace vectoriel de dimension finie, $A$ l'ensemble des sous-espaces vectoriels de $E$. Déterminer les applications $f$ de $A$ dans $\R$ telles que
\begin{equation*}
 \forall U,V \in A, \; f(U+V) = f(U) + f(V) - f(U \cap V)
\end{equation*}
```

```{solution} exo-364
:class: dropdown
Remarquons qu'on peut ajouter une constante à $f$ sans modifier la propriété. On suppose donc $f(\{0\})=0$. On montre d'abord que les espaces de dimension $1$ ont même image par $f$. Soit $a,b \in E$ non liés. D'après l'exercice {ref}`supplementaire_existe`, on peut trouver $S$ supplémentaire à la fois de $Vect(a)$ et $Vect(b)$.
On a alors $f(Vect(a)) = f(E)-f(S) = f(Vect(b))$. Notons $\lambda$ cette image. Par une récurrence immédiate il vient $f(U) = \lambda dim(U)$. Bref, dans le cas général, $f(U) = \lambda dim(U) + \mu$ avec $\lambda, \mu \in \R$.
```

```{exercise}
:label: exo-365
Soit $E$ un espace vectoriel de dimension finie, $u \in \L(E)$ nilpotente d'indice $p$. Notons $\Phi : v \in \L(E) \mapsto u\circ v - v \circ u$.

1. Montrer que, pour tout $n \in \N$, et tout $v \in \L(E)$,
\begin{equation*}
 \Phi^n(v) = \sum_{k=0}^n (-1)^k {n \choose k} u^{n-k} \circ v \circ u^k
\end{equation*}
1. Montrer que $\Phi$ est nilpotente et majorer son indice de nilpotence.
1. Soit $a \in \L(E)$. Montrer qu'il existe $b \in \L(E)$ tel que $a \circ b \circ a = a$.
1. En déduire l'indice de nilpotence de $\Phi$.

```

```{solution} exo-365
:class: dropdown

1. Simple récurrence.
1. Avec $n = 2p$, et même $2p-1$.
1. Soit $(e_1, \ldots, e_m)$ une base de $Im(a)$, et $b_1, \ldots, b_m$ tels que $a(b_i) = e_i$. Nécessairement $b_1, \ldots, b_m$ est libre. On choisit $b$ tel que $b(b_i)=e_i$, $b=0$ ailleurs. Ce tel $b$ convient.
1. On a $\Phi^{2p-2}(v) = (-1)^{p-1}{2p-2 \choose p-1} u^{p-1} \circ v \circ u^{p-1}$. Avec $v$ tel que $u^{p-1} \circ v \circ u^{p-1} = u^{p-1}$, il suit que $\Phi$ est d'indice de nilpotence exactement $2p-1$.

```

```{exercise}
:label: exo-366
Soit $F,G$ deux sous espaces vectoriels de $\R^n$. Déterminer une condition nécessaire et suffisante pour qu'il existe $u \in GL(\R^n)$ tel que $u(F)=G$.
```

```{solution} exo-366
:class: dropdown
Même dimension, en envoyant la base de $F$ sur la base de $G$.
```

```{exercise}
:label: exo-367
Soit $E$ de dimension $n$ et $f \in \L(E)$ un endomorphisme $n$-nilpotent. Montrer l'équivalence pour $g \in \L(E)$
\begin{equation*}
 f \circ g = g \circ f \Longleftrightarrow g \in Vect(Id,f,\ldots,f^{n-1})
\end{equation*}
```

```{solution} exo-367
:class: dropdown
Il est classique de montrer l'existence de $x$ tel que $(x, f(x), \ldots, f^{n-1}(x))$ est une base de $E$. On peut donc écrire $g(x) = \sum_{k=0}^{n-1} a_kf^{k}(x)$. Alors il vient que $g$ et $\sum a_kf^k$ coïncident sur $(x, f(x), \ldots, f^{n-1}(x))$  donc sur $E$. Le sens retour est trivial.
```

```{exercise}
:label: exo-368
Soit $E$ de dimension finie, $F$, $G$ deux sev de $E$ tels que $F+G=E$. Déterminer la dimension du sev de $\L(E)$ composé des $u$ tels que $u(F)\subset F$ et $u(G)\subset G$. Et si on impose $u$ bijectif ?
```

```{solution} exo-368
:class: dropdown
Isomorphisme avec $\L(F\cap G, F \cap G) \times \L(F', F) \times \L(G',G)$ où $F'$ supplémentaire de $F\cap G$ dans $F$ et $G'$ de même. Si $F',G',F\cap G$ sont de dimension respective $r,s,t$, la dimension recherchée est donc $r(r+t)+s(s+t)+t^2=r^2+t^2+s^2+t(r+s)$.
```

```{exercise}
:label: exo-369
Soit $p$ un projecteur de $E$. Définissons
\begin{align*}
F_1 &= \{ f \in \L(E) \; | \; \exists u \in \L(E), \; f=u\circ p \} \\
F_2 &= \{ f \in \L(E) \; | \; \exists u \in \L(E), \; f=u\circ (Id-p) \}
\end{align*}
Montrer que $F_1$ et $F_2$ sont supplémentaires dans $\L(E)$.
```

```{solution} exo-369
:class: dropdown
Classiquement $Ker(p)$ et $Ker(Id-p)$ sont supplémentaires dans $E$. Ainsi si $f \in \L(E)$, $f(x)=f(p(x)+x-p(x))=f(p(x))+f(x-p(x))$ d'où $F_1+F_2=E$. Si $f \in F_1 \cap F_2$, alors $Ker(p)\subset Ker(f)$ et $Ker(Id-p) \subset Ker(f)$ d'où $Ker(p)+Ker(Id-p)=E\subset Ker(f)$. Bref $f=0$.
```

```{exercise}
:label: exo-370
Soit $a, b$ deux scalaires distincts et $u\in \L(E)$ tels que
\begin{equation*}
 (u-aId) \circ (u-b(Id)) = 0
\end{equation*}

1. Montrer que $Ker(u-aId)$ et $Ker(u-bId)$ sont supplémentaires.
1. Déterminer une expression simple de la projection de $p$ sur $Ker(u-aId)$ parallèlement à $Ker(u-bId)$.
1. Montrer que $u = ap + b(Id-p)$. En déduire une expression de $u^n$ pour tout $n$.

```

```{solution} exo-370
:class: dropdown

1. Ils sont trivialement en somme directe. Le lemme des noyaux permet d'obtenir directement le résultat mais ici on se contente de le faire à la main. On a $P(u)=0$ avec $P=(X-a)(X-b)=P_1P_2$. De plus $\frac{P_1}{b-a}+\frac{P_2}{a-b}=1$. Ainsi pour tout $x\in E, \; x = \frac{u(x)-ax}{b-a}+\frac{u(x)-bx}{a-b}$.
1. On vérifie immédiatement que $\frac{u(x)-bx}{b-a}$ convient.
1. La vérification est immédiate en écrivant $Id-p=\frac{u-aId}{b-a}$, et on a $u^n=a^np+b^n(Id-p)$.

```

```{exercise}
:label: exo-371
Soit $p,q$ deux projecteurs sur le même espace (pas forcément parallèles). Soit $\lambda \in \R$. Montrer $\lambda p + (1-\lambda)q$ est un projecteur.
```

```{solution} exo-371
:class: dropdown
Il suffit de remarquer que $p \circ q = q$ et $q \circ p = p$.
```

```{exercise}
:label: exo-372
Soit $p,q$ deux projecteurs qui commutent. Montrer que $Ker(p+q)=Ker(p)\cap Ker(q)$.
```

```{solution} exo-372
:class: dropdown
Une inclusion est évidente. Pour l'autre on écrit $p(x)+q(x)=0$ donc en composant pas $p$ et $q$ on $p(x)+q\circ(p(x))=0$ et $q(x)+q\circ p(x)=0$. Bref$p(x)=q(x)=0$.
```

```{exercise}
:label: exo-373
Soit $p,q$ deux projecteurs. Montrer que $p+q$ est un projecteur si et seulement si $p \circ q = q \circ p =0$.
```

```{solution} exo-373
:class: dropdown
Un sens est évident. Pour l'autre on a $p\circ q + q \circ p =0$. En composant une fois par $p$ à gauche, une autre fois à droite, il vient que $p \circ q = q \circ p$. Cela conclut facilement.
```


```{exercise}
:label: exo-374
Soit $p$ un projection et $\lambda \in \mathbb{K}$, $\lambda \notin \{ 0,1\}$. Montrer que $p-\lambda Id$ est inversible et calculer son inverse.
```

```{solution} exo-374
:class: dropdown
$\frac{X^2+X}{\lambda^2-\lambda} -1$ annule $p-\lambda$.
```






































































 