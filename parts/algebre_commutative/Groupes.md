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

# Groupes

```{exercise}
:label: exo-220
Soit $H$ un sous-groupe stricte de $G$. Déterminer le sous-groupe engendré par le complémentaire de $H$.
```

```{solution} exo-220
:class: dropdown
Il existe $g \in G \setminus H$. Soit $h \in H$, on a $h = hg.g^{-1}$ où $hg \notin H$ et $g^{-1} \notin H$.
```

```{exercise}
:label: exo-221
Soit $G$ un groupe abélien fini de cardinal $m$ et soit $n$ premier avec $m$. Montrer que $x \mapsto x^n$ est un isomorphisme de $G$ dans $G$.
```

```{solution} exo-221
:class: dropdown
C'est un morphisme. Il est bijectif car $x^n=1$ si et seulement si $x=1$.
```

```{exercise}
:label: exo-222
Soit $G$ un groupe fini, et $x,y \in G$. Montrer que $xy$ et $yx$ ont même ordre.
```

```{solution} exo-222
:class: dropdown
$x$ et $yxy^{-1}$ ont même ordre.
```

```{exercise}
:label: exo-223
Soit $G$ muni d'une loi de composition interne associative qui possède un neutre à droite $e$ (i.e. $\forall g \in G, \; g.e = g$) et tel que tout élément $g$ possède un inverse à droite $g'$ (i.e. $gg'=e$). Montrer que $G$ est un groupe.
```

```{solution} exo-223
:class: dropdown
Soit $g \in G$, $g'$ son inverse à droite. On veut montrer $g'g=e$. Soit $h$ l'inverse à droite de $g'g$. On écrit
\begin{align*}
g.(g'g).h &= g \\
e.g.h&=g\\
g'.g.h &= g'.g \\
e &= g'.g
\end{align*}
Cela fournit par ailleurs que $e$ est un neutre à gauche puisque
\begin{equation*}
e.g = g.g^{-1}.e.g = g.(g^{-1}.g)= g.e = g
\end{equation*}
```

```{exercise}
:label: exo-224
Montrer que $(\R^*, .)$ et $(\C^*, .)$ ne sont pas isomorphes.
```

```{solution} exo-224
:class: dropdown
Impossible car tout complexe admet une racine donc un morphisme de $\C^*$ vers $\R^*$ ne prend pas de valeurs négatives.
```

```{exercise}
:label: exo-225
Montrer que les groupes suivant ne sont pas isomorphes : $(\Z,+)$, $(\Q, +)$, $(\Q^*_+, .)$
```

```{solution} exo-225
:class: dropdown
$\Z$ est monogène, pas les autres. Tout élément de $(\Q,+)$ admet une moitié, pas les autres.
```

```{exercise}
:label: exo-226
Soit $A,B$ deux parties d'un groupe fini $G$, telles que $|A|+|B| > |G|$. Montrer que $AB=G$
```

```{solution} exo-226
:class: dropdown
$a \mapsto a^{-1}g$ est injectif donc atteint $B$ sur $A$.
```

```{exercise}
:label: exo-227
Soit $G$ un groupe fini de cardinal pair. Montrer que $G$ admet un élément d'ordre 2.
```

```{solution} exo-227
:class: dropdown
On considère la relation $\equiv$ d'équivalence sur $G$ définie par
\begin{equation*}
 x \equiv y \Leftrightarrow x \in \{ y, y^{-1}\}
\end{equation*}
et soit $(x_i)_{i \in I}$ un ensemble de représentants des classes d'équivalence de $\equiv$.  Alors d'une part $\forall i, |\overline{x_i}| \leq 2$ et 
\begin{equation*}
 \sum_{i \in I} |\overline{x_i}| = |G|
 \end{equation*}
  est pair. Or $|\overline{1_G}|=1$ donc il existe un autre élément, soit $g$ tel que $|\overline{g}|=1$, i.e. $g=g^{-1}$ soit $g^2=1_G$.
```

```{exercise}
:label: exo-228
Montrer que $G$ est fini si et seulement si $G$ n'a qu'un nombre fini de sous-groupes.
```

```{solution} exo-228
:class: dropdown
Seule le sens retour mérite preuve. Soit $a \in G$, si $<a>$ est infini, $<a>$ est isomorphe à $\Z$ qui admet un nombre infini de sous-groupes. Par contraposée, $<a>$ est fini. Puis on écrit $G = \bigcup \limits_{g \in G} <g>$ et comme par hypothèse seul un nombre fini de ces sous-groupes sont distincts, on a écrit $G$ comme union finie d'ensembles finis. Finalement $G$ est fini.
```

```{exercise}
:label: exo-229
Que peut-on dire d’un groupe dont les seuls sous groupes sont triviaux ?
```
```{solution} exo-229
:class: dropdown
Soit $g\in G \setminus \{ e \}$. $\langle g \rangle$ est fini, sinon il est isomorphe à $(\Z, +)$ qui possède des sous-groupes non triviaux. Comme les seuls sous-groupes sont triviaux, $G=\langle g \rangle$ est fini. Puis $|G|$ est premier, sinon il existe des sous-groupes non triviaux.
```

```{exercise}
:label: exo-230
Soit $G$ un groupe, $H,K$ des sous-groupes de $G$. Montrer que $HK$ est un sous-groupe si et seulement si $HK=KH$.
```

```{solution} exo-230
:class: dropdown
Sens direct Soit $x$ un élément de $HK$. On a $x^{-1} = hk$ donc $x = k^{-1}h^{-1} \in KH$. Pareil pour l'inclusion inverse.

Sens retour Soit $h_1.k_1, h_2.k_2 \in HK$. On a $k_1k_2^{-1}h_2^{-1} \in KH$ donc $k_1k_2^{-1}h_2^{-1} = h'k'$. De là $h_1k_1(h_2k_2)^{-1} = hh'k' \in HK$.
```

```{exercise}
:label: exo-231
Trouver le plus petit $n$ tel qu'il existe un groupe de cardinal $n$ non abélien.
```

```{solution} exo-231
:class: dropdown
Pour $n=1$, le groupe est trivialement abélien. Pour $n=2,3,5$, il est cyclique donc abélien. Pour $n=4$, il est soit cyclique donc abélien, soit tous les éléments sont d'ordre $2$ auquel cas il est abélien (classique). Pour $n=6$, il a $\S_3$ qui n'est pas abélien.
```


```{exercise} théorème de Lagrange
:label: exo-232
Soit $(G, \cdot)$ un groupe et $H$ un sous-groupe de $G$.

1. Montrer que pour tout $a\in G$, $|aH|=|H|$.
1. Soit $a,b \in G$. Montrer que $aH=bH$ ou bien $aH \cap bH = \emptyset$.
1. En déduire que $|H|$ divise $|G|$ (Lagrange).

```

```{exercise}
:label: exo-233
Soit $(G, \cdot)$ un groupe. On note pour $a \in G$, $\tau_a : g \mapsto aga^{-1}$. Montrer que $\{ \tau_a | a \in G\}$ muni de la composition a une structure de groupe.
```

```{exercise}
:label: exo-234
Soit $G$ un groupe commutatif de cardinal $pq$, où $p$ et $q$ sont premiers distincts. Montrer que $G$ est cyclique.
```

```{solution} exo-234
:class: dropdown
Soit $g\in G, \; g \neq 1_G$. Par Lagrange $|<g>| \in \{ p, q, pq \}$. Si $|<g>|=pq$, $G$ est cyclique. Sinon par exemple $|<g>|=p$. Il suffit de trouver un élément $g'$ d'ordre $q$. On peut conclure facilement avec les groupes quotients, essayons de s'en passer. On définit la relation d'équivalence $x \equiv y$ si et seulement si $\exists h \in <g>, \; x=hy$. Chaque classe d'équivalence est de cardinal $p$, il y a donc $q$ classes d'équivalence et on peut naturellement définir une structure de groupe sur les classes d'équivalence, et ce groupe est de cardinal premier donc cyclique, engendré par $\overline{g'}$. Ainsi $q$ divise l'ordre de $g'$. Si cet ordre est $pq$, $G=<g'>$ est cyclique, sinon cet ordre est $q$ et $G=<gg'>$ est cyclique.
```








































































 