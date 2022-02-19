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

# Topologie


```{exercise}
:label: exo-130
Soit $E$ un espace vectoriel normé. On considère $A,B$ deux parties de $E$ telles que $\inf_{x\in A, y\in B}||x-y|| > 0$. Montrer qu'il existe $U,V$ deux ouverts disjoints tels que $A \subset U$ et $B \subset V$.
```

```{solution} exo-130
:class: dropdown
$d = \inf_{x\in A, y\in B}||x-y|| > 0$. Prendre $U = \mathcal{B}(A, \frac{d}{3})$ et $V = \mathcal{B}(B, \frac{d}{3})$.
```



```{exercise}
:label: exo-131
Soit $E$ un espace vectoriel normé, $a \in E$, $r > 0$. Diamètre de $\mathcal{B}(a, r)$. Unicité du centre et du rayon.
```

```{solution} exo-131
:class: dropdown
On montre que $d = diam(\mathcal{B}(a,r)) = 2r$ où $diam(X) = \sup_{x,y \in X} ||x-y||$. On a par inégalité triangulaire $d \leq 2r$. Ensuite soit $(x)_n \in \mathcal{B}(a,r)^{\N}$ telle que $||a-x_n|| \rightarrow r$. Alors pour tout $n$, $y_n=a-(x_n-a) \in \mathcal{B}(a,r)$ et $||y_n-x_n|| = 2||a-x_n|| \rightarrow 2r$.

Le rayon est unique par unicité du diamètre. Soit enfin $b$ tel que $\mathcal{B}(a,r) = \mathcal{B}(b,r) = B$, et supposons par l'absurde $a\neq b$, et notons $l = ||a-b||<r$. Notons alors $x = a + (r+\frac{l}{2})\frac{b-a}{l}$. Alors $||x-a|| = r + \frac{l}{2} > r$ donc $x \notin B$. Mais $||x-b|| = ||(r+\frac{l}{2})\frac{b-a}{l}- (b-a)|| = ||(r-\frac{l}{2})\frac{b-a}{l} ||= |r-\frac{l}{2}| = r- \frac{l}{2} < r$ donc $x\in B$, ce qui constitue une contradiction.
```



```{exercise}
:label: truc
Soit $E$ l'espace vectoriel des suites réelles bornées, muni de la norme infinie $||u||_{\infty} = \sup_{\N}|u_n|$. Déterminer si les ensembles suivants sont fermés ou non :
\begin{equation*}
 A = \{ \textrm{suites croissantes} \} \quad B = \{ \textrm{suites convergentes vers $0$} \}
\end{equation*}
L'ensemble suivant est-il compact ?
\begin{equation*}
 C = \{ u \; | \; \forall n, \; |u_n| \leq \frac{1}{n+1} \}
\end{equation*}
```

```{solution} truc
:class: dropdown
$A$ est fermé par passage à la limite des inégalités. $B$ est fermé par critère de Cauchy (preuve en $2\varepsilon$).
$C$ est fermé, montrons que $C$ est compact. Soit $(u_n^{(i)})$ des éléments de $C$. Notons $\phi_k$ une extractrice telle que $(u_k^{(\phi_k(i))})_i$ converge, mettons vers $u_k$. Considérons alors $\phi(n) = \phi_1 \circ \ldots \circ \phi_n(n)$. On montre que $(u_n^{\phi(i)})$ converge vers $(u_n)$.
```



```{exercise}
:label: exo-133
Trouver $A$ tel que les ensembles suivants soient distincts $A, \overline{A},  \mathring{A}, \mathring{\overline{A}}, \overline{\mathring{A}}$.
```

```{solution} exo-133
:class: dropdown
$A = [1, 2[ \cup (]3, 4[ \cap \Q)$ convient.
```



````{exercise}
:label: exo-135
```{prf:definition} Espace de Baire
:nonumber:
Un espace $E$ est dit de Baire s'il vérifie la propriété suivante :
pour tous $(\Omega_n)_n$ des ouverts de $E$ denses dans $E$, $\bigcap \limits_{n \in \N} \Omega_n$ est dense dans $E$.
```
```{prf:definition} Espace complet
:nonumber:
Un espace métrique $(X,d)$ est dit complet si toute suite de Cauchy de $X$ converge dans $X$. Rappel : une suite $(x_n)$ est dite de Cauchy si $\forall \varepsilon > 0$, $\exists n \in \N$, $\forall p >n$, $d(x_n,x_p) \leq \varepsilon$. Intuition : un espace métrique est complet s'il est "sans trou". Exemple : $\R$ est complet, $\R \setminus \{0\}$ n'est pas complet.
```
Montrer le lemme de Baire
```{prf:lemma} Lemme de Baire
:nonumber:
Soit $(X,d)$ un espace métrique complet et $(F_n)_{n \in \N}$ une suite décroissante de fermés de $E$ tous non vides et tels que le diamètre $\delta(F_n)$ des $F_n$ tende vers $0$. Montrer que $\bigcap \limits_{n \in \N} F_n$ est un singleton. Rappel : le diamètre d'une partie $A$ de $X$ est $\sup_{a,b \in A} d(a,b)$.
```
Montrer le théorème de Baire
```{prf:theorem} Théorème de Baire
:nonumber:
Soit $E$ un espace complet. $E$ est de Baire.
```
````

```{solution} exo-135
:class: dropdown
Démonstration du lemme :
On prend $x_n \in F_n$, on montre que $x_n$ est de Cauchy donc converge, mettons vers $x$ (on utilise les inclusions et la décroissance du diamètre vers $0$). On montre que $x$ appartient à chacun des $F_n$ donc à leur intesection (on utilise la fermeture des $F_n$). Enfin, le fait qu'il n'y a pas plusd'un élément dans l'intesection est évidente (diamètre tend vers $0$)

Démonstration du théorème :
On se donne $(\Omega_n)$ comme dans l'énoncé. Soit $x \in E$ et $B=\mathcal{B}(x, \varepsilon)$ une boule ouverte de centre $x$. On veut montrer que $B$ rencontre l'intersection des $\Omega_n$. On construit une suite décroissantes de boules fermés$F_n=\mathcal{B}(x_n, r_n)$ dont le rayon tend vers 0 et vérifiant $F_n \subset B \cap \Omega_1 \cap \Omega_2 \cap \ldots \cap \Omega_n$. Le lemme de Baire permet alors de conclure. On prend $F_0 = \overline{\mathcal{B}}(x, \varepsilon)$. $F_0, \ldots, F_n$ étant construits, on regarde $\Omega_{n+1} \cap \mathcal{B}(x_n, r_n)$, qui est non vide par densité de $\Omega_{n+1}$ et contient mettons $x_{n+1}$. Il existe un voisinage de $x_{n+1}$ contenu dans $\Omega_{n+1}$, mettons $\mathcal{B}(x_{n+1}, r_{n+1})$ avec $0 < r_{n+1} \leq r_n - d(x_n, x_{n+1})$. On pose $F_{n+1} = \overline{\mathcal{B}}(x_{n+1}, r_{n+1})$
```


````{exercise} Une application du théorème de Baire
:label: exo-136
Soit $f : \R_+ \rightarrow \R$ continue vérifiant la propriété
\begin{equation*}
\forall a > 0, \; f(na) \underset{n \rightarrow + \infty}{\longrightarrow} 0
\end{equation*}
Montrer que $f$ tend vers $0$ en $+\infty$.

```{admonition} Indication
:class: tip
La propriété de Baire a un énoncé équivalent en terme de fermés. C'est plutôt celle-ci qu'il faut utiliser.
```
````

```{solution} exo-136
:class: dropdown
Pour $\varepsilon > 0$ on regarde les fermés $F_p = \{ a \geq 0 \; | \; |f(na)| \leq \varepsilon \forall n \geq p \}$. L'union des $F_p$ est $\R$ d'après l'hypothèse, donc l'un au moins de ces $F_p$, mettons $F_{p_0}$ est d'intérieur non vide et contient par exemple $[a,b]$ avec $a<b$, donc contient tous les $[na;nb]$. Fixons $N$ suffisamment grand pour que $(N+1)a < Nb$ et soit $x > Nb$. Fixons aussi $n \geq N$ tel que $nb \leq x < (n+1)b$. Alors $x \in [nb, (n+1)b] \subset [(n+1)a;(n+1)b] \subset F_{p_0}$ donc $x \in F_{p_0}$. Si on rergarde de loin ce qu'on a montré :
\begin{equation*}
\forall x \geq Nb, \; |f(x)| \leq \varepsilon
\end{equation*}
Ce qui conclut.
```


```{exercise}
:label: exo-137
Soit $E$ l'espace vectoriel des suites réelles bornées, muni de la norme infinie $||u||_{\infty} = \sup_{\N}|u_n|$. Déterminer si les ensembles suivants sont fermés ou non :
1. L'ensemble des suites convergentes
1. L'ensemble des suites qui admettent $0$ pour valeur d'adhérence
1. L'ensemble des suites périodiques. Dans cette question on suppose connu le fait que $E$ est complet.

```

```{solution} exo-137
:class: dropdown
1. Nécessairement la suite des limites converge (elle est de Cauchy) et de là l'ensemble est fermé.
1. On se place suffisamment loin pour être proche de la suite limite. Tous les rangs proches de $0$ le sont aussi pour la suite limite. L'ensemble est donc fermé.
1. L'ensemble n'est pas fermé. On considère $v^{(n)}$ la suite indicatrice des multiples de $n$ et $u^{(n)}= \sum \limits_{k=0}^n \frac{v^{(k)}}{2^k}$. Alors $(u^{(n)})_n$ est de Cauchy donc converge, mais la limite $u$ n'est pas périodique car le $k$-ième élément donne, par son développement binaire, l'ensemble des diviseurs de $k$, donc une caractérisation de $k$ (ou plus simplement $u_0$ est la seule occurrence de $1$).

```



```{exercise}
:label: exo-138
Soit $E$ l'espace vectoriel des suites réelles bornées, muni de la norme infinie $||u||_{\infty} = \sup_{\N}|u_n|$. Montrer que $E$ est complet.
```

```{solution} exo-138
:class: dropdown
Chaque coordonnée converge, mettons vers $u_k$. $u$ définie ainsi est bien bornée. Le critère de Cauchy amène la convergence.
```



```{exercise}
:label: exo-139
Soit $K$ un compact et $f : K \rightarrow K$ 1-lipshitzienne. Soit $a \in K$. Montrer que $f_n(x) = f(\frac{1}{n}a + (1-\frac{1}{n})x)$ admet un unique point fixe. En déduire que $f$ admet un point fixe.
```

```{solution} exo-139
:class: dropdown
Une fois $x_n$ cet unique point fixe de $f_n$ trouvé, on extrait $x_{\phi(n)}$ convergente vers $x$ et on écrit $f(x)-x = f(x)-f(x_{\phi(n)}) + f(x_{\phi(n)}) - x_{\phi(n)}+x_{\phi(n)}-x$. La suite vient toute seule.
```

```{exercise}
:label: exo-140
Soit $E$ un espace de Banach (vectoriel, normé, complet). Soit $\overline{\mathcal{B}}(a_n, r_n)$ une suite décroissante de fermée telle que le rayon $r_n$ ne tend pas vers $0$.
1. Soit $a, b \in E$, $r, \rho > 0$ tels que $F_n=\overline{\mathcal{B}}(a, r) \subset \overline{\mathcal{B}}(b, \rho)$. Montrer que $||a-b|| \leq \rho-r$.
1. Démontrer que $a_n$ converge vers $a$, $r_n$ converge vers $r>0$ et $\bigcap \limits_{n \in \N} F_n = \overline{\mathcal{B}}(a, r)$.

```

```{solution} exo-140
:class: dropdown
1.
    Si $a=b$ c'est fini. Sinon on note $l = ||b-a||>0$ et on regarde $x = a-r\frac{b-a}{l}$. $x \in \mathcal{B}(a,r)$ donc $x \in \mathcal{B}(b,\rho)$. De là
    \begin{align*}
    ||b-x|| &\leq \rho \\
    i.e. \; ||b-a + \frac{r}{l}(b-a)|| &\leq \rho \\
    ||b-a|| + r &\leq \rho \\
    ||b-a||&\leq \rho-r
    \end{align*}
2. 
    Un corollaire de la question précédente est $\rho \geq r$. En particulier $(r_n)$ décroît donc converge, mettons vers $r$. Puis avec la propriété précédente, $(a_n)$ est de Cauchy, donc par complétude de $E$ converge, mettons vers $a$.

    Ensuite on montre que $\mathcal{B}(a,r) \subset \bigcap \limits_{n \in \N} F_n $. Soit donc $x\in B(a,r)$. Notons $\varepsilon = r-||x-a|| >0$. Pour tout $n$ assez grand, $||x-a_n|| \leq ||x-a|| + ||a-a_n|| = r- \varepsilon + ||a-a_n|| \leq r \leq r_n $ donc $x \in \bigcap \limits_{n \geq N} F_n = \bigcap \limits_{n \in \N} F_n$. Ainsi $\mathcal{B}(a,r) \subset \bigcap \limits_{n \in \N} F_n$.

    Puis comme une intersection de fermés reste fermée, $\overline{\mathcal{B}(a,r)} = \overline{\mathcal{B}}(a, r) \subset \bigcap \limits_{n \in \N} F_n$.

    Pour l'inclusion inverse, on fixe $\varepsilon>0$ et $n$ tel que $||a-a_n||\leq \varepsilon$ et $|r-r_n|\leq \epsilon$. Soit $x \in \bigcap \limits_{i \in \N} F_i$. Par def, $x\in F_n$ donc $||x-a_n||\leq r_n$. De là
    \begin{align*}
    ||x-a|| &= ||x-a_n +a_n -a||\\
    &\leq ||x-a_n|| + ||a_n-a|| \\
    &\leq r_n + \varepsilon \\
    &\leq r + 2\varepsilon
    \end{align*}
    Ainsi $\bigcap \limits_{n \in \N} F_n \subset \mathcal{B}(a,r+2\varepsilon)$. Ceci étant vrai pour tout $\varepsilon$, on a l'inclusion inverse.

```

```{exercise}
:label: exo-141
Soit $E$ un espace vectoriel normé. Montrer que $E$ est complet si et seulement si toute série absolument convergente est convergente.
```

```{solution} exo-141
:class: dropdown
$(\Rightarrow)$ est classique : la norme du reste tend vers $0$ donc la série est de Cauchy donc converge.

$(\Leftarrow)$ Soit $(x_n) \in E^{\N}$ de Cauchy. Par le critère de Cauchy on peut définir $j \mapsto n_j$ croissante de sorte que $y_j = x_{n_{j+1}}-x_{n_j}$ vérifie $||y_j|| \leq \frac{1}{2^j}$. Il vient que $\sum y_j$ est absolument convergente donc convergente. De là l'existence d'une extractrice $\phi : j \mapsto n_j$ telle que $x_{\phi(n)} \rightarrow x$. Immédiatement il suit $x_n \rightarrow x$.
```

````{exercise} Compacité séquentielle $\Leftrightarrow$ compacité
:label: exo-142
```{prf:definition}
:nonumber:
Un espace métrique $X$ est dit précompacte s'il admet, pour tout $r>0$, un recouvrement fini par des boules de rayon $r$.
```
Soit $(X, d)$ un espace métrique séquentiellement compact et $(\Omega_i)_{i \in I}$ un recouvrement de $X$ par des ouverts.
Montrer que $(X,d)$ est précompact.

Montrer que
\begin{equation*}
 \exists r>0, \; \forall x \in X, \; \exists i(x) \in I, \; B(x,r) \subset \Omega_{i(x)}
\end{equation*}
Conclure qu'on peut trouver $J \subset I$ fini tel que $(\Omega_j)_{j \in J}$ recouvre $X$.
````

```{solution} exo-142
:class: dropdown
La précompacité est évidente (sans quoi on peut trouver une suite d'élements tous distants d'au moins $r$ deux à deux).
```








































































 